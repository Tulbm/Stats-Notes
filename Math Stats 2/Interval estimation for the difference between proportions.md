


# Examples
$X\sim Bin(n,p_{1}), Y\sim Bin(m,p_{2}),$ assume $n,m \geq 25$ to apply [[Central Limit Theorem]]
$$
\begin{align}
 & \hat{p}_{1}= \frac{x}{n}, \hat{p}_{2} = \frac{y}{m}, \quad \hat{p}_{1}-\hat{p}_{2}= \frac{x}{n} - \frac{y}{m} \\
 & E(\hat{p}_{1}-\hat{p}_{2}) = E\left(  \frac{x}{n}- \frac{y}{m} \right) = \frac{np_{1}}{n}- \frac{mp_{2}}{m}=p_{1}-p_{2}  \\
 & Var(\hat{p}_{1}-\hat{p}_{2}) = Var(\hat{p}_{1})+Var(\hat{p}_{2}) = Var\left( \frac{x}{n} \right) + Var\left( \frac{y}{m} \right) \\
  &  =\frac{np_{1}(1-p_{1})}{n^2} + \frac{mp_{2}(1-p_{2})}{m^2}= \frac{p_{1}(1-p_{1})}{n}+ \frac{p_{2}(1-p_{2})}{m} \\
Z & = \frac{\hat{p}_{1}-\hat{p}_{2}-E(\hat{p}_{1}-\hat{p}_{2})}{\sqrt{ V\hat{a}r(\hat{p}_{1}-\hat{p}_{2}) }} = \frac{\hat{p}_{1}-\hat{p}_{2}-(p_{1}-p_{2})}{\sqrt{ \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n} +\frac{\hat{p}_{2}(1-\hat{p}_{2})}{m}}} \sim N(0,1) \text{ approx} \\
 & D= p_{1}-p_{2} , P(D_{l}\leq D \leq D_{u}) = 1-\alpha \dots \\
 & \text{CI for }D: \\
 & \left( \hat{p}_{1}-\hat{p}_{2}-Z_{1 - \frac{\alpha}{2}}\sqrt{  \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n} }+ \frac{\hat{p}_{2}(1-\hat{p}_{2})}{m}, \hat{p}_{1}-\hat{p}_{2}+Z_{1 - \frac{\alpha}{2}}\sqrt{  \frac{\hat{p}_{1}(1-\hat{p}_{1})}{n} }+ \frac{\hat{p}_{2}(1-\hat{p}_{2})}{m} \right)
\end{align}
$$
