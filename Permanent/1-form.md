---
alias: [1-forms]
tags: [differential_forms]
date created: 2021-01-11 16:36:45
date modified: Monday, 23rd January 2023, 9:50:05 pm
---

# $1-$form

## Statements

**Definition**. ([[Bachman, D. - A geometric approach to differential forms|@Bac12, Ch. 3]]) Let $p$ be a point in $\mathbb{R}^n$ and consider the [[Euclidean Tangent Space|Euclidean tangent space]] $T_p\mathbb{R}^n$, the linear function
$$\begin{array}{rrcl}
    \omega:&T_p\mathbb{R}^n&\to&\mathbb{R}\\
    &v&\mapsto&v_1\;dx_1+v_2\;dx_2+\cdots+v_n\;dx_n
 \end{array}$$
is said to be a *1-form*.

## Interpretation

A 1-form maps the coordinates $dx$ and $dy$ of the tangent passing through the point $p\in T_p\mathbb{R}^2$ into the vector $(a,b)$.

## Example

1. Let $\omega(\langle dx, dy\rangle)=-dx+4dy$.
   a. Compute $\omega(\langle 1, 0\rangle)$, $\omega(\langle 0, 1\rangle)$ and $\omega(\langle 2, 3 \rangle)$.
   b. What line does $\omega$ project vectors onto?

a. $\omega(\langle 1, 0\rangle)=-1$, $\omega(\langle 1, 0\rangle)=4$ and $\omega(\langle 2, 3 \rangle)=10$.
b. Onto $\langle -1, 4\rangle$.
