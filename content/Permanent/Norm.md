---
tags: 
alias: [normed, normed space]
date created: 2023-08-06 21:25:52
date modified: 2023-08-06 21:26:45
title: Norm
---

tag: #definition | #geometry/space

# Norm

## Definition

**Definition**. Let $X$ be a [[vector space]] over the complex number $\mathbb{C}$, a _norm_ on $X$ is a function $||\cdot||:X\to\mathbb{R}_{\geq0}$ with the following properties:
1. [Subadditivity](https://en.wikipedia.org/wiki/Subadditive_function "Subadditive function")/[Triangle inequality](https://en.wikipedia.org/wiki/Triangle_inequality "Triangle inequality"): for every $x,y\in X$, the inequality $$||x+y||\leq||x||+||y||$$ holds.
2. [Absolute homogeneity](https://en.wikipedia.org/wiki/Homogeneous_function "Homogeneous function"): for every $x\in X$ and $s\in \mathbb{C}$, $||sx||=|s|\;||x||$, where $|s|$ is the absolute value of $s$.
3. [Positive definiteness](https://en.wikipedia.org/wiki/Positive_definiteness "Positive definiteness"): for every $x\in X$, $||x||=0$ implies $x=0$.
4. Non-negativity: for every $x\in X$, $||x||\geq0$.
A [[vector space]] equipped with a norm is said to be a _normed space_.

## References

https://en.wikipedia.org/wiki/Norm_(mathematics)