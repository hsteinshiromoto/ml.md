---
tags:
  - probability_theory
  - statistics
aliases:
  - expectation
  - expectations
  - expected value
title: Expected Value of a Random Variable
date created: Friday, 30th December 2022, 19:46:24
date modified: Sunday, 22nd January 2023, 22:20:16
---

# Expected Value of a Random Variable

## Definition

([@][[D. Ostwald - The general linear model 20_21|Ost20]] Definition 6.1.1.) Let $(\Omega,\mathcal{F},P)$ denote a [[probability space]], $(\mathcal{X}, \mathcal{S})$ be a [[Measure Space|measurable space]], and let $X:\Omega\to\mathcal{X}$ denote a [[random variable]]. The _expectation_ (or _expected value_) of $X$ is defined as

$$E(X):=\sum\limits_{x\in\mathcal{X}}xP_X(x)\;,$$

when $X$ is a discrete [[random variable]] with [[Probability Mass Function|PMF]] $P_X$ and as

$$E(X):=\int_{x\in\mathcal{X}}xP_X(x)\;dx\;,$$

when $X$ is a continuous [[random variable]] with [[Probability Density Function|PDF]] $P_X$.

The expectation of a [[random variable]] is said to exist, if it is finite

## References

[[D. Ostwald - The general linear model 20_21]]