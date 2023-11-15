## Exploring multi-quantile regression with Catboost

![](https://miro.medium.com/max/700/1*LPXirZhaLZA_ug5WY8yPLw.png)

Dice. Image by Author.

How confident can we be in a machine learning model’s prediction? This question has been a prominent area of research over the last decade, and it has major implications in high-stakes machine learning applications such as finance and healthcare. While many classification models, particularly [calibrated](https://towardsdatascience.com/why-calibrators-part-1-of-the-series-on-probability-calibration-9110831c6bde) models, come with uncertainty quantification by predicting a probability distribution over target classes, quantifying uncertainty in regression tasks is much more nuanced.

Amongst many proposed methods, quantile regression is one of the most popular because no assumptions are made about the target distribution. Until recently, the main disadvantage of quantile regression was that one model had to be trained per predicted quantile. For instance, in order to predict the 10th, 50th, and 90th quantiles of a target distribution, three independent models would need to be trained. Catboost has since addressed this issue with the [multi-quantile loss function](https://catboost.ai/en/docs/concepts/loss-functions-regression#MultiQuantile:~:text=MultiQuantile,-%5Cdisplaystyle%5Cfrac%7B%5Csum) — a loss function that enables a single model to predict an arbitrary number of quantiles.

This article will explore two examples using the multi-quantile loss function on synthetic data. While these examples aren’t necessarily reflective of real-world datasets, they will help us understand how well this loss function quantifies uncertainty by predicting the quantiles of a target distribution. For a quick refresher on noise and uncertainty in machine learning, see this article:

## A Brief Overview of Quantile Regression

In supervised machine learning, the usual task is to train a model that predicts the expected value of a target given a set of input features:

![](https://miro.medium.com/max/634/1*9XED-iCQMq_-8kZBsDc__A.png)

Supervised Machine Learning. Image by Author.

Notably, training a model this way produces a single prediction indicating what the model believes is the most _likely_ value of the target given the features. In regression tasks, this is usually the mean of the target distribution conditioned on the features.

However, as illustrated in a [previous article](https://medium.com/towards-data-science/understanding-noisy-data-and-uncertainty-in-machine-learning-4a2995a84198), most machine learning models are trained on noisy datasets, and simply predicting the conditional expected value of the target does not sufficiently characterize the target distribution. To see this, consider the following noisy regression dataset:

![](https://miro.medium.com/max/700/1*FoatDs4hxmtDAy96DyokBQ.png)

Noisy Linear Regression Data. Image by Author.

Even though the model prediction fits the data optimally, it doesn’t quantify uncertainty. For instance, when x is around 0.4, the line of best fit predicts that y is 3.8. While it is true that 3.8 is the most likely value of y when x is near 0.4, there are plenty of examples in the data where y is much higher or lower than 3.8. Said differently, the conditional distribution of the target has high variability beyond its exception, and quantile regression helps us describe this.

In quantile regression, the loss function is modified to encourage a model to learn the desired quantile of the conditional target distribution.

![](https://miro.medium.com/max/700/1*wUjrJlS5Z-6rnsM0cjjk1w.png)

Quantile Regression Loss Function. Image by Author.

To gain a better intuition about this loss function, suppose a model is being trained to learn the 95th quantile of a target distribution. In the first case, consider a single training example where the target was 45 and the model predicted 60 (i.e. the model overestimated the target by 15). Assume also that each training example has a weight of 1. The loss function evaluated at these values looks like this:

![](https://miro.medium.com/max/700/1*ZvspsSBQkfSQvBLluL1wYg.png)

95th Quantile Loss Function Overestimation. Image by Author.

Now, with the same target of 45, assume that the model predicted 30 (i.e. the model underestimated the target by 15). The value of the loss function looks much different:

![](https://miro.medium.com/max/700/1*3WVR17AVAvQ1BX9A9ZGqXg.png)

95th Quantile Loss Function Underestimation. Image by Author.

Despite the model prediction being off by 15 in both examples, the loss function penalized the underestimation much higher than the overestimation. Because the 95th quantile is being learned, the loss function penalizes any prediction below the target by a factor of 0.95, and any prediction above the target by a factor of 0.05. Hence, the model is “forced” to favor overprediction above underprediction when learning the 95th quantile. This is the case when learning any quantiles above the median — the opposite is true when learning quantiles below the median. To see this better, we can visualize the loss function for each predicted quantile:

![](https://miro.medium.com/max/700/1*UtK6cJBgDr3KxmGG9An3UA.png)

95th Quantile Loss Function. Underprediction (i.e. Target — Prediction > 0) is Penalized Heavier. Image by Author.

![](https://miro.medium.com/max/700/1*FiN18XuL5uKcfMMmzGuYaA.png)

50th Quantile Loss Function. Overprediction and Underprediction are Penalized Equally. Image by Author.

![](https://miro.medium.com/max/700/1*AxNehW0IvPFCx_Ak6B_LXQ.png)

10th Quantile Loss Function. Overprediction (i.e. Target — Prediction < 0) is Penalized Heavier. Image by Author.

Catboost now extends this idea by allowing the base decision trees to output multiple quantiles per node. This allows a single model to predict multiple quantiles by minimizing a new loss function:

![](https://miro.medium.com/max/700/1*MgohfqGYaGxDlrwl7jIBHg.png)

Catboost Multi-Quantile Loss Function. Image by Author.

## Example 1 —Simple Linear Regression

To understand how the multi-quantile loss function works, let's start with a simple dataset. The following python code generates a synthetic linear dataset with gaussian additive noise:

```
import numpy as npimport pandas as pdimport matplotlib.pyplot as pltimport seaborn as snsfrom catboost import CatBoostRegressorsns.set()n = 1000x_train = np.random.rand(n)x_test = np.random.rand(n)noise_train = np.random.normal(0, 0.3, n)noise_test = np.random.normal(0, 0.3, n)a, b = 2, 3y_train = a * x_train + b + noise_trainy_test = a * x_test + b + noise_test
```

The resulting training data should look similar to this:

![](https://miro.medium.com/max/700/1*PDRNjw3FGVT1HMHna8NE5Q.png)

Noisy Linear Regression Data. Image by Author.

Next, the quantiles of the target distribution need to be specified for prediction. To illustrate the power of the multi-quantile loss, this model will seek to predict 99 different quantile values for each observation. This can almost be thought of as taking samples of size 99 from each predicted distribution.

```
quantiles = [q/100 for q in range(1, 100)]quantile_str = str(quantiles).replace('[','').replace(']','')model = CatBoostRegressor(iterations=100,                          loss_function=f'MultiQuantile:alpha={quantile_str}')model.fit(x_train.reshape(-1,1), y_train)preds = model.predict(x_test.reshape(-1, 1))preds = pd.DataFrame(preds, columns=[f'pred_{q}' for q in quantiles])
```

The resulting predictions DataFrame looks something like this:

![](https://miro.medium.com/max/700/1*MHbSF8RcR_Jb4F5oQ8OSLw.png)

Quantile Predictions. Image by Author.

Each row corresponds to a testing example and each column gives a predicted quantile. For instance, the 10th quantile prediction for the first test example was 3.318624. Since there is only one input feature, we can visualize a few predicted quantiles overlayed on the testing data:

```
fig, ax = plt.subplots(figsize=(10, 6))ax.scatter(x_test, y_test)for col in ['pred_0.05', 'pred_0.5', 'pred_0.95']:    ax.scatter(x_test.reshape(-1,1), preds[col], alpha=0.50, label=col)ax.legend()
```

![](https://miro.medium.com/max/700/1*z1LuaJAg_pqvAmqd_auBEA.png)

Testing Data overlaid with Predicted Quantiles. Image by Author.

Visually, the 95th and 5th quantiles appear to do a good job accounting for uncertainty in the data. Moreover, the 50th quantile (i.e the median) roughly approximates the line of best fit. When working with predicted quantiles, one metric we’re often interested in analyzing is coverage. Coverage is the percentage of targets that fall between two desired quantiles. As an example, coverage can be computed using the 5th and 95th quantiles as follows:

```
coverage_90 = np.mean((y_test <= preds['pred_0.95']) & (y_test >= preds['pred_0.05']))*100print(coverage_90) 
```

Using the 5th and 95th quantiles, assuming perfect calibration, we would expect to have a coverage of 95–5 = 90%. In this example, the predicted quantiles were slightly off but still close, giving a coverage value of 91.4%.

Let’s now analyze the entire predicted distribution that the model outputs. Recall, the line of best fit is y = 2x + 3. Therefore, for any input x, the mean of the predicted distribution should be around 2x + 3. Likewise, because random gaussian noise was added to the data with a standard deviation of 0.3, the standard deviation of the predicted distribution should be around 0.3. Let’s test this:

```
x = np.array([0.4])y_pred = model.predict(x.reshape(-1, 1))mu = np.mean(y_pred)sigma = np.std(y_pred)print(mu) print(sigma) fig, ax = plt.subplots(figsize=(10, 6))_ = ax.hist(y_pred.reshape(-1,1), density=True)ax.set_xlabel('$y$')ax.set_title(f'Predicted Distribution $P(y|x=4)$, $\mu$ = {round(mu, 3)}, $\sigma$ = {round(sigma, 3)}')
```

![](https://miro.medium.com/max/700/1*cYMQwLyTpuE563w5BvZvOA.png)

Predicted Distribution of y when x = 4. Image by Author.

Amazingly, the predicted distribution seems to align with our expectations. Next, let’s try a more difficult example.

## Example 2— Non-Linear Regression with Variable Noise

To see the true power of multi-quantile regression, let’s make the learning task more difficult. The following code creates a non-linear dataset with heterogeneous noise that depends on specific regions of the domain:

```
bounds = [(-10, -8), (-5, -4), (-4, -3), (-3, -1), (-1, 1), (1, 3), (3, 4), (4, 5), (8, 10)]scales = [18, 15, 8, 11, 1, 2, 9, 16, 19]x_train = np.array([])x_test = np.array([])y_train = np.array([])y_test = np.array([])for b, scale in zip(bounds, scales):        n = np.random.randint(low=100, high = 200)        x_curr = np.linspace(b[0], b[1], n)        if scale % 2 == 0:        noise_train = np.random.exponential(scale=scale, size=n)        noise_test = np.random.exponential(scale=scale, size=n)        else:        noise_train = np.random.normal(scale=scale, size=n)        noise_test = np.random.normal(scale=scale, size=n)        y_curr_train = x_curr**2  + noise_train    y_curr_test = x_curr**2  + noise_test    x_train = np.concatenate([x_train, x_curr])    x_test = np.concatenate([x_test, x_curr])    y_train = np.concatenate([y_train, y_curr_train])    y_test = np.concatenate([y_test, y_curr_test])
```

The resulting training data looks like this:

![](https://miro.medium.com/max/700/1*xYaGNJnbl9mOEU3Kre9D7Q.png)

Training Data for Example 2. Image by Author.

We’ll fit the Catboost regressor as the same way as example 1 and visualize the predictions on a test set:

```
model = CatBoostRegressor(iterations=300,                          loss_function=f'MultiQuantile:alpha={quantile_str}')model.fit(x_train.reshape(-1,1), y_train)preds = model.predict(x_test.reshape(-1, 1))preds = pd.DataFrame(preds, columns=[f'pred_{q}' for q in quantiles])fig, ax = plt.subplots(figsize=(10, 6))ax.scatter(x_test, y_test)for col in ['pred_0.05', 'pred_0.5', 'pred_0.95']:    quantile = int(float(col.split('_')[-1])*100)    label_name = f'Predicted Quantile {quantile}'    ax.scatter(x_test.reshape(-1,1), preds[col], alpha=0.50, label=label_name)ax.set_xlabel('x')ax.set_ylabel('y')ax.set_title('Testing Data for Example 2 with Predicted Quantiles')ax.legend()
```

![](https://miro.medium.com/max/700/1*SKwjtBsDFV2bRU0SO1q98w.png)

Testing Data overlaid with Predicted Quantiles. Image by Author.

Upon visual inspection, the model has characterized this non-linear, heteroscedastic relationship well. Notice how, near x = 0, the three predicted quantiles converge towards a single value. This is because the region near x = 0 has almost no noise — any model that correctly predicts the conditional probability distribution in this region should predict a small variance. Conversely, when x is between 7.5 and 10.0, the predicted quantiles are much further apart because of the inherent noise in the region. 90% coverage can be computed as before:

```
coverage_90 = np.mean((y_test <= preds['pred_0.95']) & (y_test >= preds['pred_0.05']))*100print(coverage_90) 
```

Using the 5th and 95th quantiles, assuming perfect calibration, the expected coverage is 95–5 = 90%. In this example, the predicted quantiles were even better than example 1, giving a coverage of 90.506%.

Finally, let’s look at a few inputs and their corresponding predicted distribution.

![](https://miro.medium.com/max/700/1*EeGul0jl4MxG7bnFi2elzQ.png)

Predicted Target Distribution for x = -0.06. Image by Author.

The distribution above does a nice job of capturing the target value with a relatively small variance. This is to be expected as the target values in the training data when x = 0 have little noise. Contrast this with the predicted target distribution when x = -8.56:

![](https://miro.medium.com/max/700/1*Zs4w0Pvujcgs1J5m_f8zGg.png)

Predicted Target Distribution for x = -8.56. Image by Author.

This distribution is right skewed and has a much higher variance. This is expected for this region of data because the noise was sampled from an exponential distribution with high variance.

## Final Thoughts

This article demonstrated the power of multi-quantile regression for learning arbitrary conditional target distributions. We only explored two one-dimensional examples to visually inspect model performance, but I would encourage anyone interested to try the multi-quantiles loss function on higher dimensional data. It’s important to note that quantile regression makes no statistical or algorithmic guarantees of convergence, and the performance of these models will vary depending on the nature of the learning problem. Thanks for reading!

_Become a Member:_ [_https://harrisonfhoffman.medium.com/membership_](https://harrisonfhoffman.medium.com/membership)

_Buy me a coffee:_ [_https://www.buymeacoffee.com/HarrisonfhU_](https://www.buymeacoffee.com/HarrisonfhU)

## References

1.  _Catboost Loss Functions —_ [https://catboost.ai/en/docs/concepts/loss-functions-regression#MultiQuantile](https://catboost.ai/en/docs/concepts/loss-functions-regression#MultiQuantile)