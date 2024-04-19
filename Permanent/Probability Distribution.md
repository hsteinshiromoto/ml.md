---
tags: [definition, theory/probability]
alias: [probability distribution, probability distributions, distribution, distributions, probability]
title: Probability Distribution
date created: 2022-12-30 14:49:28
date modified: Saturday, 31st December 2022, 22:02:27
---

# Probability Distribution

## Statements

**Definition**. Let $(\Omega,\mathcal{F},P)$ be a [[Probability Space|probability space]], $(\Gamma,\mathcal{S})$ be a [[Measure Space|measurable space]] and $X:\Omega\to\Gamma$ be a [[Random Variable|random variable]], then the function $P_X:\mathcal{S}\to[0,1]$ defined as $S\mapsto P(X^{-1})(S)$ is said to be the _probability distribution of the random variable_ $X$.

## Interpretation

Intuitively, the notion of randomness in the values $X(\omega)$ of $X$ is captured by this construction as follows:

1. An element $\omega\in\Omega$ is selected according to the [[Probability Measure|probability]] $P(\{\omega\})$ that is allocated to $\omega$ by the [[Probability Measure]] $P$ on $(\Omega,\mathcal{F})$.
2. This $\omega$ is mapped onto an element $X(\omega)$ in $\Gamma$, which is also referred to as a realization of the [[Random Variable]] $X$. Across realizations, the values of $X$ exhibit a [[Probability Measure|probability]] distribution that depends both on the properties of $P$ and $X$ and is denoted by $P_X$. The Figure below visualizes the situation.
   ![[Probability Distribution.png]]

Clearly, if $\mathcal{X}=\Omega$, $\mathcal{S} = \mathcal{F}$ and $X:=$ id, then $P$ and $P_X$ are identical. Importantly, the union of the [[Measure Space|measurable space]] $(\mathcal{X},\mathcal{S})$ and the [[Probability Measure]] $P_X$ forms the [[Probability Space]] $(\mathcal{X},\mathcal{S},P_X)$.

## Notation

We first note that random variables of the form $X:\Omega\to\mathcal{X}$ are often written as $X:(\Gamma,\mathcal{F})\to(\mathcal{X},\mathcal{S})$. Second, the following notational conventions for events in $\mathcal{F}$ are commonly employed

$$
\{X\in S\}=\{\omega\in\Omega |X(\omega)\in S\} 
$$

$$
\{X\diamond x\}=\{\omega\in\Omega|X(\omega)\diamond x\}, \diamond\in\{>,\geq,=,\leq,<\} 
$$

for $S\in \mathcal{S}$ and $x\in\mathcal{X}$. The [[Probability Measure|probability]] $P$ is the [[Measure]] of the above sets, e.g., $P(\xi\in S)=P(\{\omega\in\Omega|\xi(\omega)\in S\})$

## Discrete Distribution

![[Probability Mass Function]]

## Continuous Distribution

![[Probability Density Function]]

## Most Common Distributions

```dataview
TABLE title AS "Title",
	category AS "Category",
	is_continuous AS "Is_Continuous"
WHERE contains(title, "Distribution") AND title != "Probability Distribution"
SORT title ASC, category ASC
```

## References

[[D. Ostwald - The general linear model 20_21]]

[Probability distribution - Wikipedia](https://en.wikipedia.org/wiki/Probability_distribution)
