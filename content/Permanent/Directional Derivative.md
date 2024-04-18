---
alias: 
tags: analysis, linear algebra
category: definition
date created: Monday, 18th January 2021, 4:09:06 pm
date modified: Friday, 10th February 2023, 5:10:15 pm
---
%%
Friends: [[Partial Derivative]]
%%
# Directional Derivative

## Definition

**Definition**. Let $F\in\mathcal{C}^\infty(\mathbb{R}^n)$, and $c:[0,1]\to\mathbb{R}^n$ a [[curve]] passing through a point $p=(p^1,\ldots,p^n)$ with direction $v=(v^1,\ldots,v^n)$ given. The _directional derivative_ of $F$ in the direction of $v$ at $p$ is given by the [[chain rule]] as
$$D_vF(p)=\dfrac{F(c(t))-F(p)}{t}=\left.\dfrac{d}{dt}\right|_{t=0}F(c(t))=DF(p)\left.\dfrac{dc}{dt}(t)\right|_{t=0}=DF(p)v\;.$$

## References

Based on [[Tu, L. W. - An introduction to manifolds|@Tu11 pp. 11]]