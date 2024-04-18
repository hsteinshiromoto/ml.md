---
alias: 
tags: topology, linear algebra
category: definition
date created: Wednesday, 8th February 2023, 10:09:43 pm
date modified: Wednesday, 8th February 2023, 10:25:07 pm
---

# Relationship between metric and norm

## Proposition

**Proposition**. Let $X$ be a [[Norm|normed]] [[vector space]]. For any $x,y\in X$ if a [[metric]] is defined as $d(x,y)=||x-y||$, then $(X, d)$ is also [[metric space]]. Conversely, let $(X,d)$ be a [[metric space]], where $X$ is a [[vector space]] over $\mathbb{R}$ and $d$ a [[metric]] a defined on $X$ satisfying, for every $x,y\in X$ and $\alpha\in\mathbb{R}$, 
- Translation invariance: $d( x , y ) = d ( x + \alpha , y + \alpha )$.
- [Absolutely homogeneity](https://en.wikipedia.org/wiki/Absolute_homogeneity "Absolute homogeneity"): $d(\alpha x, \alpha y) = |\alpha| d(x,y)$.
Then, the tuple $(X,d)$ is a [[Norm|normed]] [[vector space]].

## References

https://en.wikipedia.org/wiki/Metric_space#Norm_induced_metric