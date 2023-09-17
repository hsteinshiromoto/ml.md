---
alias: 
aliases:
  - "[normal, normal distribution]"
tags: 
title: Gaussian Distribution
date created: 2023-09-13 21:26:52
date modified: 2023-09-17 22:18:07
---

# Gaussian Distribution

## Definition

Let $x\in\mathbb{R}^n$ be a random vector, $\mu\in\mathbb{R}^n$ the be mean vector, and $\Sigma\in\mathbb{R}^{n\times n}$ be the covariance matrix denoted in compact form, for every $i,j\in\mathbb{N}_{[1, n]}$, as $\left|\textrm{Cov}(x_i,x_j)\right|$. The probability density function is given by
$$\begin{array}{rrcl}
f:&\mathbb{R}&\mapsto&\mathbb{R}\\
&x&\to&\dfrac{\exp\left(-\dfrac{(x-\mu)^T\Sigma^{-1}(x-\mu)}{2}\right)}{\sqrt{(2\pi)^k\det(\Sigma)}}\;.
\end{array}
$$
