---
alias: 
tags: analysis
category: definition
date created: Thursday, 9th February 2023, 4:05:18 pm
date modified: Monday, 20th March 2023, 4:38:37 pm
---
%%
children: [[Partial Derivative]]
%%

# Differentiable

## Definition

**Definition**. Let $M$ and $N$ be two [[Differentiable Manifold|differentiable manifolds]] of dimension $m$ and $n$, respectively. A map $f:M\to N$ is said to be _differentiable_ (or smooth) at a point $p\in M$ if there exists [[Locally Euclidean|parametrizations]] $(U,\varphi)$ of $M$ at $p$ (i.e. $p\in\varphi(U)$) and $(V,\psi)$ of $N$ at $f(p)$ with $f(\varphi(U))\subset\psi(V)$ such that the map
$$\hat{f}:=\psi^{-1}\circ f\circ \varphi:U\subset\mathbb{R}^m\to\mathbb{R}^n$$
is smooth.

## Remarks

When $M$ and $N$ are [[Euclidean Space|Euclidean spaces]], the previous definitions reduces to the following. Let $X\subset\mathbb{R}^n$ be an [[open set]] the [[Functions and Mappings|vector-valued function]] $F:X\to\mathbb{R}^m$ is said to be _differentiable at $a\in X$_ if there exists an $m\times n$ matrix $A$ and an $m-$tuple $R(x,a)=(r^1(x,a),\ldots,r^m(x,a))$ defined on $X\times X$ such that the limit
$$\lim_{x\to a}||R(x,a)||=0$$
holds and, for every $x\in X$, the equation

$$\begin{equation}\tag{differentiable}
F(x)=F(a)+A(x-a)+||x-a||R(x,a)
\end{equation}
$$^differentiable

also holds. When $m=1$, the $m-$tuple reduces to $r(x,a)$, the matrix $A$ reduces to the vector $b=(b_1,\ldots,b_n)$ and the Equation (differentiable) reduces to
$$f(x)=f(a)+\sum_{i=1}^n b_i(x^i-a^i)+||x-a||r(x,a)\;.$$

## References

- [[L. Godinho, J. Natario - An introduction to riemannian geometry|@GodNat14, Definition 3.1]]
- [[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 pp. 21 and Definition 2.1]]
