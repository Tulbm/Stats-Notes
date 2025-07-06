A random variable $X$ has a geometric distribution $X\sim \text{geometric}(p)$ if and only if it has the probability distribution function
$$
f(x;p)=p(1-p)^{ x-1}
$$
for $x=1,2,3,\dots$
1. $f(x)\geq 0$
2. $\sum p(1-p)^{ x-1}=1$

If we are looking at the number of fails ($x=0$ is possible)
$$
f(x)=p(1-p)^x
$$
Geometric distribution is equivalent to the [[Negative Binomial Distribution]] when only looking for the first success
$X\sim \text{geometric}(p)\equiv NB(1,p)$ 
$$
E(X)=\frac{1}{p}
$$
$$
Var(X)= \frac{1}{p}\left(  \frac{1}{p}-1 \right)= \frac{1-p}{p^2}
$$
