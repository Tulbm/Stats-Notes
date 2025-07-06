- explores a possible linear relationship between two quantitative variables 
# Model
In R: `lm(Response ~ Explanatory)`

We assume $Y=\beta_{0}+\beta_{1}X+\epsilon$ using unknown statistics

Where:
- Y = response variable
- $\beta_{0}=$ true intercept
- $\beta_{1}=$ true slope
- X = explanatory variable
- $\epsilon=$ random error term (measure of the variability in the relationship)

- $E(Y|X)=\beta_{0}+\beta_{1}X$
	- expectation of Y at a value of X
	- theoretical mean of Y at X


The model performs 3 tests to estimate the parameters:
1. Intercept
- tests $H_{0}:\beta_{ 0}=0$ vs $H_{1}:\beta_{0}\neq 0$ with a t-test
2. Slope
- tests $H_{0}:\beta_{1}=0$ vs $H_{1}:\beta_{1}\neq0$ with a t-test (does it have a slope)
- measures how strong the **linear** relationship between the two variables is
3. ANOVA F-test 
- also tests $H_{0}:\beta_{1}=0$ vs $H_{1}:\beta_{1}\neq 0$ 
- same hypothesis as the second test, p-value is the same, $t^2=F$
# Estimating $\beta_{0}$ and $\beta_{1}$
$\hat{Y}=\hat{\beta}_{0}+\hat{\beta_{1}}X$ (parameters/estimations)
- least squares
	- $\sum e_i^2=\sum(Y_i-\hat{Y_i})^2$
		- goal is to find the estimators that minimize $\sum e_{i}^2$ (residual)
	- $e_{i}=Y_{i}-\hat{Y}_{i}$
		- e = residual
	- $\hat{\beta_{0}}=\bar{Y}-\hat{\beta_{1}}\bar{X}$
	- $\hat{\beta}_1=\frac{\sum(X_i-\bar{X})(Y_i-\bar{Y})}{\sum(X_i-\bar{X})^2}$ 

Confidence intervals for the two parameters
# Inference
we assume that $\epsilon \sim N(0,\sigma^2)$ and that the $\epsilon$ terms are independent
## Testing $H_{0}:\beta_{1}=0$
i.e. there is not relationship between X and Y
- true slope = 0, Y not related to X then
If we assume $\epsilon \sim N(0,\sigma^2)$ and $H_{0}:\beta_{1}=0$
- $\frac{\hat{\beta}_1-0}{SE(\hat{\beta}_1)}\sim t(n-2)$ (t statistic)
	- $SE(\hat{\beta_{1}})=\frac{S}{\sqrt{ \sum(x_{i}-\bar{x})^2 }}$
	- $S^2=\frac{\sum(y_{i}-\hat{y}_{i})^2}{n-2}$
		- n-2 because two parameters are being estimated($\beta_{0}$ and $\beta_{1}$)
# Measuring the correlation
- measure of the strength of the linear relationship 
- SLR is not made to measure correlation between non-linear relationships
	- ![](https://i.imgur.com/5IrWEtw.png)
	- last two use different techniques
	- (always plot your data beforehand)
r = [[Pearson Correlation Coefficient]]
$R^2$ =  [[Coefficient of Determination]]


$$
\begin{pmatrix}
1  & 2  & 3 \\
1  & 2  & 3  \\
4 & 5 & 6
\end{pmatrix}
$$
