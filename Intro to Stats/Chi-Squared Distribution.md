- if the random variable $Z$ has a standard normal distribution, $Z^2$ has a $\chi^2$ distribution with one degree of freedom
	- if $Z_{1},Z_{2},\dots,Z_{\nu}$ are independent normal random variables then $Z_{1}^2, Z_{2}^2,\dots,Z_{\nu}^2$ has a $\chi^2$ distribution with $\nu$ degrees of freedom
		- $\mu=\nu,\ \sigma^2=2\nu$
		- mode occurs at $\chi = df-2$ for distributions with at least 2 dfs 
			- mode = highest occurence 
		- ![](https://i.imgur.com/67KdHWi.png)
	- ![](https://i.imgur.com/cXD4hvM.png)
- the test statistic in a $\chi2$ test will have an approximate $\chi2$ distribution
- as the degrees of freedom $\to \infty$ the $\chi^2$ approximates a [[Normal Distribution|normal distribution]] with mean $=  \nu$
# PDF
A random variable $X$ has a chi-square distribution with $v$ degrees of freedom, $X\sim \chi_{v}^2$ if and only if it has the pdf
$$
f(x)=\frac{1}{2^{v/2}\Gamma(v/2)}x^{v/2-1}e^{-x/2}\quad\mathrm{~for~}x\geq0
$$

$$
\chi_{v}^2\equiv Gamma\left( \frac{v}{2},2 \right)
$$
Mean
$$
E(X)=\left( \frac{v}{2} \right)(2)=v
$$
Variance
$$
Var(X)=\left( \frac{v}{2} \right)(2^2)=2v
$$

If a random variable X has a standard normal distribution (with mean  
0 and unit variance), then a random variable Y = X2 has a χ2 distri-  
bution with 1 df (denoted by χ2  
1). If Y is the sum of k independent  
standard normal squares, Y has a χ2 distribution with k df ( χ2  
k).  
In other words, if Y is the sum of k independent χ2  
1’s, Y has a χ2  
distribution with k df ( χ2  
k).

If $x_{1},x_{2},\dots,x_{k}$ are independent random variables, $X_{i}\sim N(0,1)$
$$
Y=X^2_{1}+X_{2}^2+\dots+X_{k}^2\sim \chi_{k}^2
$$
$v=k=$ number o square of normal sum
















































