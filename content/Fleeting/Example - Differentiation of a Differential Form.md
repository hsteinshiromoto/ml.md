---
alias: 
tags: example, differential_forms
date created: Thursday, 21st January 2021, 8:39:05 am
date modified: Monday, 23rd January 2023, 10:17:54 pm
---
# Differentiation of a Differential Form

{[[D. Bachman - A geometric approach to differential forms]] pp. 72} We saw in [[constants_existence_for_1-forms_multiplication]] that, if $d\omega$ is a $2-$form in $\mathbb{R}^3$, then there exists $a,b,c:\mathbb{R}^3\to\mathbb{R}$ such that 

$$d\omega=a(x,y,z)\;dx\wedge dy+b(x,y,z)\;dy\wedge dz+c(x,y,z)\;dx\wedge dz\;.$$

To figure what $a$ is, for example, we need to determine what $d\omega$ does to the vectors $\langle1,0,0\rangle_{(x,y,z)}$ and $\langle0,1,0\rangle_{(x,y,z)}$. Let us compute $d\omega$ assuming that 

$$\omega=f(x,y,z)dx+g(x,y,z)dy+h(x,y,z)dz\;.$$

$$
\begin{eqnarray}
d\omega(\langle1,0,0\rangle, \langle0,1,0\rangle)&=&\dfrac{\partial\omega}{\partial\langle1,0,0\rangle}(\langle0,1,0\rangle)-
\dfrac{\partial\omega}{\partial\langle0,1,0\rangle}(\langle1,0,0\rangle)\\

&=&\left\langle\dfrac{\partial g}{\partial x},\dfrac{\partial g}{\partial y},\dfrac{\partial g}{\partial z}\right\rangle\cdot\langle1,0,0\rangle-\left\langle\dfrac{\partial f}{\partial x},\dfrac{\partial f}{\partial y},\dfrac{\partial f}{\partial z}\right\rangle\cdot\langle0,1,0\rangle\\
&=&\dfrac{\partial f}{\partial x}-\dfrac{\partial f}{\partial y}\;.
\end{eqnarray}
$$
Analogously, we have
$$
\begin{eqnarray}
d\omega(\langle0,1,0\rangle, \langle0,0,1\rangle)&=&\dfrac{\partial h}{\partial y}-\dfrac{\partial g}{\partial z}\\
d\omega(\langle1,0,0\rangle, \langle0,0,1\rangle)&=&\dfrac{\partial h}{\partial x}-\dfrac{\partial f}{\partial z}\;.
\end{eqnarray}
$$

Hence,

$$d\omega=\left(\dfrac{\partial f}{\partial x}-\dfrac{\partial f}{\partial y}\right)\;dx\wedge dy+\left(\dfrac{\partial h}{\partial y}-\dfrac{\partial g}{\partial z}\right)\;dy\wedge dz+\left(\dfrac{\partial h}{\partial x}-\dfrac{\partial f}{\partial z}\right)\;dx\wedge dz\;.$$
