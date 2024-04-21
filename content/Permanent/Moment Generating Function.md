---
alias: [moment, moments, MGF]
tags: [definition, theory/probability]
date created: 2024-04-21 21:39:13
---

# Moment Generating Function

## Statements

**Definition**. Let $X$ be a [[Random Variable|random variable]] with [[Permanent/Probability Distribution|distribution]] $P_X$, the [[Expected Value|expected value]]
$$
E(X^n)=\begin{cases}
\displaystyle\sum_{i\in[1,N]}x_i^nP_X(x_i),&\text{if}&P_X\ \text{is discrete}\\
\displaystyle\int x^nP_X(x)\;dx,&\text{if}&P_X\ \text{is continuous}
\end{cases}
$$
is said to the _$n-$th raw moment_. Let $\mu=E(X)$, the _$n-$th central moment_ is given by
$$
E((X-E(X))^n)=\begin{cases}
\displaystyle\sum_{i\in[1,N]}(x_i-\mu)^nP_X(x_i),&\text{if}&P_X\ \text{is discrete}\\
\displaystyle\int (x-\mu)^nP_X(x)\;dx,&\text{if}&P_X\ \text{is continuous}\;.
\end{cases}
$$

## Remarks

**Remark**. The 1st raw moment reduces to the [[Expected Value|expected value]].

**Remark**. The 2nd central moment reduces to the [[Variance and Standard Deviation|variance]].

