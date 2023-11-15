---
alias: 
tags: 
date created: Sunday, 5th February 2023, 10:35:43
date modified: Sunday, 5th February 2023, 10:42:24
---

# Correlation — When Pearson’s R Is Not Enough by Farzad Mahmoodinobar Feb, 2023 Towards Data Science

## Comparison of Various Correlation Methodologies

![](https://miro.medium.com/max/700/1*ZoY-OF9fmZk1xX7RwajopA.png)

Only One Key Will Unlock, by [DALL.E 2](https://openai.com/dall-e-2/)

We are very familiar with the phrase “correlation does not imply causation” but let’s go through a real example to understand what implications confusing correlation with causation can have. In February 1998, a [paper](https://pubmed.ncbi.nlm.nih.gov/9500320/) was published claiming a causal association between certain vaccines and autism in children. This paper was later found to be fraudulent and was [retracted in 2010](https://pubmed.ncbi.nlm.nih.gov/20137807/). One can only imagine the implication of such a claim on the lives of those who were not vaccinated based on the findings of this paper where correlation was mistaken for causation.

In this post, we are going to take a closer look at correlation to better understand what it is. We will learn that based on the type of the variables in study, what would be the recommended correlation methodology to use. Finally, we will implement some of the most common methodologies in a Python environment.

## What Is Correlation?

Correlation is a statistical measure of the relationship (or association) between two variables of interest. It quantifies the _direction_ and _strength_ of such a relationship using “Correlation Coefficient”. Let’s breakdown what we conceptually need to know about correlation coefficient:

- **Range and Direction:** Correlation coefficient ranges (almost always — we’ll talk about the exceptions) from -1 to 1, inclusive of both. Positive and negative is based on the direction of relation between the two.
- **Interpretation:** A value of 1 means that there is perfect positive correlation between the two variables (i.e. as one increases, the other one increases the same amount and vice versa). On the other hand a value of -1 means that there is a perfect but negative correlation between the two (i.e. as one increases, the other one decreases the same amount and vice versa). A correlation of 0 means that as one variable changes, the other one remains unchanged.
- **Measurement:** There is more than one way to measure correlation. We will look into various measurement methodologies in this post.

Now that we are familiar with what correlation is, let’s dive into various methodologies of calculating correlation.

_(All images, unless otherwise noted, are by the author.)_

## Overall Comparison of Correlation Methodologies

Table below provides an overview and comparison of various correlation methodologies that we will be discussing in this post. This table makes a great reference for future use.

![](https://miro.medium.com/max/700/1*u5Zv_f-up2AFcVRUWW6d6Q.png)

Comparison of Correlation Methodologies

Let’s discuss these methodologies in more detail.

## Data Set

In order to implement some of the correlation methodologies, we will be using a data set from [UCI Machine Learning Repository](https://archive-beta.ics.uci.edu/dataset/10/automobile) (CC BY 4.0), which includes car prices and a set of car properties associated with each car price. I have cleaned up and filtered the data, which can be downloaded from [this link](https://gist.github.com/fmnobar/c9b4029e08e97978a9a53f4eb034b16f). We will be looking at the correlation between car price and engine size or fuel type of the car for some of the correlation methodolgoies. For the remainder of the methodologies, we will be creating small data sets on the spot for implementation.

Let’s import the car data into a Pandas dataframe and then visualize price and engine sizes in a scatterplot to get a better sense for the visual relationship between these two variables.

```python
import numpy as np
import pandas as pd
import seaborn as sns
from scipy import stats
import matplotlib.pyplot as plt
%matplotlib inline

df = pd.read_csv('auto-cleaned.csv')
sns.regplot(data = df, x = 'price', y = 'engine-size', fit_reg = False, color = 'purple')
plt.xlabel('Price')
plt.ylabel('Engine Size')
plt.show()
```

Results:

![](https://miro.medium.com/max/700/1*odJXM2xsS3Ea32APLwnP3A.png)

Scatter Plot of Car Prices vs. Engine Size

Scatterplot demonstrates that as prices increase, engine sizes increase. Therefore, we expect the correlation to be positive. Let’s see if calculation supports this.

## Correlation Calculation Methodologies

## 1\. Pearson Correlation Coefficient

This is the most widely-used correlation. Pearson correlation coefficient (PCC), which is also known as Pearson’s _r_, is a measure of linear correlation between two variables. As the definition suggests, this method assumes a linear relationship between the two variables and therefore is not suitable for non-linear relationships. This correlation further assumes that the variables are approximately normally distributed.

Mathematically it can be calculated as follows:

![](https://miro.medium.com/max/700/1*IU_0LmXfc4WMA98G00R7Ig.png)

Pearson’s _r_

![](https://miro.medium.com/max/700/1*ZrwBV_5kYepe50YPdQQKLQ.png)

## 1.1. Pearson’s Correlation Coefficient — Implementation

Luckily for us, we do not have to calculate this mathematically ourselves. Let’s use Python to calculate Pearson’s r between price and engine size in our data set.

```python
stats.pearsonr(df['price'], df['engine-size'])
```

Results:

![](https://miro.medium.com/max/700/1*srICcTI55gQb0_GrvqWG3w.png)

“statistic” of ~0.89 is the correlation coefficient that we were looking for. As we expected, there is a positive (and relatively strong) correlation between the two. The “pvalue” is the result of the null hypothesis test that the distributions of the provided data are uncorrelated and normally distributed. The p-value is a very small number in this example, meaning we can reject the null hypothesis (i.e. there is a correlation).

## 2\. Spearman’s Rank Correlation Coefficient

Also known as Spearman’s 𝜌 (reads as “rho”) is a measure of rank correlation between two variables, which measures how well the relationship between the two variables can be described by a monotonic function. Conceptually, this is much simpler than it sounds, once we define “rank correlation” and “monotonic function”.

- **Rank Correlation:** Rank correlation measures the similarity of the order of two sets of data, relative to each other (recall that PCC did not directly measure the relative rank).
- **Monotonic Function:** A function is called monotonic if and only if it preserves the given order of its arguments — in other words, the function always increases or always decreases as the input values increase (which sounds just like correlation as we defined it). There is a distinction between a monotonic relationship and a linear relationship. Linear relationship is a specific type of monotonic relationship where the rate of increase remains constant — in other words, unlike a linear relationship, the amount of change (increase or decrease) in a monotonic relationship can vary.

Mathematically, and when all n ranks are distinct integers, it calculates as follows:

![](https://miro.medium.com/max/700/1*uULd-Ka8heWX4yjaYDep_A.png)

Spearman’s Rank Correlation Coefficient

Where:

![](https://miro.medium.com/max/700/1*_Ym_YjcDhKMV10rL4FqTWQ.png)

## 2.1. Spearman’s Rank Correlation Coefficient — Implementation

Let’s look at how this can be calculated in Python for the same two variables of price and engine size.

```python
stats.spearmanr(df['price'], df['engine-size'])
```

Results:

![](https://miro.medium.com/max/700/1*W4I2kp0xtG7K_B1Sf6U1fg.png)

Results are very similar results to Pearson’s _r_, as expected.

## 3\. Kendall’s Tau

Kendall’s Tau, denoted by 𝛕, is a non-parametric measure of rank correlation. We know what rank correlation means from the prevous correlation methodology. Non-parametric means it does not rely on the probability distribution of the underlying data. Kendall’s Tau is non-parametric because it only measures the rank correlation based on the relative ordering of the data (and not the specific values of the data).

Mathematically, Kendall’s Tau can be calculated in two different ways, which only differ in how they are normalized to be limited to the range of -1 to 1. We will define both here for reference:

![](https://miro.medium.com/max/700/1*pk6h66WyroG6plxhmRI39w.png)

Kendall’s Tau — b

Where:

![](https://miro.medium.com/max/700/1*GGEKzgJE12JAatmGn7xSsg.png)

![](https://miro.medium.com/max/666/1*kSTE0SoUHN0UrYfxZJAvIw.png)

Kendall’s Tau — c

Where:

![](https://miro.medium.com/max/700/1*v6bC6M88oNWtqjl24p6GJg.png)

Concordant pair means that both observations are ranked the same way relative to other observations. For example, let’s assume:

![](https://miro.medium.com/max/700/1*6qx5DV0jZEolqoszp3UCgw.png)

and then the two pairs of observations are (x\_1, x\_2) and (y\_1, y\_2). Then this pair is considered concordant in a case where if x\_1 is ranked higher than x\_2, then y\_1 is also ranked higher than y\_2. The reverse would be discordant.

## 3.1. Kendall’s Tau — Implementation

Let’s look at how these two interpretations of Kendall’s Tau can be calculated in Python for the same two variables of price and engine size.

```python
tau_b = stats.kendalltau(df['price'], df['engine-size'], variant = 'b')
tau_c = stats.kendalltau(df['price'], df['engine-size'], variant = 'c')

print(f"Kendall's Tau (b) is: {tau_b}")

print(f"Kendall's Tau (c) is: {tau_c}")
```

Results:

![](https://miro.medium.com/max/700/1*-_c0BSYeGxpkF3kyj1AYoA.png)

Similar to other correlation measures, there is a positive correlation along with a very small “pvalue”, suggesting the existence of a correlation. And as expected, there is not a large difference between the two implematation of Tau b or c.

## 4\. Point-Biserial

Point-Biserial correlation coefficient measures the correlation between a binary (or dichotomous) and a continuous variable. A binary or dichotomous variable is one that only takes two values (e.g. 0 or 1, female or male, etc.). As an example, recall that Pearson’s _r_ measures the correlation between the two **continuous** variables. But there are cases where we deal with one binary and one continuous variable. In such cases, we can use the Point-Biserial correlation coefficient.

Point-Biserial correlation coefficient can be calculated as follows:

![](https://miro.medium.com/max/700/1*bD2zDfbdZzZJibj6u3WhEQ.png)

Point-Biserial Correlation Coefficient

Where:

![](https://miro.medium.com/max/700/1*1ZLNDIlno7sg6Ur4N0TRaQ.png)

## 4.1. Point-Biserial — Implementation

In our data set, fuel type can either be gas or diesel, which we can use as a binary variable. First we will create a new column named “fuel-type-binary” where shows a value of 0 for gas and 1 for diesel. Then we calculate the Point-Biserial correlation coefficient between fuel type and car price.

```python
df['fuel-type-binary'] = df['fuel-type'].replace({'gas' : 0, 'diesel' : 1})stats.pointbiserialr(df['price'], df['fuel-type-binary'])
```

Results:

![](https://miro.medium.com/max/700/1*5Z9UqlISF1YiWUiCfgduJA.png)

## 5\. Phi Coefficient

Phi coefficient (a.k.a. mean square contingency coefficient), denoted by ɸ, is yet another measure of association (or correlation) between two variables but it is only used when both are binary or dichotomous variables. If you are a machine learning practitioner with a focus on classification, you may also know this as the Matthews Correlation Coefficient (MCC). In machine learning, MCC is used as a measure of quality of binary or multiclass classifications.

Mathematically, ɸ for two binary variables of X and Y is defined as follows:

![](https://miro.medium.com/max/700/1*1yS9Pryd8WCB9wsWPr92ig.png)

Where:

![](https://miro.medium.com/max/700/1*3kntMVQDkJvUzcRAbEa0Sw.png)

![](https://miro.medium.com/max/700/1*qhR9EOQCqGWvLpuzEisPJQ.png)

The tabular representation above is called a “contingency table”. Next, let’s look at how we can implement Phi Coefficient in Python. We will cover two approaches here for the sake of completeness.

## 5.1. Phi Coefficient — Implementation In Pandas

We will take the following steps in the code block below:

1. Import necessary packages
    2\. Create a dataframe from two assumed binary variables of X and Y
    3\. Create a contingency table
    4\. Calculate the Phi Coefficient

```python
import pandas as pd
import math

df = pd.DataFrame({'X': [1, 1, 0, 0, 1, 0], 'Y': [1, 0, 1, 1, 0, 1]})
table = pd.crosstab(df['X'], df['Y'])
n11 = table.iloc[0,0]
n10 = table.iloc[0,1]
n01 = table.iloc[1,0]
n00 = table.iloc[1,1]
coef = (n11*n00 - n10*n01) / (math.sqrt((n11+n10)*(n11+n01)*(n00+n10)*(n00+n01)))

print(f"Phi Coefficient: {coef}")
```

Results:

![](https://miro.medium.com/max/700/1*T_vlQE_XBbbidr-GL46cUw.png)

This is not difficult to calculate but still is relatively manual and prone to error. Let’s look at the second approach, which is much more straight forward.

## 5.2. Phi Coefficient — Implementation In Scikit-learn

Remember that Phi Coefficient is also known as the Matthews Correlation Coefficient (MCC)? scikit-learn happens to have that in their library so let’s see how we can implement it, following below steps:

1. Import necessary packages
    2\. Create two assumed binary variables
    3\. Calculate MCC

```python
from sklearn.metrics import matthews_corrcoef

X = [1, 1, 0, 0, 1, 0]
Y = [1, 0, 1, 1, 0, 1]

mcc = matthews_corrcoef(X, Y)

print(f"Matthews Correlation Coefficient: {mcc}")
```

Results:

![](https://miro.medium.com/max/700/1*LzdK_5k2GNEk0LGADlv5_Q.png)

As expected, this number is identical to the number we generated in the first approach.

> **Pro Tip:** This method is intended to measure the quality of binary (and multi-class) classifications and we are using it to calculate the association between the two variables in this example. Typical use cases in machine learning would be to use the MCC to measure the correlation or association of ground truth and predicted values in a classification problem. Our approach here is fine and it generates the correct results but that is an important caveat, in case you decide to use MCC in the future.

## 6\. Cramer’s V

Cramer’s V (a.k.a. Cramer’s Phi and denoted by V) is a measure of association (or correlation) between two categorical (**nominal**) variables. This is very similar to Phi Coefficient but it is more generalized in that it can be applied to _n\*n_ contingency tables (unlike ɸ, which can only be applied to binary variables).

> **Important Note:** This is the only measure in this post with a range of 0 to 1 (inclusive) (compared to other correlation measures with the range of -1 to 1, inclusive).

Cramer’s V can be calculated as follows:

![](https://miro.medium.com/max/700/1*zM0HiTE9cwuJXRxTbY5YFg.png)

Where:

![](https://miro.medium.com/max/700/1*zkgQ_f5GZzqElsXxkyIHKA.png)

## 6.1. Cramer’s V — Implementation

Let’s look at an example of how we can implement Cramer’s V. We will be taking the following steps:

1. Import necessary libraries
    2\. Create a dataframe of two variables of X and Y, each with two different classes
    3\. Create a contingency table
    4\. Calculate the chi-squared statistic
    5\. Calculate Cramer’s V

```python
import pandas as pd
import math

df = pd.DataFrame({'X': ['A', 'A', 'B', 'B', 'A', 'B'], 'Y': ['W', 'X', 'W', 'W', 'X', 'W']})

table = pd.crosstab(df['X'], df['Y'])
chi2, p, dof, expected = stats.chi2_contingency(table)

V = math.sqrt(chi2 / (table.values.sum()*min(table.shape[0]-1, table.shape[1]-1)))

print(f"Cramer's V: {V}")
```

Results:

![](https://miro.medium.com/max/700/1*mP9L5AHvrJ1_5nQHbcwiYw.png)

## 7\. Polychoric Correlation

Polychoric correlation is a measure of association (or correlation) between two categorical (**ordinal**) variables. Since these are ordinal variables, the correlation considers the strength and direction of association (and hence the range of -1 to 1, unlike Cramer’s V). A special case of Polychoric Correlation is Tetrachoric Correlation that is only used with binary or dichotomous variables — we will cover that one later in the post.

## 8\. Partial Correlation

Partial Correlation is a measure of correlation between two variables while controlling for one or more confounding factors. A confounding factor is a variable that is related to both independent and dependent (i.e output) variables. In other words, Partial Correlation measures the association (or correlation) between two variables when the effects of one or more other variables are removed from such a relationship.

A frequently used example of confounding factor is a study focused on the relationship between smoking (X) and lung cancer (Y). In this study, age (Z) is a confounding factor. Smokers tend to be older and age itself is a risk factor for lung cancer. Therefore, age (Z) can impact both smoking (X) and lung cancer (Y). Then partial correlation can be used to control for the confounding effect of Z (i.e. remove the impact of age from the study) and then the study will focus on the correlation between smoking (X) and lung cancer (Y) in a controlled environment.

Partial correlation can be calculated as follows:

![](https://miro.medium.com/max/700/1*mNGNgJ1CoSdg2ekOj0VB9A.png)

Partial Correlation

Where Covariance and Variance are calculated as:

![](https://miro.medium.com/max/700/1*t1Rbwo3o_H8M4inrQJoMfA.png)

![](https://miro.medium.com/max/700/1*Bg3IxrjZqIX66SKHHTrEyQ.png)

We will look at two methods of implementing Partial Correlation in Python, first by directly calculating such a correlation and second by using a Python library to streamline the process.

## 8.1. Partial Correlation — Implementation In Pandas

Partial Correlation’s formula looks daunting but it can easily be implemented in Python. Let’s look at an example where we will be taking the following steps:

1. Import necessary packages
    2\. Create a dataframe of X, Y and Z variables
    3\. Calculate the Partial Correlation between X and Y, while controlling for Z

```python
import pandas as pdd

ata = {    'X': [1, 1, 9, 0, 1, 8, 10, 7, 10, 0, 1, 9, 0, 6, 2, 6, 9, 0, 9, 7],     'Y': [8, 2, 4, 3, 0, 1, 6, 0, 5, 6, 10, 3, 2, 7, 4, 5, 6, 0, 5, 10],    'Z': [0, 2, 1, 1, 2, 2, 7, 7, 2, 6, 4, 4, 7, 7, 6, 6, 1, 6, 4, 7]}

df = pd.DataFrame(data)

corr_matrix = df.corr()

x_y_correlation = corr_matrix.loc['X', 'Y']
x_z_correlation = corr_matrix.loc['X', 'Z']
y_z_correlation = corr_matrix.loc['Y', 'Z']

partial_correlation_xy_z = (x_y_correlation - (x_z_correlation * y_z_correlation)) / ((1 - (x_z_correlation ** 2)) * (1 - (y_z_correlation ** 2))) ** 0.5

print(f"Partial Correlation (between X and Y, while controlling for Z): {partial_correlation_xy_z}")
```

Results:

![](https://miro.medium.com/max/700/1*sDkoZlNdouqaPcope4w-VQ.png)

## 8.2. Partial Correlation — Implementation In Pingouin

Previous approach helps with understanding the concept of Partial Correlation but it is not very efficient to create each of the correlations and use the formula to calculate the partial correlation — it also increases the opportunity for human error. In the code block below, we will be leveraging the [pingouin](https://pingouin-stats.org/build/html/index.html) library to make the process easier, by going through the following steps:

1. Import necessary packages
    2\. Create a dataframe of X, Y and Z variables
    3\. Calculate the Partial Correlation between X and Y, while controlling for Z

```python
import pandas as pd
import pingouin as pg

data = {    'X': [1, 1, 9, 0, 1, 8, 10, 7, 10, 0, 1, 9, 0, 6, 2, 6, 9, 0, 9, 7],     'Y': [8, 2, 4, 3, 0, 1, 6, 0, 5, 6, 10, 3, 2, 7, 4, 5, 6, 0, 5, 10],    'Z': [0, 2, 1, 1, 2, 2, 7, 7, 2, 6, 4, 4, 7, 7, 6, 6, 1, 6, 4, 7]}

df = pd.DataFrame(data)
partial_correlation_xy_z = pg.partial_corr(data = df, x='X', y='Y', covar='Z', method = 'pearson')

print(partial_correlation_xy_z)
```

Results:

![](https://miro.medium.com/max/700/1*jv_BUKBIHmMWAkwIKG8kYQ.png)

Results are helpful in that there are additional fields. Let’s look at what these fields convey ([source](https://pingouin-stats.org/build/html/generated/pingouin.partial_corr.html#pingouin.partial_corr)):

- n: Sample size
- r: Partial correlation coefficient
- CI95%: 95% parametric confidence intervals around r
- p-val: p-value

Note that we decided to use Pearson’s _r_ in this specific implementation, using `method = ‘pearson’`. Another option is to use Spearman 𝜌 by including `method = ‘spearman’`.

## 9\. Tetrachoric Correlation Coefficient

Tetrachoric Correlation Coefficient, is a special case of Polychoric Correlation that measures association between two binary (or dichotomous) variables. Recall that Phi Coefficient also measures association between two binary variables. The difference is that Phi Coefficient assumes a normal distribution of the underlying data, while Tetrachoric Correlation assumes a bivariate normal distribution. In other words, Tetrachoric Correlation assumes that the binary variables are generated from a continuous variable that follows a normal distribution, while Phi Correlation assumes that the binary variables themselves follow a normal distribution. Tetrachoric Correlation is useful in cases where the underlying continuous variable are not directly observable but can be assumed normally distributed. Such cases are common in psychological, medical, marketing and/or social sciences research where the underlying behavior is not directly observable (e.g. association between self-reported political views and actual voting behavior).

## Conclusion

In this post we discussed the importance of understanding what correlation is and how it can be measured. Depending on the type of the variables being investigated for correlation, there are specific types of correlations recommended to use. We then walked through the most common correlation methodologies and how they can be implemented in a Python environment.

## Thanks for Reading!

If you found this post helpful, please [follow me on Medium](https://towardsdatascience.com/@fmnobar) and subscribe to receive my latest posts!

## Reference

[Correlation — When Pearson’s r Is Not Enough | by Farzad Mahmoodinobar | Feb, 2023 | Towards Data Science](https://towardsdatascience.com/correlation-when-pearsons-r-is-not-enough-aded72308635)