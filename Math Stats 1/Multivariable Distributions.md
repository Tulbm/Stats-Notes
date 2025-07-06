# Discrete

### *Joint Probability Mass Function* 
For two discrete random variables $X$ and $Y$, the joint probability of the events $A = (X=x)$ and $B=(Y=y)$ is
$$
P(X=x,Y=y)=P(X=x\text{ and }Y=y)=P(A\cap B)
$$
The function of the joint probability is called the *joint probability mass function*
$$
f(x)=P(X=x,Y=y)
$$
If and only if:
1. $f(x,y)\geq0, \ \forall x,y$
2. $\sum_{x}\sum_{y}f(x,y)=1$

$$
P((X,Y)\in A)=\sum_{(x,y)}\sum_{\in A}f_{X,Y}(x,y)
$$
If the random variables $X$ and $Y$ are independent, the joint pmf is the product of the two [[Marginal Distributions]]
$$
P(X=x,Y=y)=P(X=x)P(Y=y)=f_{X}(x)f_{Y}(y)
$$
### *Joint Cumulative Distribution* 
If $X$ and $Y$ are discrete random variables and $f(x,y)$ is the joint PMF of $X$ and $Y$
$$
F(x,y)=P(X\leq x,Y\leq y)=\sum_{s\leq x}\sum_{t\leq y}f(s,t)\ \ \ \ \text{ for }x,y\in R
$$

# Continuous

### *Joint Probability Density*
A bivariate function $f(x,y)$ of continuous random variable $X$ and $Y$
$$
P[(X,Y)\in A]=\int_{A}\int f_{X,Y}(x,y)dxdy
$$
It can serve as a joint PDF of a pair of continuous random variables $X$ and $Y$ if it satisfies
1. $f(x,y)\geq0, \text{ for} -\infty<x<\infty$
2. $\int_{-\infty}^\infty \int_{-\infty}^\infty f_{X,Y}(x,y)dxdy=1$

### *Joint Cumulative Distribution
If $X$ and $Y$ are continuous random variables, the function
$$
F(X,Y)=P(X\leq x,Y\leq y)=\int_{-\infty}^y\int_{-\infty}^xf(s,t)dsdt\ \ \ x,y \in (-\infty,\infty)
$$
where $f(s,t)$ is the joint pdf of $X$ and $Y$ at $(s,t)$ is called the joint cumulative distribution of $X$ and $Y$

Similar to the single-variable functions, 
$$
f(x,y)=\frac{\partial^2}{\partial x\partial y}F(x,y)
$$

