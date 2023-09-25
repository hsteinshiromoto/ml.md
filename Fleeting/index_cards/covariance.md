---
alias: 
aliases:
  - covariance
tags: 
title: Covariance
date created: 2023-09-25 09:48:39
date modified: 2023-09-25 13:38:30
---

# Covariance

Let $X$ and $Y$ be two jointly distributed [[random variable|random variables]], the _covariance_ is defined as the [[Expected Value of a Random Variable]] of the product of their deviations from their individual expected values
$$\texttt{Cov}(X,Y)=\text{E}[(X-\text{E}[X])(Y-\text{E}[Y])]\;.$$

N.B. 1. The covariance of a variable with itself is equlas to its [[variance]] $\texttt{Cov}(X,X)=\texttt{Car}(X)$.

N.B. 2. Covariance and [[correlation]] are similar. In fact, [[correlation]] is covariance normalized by the product of the individual [[standard deviation]] of the random variables:
$$\texttt{Corr}(X,Y)=\dfrac{\texttt{Cov}(X,Y)}{\sigma_X\sigma_Y}\;.$$

![The sign of covariance of two random variables $X$ and $Y$.](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Covariance_trends.svg/170px-Covariance_trends.svg.png)