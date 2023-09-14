---
alias: 
aliases:
  - "[normal, normal distribution]"
tags: 
title: Gaussian Distribution
date created: 2023-09-13 21:26:52
date modified: 2023-09-14 22:15:13
---

# Gaussian Distribution

## Definition

Let $x=(x_1,\ldots,x_n)\in\mathbb{R}^n$ a random vector, $\mu:=(E(x_1),\ldots,E(x_n))\in\mathbb{R}^n$ the be mean vector, and $\Sigma\in\mathbb{N}^{n\times n}$ be the covariance matrix denoted, in compact form, as $\left|\textrm{Cov}(x_i,x_j)\right|$. The probability density function is given by
$$\begin{array}{rrcl}
f:&\mathbb{R}&\mapsto&\mathbb{R}\\
&x&\to&\dfrac{\exp\left(-\dfrac{(x-\mu)^T\Sigma^{-1}(x-\mu)}{2}\right)}{\sqrt{(2\pi)^k\det(\Sigma)}}\;.
\end{array}
$$
