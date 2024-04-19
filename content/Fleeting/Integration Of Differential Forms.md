---
alias: []
tags: [definition, geometry/differential]
date created: 2021-01-18 15:41:57
date modified: Monday, 23rd January 2023, 9:55:07 pm
---

# Integration Of Differential Forms

## Statements

**Definition**. Let $R$ be an [[Open Set|open set]] of $\mathbb{R}^n$ and let $f:R\to \mathbb{R}$ be an differentiable function, for each $x,y\in R$ define the [[Differential Forms|differential forms]]
$$\begin{array}{rrcl}
\omega:&T_vR\times\cdots\times T_vR&\to&\mathbb{R}\\
&(v_1,\ldots,v_n)&\mapsto&f(x_1,\ldots,x_n)\;dx_1\wedge\cdots\wedge dx_n\;.
\end{array}$$
Then, the *integration* of $\omega$ over $R$ is given by
$$\int_R\omega=\int_Rf\;dx_1\cdots dx_n\;.$$

To decide whether the right-hand side of the equation is positive or negative, an [[Orientation|orientation]] needs to be specified. 

## Using a Parametrization

Let $\phi:R\subset\mathbb{R}^n\to M\subset\mathbb{R}^m$ be a [[Curve]]. Then, the integration of $\omega$ over $M$ yields
$$\int_M\omega=\pm\int_R\omega_{\phi(x_1,\ldots,x_n)}\left(\dfrac{\partial\phi}{\partial x_1}(x_1,\ldots,x_n),\ldots,\dfrac{\partial\phi}{\partial x_n}(x_1,\ldots,x_n)\right)\;dx_1\wedge\cdots\wedge dx_n$$

## Interpretation

The above definition can be viewed in more simple term as shown in [[Bachman, D. - A geometric approach to differential forms|@Bac12, pp. 43]]. Let $R$ be an [[Open Set]] of $\mathbb{R}^2$  and let $f:R\to \mathbb{R}$ be an differentiable function, for each $x,y\in R$ define the [[Differential Forms]]
$$\begin{array}{rrcl}
\omega:&T_xR\times T_yR&\to&\mathbb{R}\\
&(v_x,v_y)&\mapsto&f(x,y)\;dx\wedge dy\;.
\end{array}$$
Then, the *integration* of $\omega$ over $R$ is given by
$$\int_R\omega=\int_Rf\;dxdy\;.$$

Let $\phi:R\to M\subset\mathbb{R}^2$ be a [[Curve]] of $R$. Then, the integration of $\omega$ over $M$ yields
$$\int_M\omega=\int_R\omega_\phi\left(\dfrac{\partial\phi}{\partial x}(x,y),\dfrac{\partial\phi}{\partial y}(x,y)\right)\;dx\wedge dy\;.$$

## Summary

To compute the integral of a [[Differential Forms|differential]] [[N-form|n-form]] $\omega$ over a region $S$, the steps are as follows:
1. Choose a parametrization $\Phi:R\to S$, where $R\subset\mathbb{R}^n$
2. Find all the $n$ vectors given by the partial derivatives of $\Phi$. Geometrically, these are the tangent vectors to $S$ which span its tangent space.
3. Plug the tangent vectors into $\omega$ at the point $\Phi(u_1,\ldots,u_n)$
4. Integrate the resulting function over $R$.

## Examples

[[example_4.2]]

[[example_21]]

The next example illustrates how to calculate the integration with a [[Curve]].

[[example_23]]

## References

1. [[Bachman, D. - A geometric approach to differential forms|@Bac12, Sections 4.5 and 4.7]]