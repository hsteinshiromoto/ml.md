---
alias: []
tags: [analysis/functional, result/proposition]
category: proposition
date created: 2023-02-09 16:17:31
date modified: Friday, 10th February 2023, 4:13:43 pm
---

# Differentiability and Partial Derivatives

## Statements

**Proposition**. Let $U\subset\mathbb{R}^n$ be an [[Open Set|open set]], if the [[Functions and Mappings|vector-valued function]] $f:U\to\mathbb{R}^m$ is [[differentiable]] at $a\in U$, then it is [[Continuous Function|continuous]] at $a$ and all the [[Partial Derivative|partial derivatives]] exist at $a$. Moreover, $R(x,a)$ and $A$ exist and $A$ is the [[Jacobian matrix]] and Equation [[Differentiable|(differentiable)]] is given by
$$
\begin{equation}
F(x)=F(a)+DF(a)(x-a)+||x-a||R(x,a)
\end{equation}
$$
When $f$ is a [[Functions and Mappings|function]], the coefficients $b_i$ are uniquely determined for each $a$ which $f$ is [[Differentiable|differentiable]]; in fact
$$b_i=\left.\dfrac{\partial f}{\partial x^i}\right|_a\;.$$
Conversely, if the [[Partial Derivative|partial derivatives]] of $f$ at $a$ exist and are [[Continuous Function|continuous]], then $f$ is [[Differentiable|differentiable]] at $a$.

## References

[[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 Chapter 2, Proposition 1.1]]