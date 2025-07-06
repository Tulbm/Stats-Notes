# Probability Density Function
A random variable $X$ has a gamma distribution $X\sim Gamma(\alpha,\beta)$ if and only if it has the pdf
$$
f(x;\alpha,\beta)= \frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-x/\beta}\quad \text{ for }x>0
$$
where $\alpha>0$ and $B>0$ and $\Gamma(\alpha)$ is the [[Gamma function]]

1. $f(x)\geq0, \quad \forall x$
2. $$\begin{align}
\int_{-\infty}^\infty f(x)dx & =\int_{0}^\infty \frac{1}{\beta^\alpha \Gamma(\alpha)}x^{ \alpha-1}e^{-x/\beta}dx \\
 & = \frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty x^{\alpha-1}e^{-x/\beta}dx \quad \left( y=\frac{x}{\beta} \right) \\
 & =\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty(\beta y)^{\alpha-1}e^{-y}\beta dy \quad(dx = \beta dy) \\
 & =\frac{1}{\beta^\alpha \Gamma(\alpha)} \beta^\alpha \int_{0}^\infty y^{\alpha-1}e^{-y}dy \\
 & = \frac{1}{\Gamma(\alpha)} \Gamma(\alpha) \\
 & =1
\end{align}
$$Mean
$$\begin{align}
\mu=E(X) & =\int_{0}^\infty x \frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-x/\beta}dx \\
 & =\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty x^{\alpha+1-1} e^{-x/\beta} \\
 & =\frac{1}{\beta^\alpha \Gamma(\alpha)}\beta^{\alpha+1}\Gamma(\alpha+1)\int_{0}^\infty \frac{1}{\beta^{\alpha+1}\Gamma(\alpha+1)}x^{\alpha+1-1}e^{-x/\beta}dx \\
 & =\beta\frac{ \Gamma(\alpha+1)}{\Gamma(\alpha)} \cdot 1 \quad \text{(PDF of }Gamma(\alpha+1,\beta)) \\
 & =\frac{\beta \alpha \Gamma(\alpha)}{\Gamma(\alpha)} \\
\mu & =\beta \alpha
\end{align}
$$
Second moment
$$\begin{align}
E(X^2) & =\int_{0}^\infty x^2 \frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-x/\beta}dx \\
 & =\frac{d^2}{dt^2}M_{X}(t) \\
 & =\frac{d}{dt} \alpha \beta(1-t\beta)^{-\alpha-1} \\
 & =\alpha \beta(-\alpha-1)(1-t\beta)^{-\alpha-2}(-\beta)|_{t=0} \\
 & =-\beta^2\alpha(-(\alpha+1))(1-0)^{-\alpha-2} \\
 & =\beta^2\alpha(\alpha+1) 
\end{align}
$$
Variance
$$
\begin{align}
Var(X) & =E(X^2)-[E(X)]^2 \\
 & =\beta^2\alpha(\alpha+1) - (\alpha \beta)^2 \\
 & = \beta^2(\alpha(\alpha+1)-\alpha^2) \\
 & =\beta^2(\alpha(\alpha+1-\alpha)) \\
 & =\beta^2(\alpha(1)) \\
Var(X) & =\beta^2\alpha
\end{align}
$$

[[Exponential Distribution]] is a special case of the gamma distribution when $\alpha=1$

The [[Chi-Squared Distribution]] is another special case of the gamma distribution with $\alpha=\frac{v}{2}$ and $\beta=2$
# [[Moments]]
The rth moment of a $Gamma(\alpha,\beta)$ distribution is given by
$$
E(X^r)=\beta^r \frac{\Gamma(\alpha+r)}{\Gamma(\alpha)}
$$
