---
alias: [vector space, vector spaces, vector, linear space, linear spaces]
tags: 
date created: 2023-08-06 21:23:34
date modified: 2023-08-06 21:28:05
title: Vector Space
---

Tags: #definition | #geometry/space

# Vector Space

## Statements

**Definition**. A _vector space_ over a field $F$ is a set $V$ together with two binary operations that satisfy the eight axioms listed below. In this context, the elements of $V$ are commonly called _vectors_, and the elements of $F$ are called _scalars_.
- The first operation, called _vector addition_ or simply _addition_ assigns to any two vectors $v_1$ and $v_1$ in $V$ a third vector in $V$ which is commonly written as $v_1+v_2$, and called the _sum_ of these two vectors.
- The second operation, called scalar multiplication, assigns to any scalar $\alpha$ in $F$ and any vector $v$ in $V$ another vector in $V$, which is denoted $\alpha v$.

For having a vector space, the eight following axioms must be satisfied for every $v_1,v_2$ and $v_3$ in $V$, and $\alpha$ and $\beta$ in $F$.

| Axiom | Meaning |
| --- | --- |
| [Associativity](https://en.wikipedia.org/wiki/Associativity "Associativity") of vector addition | $v_1 + (v_2 + v_3) = (v_1 + v_2) + v_3$ |
| [Commutativity](https://en.wikipedia.org/wiki/Commutativity "Commutativity") of vector addition | $v_1+v_2=v_2+v_1$ |
| [Identity element](https://en.wikipedia.org/wiki/Identity_element "Identity element") of vector addition | There exists an element $0\in V$, called the _[zero vector](https://en.wikipedia.org/wiki/Zero_vector "Zero vector")_, such that $v+0=v$, for every $v\in V$ |
| [Inverse elements](https://en.wikipedia.org/wiki/Inverse_element "Inverse element") of vector addition | For every $v\in V$, there exists an element $-v\in V$, called the _[additive inverse](https://en.wikipedia.org/wiki/Additive_inverse "Additive inverse")_ of $v$, such that $v + (-v) = 0$ |
| Compatibility of scalar multiplication with field multiplication | For every $v\in V$, $\alpha(\beta v)=(\alpha\beta)v$ |
| Identity element of scalar multiplication | For every $v\in V$, $1v=v$, where 1 denotes the [multiplicative identity](https://en.wikipedia.org/wiki/Multiplicative_identity "Multiplicative identity") in $F$. |
| [Distributivity](https://en.wikipedia.org/wiki/Distributivity "Distributivity") of scalar multiplication with respect to vector addition   | $\alpha(v_1+v_2)=\alpha v_1+\alpha v_2$ |
| Distributivity of scalar multiplication with respect to field addition | For every $v\in V$, $(\alpha+\beta)v=\alpha v+\beta v$ |

## References

https://en.wikipedia.org/wiki/Vector_space