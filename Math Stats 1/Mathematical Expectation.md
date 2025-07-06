# Discrete case
If $X$ is a random variable and $f(x)$ is the probability distribution of $X$ at x, the mean/expected value of $X$ is
$$
E(x)=\sum_{x}x\cdot P(X=x)=\sum_{x}x\cdot f(x)
$$
### Joint Probability Mass function
$$
E[g(X,Y)]=\sum_x\sum_yg(x,y)\cdot f_{X,Y}(x,y)
$$
# Continuous case
If $X$ is a random variable and $f(x)$ is the probability density of $X$ at x, the mean or expected value of $X$ is
$$
E(X)=\int_{\infty}^ \infty x\cdot f(x)\,dx
$$
if the integral is not finite, $E(X)$ does not exist


### Joint Probability Density Function
$$
E[g(X,Y)]=\int_{-\infty}^\infty\int_{-\infty}^\infty g(x,y)\cdot f_{X,Y}(x,y)dx
$$
# Properties
Expected value of a function of $X$

If the series is [[Convergence of Series#Absolutely Convergent Series|absolutely convergent]] / the integral is finite 
$$
E[g(X)]=\int_{-\infty}^ \infty g(x)f(x)\,dx
$$
$$
E[g(X)]=\sum_{x}g(x)f(x)
$$
Otherwise, the expectation doesn't exist

If $g(X)$ is something simple, $E[g(X)]$ could be calculated using $E[X]$, but when $g(X)$ has different behaviours depending on $X$ (piecewise, etc), the integral with both functions is necessary, possibly also splitting up the bounds




Simplifying the base definition:
$$
E[aX+b]=aE[X]+b
$$
Linear Combination
$$
E\left[ \sum_{i=1}^nc_{i}g_{i}(X) \right]=\sum_{i=1}^n c_{i}E[g_{i}(x)]
$$
Expansion with the binomial theorem
$$
\left.E[(aX+b)^n]=\sum_{i=0}^n\left(\begin{array}{c}n\\i\end{array}\right.\right)a^{n-i}b^iE(X^{n-1})
$$
# Darth Vader Rule

$$
E(X)=\int_{0}^\infty [1-F(X)]\, dx
$$
