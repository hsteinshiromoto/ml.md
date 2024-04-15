---
alias: [gamma]
tags: [probability_theory, distribution/continuous]
is_continuous: Y
category: 
title: Gamma Distribution
date created: 2023-09-25 09:48:39
date modified: 2023-10-09 17:02:01
---

# Gamma Distribution

> [!info] Parameters
> - $\alpha>0$: parameter
> - $\beta>0$: parameter

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
> - [[Expected Value of a Random Variable|Expected value]]: $E[X]=\alpha/\beta$,
> - [[Variance and Standard Deviation of a Random Variable|Variance]]: $\texttt{Var}(X)=\alpha/\beta^2$.

This random variable represents the waiting time until the $\alpha-$th occurrence of a [[Poisson distribution|Poisson]] event with average rate $\beta$.

Related distributions:
- If $\alpha=1$, the Gamma distribution is a generalisation of the [[Exponential Distribution|exponential distribution]] with parameter $\beta=\lambda$.
- Let $m>0$, if $\alpha=m/2$ and $\beta=1/2$. Then, $X$ has a [[Chi-Squared Distribution|chi-square]] distribution with $m$ degrees of freedom.