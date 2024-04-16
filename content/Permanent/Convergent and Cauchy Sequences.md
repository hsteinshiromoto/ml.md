---
alias:
tags: 
date created: 2023-07-11 22:14:55
date modified: 2023-08-06 14:01:01
title: Convergent and Cauchy Sequences
---

Convergent and Cauchy Sequences

tags: #result/theorem | #geometry/topology

# Convergent and Cauchy Sequences

## Statements

**Theorem** ([[A Short Introduction to Metric Spaces|@Eck23, Theorem 5.1]]). Any [[Limit of a Sequence|convergent sequence]] in any [[metric space]] is a [[Cauchy sequence]].

### Proof

_Proof_. Let $\{x_n\}_{n\in\mathbb{N}}$ be a sequence in the [[Metric Space|metric space]] $(X,d)$ and suppose that Let $\{x_n\}_{n\in\mathbb{N}}$ [[Limit of a Sequence|converges]] to $x$. For any $\varepsilon>0$, there exists $N>0$ such that, for every $i\geq N$, the inequality $d(x_i,x)<\varepsilon/2$ holds. Also, for every $m,n\geq N$, the inequalities $d(x_n,x_m)\leq d(x_n,x)+d(x_m,x)<\varepsilon/2 + \varepsilon/2=\varepsilon$ hold. Thus, $\{x_n\}_{n\in\mathbb{N}}$ is a [[Cauchy sequence]]

## Remark

An example of a [[Cauchy Sequence]] that is not [[Limit of a Sequence|convergent]]. Let $𝑋=\mathbb{Q}$ be the set of rational numbers with the usual metric given by $𝑑(𝑥,𝑦)=|𝑥−𝑦|$. Consider the sequence defined by

$x_1=1$
$x_{n+1}=1+1/(1+x_n)$

One can show that this [[sequence]] is a [[Cauchy Sequence]] in $\mathbb{Q}$, but there exists no $𝑥\in \mathbb{ℚ}$ that is a limit of the sequence.