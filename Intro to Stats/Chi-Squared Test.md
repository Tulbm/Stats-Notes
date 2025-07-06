# Method
- requirements to be reasonable
	1. a simple random sample from the population / randomized experiment
	2. a sample size large enough for the $\chi^2$ [[Chi-Squared Distribution|approximation]] to be reasonable
- $H_{0}:p_{1}=p_{1_{0}},p_{2}=p_{2_{0}},\dots,p_{c}=p_{c_{0}}$
	- [[Hypothesis Types|null hypothesis]] that the true proportions for the c levels of a categorical variable are equal to hypothesized values
# for one-way tables
- observations are classified according to only one categorical variable
	- each count belongs to only one cell
### Test Statistic
- $\chi^2=\sum_{\text{all cells}} \frac{\text{Observed-Expected}^2}{\text{Expected}}$
	- observed and expected represent counts with the specific category
	- the test statistic $\chi^2$ will have (approx) a $\chi^2$ [[Chi-Squared Distribution|distribution]] if the null hypothesis is true
		- test using the right-tailed [[P-values|p-value]] in the distribution with the value we got 
		- large values of $\chi^2$ give evidence against the null
	- degrees of freedom are number of cells$(c) -1$
	- each cell is one part of the proportion
		- $\hat{p}=\frac{50}{50}\to$ 2 cells, 100% divided into n groups $\to$ n cells
# for two-way tables
- observations are classified according to two categorical variables
- we wish to test the null hypothesis that there is no association between row and column variables
- [[Hypothesis Types|hypothesis could be]]
	- single sample
		- $H_{0}$: row and column variables are independent
	- multiple samples
		- $H_{0}$: the distribution of the response variable is the same for all of the populations
## Test Statistic
- $\chi^2=\sum_{\text{all cells}} \frac{\text{Observed-Expected}^2}{\text{Expected}}$
- expected count = $\frac{\text{row total x column total}}{\text{overall total}}$
- degrees of freedom: $\text{(number of rows - 1) x (number of columns - 1)}$