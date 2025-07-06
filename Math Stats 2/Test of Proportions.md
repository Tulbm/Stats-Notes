Discrete cases like $X\sim Binom$, where we have
$$
\frac{\text{occurrences}}{\text{ total trials}}
$$
# Two-sided tests
$$
H_{0}: \theta= \theta_{0}, \quad vs \quad H_{a}: \theta \neq \theta_{0}
$$
For a two-sided test, we want to define the critical regions as: if
$$\begin{align}
 \quad X\geq K\left( \frac{\alpha}{2} \right) \quad \quad \quad &  \quad &  \text{or}  &  &    X \leq K'\left( \frac{\alpha}{2} \right) \quad \quad \quad & \\
 \text{evidende to suggest }\theta>\theta_{0} &  &  &  \quad&  \text{ evidence to suggest } \theta < \theta_{0}   & 
\end{align}
$$
we reject $H_{0}$
- $K\left( \frac{\alpha}{2} \right)$ is the smallest integer for which $P(X \geq K |H_{0}) \leq \frac{\alpha}{2}$
- $K'\left( \frac{\alpha}{2} \right)$ is the largest integer for which $P(X\leq K'|H_{0})\leq \frac{\alpha}{2}$


# One-sided tests
$$
H_{0}: \theta = \theta_{0} \quad vs \quad H_{a}: \theta > \theta_{0}
$$
We define the critical region for an $\alpha$ level test as:
- $K(\alpha)$ is the largest integer for which $P(X \geq K | H_{0})\leq \alpha$

# Large n
We can use the [[Central Limit Theorem]] and use the normal approximation to the binomial distribution
$$
E(X)= n \theta_{0}, \quad var(X) =n\theta_{0} (1-\theta_{0})
$$
$$
Z= \frac{X-E(X)}{\sqrt{ Var(X) }} = \frac{X-n\theta_{0}}{\sqrt{ n\theta_{0}(1-\theta_{0}) }}\overset{approx}{\sim} N(0,1) \text{ under }H_{0}
$$
we reject $H_{0}$ if $|Z_{obs}| \geq Z_{1- \frac{\alpha}{2}}$

When n is moderate (not very large)
$$
Z= \frac{\left( x\pm \frac{1}{2} \right)-n\theta_{0}}{\sqrt{ n\theta_{0}(1-\theta_{0}) }} \overset{\text{approx}}{\sim}  N(0,1)
$$
when 
$$
\begin{cases}
x\geq n\theta_{0} \quad \to + \frac{1}{2} \\
x < n\theta_{0} \quad \to - \frac{1}{2}
\end{cases}
$$
for continuity correction

