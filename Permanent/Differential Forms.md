---
alias: [differential forms, differential form]
tags: [differential_forms]
date created: 2021-01-14 16:50:20
date modified: Tuesday, 24th January 2023, 8:05:06 am
---

# Differential Forms

## Statements

**Definition**. ([[Citation Needed]]) Let $\omega:T_p\mathbb{R}^n\times\cdots\times  T_p\mathbb{R}^n\to\mathbb{R}$ be an [[N-form|n-form]] on the [[Euclidean Tangent Space|Euclidean tangent space]] $T_p\mathbb{R}^n$. It is said to be a *differential form* if every component of $\omega$ is differentiable.

## Interpretation

([[D. Bachman - A geometric approach to differential forms]] pp. 41). Recall from [[constants_existence_for_1-forms_multiplication]] that, for a fixed $p\in\mathbb{R}^3$, every 2-form can be written as
$$\omega(v)=a_p\;dx\wedge dy+b_p\;dx\wedge dz+c_p\;dy\wedge dz,$$
where $a_p, b_p$ and $c_p$ are constants. If $p$ varies over $\mathbb{R}^3$, so will these constants. In other words, $a_p, b_p$ and $c_p$ are functions from $\mathbb{R}^3$ to $\mathbb{R}$. Hence, $\omega$ being differentiable means that each parameter $a, b$ and $c$ is differentiable.

([[D. Bachman - A geometric approach to differential forms]] pp. 42). What does $\omega$ act on? It takes a pair of vectors at each point of $\mathbb{R}^3$ and returns a number. In other words, it takes two vector fields and returns a function $\mathbb{R}^3$ to $\mathbb{R}$. A vector field is simply a choice of vector in $T_p\mathbb{R}^3$. In general, a *differential* $n-$form on $\mathbb{R}^m$ acts on $n$ vector fields to produce a function from $\mathbb{R}^m$ to $\mathbb{R}$.

## Example

[[example_17]]

[[example_4.1]]

## References

[[D. Bachman - A geometric approach to differential forms]] Pp 41