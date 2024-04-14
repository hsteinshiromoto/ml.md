Is a common metric in [[classification]].

Fails when classes are high imbalanced. For these cases [[f1-score]] is more appropriate

$$
A=\dfrac{1}{n}\sum_{i=1}^n1(\hat{y}_i=y_i)\;,
$$
where
* $n$ is the number of observations;
* $1$ is the indicator function
* $\hat{y}$ is the predicted value
* $y$ is the observed value