---
alias: [likelihood, likelihood function]
tags: []
date created: 2023-09-25 09:48:39
---

# Likelihood Function

## Definition

Let $X$ be a discrete [[random variable]] with [[probability measure|probability mass function]] $p$ depending on a parameters $\theta$. Then, the function
$$\begin{align}
L:\mathbb{R}&\to&\mathbb{R}\\
\theta&\mapsto&L(\theta|x)
\end{align}$$
is said to be the *likelihood function* of $\theta$, given the outcome $x$ of the [[random variable]] $X$.

It is calculated as $p_\theta(x)$.

N.B.: This function must not be confused with $p(\theta|x)$, i.e., $L(\theta|x)\neq p(\theta|x)$.