---
alias: [vector field, vector fields]
tags: [geometry/LinearAlgebra, definition]
category: definition
date created: 2023-01-27 12:19:00
date modified: Thursday, 16th February 2023, 9:23:58 pm
---

# Vector Field

## Statements

**Definition**. A _vector field_ $X$ on an [[Open Set|open]] subset $U$ of $\mathbb{R}^n$ is a [[Functions and Mappings|vector-valued function]] $X:U\to\mathbb{R}^m$ that assigns to each point $p\in U$ a vector $\mathbb{R}^m$.

**Remark**. From the [[Corollary Tangent Vectors are Derivations|corollary that tangent vectors are derivations]], the image of vector field $X:U\to T_p(\mathbb{R}^n)$ at $p\in U$, denoted as $X_p$, has basis $\{\partial/\partial x^i|_p\}$. Thus, the vector $X_p$ is a linear combination
$$X_p=\sum_{i=1}^na^i(p)\left.\dfrac{\partial}{\partial x^i}\right|_p\;, p\in U\;,a^i(p)\in\mathbb{R}\;.$$

## References

[[Tu, L. W. - An introduction to manifolds|@Tu11, pp. 14]] and [[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 Section 2.5]]