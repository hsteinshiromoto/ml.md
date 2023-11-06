---
alias: [differential entropy]
tags: []
date created: 2023-11-06 11:36:33
---

# Differential Entropy

Differential entropy is the continuous analog of Shannon’s entropy. Let $X$ be a [[Random Variable|random variable]] with [[Probability Density Function|probability density function]] $p_X$, the _differential entropy_ is defined by the function
$$\begin{array}{rrcl}
h:&\mathbb{R}&\to&\mathbb{R}\\
  &x&\mapsto&-\displaystyle\int p_x(x)\log_2 p_X(x)\,dx,
\end{array}$$
where the integration is over the support of $p_X$.

## References

- [Differential entropy and privacy of a random variable](https://www.johndcook.com/blog/2023/11/01/differential-entropy-and-privacy/)