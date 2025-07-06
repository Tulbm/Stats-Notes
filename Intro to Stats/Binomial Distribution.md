# Interpretation
- boolean, success or failure
	- getting heads or not
	- being universal blood donor or not
	- winning lotto or not
- needs to be independent
	- if when one trial is done, the percentages change, its not independent and not a binomial
		- X would have the hypergeometric distribution
- a distribution of the number of successes in n independent [[Bernoulli Trials]]
	- or a sequence of bernoulli trials

A random variable $Y=\sum_{i} X_{i}$ follows a binomial distribution, counting the number of successes of the random variable $X$ that follows the [[Bernoulli Distribution]] 
# Probability Distribution Function
A random variable $X$ has a binomial distribution, denoted by $X\sim Bin(n,p)$ if and only if it has the probability distribution function
$$
f(x)=P(X=x)={n\choose x}p^x(1-p)^{n-x}
$$
for $0\leq x\leq n,$ with:
1. $f(x)\geq0$
2. $\sum_{x}f(x)=1$

where $n$ represents the number of total trials, $p$ the probability of "success" and $x$ the number of "successes"
- $p^x(1-p)^{n-x}$ represents the probability of a specific ordering of $x$ successes and $n-x$ failures
- $\begin{pmatrix}   n\\   x   \end{pmatrix}$ represents number of ways it can happen


Mean$$\begin{align}
E(X) & =\sum_{x}xf(x) \\
 & =\sum_{x=0}^n x {n\choose x}p^x(1-p)^{n-x} \\
 & =\sum_{x=1}^n x \frac{n!}{x!(n-x)!}p^x (1-p)^{n-x} \\
 & =\sum_{x=1}^n \frac{n(n-1)!}{(x-1)!(n-x)!}p \cdot p^{x-1}(1-p)^{n-x} \\
 & =np \sum_{x=1}^n \frac{(n-1)!}{(x-1)!(n-1-(x-1))!} p^{x-1}(1-p)^{n-1-(x-1)} \\
 & = np \sum_{x=1}^n Bin(n-1,p) \\
 \mu& =np\cdot1 = np
\end{align}
$$Variance$$
Var(X)=np(1-p)
$$If $X$ represents the number of successes in $n$ trials, then $Y=\frac{X}{n}$ represents the [[Sample Proportion]] of successes

Using [[Chebyshev's Theorem]] we get the law of large numbers:
$$
\lim_{ n \to \infty } P(|y-p|\leq c)=1
$$
- if we repeat the trial for sufficient large number, the proportion of "success", $y=\frac{X}{n}$ will be very close to $p=P(\text{success})$

[[Moment Generating Functions#Binomial distribution|Moment-generating function]] 
$$
M_{X}(t)=[1+p(e^t-1)]^n
$$

- can be approximated with the [[Poisson Distribution#Relationship with Binomial|poisson distribution]] (which is a special case of the binomial)
	- when $n\rightarrow \infty$ and $p\rightarrow 0$ 
		- reasonable if $n>50$ and $np<5$ 
	- useful when we don't wanna deal with big factorials 
		- or if you dont know n and p, but know the mean
# examples
- 1 
	- fair dice rolled 10 times
	- probability of three coming up exactly 2 times
	- $$*P(X=2) = \begin{pmatrix}   10\\2   \end{pmatrix}(\frac{1}{6})^2(1-\frac{1}{6})^{10-2}* $$
- 2
	- n = 3, we want p(X=2)
	- pp(1-p) = p(1-p)p = (1-p)pp = p^2(1-p)
	- p(X=2) = 3p^2(1-p)
	- 3 = combination formula of (3 2)
- 3
	- 25 babies, 20% chance of acne
	- P of exactly one having acne
	- $$P(X=1) = \begin{pmatrix}   25\\1   \end{pmatrix}(\frac{1}{5})^1(1-\frac{1}{5})^{25-1} $$
	- = 0.0236....
	- P that no more than 2 babies have acne?
		- P(X<=2) = P(X = 0) + P(X = 1) + P(X = 2)
		- $$P(X\leq2) = \begin{pmatrix}   25\\0   \end{pmatrix}(0.20^0(1-0.20)^{25} + \begin{pmatrix}   25\\1   \end{pmatrix}(0.20^1(1-0.20)^{24} + \begin{pmatrix}   25\\2   \end{pmatrix}(0.20^2(1-0.20)^{23}$$
		- = 0.0982
	- P that at least one of the babies has acne
		- P(X>=1) = P(x=1) + ... + P(X=25)
		- P(X>=1) = 1 - P(X=0) = 1 - 0.8^25 = 0.996...
