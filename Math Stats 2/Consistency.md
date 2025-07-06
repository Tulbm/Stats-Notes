$\hat{\theta}$ is a **consistent** estimator of the parameter $\theta$ if and only if  $\exists\epsilon>0$
$$
\lim_{ n \to \infty } P(|\hat{\theta}-\theta|<\epsilon)=1
$$
- the estimate $\hat{\theta}$ converges to the true value of $\theta$ as $n\to \infty$

The sample mean $\bar{X}$ is a consistent estimate of the population mean, as $Var(\bar{X})=\frac{\sigma^2}{n}$. Applying [[Chebyshev's Theorem]]:
$$
P(|\bar{X}-\mu|<\epsilon)\geq 1 - \frac{\sigma^2}{n \epsilon^2}\longrightarrow 1 \text{ as } n \to \infty
$$

If $\hat{\theta}$ is an [[Unbiasedness|unbiased]] estimator of the parameter $\theta$ and the $Var(\hat{\theta})\to0$ as $n\to \infty$, then $\hat{\theta}$ is a consistent estimator of $\theta$
- like how $\frac{\sigma^2}{n}\to0$ as $n\to \infty$


Consistent tests will have their [[Error types|power]] converge to 1 as $n\to \infty$

# Examples 

The sample variance $S^2=\frac{1}{n-1} \sum_{i=1}^n (X_{i}-\bar{X})^2$ is a consistent estimator of the population variance $\sigma^2$
$$\begin{align}
\frac{(n-1)S^2}{\sigma^2} & \sim \huge\chi_{n-1}^2 \\
E\left(  \frac{(n-1)S^2}{\sigma^2} \right) & =n-1 \\
E(S^2) & =\sigma^2 \\
Var\left( \frac{(n-1)S^2}{\sigma^2} \right)& = 2(n-1)  \\
 Var(S ^2) & =\frac{2\sigma^4}{n-1}\to 0 \text{ as } n\to \infty
\end{align}
$$
Looking at the [[Order Statistics#Distribution of minimum and maximum|minimum]] statistic $X_{(1)}$ for a double exponential distribution
$$
f(x,\delta)= e^{-(x-\lambda)},\quad x\geq \delta
$$
$$
\begin{align}
F_{X}(x) & =\int_{-\infty}^\infty f(x,\delta )=\int_{\delta}^xe^{-(t-\delta)}
dt \\
 & = 1-\int_{x}^\infty e^{-(t-\delta)} \\ 
 & = 1- e^{-x-\delta}, \quad x>\delta \\
 1-F_{X}(x)  & = e^{-x-\delta}  \\
 f_{X_{(1)}} & =n[e^{-(x-\delta )}]^{n-1} e^{-(x-\delta)} \\
 & =ne^{-n(x-\delta)}\\
E(X_{(1)}) 
 & =\int_{\delta }^\infty x \, ne^{-n(x-\delta)} dx \\
 & =\int_{0}^\infty (y+\delta)ne^{-ny} \\
 & =\int_{0}^\infty y ne^{-ny}dy + \delta \int_{0}^\infty ne^{-ny}\\
 & =E(Y)+\delta \\
 & =\frac{1}{n}+ \delta \neq \delta
\end{align}
$$
$E(X_{(1)})= \frac{1}{n} + \delta$ is asymptotically unbiased
To prove that it is a consistent estimator for $\delta$
$$
\begin{align}
\lim_{ n \to \infty } P(|X_{(1)}-\delta | <\epsilon) & =P(-\epsilon\leq X_{(1)}-\delta\leq \epsilon ) \\
 & = P( \delta - \epsilon \leq X_{(1)} \leq \delta + \epsilon ) \\
 & =P(\delta \leq X_{(1)}\leq \delta + \epsilon)  \\
 & = \int_{\delta }^{ \delta+\epsilon}ne^{-n(x-\delta)}dx \\
 & =1-e^{-n \epsilon }\longrightarrow 1 \text{ as } n\to \infty
\end{align}
$$

