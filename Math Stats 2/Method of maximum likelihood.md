Finds a value for $\theta$ such that it gives the maximum probability of observing the observed data in comparison to other values of $\theta$

If $x_{1},\dots,x_{n}$ are observed values of a random sample from a population with the parameter $\theta$, the **likelihood function** of $\theta$ is
$$
L(\theta)=L(\theta;x_{1},\dots,x_{n})=f(x_{1},\dots,x_{n};\theta)=\prod_{i=1}^ n f(x_{i};\theta)
$$
The maximum likelihood estimate (MLE) of $\theta$ is the value of $\theta$ that maximizes the likelihood function $L(\theta)$

Under the [[Regularity|regular]] case, we use the **log-likelihood function**, as we will only need to differentiate a sum of functions instead of a product
$$
l(\theta)=\ln L(\theta)=\ln \prod f(x_{i};\theta)=\sum_{i=1}^ n\ln f(x_{i};\theta)
$$
And by a lemma, the $\hat{\theta}$ that maximizes $L(\theta)$ also maximizes $l(\theta)$

Properties
1. MLE of $\theta$ is a sufficient statistic, if one exists, then MLE is a function of it
2. is known to be asymptotically [[Efficiency|efficient]]
3. Invariance principle: if $\hat{\theta}$ is the MLE of $\theta$, then $g(\hat{\theta})$ is the MLE of the function $g(\theta)$
4. Lack of uniqueness: there could be more than one MLE
# Example
An experiment with 6 coin tosses, 2 heads

General pdf with arbitrary parameter:
$$
f(2;p)= {6\choose2}p^ 2(1-p)^4
$$
Different values of $p$ give us different probabilities of getting that sample
$$\begin{align}
p & =\frac{1}{4},\quad f\left( 2; 1 /4 \right)=0.3 \\
p & = \frac{1}{3}, \quad f(2;1 /3) = \text{higher idk}
\end{align}
$$

Finding the MLE of $iid\, Exponential(\theta)$
$$
\begin{align}
L(\theta) & =\prod \frac{1}{\theta} e^ {-x_{i}/\theta}=\theta^ {-n}e^ {- \sum x_{i} / \theta} \\
 l(\theta)& = \ln L(\theta) = \ln\left( \theta^ {-n}e^ {-\sum x_{i} / \theta} \right) \\
 &=-n\ln \theta - \sum \frac{x_{i}}{\theta} \\
\frac{dl(\theta)}{d\theta} & =-\frac{n}{\theta}+ \sum \frac{x_{i}}{\theta} =0 \text{ for crit point}\\
 \theta  & = \sum \frac{x_{i}}{n}=\bar{X} = \hat{\theta} \\
\frac{d^2l(\theta)}{d\theta^2} & = \frac{n}{\theta^2}- \left.\frac{2\sum x_{i}}{\theta^3}\right|_{\theta=\hat{\theta}=\bar{X}} \\
 & = \frac{n\bar{X}-2n\bar{X}}{(\bar{X})^3}= \frac{-n\bar{X}}{(\bar{X})^3}= \frac{-n}{(\bar{X})^2}<0 \\
\therefore l(\theta)  & \text{ has a maximum at } \hat{\theta}=\bar{X}, \text{ a MLE of }\theta
\end{align}
$$

On a irregular case, $iid\sim Uniform(0,\theta)$
$$
\begin{align}
L(\theta) & = \prod f(x_{i};\theta ) = \prod \frac{1}{\theta} \\
 l(\theta)& = \ln \theta^{-n} = -n\ln \theta \\
 \frac{dl(\theta)}{d\theta}& = - \frac{n}{\theta} = 0 \to \text{ no solution} \\
\dots &  \\
L(\theta) & = \prod \frac{1}{\theta} I[0<x_{i}<\theta]= \frac{1}{\theta^n}I[0<x_{1},\dots,x_{n}<\theta] \\
  \text{ aim to increase } & L(\theta) \text{ by decreasing }\theta \text{ to its lowest value possible, } X_{(n)} \\
\therefore  & \, \hat{\theta}= X_{(n)} \text{ is the MLE} of \theta
\end{align}
$$

Case: 2+ parameters ([[Critical Points#Hessian matrix|with hessian]])
MLE of $\mu,\mu^2, \sigma,\sigma^2 \sim N(\mu,\sigma^2)$
$$
\begin{align}
L(\theta) & =L(\mu,\sigma^2; \tilde{X} ) = (2\pi \sigma^2)^{-n/2}e^{-1/2\sigma^2 \cdot \sum (x_{i}-\mu)^2} \\
l(\mu,\sigma^2) & = - \frac{n}{2} \ln(2\pi \sigma^2)- \frac{1}{2\sigma^2} \sum (x_{i}-\mu)^2 \\
 & =- \frac{n}{2} \ln(2\pi) - \frac{n}{2} \ln(\sigma^2) - \frac{1}{2\sigma^2} \sum (x_{i}-\mu)^2 \\
\frac{\partial l}{\partial \mu}  & =  - \frac{1}{2\sigma^2} \sum 2(x_{i}-\mu)(-1)=  \frac{\sum(x_{i}-\mu)}{2\sigma^2}=0 \to \hat{\mu}=\bar{X} \\
\frac{\partial l}{\partial \sigma^2 } & = - \frac{n}{2\sigma^2}+ \frac{\sum(x_{i-\mu})^2}{2(\sigma^2)^2}= \frac{-n\sigma^2+\sum(x_{i}-\mu)^2}{2(\sigma^2)^2} = 0 \to \hat{\sigma}^2= \sum \frac{(x_{i}-\mu)^2}{n} \\
 & \text{ using }\hat{\mu}=\bar{X}, \text{ we have } \sigma^2= \frac{1}{n} \sum (x_{i}-\bar{X})^2
\end{align}
$$
$$
\text{if} \begin{bmatrix}
\frac{\partial^2 l }{\partial \mu^2} & \frac{\partial ^2l}{\partial \mu \partial \sigma^2} \\
\frac{\partial^2 l}{\partial \sigma^2 \partial \mu} & \frac{\partial ^2 l}{\partial (\sigma^2 )^2}
\end{bmatrix} < 0, \text{ then our} \hat{\mu}, \hat{\sigma}^2 \text{ are MLEs of }\mu, \sigma^2
$$
Then the MLE of $\mu^2: \hat{\mu}^2=g_{1}(\hat{\mu})=g_{1}(\bar{x})=\bar{X}^2$
And the MLE of $\sigma: \hat{\sigma}=g_{2}(\hat{\sigma}^2)=\sqrt{ \frac{1}{n} \sum (x_{i}-\bar{X})^2 }$

Case: area of solutions
$\sim Uniform(\theta,\theta+1)$
$$
\begin{align}
L(\theta) & = \prod f(x_{i};\theta)= \prod 1 I[\theta<c_{i}<\theta+1] \\
 & =1 I[\theta<x_{1},\dots,x_{n}<\theta+1] \\
 & =1 I[\theta<X_{(1)}]I[X_{(n)}<\theta+1]  \\
 & \text{L is maximized when both inequalities are true } \\
 & X_{(n)}-1 <\theta < X_{(1)} \\
\to &  \forall \theta \in [X_{(n)}-1,X_{(1)}], \theta \text{ is MLE of } \theta
\end{align}
$$

