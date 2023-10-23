---
alias: [likelihood, likelihood function]
tags: []
date created: 2023-09-25 09:48:39
---

# Likelihood Function

## Definition

**Definition**. Let $X$ be [[random variable]] with [[Permanent/Probability Distribution|probability distribution]] $f:\mathbb{R}^n\times\mathbb{R}^m\to\mathbb{R}$ depending on a parameters $\theta$. Then, for a given outcome $x\in\mathbb{R}^n$, the function
$$\begin{array}{rcll}
L:&\{x\}\times\mathbb{R}^m&\to    &\mathbb{R}\\
 &(x,\theta)    &\mapsto&L(\theta|x)=f(x|\theta)
\end{array}$$
is said to be the *likelihood function* of $\theta$.

## Remarks

Note that, $L(\theta|x)$ does not specify the probability that $\theta$ is true, given the observed outcome $x$.