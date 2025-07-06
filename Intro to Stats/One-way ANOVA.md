- one-way **Analysis of Variance** (ANOVA) extends the methods of the pooled-variance two-sample t tests to more than two groups
	- if we wish to prove that $H_{0}:\mu_{1}=\mu_{2}=\mu_{3}=\mu_{k}$
- assumptions
	- the same as those of the pooled-variance two-sample t
	1. The samples are simple random samples from the populations.  
	2. The populations are normally distributed.  
	3. The samples are independent.  
	4. The population variances are equal.
- based on the partitioning of the total sum of squares
	- split the total sum of squares into SS treatment and SS error
		- sum of squares
			- total variability in the response variable
			- the numerator of the sample variance formula if we were to pool all observations together
		- SS treatment
			- between groups
		- SS error
			- error within/inside each group
- calculations
	- variables
		- $k$ represents the number of groups.
		- $X_{ij}$ represents the $j$th observation in the $i$th group.
		- $\bar{X}_i$ represents the mean of the $i$th group.
		- $\bar{X}$ represents the overall mean (or grand mean). $\bar{X}=\frac{\text{Total of all observations}}{\text{Total number of observations}}$
		- $s_i$ represents the standard deviation of the $i$th group.- $n_i$ represent the number of observations in the $i$th group.
		- $n=n_1+n_2+\ldots+n_k$ represents the total number of observations.
		- ![](https://i.imgur.com/XhZPEiP.png)
			- mean square = $\frac{\text{sum of squares}}{df}$
			-  $F = \frac{MST}{MSE}$
				- ratio of $\frac{df}{df}$ 
		- $SS(\mathrm{Total})=\sum_{\mathrm{All~obs}}(X_{ij}-\bar{X})^2$
		- $SST=\sum_{\mathrm{Groups}}n_i(\bar{X_i}-\bar{X})^2$
		- $SSE=\sum_{\mathrm{Groups}}(n_i-1)s_i^2$
			- $MSE = \frac{(n_{1}-1)s_{1}^2+(n_{2}-1)s_{2}^2+\dots+(n_{k}-1)s_{k}^2}{n_{1}+n_{2}+\dots+n_{k}-k}$
	- $SS(Total)=SST+SSE$ ("between" + "within")
		- Total $df$ = Treatment $df$ + Error $df$
		- $n-1=k-1+n-k$
	- if $H_{0}$ is true 
		- $F$ has an [[F distribution]] with $(k-1,n-k)$
			- $F \sim F(k-1,n-k)$
		- $MST$ and $MSE$ are an unbiased estimator of $\sigma ^2$ 
			- $F\to 1$
	- if $H_{0}$ is false
		- $MST$ will tend to be greater than $MSE$ and the $F$ statistic will tend to be greater than it would be under $H_{0}$
			- variation between the groups > variation inside the groups
	- large values of the $F$ test statistic give evidence against $H_{0}$
		- observed value of the $F$ test in the $F$ distribution gives us the area we use to calculate [[P-values]]
			- then there is very strong evidence that the true means of the scores 
- if we find significant evidence against the $H_{0}$
	- we may investigate further, possibly comparing pairs of means
		- ${k\choose_{2}}=$ number of pairs we can make to compare them
	- different approaches
		- pooled-variance t (simplest one)
			- compare each pair of means withe either a confidence interval or hypothesis test
			- with multiple comparisons using confidence intervals, we start to get inaccuracy on the parameter
		- complicated ones


