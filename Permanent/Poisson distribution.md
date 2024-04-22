---
alias: [Poisson Distribution, Poission distribution, Poission distributions]
tags: [definition, theory/probability, statistics]
title: Poisson Distribution
date created: 2023-09-13 21:26:49
date modified: 2023-09-26 21:56:35
is_continuous: Y
is_univariate: Y
aliases:
  - Poisson
---

# Poisson Distribution

> [!info] Parameters
> - $\lambda$: rate.

A [[random variable]] is said to be _Poisson_ distributed if the probability of getting exactly $k\in\mathbb{N}$ occurrences is described by the following

> [!info] [[Probability Mass Function]]
> $$
> \begin{array}{rrcl}
> p_X(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\dfrac{\lambda^ke^{-\lambda}}{k!}\;.
> \end{array}
> $$

> [!info] Moments
> - [[Expected Value|Expected value]]: $E[X]=\lambda$,
> - [[Variance and Standard Deviation|Variance]]: $\texttt{Var}(X)=\lambda$.

The Poisson distribution is an appropriate model if the following assumptions are true:

- $x$ is the number of times an event occurs in an interval and $x$ can take values in $\mathbb{N}$.
- The occurrence of one event does not affect the probability that a second event will occur. That is, events occur independently.
- The average rate at which events occur is independent of any occurrences. For simplicity, this is usually assumed to be constant, but may in practice vary with time.
- Two events cannot occur at exactly the same instant; instead, at each very small sub-interval, either exactly one event occurs, or no event occurs.

## Relationship with other Distributions

Let $X$ be a discrete [[Random Variable|random variable]] following a [[Binomial distribution]] with parameter $n$. Then, $X$ converges to the [[Permanent/Poisson distribution|Poisson distribution]] with parameter $\lambda=np$, when $n\to\infty$ and $p\to0$.