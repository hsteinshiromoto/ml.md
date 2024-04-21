---
alias: [binary, Bernoulli]
tags: [distribution/discrete]
title: Bernoulli Distribution
date created: 2023-09-25 09:48:39
---

# Bernoulli Distribution

## Definition

Let $X$ be a discrete [[random variable]] with the

> [!info] Parameters
> - $p$: probability of success.

The [[random variable]] is said to follow a _Bernoulli_ distribution if the probability of getting s success is described by the following

> [!info] [[Probability Mass Function]]
> $$
> \begin{array}{rrcl}
> p_X(\cdot,p):&\{0,1\}&\to&\mathbb{R}\\
> &k&\to&p^k(1-p)^{1-k}\;.
> \end{array}
> $$

> [!info] Moments
> - [[Expected Value|Expected value]]: $E[X]=p$,
> - [[Variance and Standard Deviation|Variance]]: $\texttt{Var}(X)=p(1-p)$.

> [!info] Uncertainty Estimation
>