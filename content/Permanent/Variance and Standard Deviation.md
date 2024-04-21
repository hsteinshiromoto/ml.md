---
alias: [variance, variances, var, vars, standard deviation, standard deviations, std, stds]
tags: [definition, theory/probability, remark, statistics]
title: Variance and Standard Deviation of a Random Variable
date created: 2023-09-23 22:30:06
date modified: 2023-09-25 16:26:06
---

# Variance and Standard Deviation of a Random Variable

## Statements

**Definition**. ([[D. Ostwald - The general linear model 20_21|Ost20, Definition 6.2.1]]) Let $X$ be a [[random variable]] with [[Expected Value|expectation]] $E(X)$. The _variance_ $X$ is defined as

$$
\texttt{Var}(X)=E((X-E(X))^2)
$$

assuming that this [[Expected Value|expectation]] exists. The _standard deviation_ of a [[random variable]] is defined as the square root of the variance of a [[random variable]],

$$
\texttt{Std}(X)=\sqrt{\texttt{Var}(X)}.
$$

**Remark**. ([[D. Ostwald - The general linear model 20_21|Ost20, Section 6.3]]) The theoretical constructs of [[Expected Value|expectations]], [[Variance and Standard Deviation|variances]], and [[Variance and Standard Deviation|standard deviations]] should not be confused with the concepts of [[Expected Value|sample means]], [[Variance and Standard Deviation|sample variance]], and [[Variance and Standard Deviation|sample standard deviations]]. The former entities are of theoretical nature and can be evaluated once the [[Probability Distribution|distributions]] of [[Random Variable|random variables]] have been specified. The latter entities are of practical nature, can be evaluated numerically based on observed data, and serve as estimators of the former theoretical quantities ^a3bf2c

**Definition**. ([[D. Ostwald - The general linear model 20_21|Ost20, Definition 6.3.1]]) Let $(X_1, \ldots, X_n)$ be [[Random Variable|random variables]] and let $\mu$ be their [[Sample Mean|sample mean]]. Then the _sample variance_ of $(X_1, \ldots, X_n)$ is defined as
$$
\sigma^2(X)=\dfrac{1}{n-1}\sum\limits_{i=1}^{n}(\mu-X_i)^2\;.
$$

The _sample standard deviation_ is defined as

$$
\sigma(X)=\sqrt{\sigma^2(X)}\;.
$$

## References

[[D. Ostwald - The general linear model 20_21]]