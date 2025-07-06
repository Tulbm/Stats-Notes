Used to test how well a proposed model (distribution) fits the observed data. The $\chi^2$ [[Chi-Squared Test]] is often a common choice for carrying out a goodness-of-fit test

Step 1. Estimate the parameter for the assumed distribution

Step 2. Compute the probability for each observation under the assumed distribution

Step 3. Compute the expected frequencies

Step 4. Test the goodness-of-fit of the assumed distribution to the observed data
# Examples

| Number of errors | Observed frequencies $f_i$ | Poisson probability with $\lambda = 3$ | Expected frequencies $E_i$ |
|------------------|---------------------------|-----------------------------------------|----------------------------|
| 0               | 18                          |                                         |                            |
| 1               | 53                          |                                         |                            |
| 2               | 103                         |                                         |                            |
| 3               | 107                         |                                         |                            |
| 4               | 82                          |                                         |                            |
| 5               | 46                          |                                         |                            |
| 6               | 18                          |                                         |                            |
| 7               | 10                          |                                         |                            |
| 8               | 2                           |                                         |                            |
| 9               | 1                           |                                         |                            |

Step 1. Estimate the parameter for the assumed distribution
$n=440, \sum_{i}x_{i}=1341$, the number of errors observed in the sample

$$
\hat{\lambda}=\bar{x} = \frac{\sum x_{i}}{n} = \frac{1341}{440}=3.05
$$
We test
$$
H_{0}:X\sim Poisson(3) \quad vs \quad H_{a}:X \nsim Poisson(3)
$$
Could indicate that the estimate given is not good, or that the distribution doesn't fit

Step 2. Compute the probability for each observation under the assumed distribution

$$
P(x=x)=\frac{e^{- \lambda}\lambda^x}{x!} = \frac{e^{-3}3^x}{x!} \text{ under }H_{0}, \quad x= 0,\dots ,9
$$

| Number of errors | Observed frequencies $f_i$ | Poisson probability with $\lambda = 3$ | Expected frequencies $E_i$ |
| ---------------- | -------------------------- | -------------------------------------- | -------------------------- |
| 0                | 18                         | 0.0498                                 |                            |
| 1                | 53                         | 0.1494                                 |                            |
| 2                | 103                        | 0.2240                                 |                            |
| 3                | 107                        | 0.1680                                 |                            |
| 4                | 82                         | 0.1008                                 |                            |
| 5                | 46                         | 0.0504                                 |                            |
| 6                | 18                         | 0.0216                                 |                            |
| 7                | 10                         | 0.0081                                 |                            |
| 8                | 2                          | 0.0081                                 |                            |
| 9                | 1                          | 0.0038                                 |                            |

Step 3. Compute the expected frequencies

Let $E_{ij}$ be the expected # of observations that make $j$ errors among 440 observations

| Number of errors | Observed frequencies $f_i$ | Poisson probability with $\lambda = 3$ | Expected frequencies $E_i$ |
| ---------------- | -------------------------- | -------------------------------------- | -------------------------- |
| 0                | 18                         | 0.0498                                 | 21.9                       |
| 1                | 53                         | 0.1494                                 | 65.7                       |
| 2                | 103                        | 0.2240                                 | 98.6                       |
| 3                | 107                        | 0.1680                                 | 98.6                       |
| 4                | 82                         | 0.1008                                 | 73.9                       |
| 5                | 46                         | 0.0504                                 | 44.4                       |
| 6                | 18                         | 0.0216                                 | 22.2                       |
| 7                | 10                         | 0.0081                                 | 9.5                        |
| 8                | 2                          | 0.0081                                 | 3.6                        |
| 9                | 1                          | 0.0038                                 | 1.7                        |
| 10               | 0                          |                                        |                            |
| ...              |                            |                                        |                            |

- based on the fischer exact test (?), the [[Chi-Squared Test]] will become less accurate for values $<5$, we can group all those groups together

 Step 4.de
 Test the goodness-of-fit of the Poisson distribution to the observed data
$$
H_{0}:X\sim Poisson (3) \quad vs\quad H_{a}: X\nsim Poisson(3)
$$
under $H_{0}:$
$$\begin{align}
\chi^ 2 &  =  \sum_{i=0}^ 8 \frac{(f_{i}-E_{i})^2}{E_{i}} \sim \chi_{m-t-1}^2 = \chi_{7}^2 
\end{align}
$$
$df =$ number of groups - number of unknown parameters

Reject $H_{0}$ if
$$\begin{align}
\chi_{obs}^2  & \geq \chi_{7,0.95}^2 = 14.067 \\
\chi_{obs}^2 =6.83 & \geq  14.067
\end{align}
$$
