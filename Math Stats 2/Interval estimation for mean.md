Let $(\theta_{l},\theta_{u})$ be a **random interval**. With an appropriate probability $1-\alpha$ (confidence coefficient), we want to find values of $\theta_{l}$ and $\theta_{u}$ such that
$$
P(\theta_{l}\leq \theta \leq \theta_{u})=1-\alpha
$$
We refer to $(\theta_{l},\theta_{u})$ as a $100(1-\alpha)\%$ [[Confidence Intervals|confidence interval (CI)]] for $\theta$

Interpretation: on repeating sampling, there will be $k$ CI's for $\theta$, and $\theta$ will be covered by these CI's about $100(1-\alpha)\%$ of the time
- from all of those $k$ CI's, 95% of them will get it right

To determine the confidence limits $\theta_{l},\theta_{u}$, we use a statistic with a known distribution/parameters ([[Pivot Statistic]]) 

If $\bar{x}$ is the sample mean of a random sample from $N(\mu,\sigma^2)$ and $\sigma^2$ is known, then 
$$
CI = (\bar{x}-Z_{1-\alpha / 2}, \bar{x}+ Z_{1-\alpha / 2})wrong
$$
If $\theta$ is a location parameter, then the interval estimate usually involves a difference
- $\mu$ indicates the location for $N(\mu,\sigma^2)$
If $\theta$ is a scale parameter, then the interval estimate usually involves a ratio
- $\sigma^2$ indicates the spread of a $N(\mu,\sigma^2)$

The MLE or a sufficient statistic is often a good place to start for finding $\theta_{l}$ and $\theta_{u}$

# Examples
Knowing $\sigma^2$ from a normal distribution, but wanting to estimate the $\mu$:
$$\begin{align}
\hat{\mu} & =\bar{x}= \sum \frac{x_{i}}{n} \\
Z & = \frac{x-\mu}{\sigma / \sqrt{ n }} \sim N(0,1), \text{ (a pivot with known params)} \\
P(\mu_{l}\leq \mu \leq \mu_{u}) & = 1-\alpha  \\
P\left( \frac{\bar{x}-\mu_{u}}{\sigma / \sqrt{ n }} \leq \frac{\bar{x}-\mu}{\sigma /\sqrt{ n }} \leq \frac{\bar{x}-\mu_{l}}{\sigma / \sqrt{ n }} \right)  & = 1-\alpha \\
P\left( Z_{1 - \frac{\alpha}{2}} \right) \\
 &  \\
 \hat{\mu}_{l} & = \bar{x} - 1.96 \frac{\sigma}{\sqrt{ n }} \\
 \hat{\mu}_{u} & =\bar{x} + 1.96 \frac{\sigma}{\sqrt{ n } }
\end{align}
$$
$\sigma^2$ unknown
$$
\begin{align}
 & \hat{\mu}   = \bar{x},   \quad\sigma^2=s^2= \frac{1}{n-1} \sum (x_{i}-\bar{x})^2 \\
 & t  = \frac{\bar{x}-\mu}{s / \sqrt{ n }}\sim t_{n-1} \quad \text{t-statistic is a pivot statistic} \\
 & P(\mu_{l}\leq \mu \leq \mu_{u}) =1-\alpha \\
 & P\left( \frac{\bar{x}-\mu}{s / \sqrt{ n }} \leq \frac{\bar{x}-\mu}{s / \sqrt{ n }}\leq \frac{\bar{x}-\mu}{s / \sqrt{ n }} \right)= 1-\alpha \\
 & CI= \left( \bar{x} - t_{1-\alpha / 2} \frac{s}{\sqrt{ n }},\bar{x} + t_{1-\alpha / 2} \frac{s}{\sqrt{ n }} \right)
\end{align}
$$
By CLT:
$$
\begin{align}
 & Z=\frac{\bar{x}-\mu}{\sqrt{ Var(\bar{x}) }}=\frac{\bar{x}-\mu}{\sigma /\sqrt{ n }} , \quad Z\sim N(0,1) \text{ approx for big }n \geq 25 \\
 & \text{ Example}  \\
& X_{1},\dots,X_{n}\sim Bin(N,p), CI \text{ for } \mu \text{ and } p: \\
 & \mu=E(X)=np, \quad Var(X)=\sigma^2 = np(1-p) \\
 & \hat{\mu}=\bar{x}= \sum \frac{x_{i}}{n},\quad \hat{p}= \frac{\hat{\mu}}{N}=\frac{\bar{x}}{N}, \quad E(\hat{\mu})=E(\bar{x})=\mu \\
 & Var(\hat{\mu}) = Var(\bar{X})= \frac{1}{n^2}n Var(X) = \frac{\sigma^2}{n}= \frac{Np(1-p)}{n} \\
 & E(\hat{p})=E\left( \frac{\hat{\mu}}{N}  \right) = \frac{1}{N} Np=p \\
 & Var(\hat{p})=Var\left( \frac{\bar{X}}{N} \right) = \frac{1}{N^2 } \frac{nVar(X)}{n^2} = \frac{1}{nN^2} Np(1-p)=\frac{p(1-p)}{nN} \\
 & P( \mu_{l}\leq \mu \leq \mu_{u}) = 1-\alpha \\
 & P\left(  \frac{\bar{x}-\mu_{u}}{\sqrt{  \frac{Np(1-p)}{n} }} \leq   \frac{\bar{x}-\mu}{\sqrt{  \frac{Np(1-p)}{n} }} \leq   \frac{\bar{x}-\mu_{l}}{\sqrt{  \frac{Np(1-p)}{n} }} \right) = 1-\alpha \\
 &  P\left(  -Z_{1- \frac{\alpha}{2}}\leq N(0,1)\leq Z_{1 - \frac{\alpha}{2}} \right)= 1-\alpha \\
 & CI \text{ for }\mu=E(X) \text{ is }\left( \bar{X}-Z_{1- \frac{\alpha}{2} }\sqrt{ \frac{N\hat{p}(1-\hat{p})}{n} }, \bar{X}+Z_{1- \frac{\alpha}{2} }\sqrt{ \frac{N\hat{p}(1-\hat{p})}{n} } \right)  \\
\end{align}
$$
