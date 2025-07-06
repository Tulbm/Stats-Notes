
# Chi-squared test
$$\begin{align}
\pi_{ij} & = P(j^{ th}\text{ outcome and in population }i) \\
 & = P(\text{a sample is from population }i \text{ and expresses }j^{th} \text{ outcome}) \\
 & =\pi _{i.} \pi_{. j}
\end{align}
$$
Where
- $\pi_{i.}$'s are the population/rows outcomes and  $\sum \pi_{i.}=1$
- $\pi_{j.}$'s are the choices/columns outcomes and $\sum \pi_{. j}=1$

To test the independence between them (rows x columns):
$$
H_{0}:\pi_{ij}=\pi_{i .}\pi_{. j},\, \forall i,j \quad vs \quad H_{a}: \exists i,j  \text{ s.t. }\pi_{ij}\neq \pi_{i .}\pi_{.j} 
$$

under $H_{0}:$
$$
\begin{align}
\hat{\pi}_{ij}  & = \hat{\pi}_{i\cdot} \hat{\pi}_{\cdot j} \\
 & =\frac{n_{i\cdot}}{n} \cdot \frac{n_{\cdot j}}{n} \\
\end{align}
$$


We reject $H_{0}$ if
$$
\chi_{obs}^2 = \sum_{i} \sum_{j}\frac{(f_{ij}-E_{ij})^2}{E_{ij}}  > \chi_{df,1-\alpha}^2
$$
- $E_{ij}=n\hat{\pi}_{ij}=n \hat{\pi}_{i\cdot}\hat{\pi}_{\cdot j}$ 
- $df=$ number of parameters under $H_{a}$ - number of parameters under $H_{0}$
