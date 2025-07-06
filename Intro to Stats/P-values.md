The p-value is the smallest significance level at which a test would have led to a critical region, given the observed statistic, $\alpha_{0}$
$$
\text{p-value} = P(\text{test statistic is more extreme than the observed |}H_{0} \text{ is true})
$$
- testing the level of "extremicity", not just the values itself
- $x=[0,20]$, $\mu= 10$ $\to$ p-value = $2\cdot P(X \leq 4 | H_{0})$ (extremities in all directions)

- a measure of the strength of the evidence against the null hypothesis
	- probability of getting a test statistic at least as extreme as the one observed
		- assuming the null hypothesis is true
	- probablity of getting the observed value of the test statistic, or a value with at least as much evidence against the null hypothesis
	- assuming the null hypothesis is *true* 
		- chances of seeing what we saw if null is true
	- the smaller the p-value, the greater the evidence against the null
		- if null is true, then the % of the p-value is the chance we have to find what we did 
			- p-value very small = we'd have to be extremely (un)lucky to get the test we're using as evidence
	- if we are carrying out a test at the $\alpha$ level of significance, we can reject $H_0$ if p-value $\leq \alpha$ 
		- hypothesis dont have confidence levels
# interpreting p-values
-  the smaller the p-value, the stronger the evidence against $H_0$  
	- if we are carrying out the test at a fixed level of $\alpha$, the evidence against $H_0$ is statistically significant if p-value $\leq \alpha$ 
	- if we get a big p-value, we still cannot state that the $H_0$ is true
	- distribution of the p-value
		- z/t test with assumptions being true
		- if $H_0$ is true
			- ![](https://i.imgur.com/q9QDju4.png)
		- if $H_0$ is false
			- chance that we get a p-value of 1 (would be exactly on the mean) = that little bar
			- ![](https://i.imgur.com/zF6TZO0.png)
		- rough guideline
			- ![](https://i.imgur.com/Ju1ssVr.png)
# finding p-values
- example
	- suppose in a Z/t test the observed value of the test statistic is found to be 2.00
		- $H_0:\mu=\mu_0$, $H_a:\mu>\mu_0$ 
			- p-value = 1-pnorm(2) = 0.0228
		- $H_a:\mu < \mu_0$
			- pvalue = pnorm(2) = 0.977
		- $H_a:\mu\neq\mu_0$ 
			- p-value = 2* (1-pnorm(2)) = 0.0456

