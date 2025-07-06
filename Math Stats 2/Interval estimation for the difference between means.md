
## Examples
$X_{1},..,X_{n_{1}}\sim N(\mu_{X},\sigma^2_{X}),\, Y_{1},\dots,Y_{n_{2}}\sim N(\mu_{y},\sigma^2_{Y})$
If $\sigma^2_{X},\sigma^2_{y}$ are known:
$$
\begin{align}
 & \hat{\mu}_{X}=\bar{x},\quad \hat{\mu}_{Y}=\bar{y} \\
 & \bar{x}\sim N\left( \mu_{x}, \frac{\sigma^2_{x}}{n_{1}}  \right), \quad \bar{y}\sim N\left( \mu_{Y}, \frac{\sigma^2_{Y}}{n_{2}} \right) \\
 & \bar{x}-\bar{y}\sim N\left( \mu _{X},\mu_{Y}, \frac{\sigma^2_{X}}{n_{1}}+ \frac{\sigma_{Y}^2}{n_{2}} \right) , d =\mu _{X}-\mu_{Y} \\
 & Z = \frac{\bar{x}-\bar{y}-D}{\sqrt{ \frac{\sigma_{X}^2}{n_{1}}+ \frac{\sigma^2_{Y}}{n_{2}}  }} \sim N(0,1) \\
 & P(D_{l} \leq D \leq D_{u} )=1-\alpha \\
 & P\left( \frac{\bar{x}-\bar{y}-D_{u}}{\sqrt{ \frac{\sigma^2_{X}}{n_{1}}+ \frac{\sigma^2_{Y}}{n_{2}} }}  \leq \frac{\bar{x}-\bar{y}-D}{\sqrt{ \frac{\sigma^2_{X}}{n_{1}}+ \frac{\sigma^2_{Y}}{n_{2}} }}  \leq \frac{\bar{x}-\bar{y}-D_{l}}{\sqrt{ \frac{\sigma^2_{X}}{n_{1}}+ \frac{\sigma^2_{Y}}{n_{2}} }} \right) =1-\alpha\\
 & CI \text{ for } D=\mu_{X} - \mu_{Y}: ()
\end{align}
$$
$\sigma^2_{X},\sigma^2_{Y}$ are unknown:
$$\begin{align}
 & \hat{\sigma}_{X}^2 = S_{X}^2 = \sum_{i=1}^{n_{1}} \frac{(X_{i}-\bar{X})^2}{n-1} \\
 & \hat{\sigma}_{y}^2 = S^2_{y} = \sum_{i=1}^{n_{2}} \frac{(Y_{i}-\hat{Y})^2}{n_{2}-1} \\
 & \text{ for } n_{1}\geq 30, n_{2}\geq 30 \text{ replace }\sigma^2s \text{ by }S^2s \\
 & \text{ CI for }D=\mu _{x}-\mu_{y}:  \\
 & \left( \bar{x}-\bar{y}- Z_{\frac{\alpha}{2}}\sqrt{ \frac{S_{x}^2}{n_{1}}+ \frac{S_{Y}^2}{n_{2}} }, \bar{x}-\bar{y}+ Z_{\frac{\alpha}{2}}\sqrt{ \frac{S_{x}^2}{n_{1}}+ \frac{S_{Y}^2}{n_{2}} } \right) \\
 & \text{for small }n_{1},n_{2}<30, \text{ we pool information from the 2 samples} \\
 & \hat{\sigma}^2_{pooled}=S^2_{pooled} = \frac{\sum^{n_{1}}(x_{i}-\bar{x})^2+\sum^{n_{2}}(y_{i}-\bar{y})^2}{n_{1}+n_{2}-2} \\
 & = \frac{(n_{1}-1)S^2_{x}+(n_{2}-1)S_{y}^2}{n_{1}+n_{2}-2} \\
t & =\frac{\bar{x}-\bar{y}-D}{\sqrt{ V\hat{a}r(\bar{x}-\bar{y}) }} = \frac{\bar{x}-\bar{y}-D}{\sqrt{ \frac{\hat{\sigma}^2_{X}}{n_{1}} + \frac{\hat{\sigma}^2_{Y}}{n_{2}}  }} = \frac{\bar{x}-\bar{y}-D}{\sqrt{  \frac{S^2_{pooled}}{n_{1}}+ \frac{S^2_{pooled}}{n_{2}} }} \\
 & =\frac{\bar{x}-\bar{y}-D}{S_{pooled}\sqrt{ \frac{1}{n_{1}}+ \frac{1}{n_{2}} }} \sim t_{n_{1}+n_{2}-2} \\
 & \text{CI for }D = \mu _{x}-\mu_{y}: \\
 & \left( \bar{x}-\bar{y}-t_{1 - \frac{\alpha}{2}, n_{1}+n_{2}-2} \sqrt{  S^2_{pooled} \left( \frac{1}{n_{1}} + \frac{1}{n_{2}} \right) }  , \bar{x}-\bar{y}+t_{1 - \frac{\alpha}{2}, n_{1}+n_{2}-2} \sqrt{  S^2_{pooled} \left( \frac{1}{n_{1}} + \frac{1}{n_{2}} \right) }  \right)
\end{align}
$$

[[Test of Means]] 