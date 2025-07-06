# Properties
useful model when events can be thought of as occurring randomly and independently over time/area/volume
- number of chocolate chips in a cookie
- number of radioactive decays of a substance in one second
poisson approximates the [[Binomial Distribution]] when $n\rightarrow \infty$ and $p\rightarrow 0$ 
- reasonable if $n>50$ and $np<5$ 
- no natural upper bound, % goes down but could be possible to have a very large value of occurrences

# Assumptions
Independence
- number of occurrences in non-overlapping intervals needs to be independent
$$
P[x(t_{1},t_{2})=x_{1},x(t_{2},t_{3}=x_{2})]=P(x(t_{1},t_{2})=x_{1})\cdot P(x(t_{2},t_{3})=x_{2})
$$
Individuality
- the probability of more than one success during a very small time interval/region is negligible
- events can only happen one at a time
- for sufficiently short time periods of length $\Delta t$, the probability of 2 or more events occurring in the interval is close to zero i.e. events occur singly not in clusters. 
	- as $\Delta t\to0$, the probability of two or more events in the interval of length $\Delta t$ must go to zero faster than $\Delta t\to0$

Uniformity
- events occur at a uniform or homogenous rate $\lambda$ over time so that the probability of one occurrence in an interval $(\vec{t},t+\Delta t)$ is approximately $\lambda\Delta t$ for any value of t

Probability of a single success occurring in a very short time interval/region is given by $\lambda \cdot \Delta t$ 
# Probability Distribution Function
A random variable $X$ has a Poisson distribution $X\sim Poisson(\lambda)$ if and only if it has the [[Probability Densities|probability mass function]] 
$$P(X=x)=f(x;\lambda)=\frac{\lambda ^xe^{-\lambda}}{x!}, x = 0,1,2\dots,\quad \quad\lambda>0$$
1. $f(x;\lambda)>0$
2. $\sum_{x}f(x;\lambda)=1$
$$
E(X)=Var(X)=\mu=\sigma^2=\lambda
$$


Moment Generating Function
$$
M_{X}(t)=e^{\lambda(e^t-1)}=e^{e^t\lambda}e^{-\lambda}
$$

# Relationship with Binomial
The poisson distribution is derived from the [[Binomial Distribution]]

If we consider intervals of time as being the independent events from the binomial, we can use its pdf and calculate a new function for when there are infinite intervals, or an infinitesimal small interval

The probability of one or no occurrences happening in the interval fsd

$X\sim Bin(n,p), \quad n\to \infty,\quad p\to0, \quad np=\lambda, p=\frac{\lambda}{n}$
$$\begin{align}
\operatorname*{lim}_{n\to\infty}f(x;n,p) & ={n\choose x} p^x(1-p)^{n-x} \\
  & = {n\choose x} \left( \frac{\lambda}{n} \right)^x\left( 1- \frac{\lambda}{n} \right)^{n-x}  \\
 & =\frac{n(n-1)(n-2)\dots(n-x+1)(n-x)!}{x!(n-x)!} \frac{\lambda^x}{n^x} \left( 1- \frac{\lambda}{n} \right)^n \left( 1- \frac{\lambda}{n} \right)^{-x} \\
 & = \frac{n(n-1)(n-2)\dots(n-x+1)}{x!}\frac{\lambda^x}{n^x} \left( 1- \frac{\lambda}{n} \right)^n \left( 1- \frac{\lambda}{n} \right)^{-x}  \\
 & =\frac{\lambda^x}{x!} \left( 1- \frac{\lambda}{n} \right)^n \left( 1- \frac{\lambda}{n} \right)^{-x}\frac{n(n-1)\dots(n-x+1)}{n^x}\\
 & =\frac{\lambda^x}{x!} \lim_{ n \to \infty } \left( 1- \frac{\lambda}{n} \right)^n \cdot 1 \cdot 1 \cdot \left( 1- \frac{1}{n}  \right) \left( 1- \frac{2}{n}  \right) \dots \left( 1- \frac{x-1}{n} \right) \text{ (x terms on num and denom)} \\
 & = \frac{\lambda^x}{x!} e^{ -\lambda}\cdot 1 \\
 & =\frac{\lambda^xe^{-\lambda}}{x!} = P\sim(x,\lambda) 
\end{align}
$$


# Examples
- if:
	- events are occurring independently in time (knowing when one event occurs gives no information about when another event will occur)
		- ![](https://i.imgur.com/ChlJcp3.png)
		- 1st = poisson, random
		- 2nd = clumped, not poisson
		- 3rd = grid/ordered/evenly distributed, not poisson
	- the probability that an event occurs in a given length of time does not change through time (theoretical rate of events stays constant through time)
- then X = number of events in a fixed unit of time and has a
	- poisson distribution with probability mass function
		- with only one parameter
	- 
	- for x = 0,1,2,...
		- 