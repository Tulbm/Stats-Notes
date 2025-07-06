Suppose $\hat{\theta}_{1}$ and $\hat{\theta}_{2}$ are two [[Unbiasedness|unbiased]] [[Point Estimation|estimator]] of a given populations' parameter $\theta$ 

We say that $\hat{\theta}_{1}$ is relatively more efficient than $\hat{\theta}_{2}$ if
$$
var(\hat{\theta}_{1})\leq var(\hat{\theta}_{2})
$$
The **relative efficiency** is used to measure the efficiency of $\hat{\theta}_{2}$ relative to $\hat{\theta}_{1}$
$$
RE=\frac{var(\hat{\theta}_{1})}{var(\hat{\theta}_{2})}
$$

Suppose $X_{1},\dots,X_{n}\overset{iid}{\sim}Poisson(\lambda)$, $\hat{\lambda}_{1}=\bar{X}$, $\hat{\lambda}_{2}=S^2=\frac{1}{n-1}Var(\bar{X})$
Both are unbiased:
$$
E(\bar{X})=\lambda, \quad E(S^2)=var(X)=\lambda
$$
And the variances:
$$\begin{align} 
Var(\bar{X}) & =\frac{\lambda}{n}  & Var(S^2) & =Var\left( \frac{1}{n-1}\sum( x_{i}-\bar{x})^2 \right) \\
 &    &   & =\frac{n}{(n-1)^2}Var((x_{i}-\bar{x})^2) \\
 \text{(no closed form)}&  &  & =\frac{n}{(n-1)^2}E[[(x_{i}-\bar{x})-E(x_{i}-\bar{x}]^2]
\end{align}
$$
For some estimators, their variances are difficult to calculate, so we may focus on their lower bound to determine to find the most optimal one.

The efficiency of an unbiased estimator of $\theta$ is the ratio of the [[Cramér-Rao inequality|CRLB]] of the variance of the estimator
- just as how in [[Unbiasedness]] calculations we compare it to the mean
$$
\text{efficiency}(\hat{\theta})=\frac{CRLB}{Var(\hat{\theta})}\leq 1
$$
The best ratio is 1, where $Var(\hat{\theta})=CRLB$

If $\hat{\theta}$ is unbiased for $\theta$, and $\lim_{ n \to \infty } \frac{Var(\hat{\theta})}{CRLB}=1$, then $\hat{\theta}$ is **asymptotically efficient**, as $\lim_{ n \to \infty }CRLB=0$

If $\hat{\theta}$ is an unbiased estimator for $\theta$ ($E(\hat{\theta})=\theta$) and the variance of $\hat{\theta}$ attains (is equal to) the value of the [[Cramér-Rao inequality]], then $\hat{\theta}$ is the uniformly minimum variance unbiased estimator (UMVUE) for $\theta$, and $\hat{\theta}$ is optimally efficient

Comparing $\hat{\lambda}_{1}$ from the earlier example:
$$\begin{align}
Var(\hat{\lambda}_{1}) & =\frac{\lambda}{n} \\
 CRLB  & = \huge\frac{1}{nE\left[ \left( \frac{ \partial\ln e^{-\lambda}\lambda^x / x!}{\partial \lambda} \right)^2 \right]} \\
 & =\huge\frac{1}{nE\left[ \left(  \frac{\partial-\lambda+x\ln \lambda-\ln(x!)}{\partial \lambda} \right)^2 \right]}   \\
  & = \huge\frac{1}{nE\left[ \left(  -1+ \frac{x}{\lambda} \\
 \right)^2 \right]}\\
 & =\huge\frac{1}{nE\left[ \left(  \frac{x-\lambda}{\lambda} \\
 \right)^2 \right]} \\
 & =\huge\frac{1}{n \frac{1}{\lambda^2}E\left[ (x-\lambda)^2 \right]} \\
 & =\huge\frac{1}{n \frac{\lambda}{\lambda^2}} = \frac{\lambda}{n} 
\end{align}
$$
So $\hat{\lambda}_{1}$ is the UMVUE for this estimator (best in this category)


