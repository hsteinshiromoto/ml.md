---
alias: [limit, convergence]
tags: [geometry/topology, definition]
category: definition
date created: 2023-02-18 22:52:45
date modified: Tuesday, 21st February 2023, 9:55:46 pm
---

# Convergence of a Sequence in terms of a Metric

## Statements

**Definition**. Let $(X,d)$ be a [[Metric Space|metric space]]. Let $\{a_i\}_{i\in\mathbb{N}}\subset X$ be a [[Sequence|sequence]]. A point $a\in X$ is said to be the _limit of the_ [[Sequence|sequence]] $\{a_i\}_{i\in\mathbb{N}}$ if $$\lim_{n\to\infty}d(a,a_n)=0\;.$$
In this case, the sequence is said to _converge_ to $a$ and this is denoted as $\lim_{n\to\infty} a_n=a$.

Note that the [[Induced Topology of a Metric]] implies that the [[Convergence of a Sequence in terms of Open Sets|convergence of a sequence can also be stated in terms of open sets]].

## References

[[Mendelson, B. - Introduction to topology|@Men90 Definition 5.2]]