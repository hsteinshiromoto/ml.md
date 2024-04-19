---
alias: []
tags: [analysis, result/theorem]
category: theorem
date created: 2023-02-16 16:51:08
date modified: Thursday, 16th February 2023, 5:02:15 pm
---

# Inverse Function Theorem

## Statements

**Theorem**. Let $W$ be an [[Open Set|open set]] of $\mathbb{R}^n$ and, for a given $r\in\mathbb{N}_{>0}$, let $F:W\to\mathbb{R}^n$ be a [[Functions and Mappings|vector-valued function]] of [[Continous Differentiability|class]] $\mathcal{C}^r$. If $a\in W$ and the [[Jacobian Matrix]] $DF(a)$ is nonsingular, then there exists an [[Neighborhood|open neighborhood]] $N(a)\subset W$ such that $V=F(N(a))$ is [[Open Set|open]] and $F\in\mathcal{C}^r(N(a), V)$ is a [[Diffeomorphism|diffeomorphism]]. Morover, for every $x\in N(a)$ and $y=F(x)$, the following formula for the derivatives of $F^{-1}$
$$DF^{-1}(y)=DF(x)^{-1}\;,$$
holds, where $DF^{-1}$ is the inverse Jacobian matrix.

## References

[[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 Theorem 6.4]]