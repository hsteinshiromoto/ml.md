---
alias: 
aliases: 
tags:
  - distribution/discrete
title: Poisson Distribution
date created: 2023-09-13 21:26:49
date modified: 2023-09-25 14:53:29:15
---

# Poisson Distribution

> [!info] Parameters
> - $\lambda$: rate.

A [[random variable]] is said to be _Poisson_ distributed if the probability of getting exactly $k\in\mathbb{N}$ occurrences is described by the following

> [!info] [[Probability Mass Function]]
> $$\begin{array}{rrcl}
> p_X(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\dfrac{\lambda^ke^{-\lambda}}{k!}\;.
> \end{array}$$

> [!info] Moments
> - [[Expected Value of a Random Variable|Expected value]]: $E[X]=\lambda$,
> - [[The Relationship Between Sample Mean, Sample Variance and Expectation, Variance|Variance]]: $\texttt{Var}(X)=\lambda$.
