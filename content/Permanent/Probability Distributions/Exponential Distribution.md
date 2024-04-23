---
alias: [exponential distribution, exponential]
tags: [definition, theory/probability, statistics]
is_continuous: Y
category: 
title: Exponential Distribution
date created: 2023-09-25 09:48:39
date modified: 2023-10-09 16:59:07
is_univariate: Y
---

# Exponential Distribution

## Definition

Let $X$ be a discrete [[random variable]] with

> [!info] Parameters
> - $\lambda$: waiting time between two successive events in a [[Poisson distribution|Poisson]] process with the average $\lambda$.

A [[random variable]] is said to follow a _exponential_ distribution if the probability is described by the following

> [!info] [[Probability Density Function]]
> $$
> \begin{array}{rrcl}
> p_X:&\mathbb{R}&\to&\mathbb{R}\\
> 	&x&\to&\left\{\begin{array}{rcl}
> 		\lambda e^{-\lambda x},&\text{if}&x>0\\
> 		0,&\text{if}&x\leq0\;.
> 		\end{array}\right.
> \end{array}
> $$

> [!info] Moments
> - [[Expected Value|Expected value]]: $E[X]=1/\lambda$,
> - [[Variance and Standard Deviation|Variance]]: $\texttt{Var}(X)=1/\lambda^2$.

> [!info] Uncertainty Estimation
> Todo

## Relationship with Other Distributions

### Gamma Distribution

![[Gamma Distribution#^6ff921]]