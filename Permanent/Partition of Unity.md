---
alias: partitions of unity 
tags: topology
category: definition
date created: Monday, 20th March 2023, 9:07:26 am
date modified: Monday, 20th March 2023, 9:17:55 am
---

# Partition of Unity

## Definition

**Definition**. Let $(X,\tau)$ be a [[topological space]] and let $\{U_i\}_i$$ be an [[Open Set|open]] [[cover]] of $X$. A _partition of unity_ associated with this cover is a collection of [[Continuous Function|continuous functions]] $\{\varphi_i\}_i$ such that:

1. Each $\varphi_i$ is a non-negative function with compact support (i.e., it is zero outside of some [[Compact Topological Space|compact set]]).
2.  The support of each $\varphi_i$ is contained in $U_i$.
3.  The sum of all $\varphi_i$ over all $i$ is equal to 1, i.e., for every $x \in X$,
   $$\sum_i\varphi_i(x)=1\;.$$

## Remarks

**Remark**. Using a partition of unity, we can construct a smooth function on $X$ by taking a linear combination of the functions $\varphi_i$ multiplied by smooth functions on $U_i$. Specifically, if $\{f_i\}_i$ is a collection of smooth functions on $U_i$, then the function

$$\begin{array}{rrcl}
f:&X&\to&\bigcup_i f_i(U_i)\\
&x&\mapsto&\sum_i\varphi_i(x)f_i(x)
\end{array}$$
is a smooth function on X.

The partition of unity is a powerful tool in mathematics because it allows us to construct global objects (such as a smooth function on an entire [[Topological Manifold|manifold]]) by gluing together local data (the smooth functions on each open set in the cover). This technique is used in many areas of mathematics, including differential geometry, algebraic topology, and partial differential equations.

## References

- ChatGPT
- [Rowland, Todd](https://mathworld.wolfram.com/topics/RowlandTodd.html). "Partition of Unity." From [_MathWorld_](https://mathworld.wolfram.com/)--A Wolfram Web Resource, created by [Eric W. Weisstein](https://mathworld.wolfram.com/about/author.html). [https://mathworld.wolfram.com/PartitionofUnity.html](https://mathworld.wolfram.com/PartitionofUnity.html)