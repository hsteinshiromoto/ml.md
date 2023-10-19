---
alias: [Akaike, AIC]
tags: []
date created: 2023-09-23 22:30:06
---

# Akaike Information Criterion

Used to compare which model is better. AIC rewards goodness of fit (as assessed by the likelihood function), but it also includes a penalty that is an increasing function of the number of estimated parameters. The penalty discourages overfitting, which is desired because increasing the number of parameters in the model almost always improves the goodness of the fit.

## Definition

Let $k$ be the number of estimated parameters in the model. Let $\hat{L}$ be the maximum value of the [[Likelihood Function]]. Then, the _Akaike information criterion_ (AIC) value of the model is the given by the formula

$$\text{AIC}= 2 k − 2 \ln(\hat{L})$$

## How it is Used

Given a set of candidate models for the data, the **preferred model is the one with the minimum AIC value**. This formulated by

$$\begin{align}
\text{find }&f\\
\text{s.t. }&\min_{k, l} 2k-2 \ln(\hat{L})
\end{align}$$
This implies that the AIC is used as [[performance metric]] of regression models.

