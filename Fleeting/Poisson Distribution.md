---
tags: 
is_continuous: N
category:
title: Poisson Distribution
date created: Saturday, 31st December 2022, 22:10:26
date modified: Saturday, 31st December 2022, 22:23:39
---

# Poisson Distribution

## Definition

Let $X$ be a [[random variable]] with outcome set $\mathbb{N}$ and [[Probability Mass Function|PMF]] defined as

$$p_X:\mathbb{N}\to\mathbb{R}_{\geq0}$$

$$\mathbb{N}\ni x\mapsto p_X(x)=\dfrac{\lambda^xe^{-\lambda}}{x!}\;.$$

Then, $X$ is said to be a _Poisson distributed random variable_ with rate $\lambda$.

## Assumptions and Validity

The Poisson distribution is an appropriate model if the following assumptions are true:

- $x$ is the number of times an event occurs in an interval and $x$ can take values in $\mathbb{N}$.
- The occurrence of one event does not affect the probability that a second event will occur. That is, events occur independently.
- The average rate at which events occur is independent of any occurrences. For simplicity, this is usually assumed to be constant, but may in practice vary with time.
- Two events cannot occur at exactly the same instant; instead, at each very small sub-interval, either exactly one event occurs, or no event occurs.

If these conditions are true, then $X$ is a Poisson random variable, and the distribution of $X$ is a Poisson distribution.

## References

[Poisson distribution - Wikipedia](https://en.wikipedia.org/wiki/Poisson_distribution)