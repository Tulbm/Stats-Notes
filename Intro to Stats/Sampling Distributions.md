Normal distribution results
Consider $X_{1},\dots,X_{n}\sim N(\mu,\sigma^2)$. Then if $\bar{X}=\sum X_{i}/n$ and $S^2=\sum(X_{i}-\bar{X})^2 / (n-1):$
1. $\bar{X}\sim N(\mu,\sigma^2/n)$
2. $\sum(X_{i}-\mu)^2 / \sigma^2 \sim \chi_{n}^2$
3. $\sum (X_{i}-\bar{X})^2/ \sigma^2 \sim \chi_{n-1}^2$
4. $(n-1)S^2 / \sigma^2\sim \chi_{n-1}^2$
5. $\frac{\bar{X}-\mu}{S / \sqrt{ n }}\sim t_{n-1}$














- fundamental to statistical inference
	- relating statistics from the sample to the population parameters
	- we use arguments based on sampling distribution of the statistic to state how close the estimate is likely to be to the parameter
		- sampling distribution of a statistic is the probability distribution of that statistic
			- = probability distributions if samples of the same size were to be repeatedly drawn from the population
				- but we dont really do it, math can figure it out
- sampling distributions of 
	- $\bar X$
		- ![](https://i.imgur.com/Ft3MuyN.png)
	- $S^2$  
		- ![](https://i.imgur.com/Vbqdldh.png)
- sample distribution of the sample mean($\bar x$)
	- assumed that population is $\infty$ or very large compared to sample size
		- otherwise math changes a little
	- $\bar x$
		- $X_1,X_2,...,X_n$ are n independently drawn observations from a population with mean $\mu$ and sd $\sigma$
		- $\bar X = \frac{X_1+X+2+...+X_n}{n}$
			- n = sample size, not amount of sample draws
			- $E(\bar X) = E(\frac{X_1+X_2+...+X_n}{n})=\mu$
				- $E(X_1) = E(X_2) = E(X_n) = \mu$
					- thats how expectation works
				- $\bar X$ is an unbiased estimate of $\mu$
				- the expectation of a sum is always the sum of the expectations
				- we sometimes write $E(\bar X) = \mu$ as $\mu_{\bar X} = \mu$
					- mean of the sampling distribution of the sample mean = mean of the population
						- $\bar X$ can take multiple values in different samples, but their mean will be equal to the population mean
					- mean of $\bar X$, the random variable, same as expectation
			- $Var(\bar X) = Var(\frac{X_1+X_2+...+X_n}{n}) = \frac{\sigma^2}{n}$
				- if the random variables are independent, the variance of their sum is the sum of their variances
				- often denoted as $\sigma_{\bar X}^2 = \frac{\sigma ^2}{n}$
					- $\sigma(\bar X) = \frac{\sigma}{\sqrt n}$ 
						- sd of the mean of multiple samples taken will have a smaller variance
			- $\bar X$ is normally distributed if we are sampling from a normally distributed population
			- $\bar X \sim N(\mu,\frac{\sigma^2}{n})$ 
				- for the mean of n observations
				- $Z=\frac{\bar X-\mu}{\sigma/\sqrt n}$
					- tends to $Z\sim N(0,1)$ as $n \rightarrow \infty$
						- tends to the standardized normal distribution
	- $\mu_{\bar x}$ = mean of $\bar x$ 
	- $\sigma_{\bar x}$ = standard deviation of $\bar x$

If $S_{1}^2$ and $S_{2}^2$ are the sample variances of two random samples of size $n_{1}$ and $n_{2}$ from two populations with the variances $\sigma_{1}^2$ and $\sigma_{2}^2$, then
$$
F=\frac{S_1^2/\sigma_1^2}{S_2^2/\sigma_2^2}\sim F_{n_1-1,n_2-1}
$$

