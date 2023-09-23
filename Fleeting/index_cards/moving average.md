# Model
It is a model that uses the dependency between an observation and a residual error from a moving average model applied to lagged observations. ^62ea2c

It is proportion to the difference of the observed values and the moving average values.

Indicates that regression error is actually a linear combination of error terms whose values occurred contemporaneously at various times in the past.

We do a regression model as:
$$\varepsilon(t)+\theta_1\varepsilon(t-1)+\cdots+\theta_q\varepsilon(t-q)\;.$$