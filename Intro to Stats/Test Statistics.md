# Z test
- uses $\sigma$, if we don't know that [[Population and Samples|parameter]] then we need to use the T test
- $Z=\frac{\bar X-\mu}{\sigma/\sqrt n}$ has the standard normal distribution
	- converts our $\bar X$ to $N\sim (0,1)$
## For proportions
$Z=\frac{\hat{p}_{H}-\hat{p}_{N}}{SE_{0}(\hat{p}_{H}-\hat{p}_{N})} =\frac{\hat{p}-p_{0}}{\sqrt{ \frac{p_{0}(1-p_{0})}{n} }}$
# T test
- used when we dont know $\sigma$
- test statistic $t=\frac{\bar X-\mu}{s/\sqrt n}$ has the [[Normal Distribution#T distribution|t distribution]] with $n-1$ degrees of freedom
- the observed value of the test(t) statistic tells us how many standard errors of the value of $\bar X$ is from the hypothesized value of $\mu$
	- $\text{Test Statistic} = \frac{\text{Estimator}-\text{Hypothesized Value}}{SE\text{(Estimator)}}$
	- $t = \frac{\bar X - \mu_0}{SE(\bar X)}$
		- SE = standard error
	- $t = \frac{\bar X - \mu_0}{s/\sqrt n}$  
- when comparing the difference in two means
	- $t=\frac{\bar{X}_1-\bar{X}_2}{SE(\bar{X}_1-\bar{X}_2)}$ 
		- $\mu$'s cancel each other
# [[Chi-Squared Test]]
# F test
[[F distribution]]