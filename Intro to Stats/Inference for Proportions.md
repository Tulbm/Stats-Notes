# for a single [[Sample Proportion|proportion]] $p$
If we wish to test [[Hypothesis Types|a]] $H_{0}:p=p_{0}$ with a [[Test Statistics|z test]] or a [[Chi-Squared Test|chi test]]
- $\chi$ is more general than the z test
	- z compares one proportion to our hypothesized one
	- $\chi$ takes all proportions of our sample and compares it to what we would get if they all had the expected proportion we want ($H_{0}$)
Or find a confidence interval for the [[Sample Proportion]] $p$
## [[Confidence Intervals]]
- $\hat{p}\pm z_{\alpha/2}SE(\hat{p})$ are the endpoints of a $(1-\alpha)100\%$ confidence interval
- to test $H_{0}:p=p_{0}$
	- $Z=\frac{\hat{p}-p_{0}}{SE_{0}(\hat{p})}$ 
	- $SE_{0}(\hat{p})=\sqrt{ \frac{p_{0}(1-p_{0})}{n} }$ 
		- SE is an estimate of the standard deviation
# for two [[Sample Proportion|proportions]] $p$
If we wish to 
- test [[Hypothesis Types|null hypothesis]]  $H_{0}:p_{1}=p_{2}$ with a [[Test Statistics#For proportions|z test]] or a [[Chi-Squared Test|chi test]]
- find a confidence interval for $p_{1}-p_{2}$
- find relative risk $\frac{p_{1}}{p_{2}}$
- find odds ratio$\frac{p_{1}/(1-p_{1})}{p_{2}/(1-p_{2})}$
## [[Confidence Intervals]]
- $\hat{p_{1}}-\hat{p_{2}}\pm z_{\alpha/2}SE(\hat{p_{1}}-\hat{p_{2}})$ are the endpoints of a $(1-\alpha)100\%$ confidence interval
- to test $H_{0}:p=p_{0}$
	- $Z=\frac{\hat{p}-p_{0}}{SE_{0}(\hat{p})}$ 
	- $SE_{0}(\hat{p})=\sqrt{ \frac{p_{0}(1-p_{0})}{n} }$ 
- 95% confidence interval that the true proportion is contained in $\hat{p_{1}}-\hat{p_{2}}\pm z_{\alpha/2}SE(\hat{p_{1}}-\hat{p_{2}})$