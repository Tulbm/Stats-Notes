Given a random sample $X_{1},\dots,X_{n}\sim N(\mu,\sigma^2)$, we want to test if $\sigma^2 = \sigma_{0}^2$ or not at an $\alpha$ significance level

$$
\begin{aligned}
 & \sum_{i=1}^n(X_i-\mu)^2/\sigma^2\sim\chi_n^2, \\
 & \sum_{i=1}^n(X_i-\overline{X})^2/\sigma^2\sim\chi_{n-1}^2, \\
 & (n-1)S^2/\sigma^2\sim\chi_{n-1}^2,
\end{aligned}
$$

# Tests for one variance

Case 1: $\mu$ is known
$$\begin{align}
\hat{\sigma}^2  & = \sum \frac{(x_{i}-\mu)^2}{n} \\
\chi^2 & =\frac{n\hat{\sigma}^2}{\sigma_{0}^2}= \frac{\sum (x_{i}-\mu)^2}{\sigma_{0}^2} \sim \chi_{n}^2 \text{ | }H_{0} \\
\alpha  & = P\left( \chi^2 \leq \chi^2_{\frac{\alpha}{2},n} \text{ or }\chi^2\geq \chi^2_{1- \frac{\alpha}{2},n}\right) \\
\end{align}
$$
Compute $\chi_{obs}^2$ and reject $H_{0}$ if the value is too large or too small

Case 2: $\mu$ is unknown
$\hat{\mu}=\bar{x}, \bar{\sigma}^2 =s^2= \frac{1}{n-1}\sum(x_{i}-\bar{x})^2$
$$
\begin{align}
\text{pivot statistic}\to\chi^2 & = \frac{(n-1)\hat{\sigma}^2}{\sigma_{0}^2}= \frac{(n-1)S^2}{\sigma_{0}^2}= \frac{\sum(x_{i}-\bar{x})^2}{\sigma_{0}^2}\sim \chi_{n-1}^2 \\
\alpha & =P\left( \chi^2 \leq \chi_{\frac{\alpha}{2}, n-1}^2\text{ or } \chi^2 \geq \chi_{1- \frac{\alpha}{2},n-1}^2 \right) \\
\text{compute }  \chi_{obs}^2 & , \text{ reject }H_{0} \text{ if } \chi^2_{obs} \leq \chi_{\frac{\alpha}{2}, n-1}^2\text{ or } \chi^2_{obs} \geq \chi_{1- \frac{\alpha}{2},n-1}^2
\end{align}
$$

# Test for comparing two variances
$X_{1},\dots,X_{n}\sim iid N(\mu_{1},\sigma_{1}^2),\quad Y_{1},\dots,Y_{n}\sim idd N(\mu_{2},\sigma_{2}^2)$
$$
F=\frac{S_{1}^2/\sigma_{1}^2}{S_{2}^2 /\sigma_{2}^2} \sim F_{n_{1}-1,n_{2}-1}
$$
$$
\begin{align}
H_{0} & :\sigma_{1}^2  =\sigma_{2}^2 \quad   &  & vs   &   H_{a}:&\sigma_{1}\neq \sigma_{2} \\
H_{0} & : \frac{\sigma_{1}^2}{\sigma_{2}^2}=1 &  & vs   &  H_{a}: & \frac{\sigma_{1}^2}{\sigma_{2}^2}\neq 1 \\
\hat{\sigma}_{1}  & = S_{1}^2 = \frac{\sum(x_{i}-\bar{x})}{n-1},  &  &  &  \hat{\sigma}2= & S_{2}^2 = \frac{\sum(y_{i}-\bar{y})^2}{n_{2}-1} \\
F & =\frac{S_{1}^2/\sigma_{1}^2}{S_{2}^2 / \sigma_{2}^2} = \frac{S_{1}^2}{S_{2}^2}    \sim     F_{n_{1}-1,n_{2}-1}   &  &  &   \text{under }H_{0}: & \sigma_{1}^2=\sigma_{2}^2  \\
\text{reject }  & H_{0} \text{ if } F_{obs}>F_{n_{1}-1,n_{2}-1,1- \frac{\alpha}{2}} &  &  \text{ or the other}& \text{ way i guess} 
 \end{align}
$$

