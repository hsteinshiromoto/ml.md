---
alias: critical value
tags: 
date created: Thursday, 12th January 2023, 08:26:59
date modified: Monday, 16th January 2023, 16:18:37
---

# Rejection Region

## Definition

Let $\gamma$ be a [[test statistic]], the subset of the outcome space for which the tests assumes the value 1 is referred to as the rejection region of the [[Test Statistic|test]]. Formally, the rejection region is a subset of $\mathbb{R}$ defined as

$$R=\{\gamma(y)\in\mathbb{R}|\phi(y)=1\}.$$

**Remark**. The random events $\phi(y) = 1$ and $\gamma(y) \in R$$ are thus equivalent and associated with the same [[Test Statistic|probability under]] $p_\theta$. In a concrete [[Test Statistic|test]] scenario, it is hence usually the [[probability distribution]] of the [[Statistical Test|test statistic]] that is of principal concern for assessing the test’s outcome behaviour.

**Remark**. In general, [[Test Statistic|test]] decision rules considered are based on the [[Statistical Test|test statistic]] exceeding a _critical value_ $u\in R$. By means of the [[indicator function]] $1_{\gamma\geq u}$ , the tests considered here can thus be written as

$$\begin{array}{rrcl}
\phi:&\mathbb{R}^n&\to&\{0,1\}\\
&y&\mapsto&\phi(y)=1_{\gamma\geq u}\;.
\end{array}$$

## References

[[D. Ostwald - The general linear model 20_21|Ost20 pp. 117]]