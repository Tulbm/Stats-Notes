

# Probability Density Function
A random variable $X$ has a normal distribution $X\sim N(\mu,\sigma^2)$ if and only if if has a pdf in the form of
$$
f(x;\mu,\sigma^2)= \frac{1}{\sqrt{ 2\pi \sigma^2 }}e^{-(x-\mu)^2/2\sigma^2}
$$

for $-\infty<x<\infty$ where $\sigma^2>0$

If $X\sim N(\mu,\sigma^2)$ then
$$
Z=\frac{X-\mu}{\sigma}\sim N(0,1)
$$
It follows that
$$\begin{align}
P(X<x) & =P\left( \frac{X-\mu}{\sigma} < \frac{x-\mu}{\sigma}\right) \\
 & =P\left( Z< \frac{x-\mu}{\sigma} \right)
\end{align}
$$
Moment-generating function
$$
M_{X}(t)=e^{\mu t+\frac{1}{2}\sigma^2t^2}
$$
And for the standard normal distribution $Z\sim N(0,1)$:
$$
M_{Z}(t)=e^{0t+\frac{1}{2}1t^2}=e^{t^2/2}
$$
$$\begin{align}
E(X) & =\left.\frac{dM_{X}(t)}{dt}\right|_{t=0} \\
 & =\frac{d}{dt} e^{\mu t+\frac{1}{2}\sigma^2t^2} \\
 & =e^{\mu t+\frac{1}{2}\sigma^2t^2}(\mu+\sigma^2t)|_{t=0} \\
 & =\mu \\
 \\
E(X^2) & =\frac{d^2}{dt^2}M_{X}(t) \\
 & =\left.e^{ut+\frac{1}{2}\sigma^2t^2}(\mu+\sigma^2t)^2+e^{\mu t+\frac{1}{2}\sigma^2t}(\sigma^2)\right|_{t=0} \\
 & =\mu^2+\sigma^2 \\
 \\
Var(X) & =(\mu^2+\sigma^2)-(\mu)^2 \\
 & =\sigma^2
\end{align}
$$

If $X\sim Bin(n,p)$ then the moment-generating function of 
$$
Z=\frac{X-np}{\sqrt{ np(1-p) }}=\frac{X-\mu}{\sigma}
$$
approaches that of the standard normal distribution

then
$$
P(X\leq x)=P\left( Z\leq \frac{x-\mu}{\sigma} \right)
$$
(sampling distribution of the [[Binomial Distribution]] goes to normal :D)



# Standard Normal Distribution
- Standard Normal Distribution (SND)
	- a normal distribution with $\mu =0, \sigma = 1(\sigma^2=1)$ 
	- represent random variables that have the SND with a Z
		-  $Z\sim N(0,1)$
	- standardizing normally distributed random variables
		- converting it to the SND
		- $X\sim N(\mu,\sigma^2)$
		- $Z=\frac{X-\mu}{\sigma}$ 
		- mean - mean = 0, sd/sd = 1
		- example
			- $P(X<0.22)\longrightarrow P(\frac{x-\mu}{\sigma} < \frac{0.22-\mu}{sigma})\longrightarrow P(Z<-1.5)$  
	- PDF
		- ![](https://i.imgur.com/nb2UMRS.png)
	- CDF
		- $P(Z\leq -1.31)$ 
		- ![](https://i.imgur.com/9MhkgDg.png)
- PDF
	- $$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2\sigma^2}(x-\mu)^2}$$
	- for $-\infty < x < \infty$
	- 2 parameters = $\mu, \sigma/\sigma^2$
	- if x is normally distributed with mean $\mu$ and variance $\sigma^2$, we write it as $X\sim N(\mu,\sigma^2)$  
- symmetric about $\mu$
	- $\mu$ is the mean and the median
	- empirical rule
		- ![](https://i.imgur.com/GtFWcXu.png)
- many techniques are based on it
- real world variables, bell shaped curved![](https://i.imgur.com/LSUguvG.png)
[[Z distribution]]