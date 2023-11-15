---
alias: 
tags: 
date created: Wednesday, 11th January 2023, 22:33:46
date modified: Thursday, 12th January 2023, 08:24:28
---

# Test

## Definition

Given the test hypotheses scenario introduced above, a _test_ is defined as a mapping from the data outcome space $\mathbb{R}^n$ to the set $\{0, 1\}$, formally

$$\begin{array}{rrcl}
\phi:&\mathbb{R}^n&\to&\mathbb{R}\\
&y&\mapsto&\phi(y)\;.
\end{array}$$
Here, the test value $\phi(y) = 0$ represents the act of not rejecting [[Statistical Test|null hypothesis]], while the test value $\phi(y) = 1$ represents the act of rejecting the [[Statistical Test|null hypothesis]].

The test is considered as a composition between the [[test statistic]] $\gamma$ and the [[decision rule]] $\delta$ and is defined as $\phi=\delta\circ\gamma:\mathbb{R}^n\to\{0,1\}$.

## Reference

[[D. Ostwald - The general linear model 20_21|Ost20 pp. 116-117]] .