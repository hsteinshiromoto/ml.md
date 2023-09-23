The term [[autoregression]] describes a regression of the variable against itself.

# Model
In ARIMA model, autoregression is a regression model that utilizes the dependent relationship between a current observation and observations over a preivous period. An [[autoregression]] is run against a set of lagged values of order $p$. ^1dfe39

Let $c$ be a constant, $\phi_1,\ldots,\phi_p$ be lag coefficients and $\epsilon_t$ be a white noise. The AR model is given by

$$y(t)=c+\phi_1y(t-1)+\cdots+\phi_p y(t-p)+\epsilon_t\;.$$

The simplest model is the AR(1):
$$y(t)=c+\phi_1y(t-1)+\epsilon_t\;.$$