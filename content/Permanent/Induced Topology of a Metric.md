---
alias: 
tags: topology
category: proposition
date created: Monday, 11th January 2021, 1:18:43 pm
date modified: Friday, 3rd February 2023, 11:29:44 am
---
# Induced Topology of a Metric

## Proposition

**Proposition**. Let $(X, d)$ a [[metric space]], if for every $y\in X$, there exists $\varepsilon>0$, such that the [[open ball]]
$$ B_{<\varepsilon}(y)=\{x\in X| d(y,x)<\varepsilon\} $$
satisfies $B_{<\varepsilon}(y)\subset X$, then $X$ is an [[open set]] and there exists a collection of [[Open Ball|open balls]] that forms a [[topology]] $\tau$ on $X$ and the triple $(X,d,\tau)$ forms a [[topological space]].

_Proof_. Let $\tau=\{B_{<i}(y)\}_{i\in\mathbb{N}}$ be a [[sequence]] of [[Open Ball|open balls]]. Under the hypothesis of the proposition, $X$ and $\emptyset$ belong to the [[sequence]] of [[Open Ball|open balls]]. The other two properties follows from the definition of the [[topology]]. Thus, $X$ is an [[open set]].

## References

https://math.stackexchange.com/questions/1409687/what-is-the-topology-induced-by-a-metric/1409698
