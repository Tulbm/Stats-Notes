Based upon the view of probability as a 'degree of belief', we consider the parameter $\theta$ to be a random variable that follows a distribution. We make an assumption about the distribution that the $\theta$ follows before we see the data. This distribution is called the **prior distribution**. We denote the prior probability distribution function of $\theta$ by $g(\theta)$

We update the information about the population of the parameter from the prior distribution by that in the data via the likelihood function to obtain a distribution that models the parameter better, and this distribution is called the **posterior distribution**

Prior distribution of $\theta:$ $\theta\sim g(\theta)$, unconditional distribution of $\theta$, marginal distribution of $\theta$

The likelihood of $\theta$ given the data:
$$\begin{align}
 & x_{1},\dots,x_{n} \sim f(x;\theta) \\
L(\theta) & = \prod f(x_{i};\theta ) = f(x_{1},\dots,x_{n};\theta)
\end{align}
$$
Posterior distribution of $\theta:$ $h(\theta|\tilde{x})$, conditional distribution of $\theta$ given data
$$
\begin{align}
h(\theta|\tilde{x}) & = \frac{f(x_{1},\dots ,x_{n},\theta)}{f(x_{1},\dots,x_{n)}} , \theta\text{ as a random variable, not given } \\
 & = \frac{\text{joint distribution of data and }\theta}{\text{marginal distribution of data, independent of }\theta}
\end{align}
$$
Marginal distribution is called normalization constant

$$
\begin{align}
\int h(\theta|x)d\theta & =\int \frac{f(x,\theta)}{f(x)}d\theta = \frac{1}{f(x)} \int f(x,\theta)d\theta= \frac{f(x)}{f(x)}=1
\end{align}
$$
Given the posterior distribution of $\theta$, the posterior mean or the posterior median is a typical **Bayesian estimate** of $\theta$. The posterior mean of $\theta$ is
$$
\hat{\theta}_{B}=E(\theta|x_{1},\dots,x_{n}) = \int \theta h(\theta|x)d\theta
$$
A prior distribution that leads to the posterior distribution belonging to the same distribution family is called a conjugate prior, the distribution family that both prior and posterior distributions belong to is called the conjugate family

The conjugate family has a nice property in that the posterior follows know form of distribution (?)

Note: if the prior is informative, it will have more impact on the estimator than the data

If it is hard to know the parameters of the prior distribution, we can use it flat/vague

# Examples
$X\sim Uni(0,\theta)$, we assume that $\theta\sim Gamma(2,1)$ 
$$
\begin{align}
\text{(prior dist'n) } g(\theta) & = \frac{1}{\Gamma(2)1^2}\theta^{2-1}e^{-\theta/1}= \theta e^{-\theta}, \theta>0 \\
\text{(likelihood) }  L(\theta) & = \frac{1}{\theta}, \quad 0<x<\theta \\
\text{(posterior dist'n) } h(\theta|X) & = \frac{f(x,\theta)}{f(x)}=\frac{f(x;\theta)g(\theta)}{f(x)}= \frac{L(\theta)g(\theta)}{f(x)} \\
L(\theta )g(\theta) & = \frac{1}{\theta}\theta e^{-\theta}= e^{-\theta} \\
f(x) & =\int_{x}^\infty e^{-\theta}d\theta = e^{-x}, \quad 0<x<\theta \\
 h(\theta|x)  & =\frac{L(\theta)g(\theta)}{f(x)}  \\
 & =\frac{e^{-\theta}}{e^{-x}} = e^{x-\theta} \\
\hat{\theta}_{B} & =E(\theta|x)= \int_{x}^\infty \theta h(\theta|x)d\theta \\
 & =\int_{x}^\infty \theta e^{x-\theta}d \theta \\
 & =e^x \int_{x}^\infty \theta e^{-\theta}d\theta \\
 & =e^x \left. \left[ \theta \cdot (-e^{-\theta})\right|_{x}^\infty - \int_{x}^\infty -e^{-\theta}d\theta \right] \\
 & =e^x [xe^{-x}- e^{-\theta}|_{x}^\infty]  \\
\hat{\theta}_{B} & =x+1
\end{align}
$$

Suppose $X\sim Binomial(n,p)$, we assume that $p\sim beta(\alpha,\beta)$, the posterior distribution of p:
$$
\begin{align}
g(p) & =\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}p^{\alpha-1}(1-p)^{\beta-1} \\
 L(p) & =f(x;p) = {n\choose x} p^x (1-p)^{n-x} \\
f(x,p) & =L(p)g(p)= {n\choose x} p^x (1-p) ^{n-x} \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}p^{\alpha-1}(1-p)^{\beta-1} \\
 & ={n\choose x} \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} p^{x+\alpha-1}(1-p)^{n-x+\beta-1} \\
f(x) & = \int_{0}^1 f(x,p)dp \\
 & ={n\choose x} \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}   \frac{\Gamma(x+\alpha)\Gamma(n-x+\beta)}{\Gamma(x+\alpha+n-x+\beta)}\int_{0}^1 \frac{\Gamma(x+\alpha+n-x+\beta)}{\Gamma(x+\alpha)\Gamma(n-x+\beta)} p^{x+\alpha-1}(1-p)^{n-x+\beta-1} \\
 & ={n\choose x} \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}   \frac{\Gamma(x+\alpha)\Gamma(n-x+\beta)}{\Gamma(x+\alpha+n-x+\beta)} \cdot 1 \quad \text{ Beta distribution} \\
 h(\theta|x)& = \frac{f(x,\theta)}{f(x)} = \frac{\Gamma(x+\alpha+n-x+\beta)}{\Gamma(x+\alpha)\Gamma(n-x+\beta)}p^{x-\alpha+1}(1-p)^{n-x+\beta} \\
 & =\frac{\Gamma(\alpha+\beta+n)}{\Gamma(x+\alpha)\Gamma(n-x+\beta)} p^{x-\alpha+1} (1-p)^{n-x+\beta} \text{ (posterior belongs to the same family)} \\
\hat{p}_{B} & =E(p|x)= \int_{0}^1 p h(p|x)dp = \frac{x+\alpha}{x+\alpha+n-x+\beta}  \\
 & =\frac{x+\alpha}{n+\alpha+\beta} \\
 & =\frac{x}{n+\alpha+\beta} + \frac{\alpha}{n+\alpha+\beta}  = \frac{x}{n} \cdot \frac{n}{n+\alpha+\beta}+ \frac{\alpha}{\alpha+\beta}\cdot \frac{\alpha+\beta}{n+\alpha+\beta} \\
 & = \frac{x}{n}(\hat{p}) \cdot w + \frac{\alpha}{\alpha+\beta}(E(p))\cdot (1-w) \\
 & = \text{page 75} 
\end{align}
$$





