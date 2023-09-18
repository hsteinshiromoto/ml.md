---
aliases:
  - Poisson
tags: 
title: Poisson distribution
date created: 2023-09-13 21:26:49
date modified: 2023-09-13 21:26:49
---

# Poisson Distribution

> [!info] Parameters
> - $\lambda$: rate.

The random variable is said to be Poisson distributed if the probability of getting exactly $k\in\mathbb{N}$ occurrences is described by the following

> [!info] Probability Mass Function
> $$\begin{array}{rrcl}
> f(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\dfrac{\lambda^ke^{-\lambda}}{k!}\;.
> \end{array}$$

> [!info] Moments
> - Expected value: $E[X]=\lambda$,
> - Variance: $\texttt{Var}(X)=\lambda$.
