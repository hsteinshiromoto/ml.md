---
alias: [geometric]
aliases: []
tags: [distribution/discrete]
title: Geometric Distribution
date created: 2023-09-13 21:26:44
date modified: 2023-09-25 16:20:47
is_continuous: N
is_univariate: Y
---

# Geometric Distribution

## Definition

Let $X$ be a discrete [[random variable]] with

> [!info] Parameters
> - $p$: probability of success.

A [[random variable]] is said to follow a _geometric_ distribution if it is the number of failures between two consecutive successful trials in a [[Bernoulli distribution|Bernoulli]] trials with parameter $p$.

> [!info] Probability Mass Function
> $$
> \begin{array}{rrcl}
> p_X(\cdot,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&(1-p)^kp\;.
> \end{array}
> $$

> [!info] Moments
> - [[Sample Mean|Mean]]: $E[X]=(1-p)/p$.
> - [[The Relationship Between Sample Mean, Sample Variance and Expectation, Variance|Variance]]: $(1-p)/p^2$.

> [!info] Uncertainty Estimation
> Todo
