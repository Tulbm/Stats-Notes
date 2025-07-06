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

$$
\sum_{n=0}^{x} a r^n = \frac{a(1-r^{x+1})}{1-r}
$$
$$
\begin{align}
 & \textbf{Confidence Intervals:} \\
 \mu  & = \bar{X} \pm z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} \quad (\text{known } \sigma)
\newline
\mu  & = \bar{X} \pm t_{n-1,\alpha/2} \cdot \frac{S}{\sqrt{n}} \quad (\text{unknown } \sigma)
\newline
\mu  & = \bar{X} \pm z_{1-\alpha/2} \cdot \frac{S}{\sqrt{n}} \quad (\text{CLT})
\newline
\mu_1 - \mu_2  & = (\bar{X}_1 - \bar{X}_2) \pm z_{1- \frac{\alpha}{2}} \cdot \sqrt{ \frac{\sigma_{1}^{2}}{n_{2}}+ \frac{\sigma_{2}^{2}}{n_{2}} }
\newline
\mu_1 - \mu_2  & = (\bar{X}_1 - \bar{X}_2) \pm t_{\nu,\alpha/2} \cdot \sqrt{ \frac{S_1^2}{n_1} + \frac{S_2^2}{n_2} }  \quad (n_{1},n_{2}\geq 30)
\newline
\mu_1 - \mu_2  & = (\bar{X}_1 - \bar{X}_2) \pm t_{n_1+n_2-2,\alpha/2} \cdot \sqrt{S_p^2 \left( \frac{1}{n_1} + \frac{1}{n_2} \right)}  
\newline
S_p^2  & = \frac{(n_1-1)S_1^2 + (n_2-1)S_2^2}{n_1 + n_2 - 2}
\newline
 \sigma^2  & =  \left( \frac{\sum (X_i - \mu)^2}{\chi^2_{1 - \alpha/2, \, n}}, \frac{\sum (X_i - \mu)^2}{\chi^2_{\alpha/2, \, n}} \right)\text{ (known } \mu)
 \\
\sigma^2  & = \left( \frac{(n-1)S^2}{\chi^2_{1-\alpha/2,n-1}}, \frac{(n-1)S^2}{\chi^2_{\alpha/2,n-1}} \right)
\newline 
p  & = \hat{p} \pm z_{1-\alpha/2} \cdot \sqrt{ \frac{\hat{p}(1 - \hat{p})}{n} }
\newline
p_1 - p_2  & = (\hat{p}_1 - \hat{p}_2) \pm z_{1-\alpha/2} \cdot \sqrt{ \frac{\hat{p}_1(1 - \hat{p}_1)}{n_1} + \frac{\hat{p}_2(1 - \hat{p}_2)}{n_2} }
\newline
\frac{\sigma_1^2}{\sigma_2^2}  & = \left( \frac{S_1^2}{S_2^2} \cdot \frac{1}{F_{1-\alpha/2, n_1-1, n_2-1}}, \frac{S_1^2}{S_2^2} \cdot \frac{1}{F_{\alpha/2, n_1-1, n_2-1}} \right)
\end{align}
$$
$$
\begin{align}
 & \text{Test function: } \phi(x_1,\dots,x_n) = 
 \begin{cases}
1 & \text{if } (x_1,\dots,x_n) \in C \quad \text{(reject } H_0) \\
0 & \text{otherwise}
\end{cases} \\
\text{Type I error} & = \alpha = P(\text{reject } H_0 \mid H_0 \text{ true}) \\
\text{Type II error} & = \beta = P(\text{fail to reject } H_0 \mid H_0 \text{ false}) \\
\text{Power} & = 1 - \beta = P(\text{reject } H_0 \mid H_1 \text{ true}) \\
\pi(\theta) & = P(\text{reject } H_0 \mid \theta) \quad \text{(power function)} \\
\\
 & \text{Neyman–Pearson Lemma (for simple } H_0 \text{ vs simple } H_1): \\
L_0 & = \prod_{i=1}^n f(x_i; \theta_0) \quad \text{(likelihood under } H_0) \\
L_1 & = \prod_{i=1}^n f(x_i; \theta_1) \quad \text{(likelihood under } H_1) \\
\frac{L_0}{L_1} & \leq k \quad \Rightarrow \text{ reject } H_0 \\
 & \text{Choose } k \text{ to satisfy } P(\text{reject } H_0 \mid H_0) = \alpha \\
 & \text{Critical region: set of values making } \frac{L_0}{L_1} \leq k \\
\\
 & \text{Likelihood Ratio Test (general):} \\
L(\theta) & = \prod_{i=1}^n f(x_i; \theta) \quad \text{(full likelihood)} \\
\Uplambda  & = \frac{\text{max }L_{0}}{\text{max }L}=\frac{L(\tilde{\theta})}{L(\hat{\theta})} = \frac{\prod_{i=1}^nf(x_{i},\theta_{0})}{\prod_{i=1}^n f(x_{i},\hat{\theta})} \\
\text{Reject } H_0 & \text{ if } \Lambda \leq k \quad \text{(or equivalently, } -2\ln \Lambda \geq c) \\
 & \text{Choose } k \text{ (or } c) \text{ so that test has level } \alpha \\
 & \text{Asymptotically: } -2\ln\Lambda \sim \chi^2_{\text{df}} \text{ under } H_0
\end{align}
$$
$$
\begin{align}
 & \textbf{Z/T Tests for Mean} (t_{n-1} ) \\
C & =\left\{ (x_{1},\dots,x_{n});|\bar{x}-\mu_{0}|  \geq Z_{1 - \frac{\alpha}{2}} \frac{\sigma}{\sqrt{ n }}  \right\} \text{ (2 sided test)} \\
\theta<\theta_{0} :z & \leq -Z_{1-\alpha} ,\quad \theta > \theta_{0}:z  \geq Z_{1-\alpha} \\ \\
 & \textbf{Difference in Means (Unknown Variances)} \\
Z_{obs} &= \frac{\bar{x} - \bar{y} - \delta_0}{\sqrt{ \frac{S_1^2}{n_1} + \frac{S_2^2}{n_2} }} \quad n \geq 30 \\
t &= \frac{\bar{x} - \bar{y} - \delta_0}{\sqrt{S_p^2 \left( \frac{1}{n_1} + \frac{1}{n_2} \right)}} \sim t_{n_1 + n_2 - 2} \quad n<30, \text{pooled }\sigma^{2} \\ \\
 & \textbf{Test for Variances} \\
\text{Known } \mu: \chi^2 &= \frac{n \hat{\sigma}^2}{\sigma_0^2} = \frac{\sum (x_i - \mu)^2}{\sigma_0^2} \sim \chi_n^2 \\
\text{Unknown } \mu: \chi^2 &= \frac{(n - 1) s^2}{\sigma_0^2} \sim \chi_{n - 1}^2 \\
\text{Reject } H_0 &: \chi^2_{obs} < \chi^2_{\alpha/2} \text{ or } \chi^2_{obs} > \chi^2_{1 - \alpha/2} \\ 
F &= \frac{S_1^2}{S_2^2} \sim F_{n_1 - 1, n_2 - 1} \\
\text{Reject } H_0 &: F_{obs} > F_{1 - \alpha/2}, \text{ or } F_{obs} < F_{\alpha/2} \\ \\
 & \textbf{Binomial Proportion Test (Exact)} \\
\text{Two-sided} &: X \ge K(\alpha/2) \text{ or } X \le K'(\alpha/2), \text{ K smallest and }K'\text{ largest for } \frac{\alpha}{2}\\
\text{One-sided} &: X \ge K(\alpha), \text{ where } P(X \ge K | H_0) \le \alpha \\ \\
 & \textbf{Binomial Proportion (Normal Approx.)} \\
Z &= \frac{X - n \theta_0}{\sqrt{n \theta_0 (1 - \theta_0)}} \approx N(0,1) \\
\text{Continuity correction:} \\
Z &= \frac{\left( x \pm \frac{1}{2} \right) - n \theta_0}{\sqrt{n \theta_0 (1 - \theta_0)}} \\
\text{Use } +\frac{1}{2} &: x \ge n \theta_0, \quad -\frac{1}{2} \text{ if } x < n \theta_0 \\ \\
 & \textbf{Chi-squared Test, Reject if }\chi^{2}_{obs}\geq \chi^{2}_{df, 1-\alpha} \\
\sum_{i=1}^K Z_{i}^2  &  \sim \chi_{k}^2 = \sum\left( \frac{x_{i}-n_{i}\theta_{i}}{\sqrt{ n_{i}\theta_{i}(1-\theta_{i}) }}  \right)^2 = \sum_{i}\sum_{j} \frac{(f_{ij}-E_{ij})^2}{E_{ij}} \sim \chi_{df}^ 2  \\
df & = (k-1)(c-1) , \text{ or } k(c-1) \text{ if } \theta _{j}'s \text{ are given}
\end{align}
$$
To test for association (independence):
$$
E_{ij}= n \hat{\pi}_{ij}=n\hat{\pi}_{i\cdot}\hat{\pi}_{\cdot j},\quad df = H_{a}-H_{0}
$$
Step 1. Estimate the parameter for the assumed distribution
Step 2. Compute the probability for each observation under the assumed distribution
Step 3. Compute the expected frequencies
Step 4. Test the goodness-of-fit of the assumed distribution to the observed data
$df=k-1-$# parameters estimated
