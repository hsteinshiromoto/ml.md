---
alias: [manifold, differentiable structure, smooth manifold, smooth manifolds, differentiable manifolds]
tags: [geometry/differential, definition]
category: definition
date created: 2023-02-17 15:36:43
date modified: Monday, 20th March 2023, 4:31:01 pm
---

# Differentiable Manifold

## Statement

**Definition**. A [[topological manifold]] $M$ is said to be _differentiable_ if there exist a family of [[Locally Euclidean|parametrizations]] $\varphi_\alpha:U_\alpha\to M$ defined on open sets $U_\alpha\subset\mathbb{R}^n$ such that
1. The [[Coordinate Neighborhood|coordinate neighborhoods]] $\{U_\alpha\}_{\alpha\in\mathbb{N}_{>0}}$ [[Cover|covers]] $M$;
2. For each pair of indices $\alpha,\beta$ such that
   $$W:=\varphi_\alpha(U_\alpha)\cap\varphi_\beta(U_\beta)\neq\emptyset\;,$$
   the overlap mapps
   $$\begin{array}{rrcl}
   \varphi_\beta^{-1}\circ\varphi_\alpha:&\varphi^{-1}_\alpha(W)&\to&\varphi^{-1}_\beta(W)\\
   \varphi_\alpha^{-1}\circ\varphi_\beta:&\varphi^{-1}_\beta(W)&\to&\varphi^{-1}_\alpha(W)\\
   \end{array}$$ are $\mathcal{C}^\infty$.
3. The family $\mathscr{A}=\{(U_\alpha,\varphi_\alpha\}$ is maximal with respect to 1 and 2, meaning that if $\varphi_0\to  M$ is a [[Locally Euclidean|parametrization]] such that $\varphi_0^{-1}\circ\varphi$ and $\varphi^{-1}\circ\varphi_0$ are $\mathcal{C}^\infty$ for all $\varphi\in\mathscr{A}$, then $(U_0,\varphi_0)\in\mathscr{A}$.
A _differentiable manifold_ is a [[topological manifold]] with a differentiable structure.

![[manifold.png]]

## References

- [[L. Godinho, J. Natario - An introduction to riemannian geometry|@GodNat14, Definition 2.1]]
- [[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 Chapter 3 Definition 1.2]]