If as estimator $\hat{\theta}(X_{1},\dots,X_{n})$ provides all information that the sample contains for estimating $\theta$, $\hat{\theta}$ is said to be sufficient for $\theta$
- each observation provides information about the value of $\theta$

We determine the sufficiency by determining if the conditional joint distribution of $X_{1},\dots,X_{n}$ given the estimator $\hat{\theta}$ depends on the parameter $\theta$ or not
$$\begin{align}
f(X_{1}=x_{1},\dots,X_{n}=x_{n}|\hat{\theta}) & =\frac{f(X_{1}=x_{1},\dots,X_{n}=x_{n},\hat{\theta})}{g(\hat{\theta})\leftarrow \text{ pdf of }\hat{\theta}}  \\
 ((\cap \hat{\theta})\text{ is always true})\quad& = \frac{f(X_{1}=x_{1},\dots,X_{n}=x_{n})}{g(\hat{\theta})}
\end{align}
$$
If $f(X_{1}=x_{1},\dots,X_{n}=x_{n}|\hat{\theta})$ depends on $\theta$, the sample values of $x_{1},x_{2},\dots,x_{n}$ would provide additional information of $\theta$ (given $\hat{\theta}$), so $\hat{\theta}$ is not sufficient enough

If it is independent on $\theta$, then (given $\hat{\theta}$) $\theta$ does not provide any more information not already contained in $\hat{\theta}$
- not a function of $\theta$


# Factorization Theorem
Factorize the joint into two parts to show the sufficiency of an estimator without (a lot of work)

$\hat{\theta}$ is a sufficient estimator of the parameter $\theta$ if and only if the joint distribution/density of the random sample can be factorized as:
$$
f(X_{1}=x_{1},\dots,X_{n}=x_{n};\theta)=g(\hat{\theta},\theta) \cdot h(x_{1},\dots ,x_{n})
$$
where $g(\hat{\theta},\theta)$ depends only on $\hat{\theta}$ and $\theta$, and $h(x_{1},\dots,x_{n})$ does not depend on $\theta$


We can use the dependence of the sample space on the parameter $\theta$ to show the sufficiency of a estimator

$$
\begin{align}
f(X_{1}=x_{1},\dots,X_{n}x_{n},\theta) & = \\
 & = \\
 & = \\
 & = \theta^ {-n}I[X_{(n)}<\theta] \cdot I[0<X_{(1)}] \\
 & = g(\hat{\theta},\theta) \cdot h(x_{1},\dots,x_{n})
\end{align}
$$





# examples

$X_{1},X_{2},X_{3}\sim Be\mathrm{rnoulli(p)}$
$\hat{p}=\frac{1}{6}(X_{1}+2X_{2}+3X_{3})$

Let $x_{1}=1,x_{2}=1,x_{3}=0$ be a realization of the sample, then $\hat{p} = \frac{1}{2}$
$$
\begin{align}
 & =f(X_{1}=x_{1},X_{2}=x_{2},X_{3}=x_{3}|\hat{p})   \\
 & =\frac{f(X_{1}=1,X_{2}=1,X_{3}=0, \hat{p}=1/2)}{p(\hat{p}=1 /2)} \\
  &  =\frac{P(\hat{p}= 1 /2 |X_{1}=1,X_{2}=1,X_{3}=0)P(X_{1}=1,X_{2}=1,X_{3}=0)}{P(\hat{p}) = 1 /2} \\
 & = \frac{\left( \text{ 2 possible situations for }\hat{p} = \frac{1}{2}  \right)\quad\quad1\cdot p^2(1-p)}{P\left( \hat{p}= \frac{1}{2}|X_{1}=1,X_{2}=1,X_{3}=0 \right)P(X_{1}=1,X_{2}=1,X_{3}=0)+P\left( \hat{p}=\frac{1}{2}|X_{1}=0,X_{2}=0,X_{3}=1 \right)P(X_{1}=0,X_{2}=0,X_{3}=1)} \\
 & =\frac{p^2(1-p)}{1\cdot p^2(1-p)+ 1 \cdot p(1-p)^2}=p \text{ (not independent of p)}
\end{align}
$$
$\hat{p}$ is not sufficient for p


## factorization theorem
$\sim N(\mu,\sigma^2)$
$\bar{X}= \frac{1}{n} \sum X_{i}$

$$
\huge\begin{align}
 & f(X_{1}=x_{1},\dots,X_{n}=x_{n};\mu;\sigma^2) \\
= & \Pi  \frac{1}{\sqrt{ 2\pi \sigma^2 }}e^{-(x_{i}-\mu)^2/2\sigma^2} \\
 = & (2\pi \sigma^2)^{-n/2} e^{-\sum(x_{i}-\mu)^2/2\sigma^2} \\
=& (2\pi \sigma^2)^{-n/2} e^{-\sum(x_{i}-\bar{x}+\bar{x}+\mu)^2/2\sigma^2} \\
=& (2\pi \sigma^2)^{-n/2} e^{-\left( \sum(x_{i}-\bar{x})^2+2 \sum (x_{i}-\bar{x})(\bar{x}-\mu)+\sum(\bar{x}-\mu)^2 \right)/2\sigma^2} \\
= & (2\pi \sigma^2)^{-n/2}e^{- \sum(x_{i}-\bar{x})^2 / 2\sigma^2} e^{- 2(\bar{x}-\mu)**\sum(x_{i}-\bar{x})**/2\sigma^2} e^{- \sum (\bar{x}-\mu)^2/2\sigma^2} \\
= & (2\pi \sigma^2)^{-n/2}e^{- \sum(x_{i}-\bar{x})^2 / 2\sigma^2} \cdot 1 \cdot  e^{- \sum (\bar{x}-\mu)^2/2\sigma^2}  \\
= & e^{-n (\bar{x} -\mu)^2/2\sigma^2} \cdot(2\pi \sigma^2)^{-n/2} e^{- \sum (x_{i}-\bar{x})^2/2\sigma^2} \\
= & g(\bar{x},\mu) \cdot h(x_{1},\dots,x_{n})  \\
 & \therefore \bar{x} \text{ is a sufficient estimate for }\mu
\end{align}
$$


