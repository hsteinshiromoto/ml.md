---
alias: [Gaussian, normal, bell curve, bell shape]
tags: [distribution/continuous]
title: Gaussian Distribution
date created: 2023-09-13 21:26:52
date modified: 2023-09-18 21:57:37
is_continuous: Y
is_univariate: N
---

# Gaussian Distribution

Let $X\in\mathbb{R}^n$ be a continuous random vector with the

> [!info] Parameters
> - $\mu\in\mathbb{R}^n$: the mean vector.
> - The covariance matrix
  > $$\Sigma=\begin{pmatrix}
> \texttt{Var}(X_1)&\texttt{Cov}(X_1,X_2)&\cdots&\texttt{Cov}(X_1,X_n)\\
>  \texttt{Cov}(X_2,X_1)&\texttt{Var}(X_2)&\cdots&\texttt{Cov}(X_2,X_n)\\
>  \vdots&\vdots&\ddots&\vdots\\
>  \texttt{Cov}(X_n,X_1)&\cdots&\texttt{Cov}(X_n,X_{n-1})&\texttt{Var}(X_n)\\
>  \end{pmatrix}\;.$$

The random variable is said to be Gaussian distributed if it described by the following

> [!info] probability density function
> $$\begin{array}{rrcl}
> f:&\mathbb{R}&\mapsto&\mathbb{R}\\
> &x&\to&\dfrac{\exp\left(-\dfrac{(x-\mu)^T\Sigma^{-1}(x-\mu)}{2}\right)}{\sqrt{(2\pi)^k\det(\Sigma)}}\;.
> \end{array}
> $$
