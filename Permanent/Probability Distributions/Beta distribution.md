---
alias: [Beta, beta]
tags: [distribution/discrete]
is_continuous: Y
is_univariate: N
title: Beta Distribution
date created: 2023-10-04 12:06:30
date modified: 2023-10-04 12:24:16
---

# Beta Distribution

> [!info] Parameters
> - $\mathbb{R}_{>0}\ni\alpha$
> - $\mathbb{R}_{>0}\ni\beta$

A [[random variable]] is said to be _Beta_ distributed if it is described by the following

> [!info] [[Probability Density Function]]
> $$
> \begin{array}{rrcl}
> p_X(\cdot,\alpha,\beta):&[0,1]&\to&\mathbb{R}\\
> &x&\to&\left\{\begin{array}{rcl}
> 			\dfrac{1}{B(\alpha,\beta)}x^ {\alpha-1}(1-x)^{\beta-1},&\text{if}&x\in[0,1]\\
> 			0,&\text{if}&\text{otherwise}\;,
> 		\end{array}\right.
> \end{array}
> $$
> where $B(\alpha,\beta)=\Gamma(\alpha+\beta)/(\Gamma(\alpha)\Gamma(\beta))$.

> [!info] Moments
> - [[Expected Value of a Random Variable|Expected value]]: $E[X]=\alpha/(\alpha+\beta)$.
> - [[Variance and Standard Deviation of a Random Variable|Variance]]: $\texttt{Var}(X)=\alpha\beta/((\alpha+\beta)^2(\alpha+\beta+1))$.

The distribution is an appropriate model if the following assumptions are true:

## Rationale

Let $X$ be a [[Binomial distribution|binomial]] [[Random Variable|random variable]] with parameters $n$ and $p$, where $p$ is unknown. By assuming that $p$ has a Beta distribution, then for $X=k$ (i.e., $k$ successes in $n$ Bernoulli trials) $X\sim\text{Beta}(\alpha+k,\beta+k)$.