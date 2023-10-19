---
alias: [binomial]
tags: [distribution/discrete]
title: Binomial Distribution
date created: 2023-09-13 21:26:44
date modified: 2023-09-25 16:28:55
is_continuous: N
is_univariate: Y
---

# Binomial Distribution

## Definition

Let $X$ be a discrete [[random variable]] with the

> [!info] Parameters
> - $n$: number of independent Bernoulli trials.
> - $p$: probability of success.

The [[random variable]] is said to follow a _binomial_ distribution if the probability of getting exactly $k\in\mathbb{N}_{[1,n]}$ successes is described by the following

> [!info] [[Probability Mass Function]]
> $$\begin{array}{rrcl}
> p_X(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\begin{pmatrix}n\\ k\end{pmatrix}p^k(1-p)^{n-k}\;.
> \end{array}$$

> [!info] Moments
> - [[Expected Value of a Random Variable|Expected value]]: $E[X]=np$,
> - [[Variance and Standard Deviation of a Random Variable|Variance]]: $\texttt{Var}(X)=np(1-p)$.

> [!info] Uncertainty Estimation
> - $\alpha$: confidence level
> - $\hat{p}$: success probability
> - Confidence interval
>   $$\hat{p}\pm z\sqrt{\dfrac{\hat{p}(1-\hat{p})}{{n}}}\;,$$
>   where $z=1-\alpha/2$.

When $n=1$, a binomial distributed random variable is [[Bernoulli distribution|Bernoulli]] distributed.