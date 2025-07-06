A distribution similar to the binomial, but where the probability of success $p$ is not a constant

# Probability Distribution Function
A random variable $X$ has a beta distribution if and only if it has the pdf
$$
f(x;\alpha,\beta)=\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1}
$$
for $0<x<1, \quad\alpha>0,\quad \beta>0$

Beta is the continuous [[Binomial Distribution]], where the combination is replaced by the continuous factorials in the [[Gamma function]]
$$
{n\choose x} = \frac{n!}{(n-x)!x!} = \frac{(n-x+x)!}{(n-x)!x!}=
$$

$$
\int_{0}^1f(x;\alpha,\beta)=\int
$$

Mean
$$\begin{align}
E(X^r) & =\int_{0}^1x^r \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1}dx \\
 & =\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \frac{\Gamma(r+\alpha)\Gamma(\beta)}{\Gamma(r+\alpha+\beta)}\int_{0}^1 \frac{\Gamma(r+\alpha+\beta)}{\Gamma(r+\alpha)\Gamma(\beta)}x^{r+\alpha-1}(1-x)^{\beta-1}dx \\
 & =\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \frac{\Gamma(r+\alpha)\Gamma(\beta)}{\Gamma(r+\alpha+\beta)} \cdot 1 \\
 & =\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha+\beta+r)} \frac{\Gamma(r+\alpha)}{\Gamma(\alpha)} \\
 & =\frac{(\alpha+r-1)(\alpha+r-2)\dots\alpha}{(\alpha+\beta+r-1)(\alpha+\beta+r-2)\dots(\alpha+\beta)},\quad \quad r=1,2,3\dots
\end{align}
$$





[[Uniform Distribution]] is a special case of the beta distribution with $\alpha=1$ and $\beta =1$
$$
X\sim unif(0,1)\equiv Beta(1,1)
$$
$$
f(x)=\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1}=\frac{\Gamma(2)}{\Gamma(1)\Gamma(1)}x^0(1-x)^0=1,\quad 0<x<1
$$

