---
tags: 
title: Statistical Test
alias: [hypothesis test, null hypothesis, nill hypothesis, Hypothesis 0, H0, Hypothesis 1, H1, statistical test, alternative hypothesis]
date created: Saturday, 7th January 2023, 21:03:59
date modified: Monday, 16th January 2023, 16:56:57
---

# Statistical Test

**Definition** ([[D. Ostwald - The general linear model 20_21|Ost20 pp.116]], Statistical Test, Null and Alternative Hypotheses). Let $p_\theta(y)$ be a [[Parametric Probabilistic Model]]. The space parameter $\Theta$ is partitioned into two disjoint subsets $\Theta_0$ and $\Theta_1$. A _test hypothesis_ is a statement about the parameter governing $p_\theta(y)$$ in relation to these parameter space subsets. Specifically, the statement $$\theta\in\Theta_0\Leftrightarrow H=0$$is referred to as the _null hypothesis_ and the statement $$\theta\in\Theta_!\Leftrightarrow H=1$$is referred to as the _alternative hypothesis_.

**Remark**. A statistical hypothesis is a statement about the parameter of a probabilistic model. In the following, we will use the subscript notations $p_{\theta_0}$ and $p_{\theta_1}$ to indicate that the parameter $\theta$ of the probabilistic model $p_\theta$ is an element of $\Theta_0$ or $\Theta_1$, respectively.

**Remark**. The term null hypothesis is not necessarily the statement that some parameter assumes the value zero, even if this is often the case in practice. Rather, the null hypothesis in a statistical testing problem is the statement about the parameter one is willing to nullify, i.e., reject. Finally, the expressions $H = 0$ and $H = 1$ are not conceived as realizations of a [[random variable]] and hence hypothesis-[[Conditional Probability]] statements are not meaningful. The statements $H = 0$ and $H = 1$ are merely equivalent expressions for $\theta\in\Theta_0$ and $\theta\in\Theta_1$, respectively: $H = 0$ refers to the true, but unknown, state of the world that the null hypothesis is true and the alternative hypothesis is false ($\theta\in\Theta_0$), and $H = 1$ refers to the true, but unknown, state of the world that the alternative hypothesis is true and the null hypothesis is false ($\theta\in\Theta_1$).