---
alias: []
tags: [geometry/topology, geometry/LinearAlgebra, results/proposition, definition]
category: definition
date created: 2023-02-08 22:09:43
date modified: Wednesday, 8th February 2023, 10:25:07 pm
---

# Relationship between Metric and Norm

## Statements

**Proposition**. Let $X$ be a [[Norm|normed]] [[Vector Space|vector space]]. For any $x,y\in X$ if a [[Metric|metric]] is defined as $d(x,y)=||x-y||$, then $(X, d)$ is also [[Metric Space|metric space]]. Conversely, let $(X,d)$ be a [[Metric Space|metric space]], where $X$ is a [[Vector Space|vector space]] over $\mathbb{R}$ and $d$ a [[Metric|metric]] a defined on $X$ satisfying, for every $x,y\in X$ and $\alpha\in\mathbb{R}$,
- Translation invariance: $d( x , y ) = d ( x + \alpha , y + \alpha )$.
- [Absolutely homogeneity](https://en.wikipedia.org/wiki/Absolute_homogeneity "Absolute homogeneity"): $d(\alpha x, \alpha y) = |\alpha| d(x,y)$.
Then, the tuple $(X,d)$ is a [[Norm|normed]] [[Vector Space|vector space]].

## References

https://en.wikipedia.org/wiki/Metric_space#Norm_induced_metric