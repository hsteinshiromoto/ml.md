---
tags: 
alias: [probability triple]
title: Probability Space
date created: Friday, 30th December 2022, 14:04:16
date modified: Friday, 30th December 2022, 14:24:20
---

# Probability Space

## Definition

A probability space is a triple $(\Omega ,{\mathcal {F}},P)$ consisting of:

- The [sample space](https://en.wikipedia.org/wiki/Sample_space "Sample space") $\Omega$ - an arbitrary,
- The [[Sigma Algebra|σ-algebra]] ${\displaystyle {\mathcal {F}}\subseteq 2^{\Omega }}$ (also called $\sigma$-field) - a set of subsets of $\Omega$ , called [events](https://en.wikipedia.org/wiki/Event_(probability_theory) "Event (probability theory)"), such that:
    - ${\mathcal {F}}$ contains the sample space: ${\displaystyle \Omega \in {\mathcal {F}}}$.
    - ${\mathcal {F}}$ is closed under [complements](https://en.wikipedia.org/wiki/Complement_(set_theory) "Complement (set theory)"): if $A\in\mathcal{F}$, then ${\displaystyle (\Omega \setminus A)\in {\mathcal {F}}}$.
    - ${\mathcal {F}}$ is closed under [countable](https://en.wikipedia.org/wiki/Countable_set "Countable set") [unions](https://en.wikipedia.org/wiki/Union_(set_theory) "Union (set theory)"): if ${\displaystyle A_{i}\in {\mathcal {F}}}$ ${\displaystyle i=1,2,\dots }$ , then also ${\textstyle (\bigcup _{i=1}^{\infty }A_{i})\in {\mathcal {F}}}$. [^1]
- The [[Probability Measure]] ${\displaystyle P:{\mathcal {F}}\to [0,1]}$ - a function on ${\mathcal {F}}$ such that:
    - $P$ is [countably additive](https://en.wikipedia.org/wiki/Countably_additive "Countably additive") (also called σ-additive): if ${\displaystyle \{A_{i}\}_{i=1}^{\infty }\subseteq {\mathcal {F}}}$ is a countable collection of pairwise [disjoint sets](https://en.wikipedia.org/wiki/Disjoint_sets "Disjoint sets"), then the equality
    - $P$ is [countably additive](https://en.wikipedia.org/wiki/Countably_additive "Countably additive") (also called σ-additive): if ${\displaystyle \{A_{i}\}_{i=1}^{\infty }\subseteq {\mathcal {F}}}$ is a countable collection of pairwise [disjoint sets](https://en.wikipedia.org/wiki/Disjoint_sets "Disjoint sets"), then the equality $${\textstyle P(\bigcup _{i=1}^{\infty }A_{i})=\sum _{i=1}^{\infty }P(A_{i}),}$$ holds.
    - $P$ is [countably additive](https://en.wikipedia.org/wiki/Countably_additive "Countably additive") (also called σ-additive): if ${\displaystyle \{A_{i}\}_{i=1}^{\infty }\subseteq {\mathcal {F}}}$ is a countable collection of pairwise [disjoint sets](https://en.wikipedia.org/wiki/Disjoint_sets "Disjoint sets"), then the equality
    - The measure of entire sample space is equal to one: ${\displaystyle P(\Omega )=1}$.

## References

[Probability space - Wikipedia](https://en.wikipedia.org/wiki/Probability_space)

[^1]: The corollary from the previous two properties and [De Morgan’s law](https://en.wikipedia.org/wiki/De_Morgan%E2%80%99s_law "De Morgan’s law") is that ${\mathcal {F}}$ is also closed under countable [intersections](https://en.wikipedia.org/wiki/Intersection_(set_theory) "Intersection (set theory)"): if ${\displaystyle A_{i}\in {\mathcal {F}}}$ $i = 1,2,\dots$, then also ${\textstyle (\bigcap _{i=1}^{\infty }A_{i})\in {\mathcal {F}}}$.