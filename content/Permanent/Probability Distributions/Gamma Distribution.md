---
alias: [gamma]
tags: [definition, theory/probability, statistics]
is_continuous: Y
category: 
title: Gamma Distribution
date created: 2023-09-25 09:48:39
date modified: 2023-10-09 17:02:01
---

# Gamma Distribution

## Statements

> [!info] Parameters
> - $\alpha>0$: Number of occurrence of a [[Poisson distribution]] event.
> - $\beta>0$: Average rate of occurrence.

A [[random variable]] is said to be _Gamma_ distributed if it is described by the following

> [!info] [[Probability Density Function]]
> $$
> \begin{array}{rrcl}
> p_X(\cdot,\alpha,\beta):&\mathbb{R}&\to&\mathbb{R}\\
> &x&\to&\left\{\begin{array}{rcl}
> 			\dfrac{\beta^\alpha}{\Gamma(\alpha)}x^{\alpha-1}e^{-\beta x},&\text{if}&x>0\\
> 			0,&\text{if}&x\leq0\;.
> 		\end{array}\right.
> \end{array}
> $$

> [!info] Moments
> - [[Expected Value|Expected value]]: $E[X]=\alpha/\beta$,
> - [[Variance and Standard Deviation|Variance]]: $\texttt{Var}(X)=\alpha/\beta^2$.

## Relationship with Other Distributions

### Exponential Distribution

When $\alpha=1$, the Gamma distribution reduces to the [[Exponential Distribution|exponential distribution]] with parameter $\beta=\lambda$. ^6ff921

### Chi-Square

For a value $m>0$, let $\alpha=m/2$ and $\beta=1/2$. Then, $X$ has a [[Chi-Squared Distribution|chi-square]] distribution with $m$ degrees of freedom. ^c14c0f