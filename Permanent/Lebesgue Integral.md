---
alias: [Lebesgue integral, Lebesgue integrals, Lebesgue Integrals]
tags: []
date created: 2024-04-19 22:14:13
---

# Lebesgue Integral

## Context

Every [[Measurable Function|measurable function]] may be approximated by _simple functions_. A function $s:A\subseteq\mathbb{R}^n \to \mathbb{R}$ is said to be _simple_ if its range is constituted by a finite number of values $s_1,\ldots, s_N$, attained respectively on measurable sets $A_1,\ldots,A_N$, contained in $A$. Introducing the _characteristic functions_ $\chi_{A_j}$, we may write
$$
s=\sum_{j=1}^Ns_j\chi_{A_j}\;.
$$

## Statements

**Definition**. Let ${\displaystyle (\Omega,{\mathcal {F}},P )}$ be a [[Measure Space|measurable space]], $A\subset\mathcal{F}$ be [[Measure|measurable set]] and $f:A\to\mathbb{R}$ be a [[Measurable Function|measurable function]]. The _Lebesgue integral_ of $f$ is defined as
$$
\int_A f=\sum_{j=1}^Ns_jP(A_j)\;,
$$
with the convention that, if $s_j = 0$ and $|A_j| = +\infty$, then $s_j P(A_j) = 0$.

## References

[[Salsa S. - Partial Differential Equations in Action|@Sal08, pp. 541]]