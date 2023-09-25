---
alias: 
aliases:
  - Poisson
tags:
  - distribution/discrete
title: Poisson Distribution
date created: 2023-09-13 21:26:49
date modified: 2023-09-25 14:57:32
---

# Poisson Distribution

> [!info] Parameters
> - $\lambda$: rate.

A [[random variable]] is said to be _Poisson_ distributed if the probability of getting exactly $k\in\mathbb{N}$ occurrences is described by the following

> [!info] [[Probability Mass Function]]
> $$\begin{array}{rrcl}
> p_X(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
> &k&\to&\dfrac{\lambda^ke^{-\lambda}}{k!}\;.
> \end{array}$$

> [!info] Moments
> - [[Expected Value of a Random Variable|Expected value]]: $E[X]=\lambda$,
> - [[The Relationship Between Sample Mean, Sample Variance and Expectation, Variance|Variance]]: $\texttt{Var}(X)=\lambda$.

The Poisson distribution is an appropriate model if the following assumptions are true:

- $x$ is the number of times an event occurs in an interval and $x$ can take values in $\mathbb{N}$.
- The occurrence of one event does not affect the probability that a second event will occur. That is, events occur independently.
- The average rate at which events occur is independent of any occurrences. For simplicity, this is usually assumed to be constant, but may in practice vary with time.
- Two events cannot occur at exactly the same instant; instead, at each very small sub-interval, either exactly one event occurs, or no event occurs.