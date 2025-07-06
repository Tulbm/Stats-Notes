A random variable $X$ has a exponential distribution $X\sim Exp(\theta)$ if and only if it has the pdf
$$
f(x;\theta)= \frac{1}{\theta}e^{-x/\theta} \quad \text{ for x}>0
$$
Mean $\mu=\theta$

Variance $\sigma^2=\theta^2$

Equivalent to the pdf of a [[Gamma Distribution]] with $\alpha=1$
$$
\frac{1}{\theta^1\Gamma(1)}x^{1-1}e^{-x/\theta}
$$
Recall that if recurrent events happen according to a Poisson process with mean number of events per unit time is λ, then the number of events that occurs during an unit of time has a Poisson distribution with mean λ. The waiting time until the first event occurs has an exponential distribution with parameter θ = 1  λ and the mean waiting time is 1 λ . In addition, the waiting time between two successive events has the same exponential distribution

[[Probability Densities#Cumulative Distribution Function (CDF)|CDF]]
$$
F_{X}(x)=1-e^{-x/\theta},\quad x>0, \theta > 0
$$


# [[Order Statistics]]
$$\begin{align}
f_{X_{(1)}} & = \frac{1}{\theta /n } e^{-x/(\theta/n) } \\
 & \sim Exponential \left( \frac{\theta}{n} \right)
\end{align}
$$
$$\begin{align}
f_{X_{(n)}} & =n[F_{X}(x)]^{n-1} f_{X}(x) \\
 & =\frac{n}{\theta}e^{-x/\theta} [1-e^{-x/\theta}]^{n-1}
\end{align}
$$
Let $n=2m+ 1$
$$
f_{\tilde{X}}(x)=\frac{(2m+1)!}{m! m!} \frac{1}{\theta} e^{-(m+1)x/\theta} (1-e^{-x/\theta})^m
$$