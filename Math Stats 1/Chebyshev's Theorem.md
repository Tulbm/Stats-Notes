or Tchebysheff's Theorem

Let $X$ be a random variable with finite mean $\mu$ and variance $\sigma^2\neq0$, then $\forall k>0$
$$
P(|X-\mu|<k\sigma)\geq1- \frac{1}{k^2}, \quad \text{or} \quad P(|X-\mu|\geq k\sigma)\leq \frac{1}{k^2}
$$
Probability that the sample points sit within $k$ standard deviations of the mean get squeezed to 1 as $k$ increases

At $k=2$, probability for any random variable under any distribution is at least 75% (for the normal, we have 95%)

Applies to a new random variable $Y=g(X)$, as long as $\mu_{y}$ and $\sigma^2_{y}$ exists

If the exact value is not needed when finding $P(X>c)$, we can use the theorem to quickly calculate a bound instead of doing a laborious integration 

Just plugging in $k = \frac{k}{\sigma}:$
$$
P(|X-\mu|\geq k) \leq \frac{\sigma^2}{k^2}
$$
# Law of large numbers
For [[Normal Distribution|normal random variable]] $X$ and [[Sample Proportion]] $Y=\frac{X}{n}=\hat{p}$
- $\mu_{Y}=p, \sigma_{y}=\sqrt{ p(1-p)/n },$ let $c=k\sigma\to k=c/\sigma$ 
$$\begin{align}
P(|Y-p|\leq c) = P(|Y-p|\leq k\sigma)  & \geq 1- \frac{1}{k^2}  \\
 & \geq 1- \frac{1}{(c/\sigma)^2} \\
 \text{as }n\to \infty \quad \quad \quad& \geq 1- \frac{p(1-p)}{c^2n} \\
 \text{squeezed at 1 by axioms} \quad& \geq 1- 0 \\
P(|Y-p|\leq c)  & = 1
\end{align}
$$
for any arbitrary positive integer $c$ 

With the equivalent symmetrical inequality and $Var(\bar{x})=\frac{\sigma^2}{n}:$
$$\begin{align}
P(|\bar{x}-\mu|\geq k)  & \leq \frac{Var(\bar{x})}{k^2}=\frac{\sigma^2}{nk^2} \\
P(|\bar{x}-\mu|\geq k)  & \leq 0 \quad \text{ as n}\to \infty
\end{align}
$$
- sample mean converges to population mean with large sample sizes





