---
tags: [definition, theory/probability, theory/measure]
alias: [measure, measures, measurable set, measurable sets]
title: Measure
date created: 2022-12-30 13:49:56
date modified: Friday, 30th December 2022, 21:31:04
---

# Measure

## Statements

**Definition**. Let $\Omega$ be a set and $\mathcal{F}$ a [[Sigma Algebra|σ-algebra]] over $\Omega$. A [set function](https://en.wikipedia.org/wiki/Set_function "Set function") $P:\mathcal{F}\to\mathbb{R}\cup\{\infty\}$ is said to be a _measure_ if it satisfies the following properties:

1. Non-negativity: For all $F \in \mathcal{F}$ , $P(F)\geq0$
2. Null empty set: $P(\emptyset) = 0$.
3. Countable additivity (or [σ-additivity](https://en.wikipedia.org/wiki/Sigma_additivity "Sigma additivity")): For all [countable](https://en.wikipedia.org/wiki/Countable "Countable") collections ${\displaystyle \{F_{i}\}_{i\in\mathbb{N}}}$ of pairwise [disjoint sets](https://en.wikipedia.org/wiki/Disjoint_sets "Disjoint sets") in $F$, the equality
$$
P\left(\bigcup_{i\in\mathbb{N}}\right)=\sum\limits_{i\in\mathbb{N}}^{\infty}P(F_i)
$$

   holds. The elements of $\mathcal{F}$ are said to be _measurable sets_.

## References

[Measure (mathematics) - Wikipedia](https://en.wikipedia.org/wiki/Measure_(mathematics))