- [[Binomial Distribution]] with only a single [[Bernoulli Trials|trial]]
# Probability Distribution Function
A random variable $X$ has a Bernoulli distribution, denoted by $X\sim Bernoulli(p)$ if and only if it has the probability distribution function as
$$
f(x)= p^x(1-p)^{1-x} \quad \quad \text{ for }x=0,1
$$
where $p=P(X=1)$

$$
E(X)=\sum_{x}xf(x)=p
$$
$$\begin{align}
Var(X) & =E(X^2)-[E(X)]^2 \\
 & =p-p^2 \\
 & =p(1-p) \\
\end{align}
$$