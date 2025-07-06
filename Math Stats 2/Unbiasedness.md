We say $\hat{\theta}$ is an unbiased [[Point Estimation|estimator]] of $\theta$ iff 
$$
E[\hat{\theta}(X_{1},..,X_{n})]=\theta
$$
If an estimator $\hat{\theta}$ is biased for $\theta$, the amount of bias is given by
$$
bias(\hat{\theta})=E(\hat{\theta}-\theta)=E(\hat{\theta})-\theta
$$
An estimator $\hat{\theta}(X_{1},\dots,X_{n})$ is [[Analysis|asymptotically]] unbiased for $\theta$ if
$$
\lim_{ n \to \infty } bias(\hat{\theta}(X_{1},\dots,X_{n}))=0
$$
$E(\hat{\theta})\to \theta$ as $n\to \infty$
# Examples
Using [[Order Statistics#Distribution of minimum and maximum|maximum]] statistic as an estimator of $\theta$, $X\sim uniform$
$$
\begin{align}
E(X_{(n)}) & =\int xf_{X_{(n)}}(x) dx \\
 & =\int_{0}^\theta x \frac{nx^{n-1}}{\theta^n}d x \\
 & =\frac{n}{\theta^n}\left[ \frac{1}{n+1} x^{n+1} \right|_{0}^\theta \\
 & =\frac{n}{n+1}\theta\quad \text{ biased underestimator}
\end{align}
$$
An unbiased estimator would be $\hat{\theta}=\frac{n+1}{n}X_{(n)}$
$X_{(n)}$ is still asymptotically unbiased as $n\to \infty$

Estimating the variance of a sampling distribution:
$$
S_{1}^2=\frac{1}{n}\sum_{i=1}^n (X_{i}-\mu)^2 =\sigma^2\text{ is unbiased}
$$
Using only the sample mean:
$$\begin{align}
S_{2}^2  & = \frac{1}{n}\sum_{i=1}^n (X_{i}-\bar{X})^2 \\
E(S_{2}^2) &= E\left( \frac{1}{n}\sum (x_{i}-\bar{x}) \right)^2 \\
 & =\frac{1}{n}E\left( \sum_{i=1}^n(x_{i}-\mu + \mu -\bar{x})^2\right) \\
 &= \frac{1}{n} E\left( \sum _{i=1}^n(x_{i}-\mu)^2+2(x_{i}-\mu)(\mu-\bar{x})+(\mu-\bar{x})^2 \right) \\
 & =\frac{1}{n}E\left( \sum (x_{i}-\mu)^2 \right)+ \frac{1}{n}E\left( \sum 2(x_{i}-\mu)(\mu-\bar{x}) \right) + \frac{1}{n} E\left( \sum (\mu-\bar{x})^2 \right) \\
 & =\frac{1}{n} n\sigma^2 + \frac{2}{n}E\left( (\mu-\bar{x})\sum (x_{i}-\mu)  \right) + \frac{1}{n} n E((\mu-\bar{x})^2) \\
 & =\sigma^2 + 2E((\mu-\bar{x})(x_{i}-\mu))+ \frac{\sigma^2}{n} \\
 & =\sigma^2 - 2 E((\bar{x}-\mu)^2) + \frac{\sigma^2}{n} \\
 & =\sigma^2 - 2 \frac{\sigma^2}{n} + \frac{\sigma^2}{n} \\
 & =\frac{n-1}{n}\sigma^2 \quad \text{(a biased estimator for } \sigma ^2 )\\
\end{align}
$$
That's why we estimate the variance with
$$
\frac{1}{n-1} \sum_{i=1}^n(X_{i}-\bar{X})^2
$$
An unbiased estimate for $\sigma^2$ 



[[Mean square error]]