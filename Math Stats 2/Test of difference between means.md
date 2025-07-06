Let X1, · · · , Xn1 be a random sample from a N (μ1, σ2 1 ) distribution  and Y1, · · · , Yn2 be a random sample from a N (μ2, σ2  2 ) distribution.
We want to test:
$$
H_{0}:\mu_{1}-\mu_{2} = \delta\quad \text{vs}\quad H_{a}:\mu_{1}-\mu_{2}\neq \delta
$$
[[Method of maximum likelihood|MLEs]] of $\mu_{1}$ and $\mu_{2}$ are $\bar{x}$ and $\bar{y}$
[[Method of maximum likelihood|MLEs]] of $\delta=\mu_{1}-\mu_{2}$ is $\hat{\delta}=\bar{x}-\bar{y}$
# Known Variances


120


# Unknown Variances

Case 1:
Sample sizes of $n_{1},n_{2} \geq 30$
$$
\begin{align}
 & \hat{\sigma}_{1}^2 = S_{1}^2, \quad \hat{\sigma}_{2}^2 = S_{2}^2 \\
 & Z = \frac{\bar{x}-\bar{y}-\delta_{0}}{\sqrt{ \frac{S_{1}^2}{n_{1}}+ \frac{S_{2}^2}{n_{2}}}} \sim N(0,1) \\
 & \dots
\end{align}
$$

Case 2:
Either or both sample sizes are small ($\leq 30$)

Assume $\sigma_{1}^2=\sigma_{2}^2=\sigma^2$
$$
\begin{align}
 & \hat{\sigma}^2 = S_{pooled}^2 = \frac{(n_{1}-1)S_{1}^2+(n_{2}-1)S_{2}^2}{n_{1}+n_{2}-2} \\
 & t = \frac{\bar{x}-\bar{y}-\delta_{0}}{\sqrt{ \frac{\hat{\sigma}^2}{n_{1}} + \frac{\hat{\sigma}^2}{n_{2}} }}= \frac{\bar{x}-\bar{y}-\hat{\delta}_{0}}{\sigma \sqrt{  \frac{1}{n_{1}} + \frac{1}{n_{2}} }} \sim t_{n_{1}+n_{2}-2}
\end{align}
$$
