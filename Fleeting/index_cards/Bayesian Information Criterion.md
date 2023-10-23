---
alias: [BIC, Bayesian information criterion]
tags: []
date created: 2023-09-23 22:30:06
---

# Bayesian Information Criterion

## Assumptions

1. The approximation is only valid for sample size $n$ much larger than the number $k$ of parameters in the model.
2. The BIC cannot handle complex collections of models as in the variable selection problem in high-dimension.

## Definition

The BIC is formally defined as
$$\text{BIC}=k\ln(n)-2\ln(\hat{L}),$$
where
- $\hat{L}$ is the maximized value of the [[Likelihood Function|likelihood function]] of the model $M$, i.e. $\hat{L}=p(x|\hat{\theta},M)$ with $\hat{\theta}$ is the parameter value that maximizes the [[likelihood function]].
- $x$ is the observed data.
- $n$ is the number of data points in $x$, the number of observations.
- $k$ is the number of parameters estimated by the model.

## Remarks

- **BIC and AIC penalties**: BIC is similar to [[Akaike Information Criterion|AIC]], but with a different penalty for the number of parameters. With [[Akaike Information Criterion|AIC]] this penalty is $2k$, whereas with BIC the penalty is $\ln(n)k$.

