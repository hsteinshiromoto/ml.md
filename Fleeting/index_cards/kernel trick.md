[[support vector classifiers]] can be written as
$$b+\sum_i\alpha_i x^Tx^{(i)}\;,$$
where 
* $b$ is the bias
* $\alpha_i$ is the parameter
* $x^{(i)}$ is the observation

The kernel trick is to replace the dot product with a functional $k:\mathbb{R}^n\times\mathbb{R}^n\to\mathbb{R}$:

$$b+\sum_i\alpha_i k(x, x^{(i)})\;.$$

It allows for non-linear decision boundaries.