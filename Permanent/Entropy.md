---
alias: [entropy, differential entropy]
tags: []
date created: 2024-04-15 22:01:20
---

# Entropy

In information theory, the _entropy_ of a [[Random Variable|random variable]] is the average level of "information". The core idea of information theory is that the "informational value" of a communicated message depends on the degree to which the content of the message is surprising. If a highly likely event occurs, the message carries very little information. On the other hand, if a highly unlikely event occurs, the message is much more informative. For instance, the knowledge that some particular number _will not_ be the winning number of a lottery provides very little information, because any particular chosen number will almost certainly not win. However, knowledge that a particular number _will_ win a lottery has high informational value because it communicates the outcome of a very low probability event.

## Definition

Let $(\Omega,\mathcal{F},P)$ be a [[Probability Measure|probability]] space and $X:\Omega\to\mathcal{X}$ a [[Random Variable|random variable]]. The _entropy_ of $H$ of $X$ is defined by the formula
$$
H(X)=E[-\log\;p_X]=
\begin{cases} \displaystyle-\sum_{x\in\mathcal{X}}p_X(x)\log(p_X(x)),&\text{if}& X\ \text{is discrete}\\
\displaystyle-\int_\mathcal{X} p_X(x)\log(p_X(x)),&\text{if}& X\ \text{is continuous}\;,
\end{cases}
$$
where $p_x:\mathcal{X}\to[0,1]$ is the
- [[Probability Mass Function|probability mass function]], when $X$ is discrete
- [[Probability Density Function|probability density function]], when $X$ is continuous. In this case, the entropy is also called as _differential entropy_.
