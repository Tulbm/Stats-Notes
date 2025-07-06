the chi-squared test of a single proportion is the square of the z-test

# 2 choices
[[Binomial Distribution]]
$$
H_{0}: \theta_{1} = \theta_{2} = \dots = \theta_{k} = (\theta_{0}) \text{ vs }H_{a}: \exists i \neq j, \theta i \neq \theta_{j}
$$
If the $n_{i}$ are sufficiently large for each population, we construct $k$ independent test statistics
$$
E(X_{i})=n_{i}\theta_{i}, \quad Var(X_{i})=n_{i}\theta_{i}(1-\theta_{i})
$$
By CLT:
$$\begin{align}
Z_{i} & = \frac{x_{i}-n_{i}\theta_{i}}{\sqrt{ n_{i}\theta_{i}(1-\theta_{i}) }} \overset{\text{approx}}{\sim} N(0,1) \\
\sum_{i=1}^K Z_{i}^2  &  \sim \chi_{k}^2 = \sum\left( \frac{x_{i}-n_{i}\theta_{i}}{\sqrt{ n_{i}\theta_{i}(1-\theta_{i}) }}  \right)^2\\
\end{align}
$$
Reject $H_{0}$ if (fix, 130,131) 
$$
\chi_{obs}^2 = \sum  \frac{(x_{i}-n_{i}\theta_{i})^2}{ n_{i}\theta_{i}(1-\theta_{i}) }  \geq \chi_{k, 1- \alpha}^2
$$


When $\theta_{0}$ is not given (testing only if they are not the same), we need to estimate it first
$$\begin{align}
\hat{\theta}_{0}  & = \frac{\sum x_{i}}{\sum n_{i}} \\
\chi^2  & = \sum  \frac{(x_{i}-n_{i}\theta_{i})^2}{ n_{i}\theta_{i}(1-\theta_{i}) } \sim \chi_{k-1}^2
\end{align}
$$


$X_{1},\dots,X_{k}$ observations from $k$ independent trials of size $n_{1},\dots ,n_{k}$ 

|            | successes | failures    |
| ---------- | --------- | ----------- |
| sample 1   | $x_1$     | $n_1 - x_1$ |
| sample 2   | $x_2$     | $n_2 - x_2$ |
| $\vdots$   | $\vdots$  | $\vdots$    |
| sample $k$ | $x_k$     | $n_k - x_k$ |
Let $f_{ij}$ be the observed frequency in the $i$th row and $j$th column
Under the hypothesis that $\theta_{1}=\theta_{2}=\dots=\theta_{k}=\theta_{0}$, the expected cell frequencies $E_{ij}$'s are given by
$$
E(X_{i1})=n_{i}\theta_{0}=E_{i1}, \quad E(X_{i_{2}})=n_{i}(1-\theta_{0}) =E_{i 2}
$$

$$
\begin{align}
\chi^ 2 &  = \sum_{i=1}^ k \sum_{j=1}^ 2 \frac{(f_{ij}-E_{ij})^2}{E_{ij}}  \quad\text{ easier formula}\\
 & = \sum_{i=1}^ k \left[ \frac{(x_{i}-n_{i}\theta_{0})^2}{n_{i}\theta_{0}} + \frac{(n_{i}-x_{i}-n_{i}(1-\theta_{0}))^2}{n_{i}(1-\theta_{0})} \right]   \\
 & = \sum_{i}^k \left[  \frac{(x_{i}-n_{i}\theta_{0})^2(1-\theta_{0})+(n_{i}-x_{i}-n_{i}+n_{i}\theta_{0})^ 2\theta_{0}}{n_{i}\theta_{0}(1-\theta_{0})} \right]  \\
 & = \sum_{i=1}^ k \left[  \frac{(x_{i}-n_{i}\theta_{0})^2(1-\theta_{0})+(x_{i}-n_{i}\theta_{0})^ 2\theta_{0}}{n_{i}\theta_{0}(1-\theta_{0})} \right]  \\
\chi^ 2 & =\sum_{i=1}^ k \frac{(x_{i}-n_{i}\theta_{0})^2}{n_{i}\theta_{0}(1-\theta_{0})} \quad \text{actual definition}
\end{align}
$$
when $\theta_{0}$ is given or specified, $\chi^ 2\sim \chi^2_{k}$ under $H_{0}$
when $\theta_{0}$ is not given, $\hat{\theta}= \frac{\sum x_{i}}{\sum n_{i}}$ to compute $E_{ij}$'s, then $\chi^ 2\sim \chi_{-1}^ 2$ under $H_{0}$

# With more than 2 choices
If instead of success and failure we have multiple choices, a [[Multinomial Distribution]] instead

|            | choice 1 | choice 2 | choice 3 |
| ---------- | -------- | -------- | -------- |
| sample 1   | $x_1$    | $y_{1}$  | $z_{1}$  |
| sample 2   | $x_2$    | $y_{2}$  | $z_{2}$  |
| $\vdots$   | $\vdots$ | $\vdots$ |          |
| sample $k$ | $x_k$    | $y_{k}$  | $z_{k}$  |

- $x_{i.}+y_{i.}+z_{i.}+\dots=n_{i.}$ (row total)
- $x_{.j}+y_{.j}+z_{.j}+\dots=n_{j}$ (column total)

# Not testing the rows

 $(X_{i},Y_{i},Z_{i})\sim \text{Multinomial}(n_{i},(\theta_{i1},\theta_{i 2},(1-\theta_{i 1}-\theta_{i 2})))$ (last term not estimated)

$H_{0}:$ all $\theta_{i 1}$'s are equal, all $\theta_{i_{2}}$'s are equal, ...
$H_{a}:$ not all $\theta_{i 1}$'s are equal or not all $\theta_{i_{2}}$'s are equal or ...

Under the $H_{0}:  \theta_{i 1}= \theta_{1},\dots,\theta_{i j-1}= \theta_{j-1}$, where $\theta_{j}$'s are not specified: (the last column has no freedom)
$$\begin{align}
\hat{\theta}_{j}  & = \frac{\sum f_{ij}}{\sum n_{i}} \\
\chi^ 2  & = \sum_{i}\sum_{j} \frac{(f_{ij}-E_{ij})^2}{E_{ij}} \sim \chi_{df}^ 2 \\
df & =(k-1)(c-1)= \# H_{a}'\text{s parameters} - \# H_{0}'\text{s parameters} = i(j-1) - (j-1)
\end{align}
$$
Reject $H_{0}$ if 
$$
\huge \chi_{obs}^ 2 > \chi^2_{df,1-\alpha}
$$

# Testing rows

$\sum_{j} \theta_{ij}=1$,  $\sum_{j}X_{ij}=n_{i.}$

For each population $i$
$$
\begin{align}
(X_{i1},X_{i 2},X_{i 3})  & \sim \text{Multinomial}(n_{i.}, (\theta_{i 1}, \theta_{i 2}, 1- \theta_{i 1}- \theta_{i 2})) \\
\equiv (X_{i1},X_{i 2})  & \sim \text{Multinomial}(n_{i.}, (\theta_{i 1}, \theta_{i 2})  \\
P(X_{i1}=x_{i 1}, X_{i 2}= x_{i 2}) & =\frac{n_{i.}!}{x_{i 1}!x_{i 2}! (n_{i .}-x_{i 1}-x_{i 2})!}\theta
\end{align}
$$

Testing if $\theta_{i 1}$'s  and $\theta_{i 2}$'s are equal 
$$\begin{align}
H_{0} & : \forall i\quad     &  &  \theta_{i 1} = \theta_{ 1}, \theta_{i 2}=\theta_{2},\dots \\
H_{a} & :  \forall i  &  & \theta_{i 1}  \neq \theta_{ 1}, \text{or } \theta_{i2} \neq \theta_{ 2}
\end{align}
$$
When $\theta_{j}$'s are given, the $df=k(c-1)$

Reject $H_{0}$ if
$$
\chi_{obs}^2 = \sum_{i} \sum_{j}\frac{(f_{ij}-E_{ij})^2}{E_{ij}}  > \chi_{df,1-\alpha}^2
$$

[[Association Test]] between the rows and columns if we want to determine their independency


