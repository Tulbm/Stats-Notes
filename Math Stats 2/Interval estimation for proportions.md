# Interval estimation for proportions
To estimate proportions, percentiles or rates we assume we sample from a binomial distribution with size of $n$ with probability $p$ of the event



## Examples
$X\sim Bin(n,p)$, find $95\% \,CI$ for $p$
$$
\begin{align}
 & X = \sum Y_{i}, \quad Y_{1},\dots,Y_{n}\sim Bernoulli(p)\equiv Bin(1,p) \\
 & E(X)=np, \quad Var(X)=np(1-p), \quad n\text{ iis the sample size} \\
 & \text{ For a large sample size }(n\geq 25), \text{ we apply CLT} \\
 & \bar{y}= \frac{x}{n}= \sum \frac{y_{i}}{n}=\hat{p}, \quad Var(\hat{y})=\frac{Var(y)}{n}=\frac{p(1-p)}{n} \\
 & Z= \frac{\hat{y}-p}{\sqrt{ Var(\hat{y}) }}= \frac{\hat{p}-p}{\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }}\sim N(0,1) \\
 & P(p_{l}\leq p \leq p_{u}) = 1-\alpha \\
 & P\left( \frac{\hat{p}-p_{u}}{\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }}  \leq \frac{\hat{p}-p}{\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }} \leq \frac{\hat{p}-p_{l}}{\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }} \right) = 1-\alpha \\ 
& P\left( -Z_{1-\alpha /2}  \leq \frac{\hat{p}-p}{\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }} \leq \frac{\hat{p}-p_{l}}{\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }} \right) = 1-\alpha \\
 & CI \text{ for p is }(\hat{p}-) 
\end{align}
$$

$$
\begin{align} & X = \sum Y_{i}, \quad Y_{1},\dots,Y_{n}\sim Bernoulli(p)\equiv Bin(1,p) \\ & E(X)=np, \quad Var(X)=np(1-p), \quad n\text{ is the sample size} \\ & \text{For a large sample size }(n\geq 25), \text{ we apply the Central Limit Theorem (CLT)} \\ & \bar{Y}= \frac{X}{n}= \sum \frac{Y_{i}}{n}=\hat{p}, \quad Var(\bar{Y})=\frac{Var(Y)}{n}=\frac{p(1-p)}{n} \\ & Z= \frac{\hat{p}-p}{\sqrt{Var(\hat{p})}}= \frac{\hat{p}-p}{\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}}\sim N(0,1) \\ & P(p_{l}\leq p \leq p_{u}) = 1-\alpha \\ & P\left( \frac{\hat{p}-p_{u}}{\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}} \leq \frac{\hat{p}-p}{\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}} \leq \frac{\hat{p}-p_{l}}{\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}} \right) = 1-\alpha \\ & P\left( -Z_{1-\alpha /2} \leq \frac{\hat{p}-p}{\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}} \leq Z_{1-\alpha /2} \right) = 1-\alpha \\ & CI \text{ for } p \text{ is } \left(\hat{p} - Z_{1-\alpha/2}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}, \hat{p} + Z_{1-\alpha/2}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}\right) \end{align}
$$

$$
\begin{align}
 &P(p_{l}\leq p \leq p_{u})= P\left( \frac{\hat{p}-p_{u}}{\sqrt{ \frac{p(1-p)}{nN} }} \leq \frac{\hat{p}-p}{\sqrt{ \frac{p(1-p)}{nN} }} \leq \frac{\hat{p}-p_{l}}{\sqrt{ \frac{p(1-p)}{nN} }} \right) \\
 & CI \text{ for }p: \left( \hat{p}-Z_{1- \frac{\alpha}{2}} \sqrt{  \frac{\hat{p}(1-\hat{p})}{nN} }, \hat{p}+Z_{1- \frac{\alpha}{2}} \sqrt{  \frac{\hat{p}(1-\hat{p})}{nN} } \right)
\end{align}
$$
