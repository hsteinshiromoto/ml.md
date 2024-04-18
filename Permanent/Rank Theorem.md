---
alias: 
tags: linear algebra
category: theorem
date created: Friday, 17th February 2023, 12:08:14 pm
date modified: Friday, 17th February 2023, 12:27:02 pm
---

# Rank Theorem

## Theorem

**Theorem**. Let $A_0\subset\mathbb{R}^n$ and $B_0\subset\mathbb{R}^m$ be [[Open Set|open sets]] and, for a given $r\in\mathbb{N}_{>0}$, let $F\in\mathcal{C}^r(A_0,B_0)$ be a [[Functions and Mappings|vector-valued function]] of [[Rank of a Vector-Valued Function|rank]] $k$ on $A_0$. For every $a\in A_0$ and $b=F(a)$, there exist [[Open Set|open sets]] $U\subset\mathbb{R}^n$,  $V\subset\mathbb{R}^m$, $A\subset A_0$ and $B\subset B_0$ with $a\in A$ and $b\in B$, and there exist [[Diffeomorphism|diffeomorphisms]] $G\in\mathcal{C}^r(A,U)$ and $G\in\mathcal{C}^r(B,V)$ such that the image of the composition 
$$\begin{array}{rrcl}
H\circ F\circ G^{-1}:&U&\to&V\\
&(x^1,\ldots,x^n)&\mapsto&(x^1,\ldots,x^k,0,\ldots,0)
\end{array}
$$
is contained in $V$.

## Remarks

**Remark**. The rank theorem tells us that a mapping of constant rank $k$ behaves locally like a projection of $\mathbb{R}^n=\mathbb{R}^k\times\mathbb{R}^{n-k}$ to $\mathbb{R}^k$, i.e., $F\circ G^{-1}:\mathbb{R}^n\to\mathbb{R}^k$ followed by a injection of $\mathbb{R}^k$ onto $\mathbb{R}^k\times\{0\}\subset\mathbb{R}^k\times\mathbb{R}^{m-k}=\mathbb{R}^m$, i.e., $H\circ F\circ G^{-1}:\mathbb{R}^n\to\mathbb{R}^k\times\{0\}$.

## References

[[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 Theorem 7.1]]