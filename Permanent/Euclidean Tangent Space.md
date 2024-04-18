---
alias: [Euclidean tangent space, Euclidean tangent spaces]
tags: [linear, algebra]
category: definition
date created: 2021-01-15 13:42:35
date modified: Tuesday, 21st February 2023, 10:42:53 pm
---

# Tangent Space

## Statements

**Definition**. Let $V^n$ be an [[Euclidean space]]. The _tangent space_, denoted as $T_a(\mathbb{R}^n)$, is the set of pair of points $(a,x)$ in $\mathbb{R}^n\times\mathbb{R}^n$, where $a$ are initial points and $x$ are terminal points $\vec{ax}$ having each pair is denoted as $X_a$ and as called as _tangent vectors_. Together with the injection
$$\begin{array}{rrcl}
\varphi_a:&T_a(\mathbb{R}^n)&\to&V^n\\
&X_a&\mapsto&(x^1-a^1,\ldots,x^n-a^n)\;.
\end{array}
$$
satisfying the operations
$$X_a+Y_a=\varphi_a^{-1}(\varphi_a(X_a)+\varphi_a(Y_a))$$
and, for every $\alpha\in\mathbb{R}$,
$$\alpha X_a=\varphi_a^{-1}(\alpha\varphi_a(X_a))\;.$$
the tangent space is a [[Vector Space|vector space]].

**Remark**. This definition is a particular case of [[Tangent Space|tangent spaces to a manifold]]. More especifically, when the [[Differentiable Manifold|manifold]] is an [[Euclidean space]].

## References

[[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 pp. 30]]
[[Tu, L. W. - An introduction to manifolds|@Tu11 pp. 11]]