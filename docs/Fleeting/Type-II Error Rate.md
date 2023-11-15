---
alias: test power, power, Type II Error Rate
tags: 
date created: Monday, 16th January 2023, 16:25:38
date modified: Tuesday, 17th January 2023, 21:56:06
---

# [[Type II Error|Type-II Error]] Rate

## Definition

Let $\phi$ be a [[test]], the [[Probability Distribution|probability]] of a [[Type II Error]] under a given probabilistic model is central to the quality of a [[Statistical Test|test]]. The [[Probability Distribution|probability]] of a [[Type II Error]] is defined as

$$p_{\Theta_1}(\phi(y)=0)\;,$$

and referred as _Type II error rate_ of the [[Statistical Test|test]]. Its complementary [[Probability Distribution|probability]] is calculated as

$$\begin{equation}\tag{test power}\beta:=p_{\Theta_1}(\phi(y)=1)\;.\end{equation}$$^testpower

and called as the _power_ of a [[Statistical Test|test]].

## Interpretation

The power of a [[test]] is thus the [[Probability Distribution|probability]] of accepting the [[Statistical Test|alternative hypothesis]] (rejecting the [[Statistical Test|null hypothesis]]), if $\theta\in\Theta_1$, i.e., if the [[Statistical Test|alternative hypothesis]] is true.

> [!note]
> Basic introductions to [[Statistical Test|test|test]] error probabilities often denote the [[Probability Distribution|probability]] of a [[Type II error]] by $\beta\in[0, 1]$ and thus define power by $1-\beta$.

## Reference

[[D. Ostwald - The general linear model 20_21|D. Ostwald - The general linear model 20_21 pp 117]]