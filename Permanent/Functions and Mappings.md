---
alias: function, functions, projection, projections, mapping, mappings, coordinate function, coordinate functions, vector-valued function, vector-valued functions, vector function, vector functions
tags: analysis
category: definition
date created: Friday, 10th February 2023, 2:35:52 pm
date modified: Friday, 10th February 2023, 4:07:37 pm
---

# Functions and Mappings

## Definition

**Definition**. Let $X$ be a set with dimension $n\in\mathbb{N}_{>0}$ and set $Y$ set with dimension 1, a _function_ is relationship between these sets defined as
$$\begin{array}{rrcl}
f:&X&\to&Y\\
&(x^1,\ldots,x^n)&\mapsto& f(x^1,\ldots,x^n)\;.
\end{array}
$$
A _mapping_ or a _vector-valued function_ is a tuple of functions, i.e., it is a relationship between a set $X$ having dimension $n\in\mathbb{N}_{>0}$ into a set $Y$ having  dimension $m\in\mathbb{N}_{>1}$
$$\begin{array}{rrcl}
F:&X&\to&Y\\
&(x^1,\ldots,x^n)&\mapsto&(f^1(x^1,\ldots,x^n),\ldots,f^m(x^1,\ldots,x^n))\;,
\end{array}
$$ where each function $f^i$ is said to be a _coordinate function_. For a mapping, the function 
$$\begin{array}{rrcl}
\pi^i:&X&\to&\mathbb{R}\\
&(x^1,\ldots,x^i,\ldots,x^n)&\mapsto&x^i
\end{array}
$$
is said to be the _projection_ of $X$ into $\mathbb{R}$.

## References

[[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 pp. 25]]