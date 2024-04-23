---
alias: [$\chi^2$ Distribution, chi-square distribution, chi-square]
tags: [theory/probability, definition, statistics]
is_continuous: Y
category: 
title: $\chi^2$ Distribution
linter-yaml-title-alias: $\chi^2$ Distribution
date created: 2022-12-31 14:50:10
date modified: Saturday, 31st December 2022, 15:02:41
---

# Chi-Squared Distribution

Let $n\in\mathbb{N}_{>0}$, a [[Random Variable|random variable]] $X$ is said to be _$\chi^2$ distributed with_

> [!info] Parameters
> - $n>0$: Degrees of freedom

if is described by the following

> [!info] [[Probability Density Function]]
> $$
> \begin{array}{rrcl}
> 	p_X:&\mathbb{R}_{>0}&\to&\mathbb{R}_{>0}\\
> 	&x&\mapsto& \dfrac{x^{\tfrac{n}{2}-1}}{\Gamma(n/2)2^{n/2}}\exp(-x/2)\;.
> \end{array}
> $$

The [[Probability Density Function|PDF]] of a chi-squared [[random variable]] by $\chi^2(\cdot;n)$.

## Relationship with Other Distributions

### Gamma Distribution

![[Gamma Distribution#^c14c0f]]

## References

[[D. Ostwald - The general linear model 20_21|Ost20, Definition 7.4.1]]