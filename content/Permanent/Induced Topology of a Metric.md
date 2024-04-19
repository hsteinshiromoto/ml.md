---
alias: []
tags: [result/proposition, geometry/topology]
category: proposition
date created: 2021-01-11 13:18:43
date modified: Friday, 3rd February 2023, 11:29:44 am
---

# Induced Topology of a Metric

## Statements

**Proposition**. [^1] Let $(X, d)$ a [[Metric Space|metric space]], if for every $y\in X$, there exists $\varepsilon>0$, such that the [[Open Ball|open ball]]
$$
B_{<\varepsilon}(y)=\{x\in X| d(y,x)<\varepsilon\}
$$
satisfies $B_{<\varepsilon}(y)\subset X$, then $X$ is an [[Topological Open Set|open set]] and there exists a collection of [[Open Ball|open balls]] that forms a [[Topology|topology]] $\tau$ on $X$ and the triple $(X,d,\tau)$ forms a [[Topological Space|topological space]].

_Proof_. Let $\tau=\{B_{<i}(y)\}_{i\in\mathbb{N}}$ be a [[Sequence|sequence]] of [[Open Ball|open balls]]. Under the hypothesis of the proposition, $X$ and $\emptyset$ belong to the [[Sequence|sequence]] of [[Open Ball|open balls]]. The other two properties follows from the definition of the [[Topology|topology]]. Thus, $X$ is a [[Topological Open Set|topological open set]].

## References

[1] https://math.stackexchange.com/questions/1409687/what-is-the-topology-induced-by-a-metric/1409698
