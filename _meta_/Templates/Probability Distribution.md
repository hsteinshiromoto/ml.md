---
tags: distribution/[continuous, discrete]
alias: 
is_continuous:
  - Y
  - N
is_univariate:
  - Y
  - N
---

# Probability Distribution

> [!info] Parameters
> - $p$: parameter

A [[random variable]] is said to be _y_ distributed if it is described by the following

> [!info] [[Probability Mass/Density Function]]
> $$\begin{array}{rrcl}
> p_X(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\dfrac{\lambda^ke^{-\lambda}}{k!}\;.
> \end{array}$$

> [!info] Moments
> - [[Expected Value|Expected value]]: $E[X]=$,
> - [[Variance and Standard Deviation|Variance]]: $\texttt{Var}(X)=$.

The distribution is an appropriate model if the following assumptions are true:

- 