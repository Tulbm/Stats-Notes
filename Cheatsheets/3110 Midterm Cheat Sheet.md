$$\begin{align}\text{Change of variables} \quad  & \text{Distribution function technique} \\
 F_{Y}(y) & =P(Y\leq y)=P(h(X_{1},\dots ,X_{n})\leq y), \quad f_{Y}(y)= \frac{\partial F_{Y}(y)}{\partial y}\\
 & \text{Transformation technique}\\
f_{y}(y) & =f_{X}(h^{-1}(y))\cdot \left|  \frac{\partial h^{-1}(y)}{\partial y}\right| \text{ if only one region}\\
f_{Y}(y) & =f_{X}(h_{1}^{-1}(y)) \left| \frac{dh_{1}^{-1}(y)}{dy}\right| + f_{x}(h_{2}^{-1}(y)) \left|\frac{|dh_{2}^{-1}(y)}{dy}\right| \\
f_{Y_1,...,Y_n}(y_1,...,y_n) & =f_{X_1,...,X_n}(g_1(y_1,...,y_n),...,g_n(y_1,...,y_n))\cdot|J| \\
|J| & = \det
\begin{bmatrix}
\frac{\partial X_1 }{\partial Y_{1}} & \frac{\partial X_{1}}{\partial Y_{2}} \\
\frac{\partial X_{2}}{\partial Y_{1}} & \frac{\partial X_{2}}{\partial Y_{2}} 
\end{bmatrix} \text{ (integrate the dummy vars)}
\end{align}
$$
$$
\begin{align} 
 & \text{Order Statistics} \\
f_{X_{(1)}} & =n[1-F_{X}(x)]^{n-1}f_X(x) \\
f_{X_{(n)}} & =n[F_{X}(x)]^{n-1}f_{X}(x) \\
f_{X_{(r)}}(x) & = \frac{n!}{(r-1)!(n-r)!} [F_{X}(x)^{r-1}]f_{X}(x)[1-F_{X}(x)]^{n-r} \\
f_{\tilde{X}}(x)  & =f_{X_{(n+1)}}(x)= \frac{(2n+1)!}{n!\cdot n!} [F_{X}(x)]^n f_{X}(x) [1-F_{X}(x)]^n
\end{align}
$$
$$\begin{align}
  & \text{Unbiasedness}\\
bias(\hat{\theta}) & =E(\hat{\theta}-\theta)=E(\hat{\theta})-\theta \\
 MSE(\hat{\theta}) & =E[(\hat{\theta}-\theta)^2]=var(\hat{\theta})+[E(\hat{\theta})-\theta]^2
\end{align}
$$
$$
\begin{align}
 & \text{Efficiency (compare unbiased estimators)} \\
\text{efficiency}(\hat{\theta}) & =\frac{CRLB}{Var(\hat{\theta})}\leq 1\quad \text{ if } Var(\hat{\theta})=CRLB \to \text{UMVUE}\\
var(\hat{\theta}) & \geq\huge\frac{1}{nE\left[\left(\frac{\partial\ln f(x;\theta)}{\partial\theta}\right)^2\right]} 
\end{align}
$$

| **Distribution**            | **PDF / PMF**                                                                                                  | **(E(X))**                      | **E(X²)**                                                         | **(Var(X))**                                                 |
| --------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------------ |
| **Uniform(a, b)**           | $\frac{1}{b - a}, \quad a \le x \le b$                                                                         | $\frac{a + b}{2}$               | $\frac{a^2 + ab + b^2}{3}$                                        | $\frac{(b - a)^2}{12}$                                       |
| **Beta($\alpha$, $\beta$)** | $\frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha - 1}(1 - x)^{\beta - 1}, \quad 0 < x < 1$ | $\frac{\alpha}{\alpha + \beta}$ | $\frac{\alpha(\alpha + 1)}{(\alpha + \beta)(\alpha + \beta + 1)}$ | $\frac{\alpha\beta}{(\alpha + \beta)^2(\alpha + \beta + 1)}$ |
| **Gamma(k, $\theta$)**      | $\frac{1}{\Gamma(k)\theta^k}x^{k - 1}e^{-x/\theta}, \quad x > 0$                                               | $k\theta$                       | $k(k + 1)\theta^2$                                                | $k\theta^2$                                                  |
| **Poisson($\lambda$)**      | $\frac{\lambda^x e^{-\lambda}}{x!}, \quad x = 0, 1, 2, \dots$                                                  | $\lambda$                       | $\lambda(\lambda + 1)$                                            | $\lambda$                                                    |
| **Binomial(n, p)**          | $\binom{n}{x}p^x(1 - p)^{n - x}, \quad x = 0, 1, \dots, n$                                                     | $np$                            | $np(1 - p) + np^2$                                                | $np(1 - p)$                                                  |
| **Geometric(p)**            | $(1 - p)^{x - 1}p, \quad x = 1, 2, 3, \dots$                                                                   | $\frac{1}{p}$                   | $\frac{2 - p}{p^2}$                                               | $\frac{1 - p}{p^2}$                                          |
| **$\chi^2(k)$**             | $\frac{1}{2^{k/2}\Gamma(k/2)}x^{k/2 - 1}e^{-x/2}, \quad x > 0$                                                 | $k$                             | $k(k + 2)$                                                        | $2k$                                                         |
| **Expntl($\lambda$)**       | $\lambda e^{-\lambda x}, \quad x > 0$                                                                          | $\frac{1}{\lambda}$             | $\frac{2}{\lambda^2}$                                             | $\frac{1}{\lambda^2}$                                        |
| **Normal($\mu,\sigma^2$)**  | $\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2\sigma^2}(x-\mu)^2}$                                                 | $\mu$                           | $\mu^2+\sigma^2$                                                  | $\sigma^2$                                                   |

- **Consistency**
$\hat{\theta}$ is a **consistent** estimator of the parameter $\theta$ if and only if  $\exists\epsilon>0$
$$
\lim_{ n \to \infty } P(|\hat{\theta}-\theta|<\epsilon)=P(-\epsilon\leq \hat{\theta}-\theta\leq \epsilon ) 
  = P( \theta - \epsilon \leq \hat{\theta} \leq \theta + \epsilon ) =1
$$
If $\hat{\theta}$ is an [[Unbiasedness|unbiased]] estimator of the parameter $\theta$ and the $Var(\hat{\theta})\to0$ as $n\to \infty$, then $\hat{\theta}$ is a consistent estimator of $\theta$
$$\begin{align} 
 & \text{
Chebyshev's Theorem}\\
P(|X-\mu|<k\sigma) &\geq1- \frac{1}{k^2}, \quad  \text{or} \quad P(|X-\mu|\geq k\sigma)\leq \frac{1}{k^2}
\end{align}
$$
**Sufficiency**
If the conditional given $\hat{\theta}$ depends on $\theta$, $\hat{\theta}$ is not sufficient
$$
f(X_{1}=x_{1},\dots,X_{n}=x_{n}|\hat{\theta})  =\frac{f(X_{1}=x_{1},\dots,X_{n}=x_{n},\hat{\theta})}{g(\hat{\theta})\leftarrow \text{ pdf of }\hat{\theta}} = \frac{f(X_{1}=x_{1},\dots,X_{n}=x_{n})}{g(\hat{\theta})}
$$
$\hat{\theta}$ is a sufficient estimator iff the joint can be factorized (fact. theorem)
$$
f(X_{1}=x_{1},\dots,X_{n}=x_{n};\theta)=g(\hat{\theta},\theta) \cdot h(x_{1},\dots ,x_{n})
$$

$$
\begin{align}
 & \text{Method of Moments        (k moments for k parameters)} \\
E(X) & =\bar{X}, \quad E(X^2)=\bar{X}^2 \\
 & \text{Method of maximum likelihood estimator} \\
L(\theta) & =L(\theta;x_{1},\dots,x_{n})=f(x_{1},\dots,x_{n};\theta)=\prod_{i=1}^ n f(x_{i};\theta) \\
l(\theta) & =\ln L(\theta)=\ln \prod f(x_{i};\theta)=\sum_{i=1}^ n\ln f(x_{i};\theta) \\
\frac{dl(\theta)}{d\theta} & = 0 \quad \text{ to find crit point at } \hat{\theta}\\
\left.\frac{d^2l(\theta)}{d\theta^2}\right|_{\theta=\hat{\theta}} & = \quad \, \,\text{ to check maximum, should be } <0 \\
 & \text{ case 2+ parameters:} \\
 \text{if}  & \begin{bmatrix}
\frac{\partial^2 \ell}{\partial \theta_1^2} & \frac{\partial^2 \ell}{\partial \theta_1 \partial \theta_2} \\
\frac{\partial^2 \ell}{\partial \theta_2 \partial \theta_1} & \frac{\partial^2 \ell}{\partial \theta_2^2}
\end{bmatrix} < 0, \text{ then our } \hat{\theta_1}, \hat{\theta_2} \text{ are MLEs of } \theta_1, \theta_2
\end{align}
$$
$$
\begin{align}  & \text{Bayesian Estimation} \\
 \text{(Prior distribution) } g(\theta) &= \text{Prior belief about } \theta \\ \text{(Likelihood) } L(\theta) &= f(x;\theta) = \text{Data's likelihood given } \theta \\ \text{(Posterior distribution) } h(\theta|x) &= \frac{f(x,\theta)}{f(x)}=\frac{f(x;\theta)g(\theta)}{f(x)}=\frac{L(\theta)g(\theta)}{f(x)} \\ L(\theta)g(\theta) &= \text{Unnormalized posterior} \\ f(x) &= \int_{\text{all } \theta} L(\theta)g(\theta)d\theta = \text{Marginal likelihood} \\ h(\theta|x) &= \frac{L(\theta)g(\theta)}{f(x)} = \text{Normalized posterior} \\ \hat{\theta}_B &= E(\theta|x) = \int_{\text{all } \theta} \theta h(\theta|x)d\theta = \text{Bayesian estimate} \end{align}
$$
