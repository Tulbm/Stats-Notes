For samples following a normal distribution, use [[Test Statistics#Z test|Z statistic]] or the [[Test Statistics#T test|T statistic]] if $\sigma$ is unknown 
## Two-sided alternative
A two-tailed test
$$
\text{p-value}=P(Z>|Z_{obs}| \times 2) < \alpha \longrightarrow \text{Reject }H_{0}
$$
Only one case:
$$
H_{0}:\mu=\mu_{0}\quad \text{vs} \quad H_{a}:\mu \neq \mu_{0}
$$
Using the [[Likelihood ratio test]] statistic, the critical region for an $\alpha$ level test is given by
$$
\begin{align}
|\bar{x}-\mu_{0}|  & \geq Z_{1 - \frac{\alpha}{2}} \frac{\sigma}{\sqrt{ n }}  \\
C & =\{(x_{1},\dots,x_{n});|\bar{x}-\mu_{0}|  \geq Z_{1 - \frac{\alpha}{2}} \frac{\sigma}{\sqrt{ n }} \} \\
C & =\{(x_{1},\dots,x_{n});z  \geq Z_{1 - \frac{\alpha}{2}},z  \leq -Z_{1 - \frac{\alpha}{2}} \} 
\end{align}
$$

## One-sided alternative
A one tailed test
$$
\text{p-value}=P(Z>Z_{obs}) < \alpha \longrightarrow \text{Reject }H_{0}
$$
Case 1:
$$
H_{0}: \theta=\theta_{0} \quad \text{vs} \quad H_{a}: \theta<\theta_{0}
$$
We would like to reject $H_{0}$ if $\hat{\theta}$ is much smaller than $\theta_{0}$

With samples from a normal distribution:
$$\begin{align}
\alpha & =P\left( \bar{x}-\mu_{0}\leq -Z_{1-\alpha} \frac{\sigma}{\sqrt{ n }} \right)\\
C & =\{(x_{1},\dots,x_{n});z \leq -Z_{1-\alpha}\}
\end{align}
$$
Case 2:
$$
H_{0}: \theta=\theta_{0} \quad \text{vs} \quad H_{a}: \theta>\theta_{0}
$$
We would like to reject $H_{0}$ if $\hat{\theta}$ is much larger than $\theta_{0}$
$$
\begin{align}
\alpha & =P\left( \bar{x}-\mu_{0}\geq Z_{1-\alpha} \frac{\sigma}{\sqrt{ n }} \right)\\
C & =\{(x_{1},\dots,x_{n});z \geq Z_{1-\alpha}\}
\end{align}
$$
