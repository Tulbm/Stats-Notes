The *rth* moment of a [[Random Variables|random variable]] $X$ ($\mu'$) is the expected value of $X^r$
$$
\begin{align}
\mu_{r}^{\prime}=E(X^{r})  =\sum_{x}x^{r}f(x) & \quad(discrete)\\ 
\mu_{r}^{\prime}=E(X^{r})  =\int_{-\infty}^{\infty}x^{r}f(x)dx & \quad(continuous)
\end{align}
$$
for $r=0,1,2\dots$
- $\mu_{0}'=E(X^0)=1$
- $\mu_{1}'=E(X)$, the mean
- $\mu_{2}'=E(X^2)$
### Central Moments
The *rth* moment about the mean of a random variable $X$ ($\mu _r$) is $E[(X-\mu)^r]$
$$
\begin{align}
\mu_r=E[(X-\mu)^r]=\sum_x(x-\mu)^r\cdot f(x) & \quad (discrete)\\
\mu_r=E[(X-\mu)^r]=\int_{-\infty}^\infty(x-\mu)^r\cdot f(x)dx & \quad(continuous)
\end{align}
$$
- $\mu_{0}$ =1 and $\mu_{1}=0$ provided that $\mu$ is a number ($|\mu|<\infty$)

The second central moment is the *variance* of $X$
$$
\text{var}(X)=\sigma^2=\mu_{2}=E[(X-\mu)^2]=E(X^2)-[E(X)]^2
$$
- $E(X^2-2X\mu + \mu^2)= E{(X^2)-2E(X)\mu+\mu^2}=E(X^2)-[E(X)]^2$ as $\mu=E[X]$
# Properties
$$
\text{var}(aX+b)=a^2[E(X^2)-[E(X)]^2]=a^2\sigma^2=a^2\text{var}(X)
$$
$$
var(aX+bY)=a^2var(X)+2ab\text{cov}(X,Y)+b^2var(Y)
$$
If $X$ and $Y$ are independent, the [[Covariance]] is 0, and the variance simplifies

[[Chebyshev's Theorem]]

[[Moment Generating Functions]]