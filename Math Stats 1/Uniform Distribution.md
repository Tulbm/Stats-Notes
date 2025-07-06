Similar to the [[Discrete Uniform Distribution]], but with a continuous range for the random variable $X$

# Probability Density Function
A random variable has a uniform distribution $X\sim unif(\alpha,\beta)$ if and only if it has the pdf
$$
f(x;\alpha,\beta)=\frac{1}{\beta-\alpha}, \quad \alpha\leq x\leq\beta
$$
1. $f(x)\geq0\quad \forall \alpha\leq x \leq \beta$
2. $$\int_{-\infty}^\infty f(x)dx=\int_{\alpha}^\beta  \frac{1}{\beta-\alpha}=1$$
Mean
$$\begin{align}
\mu=E(X) & =\int_{\alpha}^\beta x \frac{1}{\beta-\alpha}dx \\
 & =\frac{1}{\beta-\alpha} \left[ \frac{x^2}{2} \right|_{ \alpha}^\beta \\
 & =\frac{\alpha+\beta}{2}
\end{align}
$$
Variance
$$\begin{align}
E(X^2) & =\int_{\alpha}^\beta x^2 \frac{1}{\beta-\alpha} \\
 & \dots \\
 & =\frac{\beta^2+\alpha \beta+\alpha^2}{3} \\
Var(X) & =E(X^2)-[E(X)]^2 \\
 & \dots \\
 & =\frac{1}{12} (\alpha-\beta)^2
\end{align}
$$
CDF
$$
F(x)\int_{\alpha}^x \frac{1}{\beta-\alpha} =\frac{x-\alpha}{\beta-\alpha}
$$

As possible values of x depend on $\alpha,\beta$ this distribution is called a irregular case

