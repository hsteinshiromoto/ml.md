---
alias: [partial derivatives, derivative, derivatives]
tags: [definition, analysis]
category: definition
date created: 2023-02-09 16:05:18
date modified: Friday, 10th February 2023, 5:07:46 pm
---

# Partial Derivative

## Statements

**Definition**. ([[Boothby, W. M. - An introduction to differentiable manifolds and riemannian geometry|@Boo75 pp. 21]]) Let $U\subset\mathbb{R}^n$ be an [[Open Set|open set]] and consider the function
$$\begin{array}{rcl}
f:&U&\to&\mathbb{R}\\
&x&\mapsto&f(x)\;.
\end{array}$$For every $a\in U$, the _partial derivative of $f$ at $a$ with respect to $x^j$_ is given by the limit
$$\left.\dfrac{\partial f}{\partial x_j}\right|_a=\displaystyle\lim_{h\to 0}\dfrac{f(a^1,\ldots,a^j+h,\ldots,a^n)-f(a^1,\ldots,a^j,\ldots,a^n)}{h}$$
if it exists.