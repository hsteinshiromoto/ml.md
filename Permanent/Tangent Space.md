---
alias: [tangent spaces, tangent space, tangent vector, tangent vectors]
tags: [geometry/differential, definition]
category: definition
date created: 2023-02-21 22:31:12
date modified: Friday, 24th March 2023, 4:50:49 pm
---

# Tangent Space to a Manifold

## Definition

**Definition**. Let $c:(-\varepsilon,\varepsilon)\to M$ be a [[Differentiable|differentiable]] curve on a [[Differentiable Manifold|smooth manifold]] $M$. Consider the set set $\mathcal{C}^\infty(p)$ of all functions $f:M\to\mathbb{R}$ that are differentiable at $c(0)=p\in M$. The _tangent vector to the curve_ $c$ at $p$ is the operator
$$\begin{array}{rrcl}
\dot{c}(0):&\mathcal{C}^\infty&\to&\mathbb{R}\\
&f&\mapsto&\dot{c}(0)(f)=\dfrac{d(f\circ c)}{dt}(0)\;.
\end{array}$$
The _tangent space_ at $p$ is the space $T_p(M)$ of all tangent vectors at $p$.

## Remarks

**Remarks**. The tagent vector satisfies, for every $\alpha,\beta\in\mathbb{R}$, and for every $f,g\in\mathcal{C}^\infty(p)$ the two conditions
1. Linearity: $\dot{c}(0)(\alpha f+\beta g)=\alpha \dot{c}(0)(f)+\beta \dot{c}(0)(g)$.
2. [[Chain rule]]: $\dot{c}(0)(fg)=(\dot{c}(0)(f))g(0)+f(0)\dot{c}(0)(g)$
 The tangent space $T_pM$ is a [[vector space]] with operations in defined, for every [[differentiable]] curves $c_1,c_2\in M$ by
$$(\dot{c}_1(0)+\dot{c}_2(0))f=\dot{c}_1(0)(f)+\dot{c}_2(0)(f)$$
$$\alpha (\dot{c}(0)(f))=(\alpha \dot{c}(0))(f)\;.$$

## References
- [[L. Godinho, J. Natario - An introduction to riemannian geometry|@GodNat14, Definition 4.1]]
- [[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 Chapter 4 Definition 1.1]]