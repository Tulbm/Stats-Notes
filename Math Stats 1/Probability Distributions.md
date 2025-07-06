[[Random Variables]]
With $X$ being a discrete random variable, $f(x)=P(X=x)$ for each $x$ within the domain of $X$ is called the probability distribution of $X$
- or the probability mass function (PMF)

A function $f(x)$ can serve as a PMF of a discrete random variable $X$ if and only if:
1. $f(x)\geq0\ \ , \forall x\in X$
2. $\sum_{x}f(x)=1$

PMFs can be represented by simple histograms or bar charts

Cumulative Distribution Function of $X$ (CDF):
$$
F(x)=P(X\leq x)=\sum_{t\leq x}f(t),\ \forall -\infty<x<\infty
$$
where $f(t)$ is the probability distribution of the discrete random variable $X$ at $t$

The values $F(x)$ of $X$ need to satisfy:
1. $F(-\infty)=0,\text{ and }F(\infty)=1$
2. $a<b\to F(a)\leq F(b)$ for any $a$ and $b$ (non-decreasing at every point)

If the range of a random variable $X$ consists of $k$ values $x_{1}<x_{2}<\dots<x_{k}$ , then 
- $f(x_{1})=F(x_{1})$
- $f(x_{i})=F(x_{i})-F(x_{i-1}),\ \ \ \forall i=1,2,\dots k$

[[Probability Densities]]


# Probability distribution of a random variable
- probability mass function
	- P(X = x)
	- cumulative distribution function
		- $F(x) = P(X \geq )$
- a listing of all possible values of X and their probabilities of occurring
- $P(X = x) = \begin{pmatrix}   2\\   x   \end{pmatrix}0.03^x0.97^{2-x}$
	- for x = 0,1,2
- ![](https://i.imgur.com/2PEm6my.png)
- expectation and variance
	- expected value/expectation
		- the theoretical mean of the random variable, or equivalently, the mean of its probability distribution
			- real distribution is never gonna be exactly = the theoretical one
			- ![](https://i.imgur.com/XyZIXXt.png)
		- E(x)
			- values x probability of occurring
			- $$E(X) = \sum_{all\ x}xp(x)$$
			- Mu = theoretical mean = E(x)
		- expectation of a function g(X)
			- $$E[g(X)] = \sum_{all\ x}g(x)p(x)$$
		- variance of a disc random variable
			- the expectation of its squared distance from the mean
			- $$Var(X) = E[(X-\upmu )^2] = \sum_{all\ x}(x- \upmu )^2p(x)$$
			- handy relationship
				- theoretically the same, often easier to calculate
				- $$ E[(X-\upmu )^2] = E(X^2) - [E(X)]^2 $$
					- $E(x)=\mu$
					- $E[(x-\mu)^2] = E[x^2-2x\mu+\mu ^2]=E(x^2)-2E(x\mu)+E(\mu^2)$
					- $=E(x^2)-2E(x)\cdot \mu +\mu^2$
					- $=E(x^2)-2\mu\mu+\mu^2= E(x^2)-\mu^2=E(x^2)-[E(x)]^2$
		- sd of a random variable(σ)
			- sqrt of variance (Var(X))
[[Hypergeometric Distribution]]
[[Bernoulli Distribution]]