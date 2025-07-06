The test procedure partitions the sample space into an acceptance region and a rejection/critical region for $H_{0}$

When the $H_{0}$ is true, the probability of obtaining a value of test statistics that the corresponding random samples fall inside the critical region is called the **size** of the critical region or the **level of significance** of the test
- the level of evidence against the null
General procedure:
- Assume $H_{0}$ is true, so that the observations follow the distribution described by $H_{0}$
- Partition the sample space into a critical/rejection $C$ and its complement $C^c=\bar{C}$
- decide whether to reject or accept $H_{0}$ based on the data and $C/\bar{C}$

For discrete distributions, we may specify $C$ with a maximum size of test to be $\alpha$ instead of a specific value, if $C=\{X\leq 14\}:$
$$\begin{align}
\alpha & =P(X\leq 14|p=0.9) \\
 & = 1-P(X \geq 15 |p=0.9)= 0.0114 \\
\beta  & =P(X >14|p=0.6) =0.1255
\end{align}
$$
We can then alter the critical region to adjust $\alpha$ and $\beta$ : $C=\{X \leq 15\}\to \alpha=0.043, \beta=0.0509$
- the larger $C$, the larger $\alpha$, and smaller $\beta$


[[Test function]]


