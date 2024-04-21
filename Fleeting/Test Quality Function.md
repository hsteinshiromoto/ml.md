---
alias: 
tags: 
date created: Monday, 16th January 2023, 17:15:53
date modified: Tuesday, 17th January 2023, 21:57:09
---

# Test Quality Function

## Definition

Let $\phi$ be a [[test]], and $p_\theta$ be a [[Parametric Probabilistic Model|probabilistic model parametrized by]] $\theta$, and $E_{p_\theta}$ the [[Expected Value|expectation]] of a [[random variable]] under $p_\theta$. The function defined as

$$\begin{array}{rrcl}
q:&\Theta&\to&[0,1]\\
&\theta&\mapsto&E_{p_\theta(y)}(\phi(y))
\end{array}$$

is said to be a _test quality function_.

> [!note] Remark
> The test quality function maps the parameter $\theta$ in the value given by the [[Expected Value|expectation]] of the test $\phi$ under the probabilistic model $p_\theta(y)$.
>
>
> The definition of the test quality function is motivated by the value it assumes for $\theta\in\Theta_0$ and $\theta\in\Theta_1$: because the [[random variable]] $\phi$ only takes on values in $\{0, 1\}$, the expected value $E_{p_\theta(y)}(\phi(y))$ is identical to the [[Probability Distribution|probability]] of the event $\phi(y)=1$ under $p_\theta(y)$. Thus, for $\theta\in\Theta_0$, the test quality function returns the size of the test (Eq. [[Type-I Error Rate#^testsize|(test size)]]) and for $\theta\in\Theta_1$, the test quality function returns the power of the test (Eq. [[Type-II Error Rate#^testpower|(testpower)]]).

## References

[[D. Ostwald - The general linear model 20_21|D. Ostwald - The general linear model 20_21 pp 118]]