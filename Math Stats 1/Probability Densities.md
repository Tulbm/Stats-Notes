Also called, probability density functions (pdf), densities
- have a continuous 

Probabilities can be thought of as areas under the curves of functions (found by integration)
- A single point on the line has no *width* ($P(X=a)=0$)
- implies $P(X\leq a) = P(X<a),P(a\leq X \leq b) = P(a\leq X < b) = P(a<X\leq b) = P(a<X<b)$

A function $f(x)$ is called a probability density function (pdf) of the continuous random variable $X$ if and only if
$$P(a\leq X\leq b) = \int_a^bf(x)dx$$
for any real constants $a$ and $b$ with $a\leq b$

A function can *serve* as a probability density of a continuous random variable $X$ if all $f(x)$:
1. $f(x)\geq0,$ for $-\infty<x<\infty$ (pdf will never go below the x axis)
2. $\int_{-\infty}^\infty f(x)dx=1$



- often represented by a probability density function (PDF), f(x) that gives the relative likelihood of all values of x
	- f(x) = height of the curve at point x
		- not a probability
			- probabilities = areas under the curve
	- theoretical mean = E(X)
		- $E(X)= \int_{-\infty}^\infty xf(x)dx$
	- variance = $\sigma ^2$
		- $Var(X)=E[(X-\mu)^2]$ 
			- = $\int_{-\infty}^\infty (x-\mu)^2f(x)dx$
		- handy relationship
			-  $E[(X-\mu)^2]=E(X^2)-(E(X))^2$
				- $E(x)=\mu$
				- $E[(x-\mu)^2] = E[x^2-2x\mu+\mu ^2]=E(x^2)-2E(x\mu)+E(\mu^2)$
				- $=E(x^2)-2E(x)\cdot \mu +\mu^2$
				- $=E(x^2)-2\mu\mu+\mu^2= E(x^2)-\mu^2=E(x^2)-[E(x)]^2$
# Cumulative Distribution Function (CDF)
For a continuous random variable $X$ that has the *probability density* at $t$ as $f(t)$, the cumulative distribution of $X$ is

$$
F(x)=P(X\leq x)=\int_{-\infty}^xf(t)dt, \ \ \ \ \forall x\in[-\infty,\infty]
$$
If $f(x)$ and $F(x)$ are the pdf and cdf of $X$, then
$$
\begin{align}
P(a\leq X\leq b)  =F(b)-F(a),\ \ \ \  & \text{for any real constants } a,b,\ a\leq b
 \\
\text{and}\   F'(x)   & =f(x)
\end{align}
$$

