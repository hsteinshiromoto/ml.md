---
alias: [directional derivative, directional derivatives]
tags: [analysis, geometry/LinearAlgebra, definition]
category: definition
date created: 2021-01-18 16:09:06
date modified: Friday, 10th February 2023, 5:10:15 pm
---
%%
Friends: [[Partial Derivative]]
%%

# Directional Derivative

## Statements

**Definition**. ([[Tu, L. W. - An introduction to manifolds|@Tu11 pp. 11]]) Let $F\in\mathcal{C}^\infty(\mathbb{R}^n)$, and $c:[0,1]\to\mathbb{R}^n$ a [[Curve|curve]] passing through a point $p=(p^1,\ldots,p^n)$ with direction $v=(v^1,\ldots,v^n)$ given. The _directional derivative_ of $F$ in the direction of $v$ at $p$ is given by the [[chain rule]] as
$$D_vF(p)=\dfrac{F(c(t))-F(p)}{t}=\left.\dfrac{d}{dt}\right|_{t=0}F(c(t))=DF(p)\left.\dfrac{dc}{dt}(t)\right|_{t=0}=DF(p)v\;.$$

## References

Based on [[Tu, L. W. - An introduction to manifolds|@Tu11 pp. 11]]