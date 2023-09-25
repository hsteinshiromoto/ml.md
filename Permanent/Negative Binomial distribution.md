---
alias: 
aliases:
  - negative binomial
tags:
  - distribution/discrete
title: Negative Binomial Distribution
date created: 2023-09-13 21:26:44
date modified: 2023-09-25 09:32:18
---

# Negative Binomial Distribution

## Definition

Let $X$ be a discrete random variable with the

> [!info] Parameters
> - $n$: number of independent Bernoulli trials.
> - $p$: probability of success.

The random variable is said to follow a _negative binomial_ distribution if the probability of getting exactly $k\in\mathbb{N}_{[1,n]}$ failures before $r$ success are occurs.

> [!info] Probability Mass Function
> $$\begin{array}{rrcl}
> \text{NBin}(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\begin{pmatrix}k+r-1\\ k\end{pmatrix}(1-p)^kp^r\;.
> \end{array}$$

> [!info] Moments
> - Mean: $E[X]=r(1-p)p$.
> - Variance: $(E[X]-X)^2=r(1-p)/p^2$.

> [!info] Uncertainty Estimation
> Todo

> [!info] Relationship with other distributions
> When $r=1$, a negative binomial distributed random variable is [[Geometric Distribution|geometrically]] distributed.