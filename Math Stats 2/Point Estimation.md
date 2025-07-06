Using a point estimator $\hat{\theta}$ to estimate $\theta$
$$
P(\hat{\theta}=\theta)=0
$$
Suppose a random sample $X_{1},\dots,X_{n}$ is collected from a population and it is assumed that $X_i\overset{iid}{\sim}f(x;\theta)$ 
Let the estimator of $\theta$ be $\hat{\theta}=\hat{\theta}(X_{1},\dots,X_{n})$ be a function of $X_{i}'$s meant to estimate $\theta$

[[Finding point estimators]]
# Evaluation
Properties of a good estimator:
1. [[Unbiasedness]]: $E(\hat{\theta})=E(\hat{\theta}(X_{1},\dots,X_{n}))=\theta$
2. [[Efficiency]]: $var(\hat{\theta}(X_{1},\dots,X_{n}))$ is as small as possible (more efficient per sample size)
3. [[Consistency]]: $\hat{\theta}(X_{1},\dots,X_{n})\to \theta$ as $n\to \infty$
4. [[Sufficiency]]: Does $\hat{\theta}$ utilize all the information contained in the data to estimate $\theta$?
5. Likeliness: $\hat{\theta}(X_{1},\dots,X_{n})$ is the most likely value of $\theta$ give the data ($\hat{\theta}$ is the choice with highest probability for the data)
6. Robustness: $\hat{\theta}(X_{1},\dots,X_{n})$ has a sampling distribution that is not too adversely affected by violations of assumptions made in the model/analysis

An estimator $\hat{\theta}(X_{1},\dots,X_{n})$ is [[Analysis|asymptotically]] unbiased for $\theta$ if
$$
\lim_{ n \to \infty } bias(\hat{\theta}(X_{1},\dots,X_{n}))=0
$$
$E(\hat{\theta})\to \theta$ as $n\to \infty$

If $\hat{\theta}$ is unbiased for $\theta$, and $\lim_{ n \to \infty } \frac{Var(\hat{\theta})}{CRLB}=1$, then $\hat{\theta}$ is **asymptotically efficient**

