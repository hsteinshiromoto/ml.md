---
alias: 
aliases:
  - binomial
tags: 
title: Binomial Distribution
date created: 2023-09-13 21:26:44
date modified: 2023-09-17 23:12:32
---

# Binomial Distribution

## Definition

Let $X$ be a random variable, $n\in\mathbb{N}$ and $p\in[0,1]$. The probability of getting exactly $k\in\mathbb{N}_{[1,n]}$ successes in $n$ independent Bernoulli trials with parameters $n$ and $p$ is given by the probability mass function:
$$\begin{array}{rrcl}
f(\cdot,n,p):&\mathbb{N}&\to&\mathbb{R}\\
&k&\to&\begin{pmatrix}n\\ k\end{pmatrix}p^k(1-p)^{n-k}\;.
\end{array}$$

## Properties

### Expected Value

$$E[X]=np\;.$$
### Variance

$$\text{Var}(X)=np(1-p)\;.$$