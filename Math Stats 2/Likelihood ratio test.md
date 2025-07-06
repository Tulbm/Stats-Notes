To construct critical regions for a test of composite hypothesis:
$$
H_{0}: \theta\in \vartheta_{0}\quad vs\quad H_{a}: \theta\ \in \vartheta_{1}
$$

LRTs are generalizations of the [[Neyman-Pearson lemma]] that are not necessarily uniformly most powerful

LRTs compare the restricted maximum likelihood under $H_{0}$ 
$$
\text{max}\,L_{0}=\text{max}_{\theta\in\vartheta_{0}}L(\theta)
$$
against the unrestricted maximum likelihood over any value in the parameter space, $\theta\in\Theta=\Theta_{0}\cup\Theta_{1}$
$$
\text{max}L=\text{max}_{\theta\in\Theta}L(\theta)
$$

Suppose we have a random sample $X_{1},..,X_{n}\sim iid\, f(x;\theta)$. The maximum likelihood under $H_{0}$ and for all values of $\theta\in \Theta$ are given by
$$\begin{align} 
\text{max}_{\theta\in \Theta_{0}}L(\theta) & = \prod f(x_{i};\tilde{\theta})\\
\text{max}_{\theta\in \Theta}L(\theta) & = \prod f(x_{i};\hat{\theta})
\end{align}
$$
where $\tilde{\theta}=\Theta_{0}$, the MLE of $\theta$ within $\Theta_{0}$ (restricted MLE) and $\hat{\theta}$ is the unrestricted MLE of $\theta$

The likelihood ratio statistic     109,110
$$
\Uplambda = \frac{\text{max }L_{0}}{\text{max } L}
$$
If $\Uplambda\approx 0$ we would like to reject $H_{0}$
If $\Uplambda \approx 1$ we would like to accept $H_{0}$



If $\Theta=\Theta_{0} \cup \Theta_{1}$, $\Theta_{0}\cap \Theta_{1}= \emptyset$ and
$$
\Uplambda = \frac{\text{max }L_{0}}{\text{max }L}=\frac{L(\tilde{\theta})}{L(\hat{\theta})}
$$
then the critical region $\Uplambda \leq k$, $0<k<1$ is a likelihood ratio test for testing $H_{0}$ against $H_{a}$

If we don't know the distribution of $\Uplambda$, but have a large sample size $n$:
$$
-2 \ln \Uplambda = -2\ln\left( \frac{\text{max }L_{0}}{\text{max }L} \right) = -2[l(\tilde{\theta})-l(\hat{\theta})]\sim \chi_{1}^ 2 \text{ approx}
$$
If the samples come from a normal distribution, $-2[l(\tilde{\mu})-l(\hat{\mu})]\sim \chi_{1}^ 2$ exactly
- or just $2[l(\hat{\mu}-l(\tilde{\mu}))]$
# Examples
111,112



*Removed bc from assignment*
:(