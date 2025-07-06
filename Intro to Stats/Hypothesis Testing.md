Testing a [[Hypothesis Types|statistical hypothesis]]. If the conjecture is false then the complementary hypothesis must be true

[[Critical Region]] and $\alpha$ depend on each other, we can find one out from the other
- critical region $C$ is implemented on the observed values of a statistic, and the decision rule depends on the distribution of that statistic and $\alpha$
- [[Error types]]

To test a simple null hypothesis $H_{0}: \theta = \theta_{0}$ against a simple alternative hypothesis $H_a: \theta = \theta_{1}$ we use the [[Neyman-Pearson lemma]]

For a more general framework $H_{0}: \theta \in \vartheta_{0}$ vs $H_{a}: \theta \in \vartheta_{1}$, where $\vartheta= \vartheta_{0} \cup \vartheta_{1}$, the parameter space we use the [[Power function of a test]] and the [[Likelihood ratio test]]

If a test satisfies $P(\text{reject }H_{0}|H_{0} \text{ is true})\leq \alpha$, then the test is called an $\alpha$ **level significance test** 
# General procedure

1. Formulate $H_{0}$ and $H_{a}$ and specify the size of test $\alpha$
2. Find an appropriate test statistic - generally a [[Pivot Statistic]] with a distribution not dependent on the parameters under the $H_{0}$
3. Determine the critical region based on the size of test $\alpha$
4. Compute the value of the observed test statistic based on the sample data
5. Reject $H_{0}$ if the observed value falls in the critical region, otherwise do not reject $H_{0}$

More specifically:
[[Test of Means]]
[[Test of difference between means]]
[[Test of Variances]]
[[Test of Proportions]]
[[Test of k proportions]]
[[Goodness of fit test]]




# intro stats
- translating a question into a hypothesis about the value of a parameter(s)
	- we then carry out a statistical test of that hypothesis
- [[Hypothesis Types]]
- logic of hypothesis testing
	- consists of
		- Formulating a null hypothesis ($H_0$) and an alternative hypothesis ($H_a$). These hypotheses are based on the research question of interest, and not on the observed sample data.   
		- Choosing and calculating an appropriate test statistic.  
			- based on sample data
			- will yield a p-value
		- Stating an assessment of the strength of the evidence against the null hypothesis.  
		- Properly interpreting the results in the context of the problem at hand.
	- example
		- tom says he can get heads more often
			- $H_0:p=0.5$ (Tom's probability of getting heads is 0.5)
				- if null hypothesis is true then we have a binomial distribution with parameters $n=100\ \text{and}\ p=0.5$ 
					- ![](https://i.imgur.com/NV70OMo.png)
				- what's $P(X\geq68)$ (evidence against the null hypothesis)
					- $X \sim \text{Bin}(100,.5)$
					- $=1-\text{pbinom}(67,100,.5)$
					- $\approx 0.0002$ (p-value)
					- there's strong evidence that Tom's probability of tossing heads is greater than 0.5
			- $H_a:p>0.5$ 
- hypothesis tests for a population mean $\mu$
	- assuming we have a simple random sample from a normally distributed population
	- constructing appropriate hypotheses
		- is there strong evidence that $\mu$ differs from a hypothesized value?
			- $H_0:\mu=\mu_0$
			- $H_a$'s:
				- one-sided alternatives
					- if we only care about one side
					- $H_a:\mu > \mu_0$
					- $H_a:\mu<\mu_0$
				- two sided alternative
					- proves more
					- $H_a:\mu \neq \mu_0$
	- [[Test Statistics]]
		- recap
			- $Z=\frac{\bar X-\mu}{\sigma/\sqrt n}$ has the standard normal distribution
			- $t=\frac{\bar X-\mu}{s/\sqrt n}$ has the t distribution with $n-1$ degrees of freedom
		- depends if we know $\sigma$ or not (like in CI)
		- if the null hypothesis is true
			- Z test statistic has the standard normal distribution
			- t test statistic has a t distribution with n-1 degrees of freedom
		- the observed value of the test(t) statistic tells us how many standard errors of the value of $\bar X$ is from the hypothesized value of $\mu$
			- $\text{Test Statistic} = \frac{\text{Estimator}-\text{Hypothesized Value}}{SE\text{(Estimator)}}$
			- $t = \frac{\bar X - \mu_0}{SE(\bar X)}$
				- SE = standard error (estimates standard deviation)
			- $t = \frac{\bar X - \mu_0}{s/\sqrt n}$  
- rejection region approach
	- one method of determining whether the evidence against the null hypothesis is statistically significant
	- steps
		- decide on an appropriate value of $\alpha$, the significance level of the test
			- often chosen to be a small value (like 0.05)
			- probability of rejecting the null hypothesis, given it's true 
		- find the appropriate rejection region
		- calculate the value of the appropriate test statistic
		- reject the null hypothesis if the test statistic falls in the rejection region
			- / say that the evidence against $H_0$ (and in favour of $H_a$ ) is statistically significant at the $\alpha$ level of significance
				- we're not actually making a decision between the hypothesis, we're just assessing the evidence
					- rejecting a hypothesis is very strong
	- examples
		- we wish to test the null hypothesis $H_0:\mu=\mu_0$ against $H_a:\mu\neq\mu_0$
			- suppose $\alpha = 0.05$ and we're doing a z test
				- same logic as confidence interval
				- reject $H_0\ \text{if}\ z\leq -1.96$ or $z\geq 1.96$ 
					- or say that we have statistically significant evidence against $H_0$ at $\alpha = 0.05$
					- ![](https://i.imgur.com/OYz0ZEb.png)
		- $H_a:\mu<\mu_0$
			- reject $H_0$ if $z\leq-1.645$
				- ![](https://i.imgur.com/RNyXFqI.png)
			- suppose it's a t with 10 degrees of freedom
				- then we reject if $t\leq-1.812$
		- $H_a:\mu>\mu_0$
			- reject $H_0$ if $z\geq 1.645$ 
				- ![](https://i.imgur.com/gN5kS80.png)
			- imagine 3 z statistic values
				- 1.64
					- do not reject $H_0$ at $\alpha = 0.05$ 
				- 1.65
					- reject $H_0$ at $\alpha = 0.05$
				- 37.6
					- eject $H_0$ at $\alpha = 0.05$
- [[P-values]]
