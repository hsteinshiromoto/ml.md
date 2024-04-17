---
alias: [metric spaces are Hausdorff]
tags: [result/proposition]
date created: 2024-04-17 22:18:20
---

# Metric Spaces Are Hausdorff

## Statements

**Proposition**. Every [[Metric Space|metric space]] is [[Hausdorff Space|Hausdorff]].

_Proof_. Let $(X, d)$ be a [[Metric Space|metric space]] and let $x, y\in X$ with $x \neq y$. Let $r = d(x, y)$. Let
$U = B_{<r/2}(x)$ and $V = B_{<r/2}(y)$. Then $x\in U$ , $y\in V$. We claim $U\cap V = \emptyset$. If not there
exists $z \in U \cap V$ . But then $d(x, z) < r/2$ and $d(z, y) < r/2$ so we get
$r = d(x, y) \leq d(x, z) + d(z, y) < r/2 + r/2$ i.e. $r < r$, a contradiction. Hence $U \cap V = \emptyset$ and $X$ is [[Hausdorff Space|Hausdorff]].