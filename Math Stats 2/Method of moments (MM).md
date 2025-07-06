Also called the substitution method

The rth sample moment is
$$
m_{r}' =  \frac{\sum x_{i}^r}m{}
$$
If we have $k$ parameters in the population distribution, we need $k$ equations to solve for the $k$ unknown parameters

1 parameter, Exponential($\theta$)
$$
E(X)=\theta=\bar{X}\longrightarrow \hat{\theta}=\bar{X}
$$
2 parameters, $E(X)=g_{1}(\theta_{1},\theta_{2}), E(X^ 2)=g_{2}(\theta_{1},\theta_{2})$
$$
\begin{align}
E(X) & =\bar{X}=g_{1}(\theta_{1},\theta_{2})  &  \longrightarrow  &  & \hat{\theta}_{1}  =h_{1}(\bar{X},\bar{X^ 2}) \\
E(X^ 2) & =\bar{X^ 2}=g_{2}(\theta_{1},\theta_{2})  & \longrightarrow & & \theta_{2} = h_{2}(\bar{X},\bar{X^ 2}) 
\end{align}
$$
We can also use the variance rather than the second moment
$$
S_{0}^ 2= \frac{1}{n} \sum_{i=1}^ n (X_{i}-\bar{X})^ 2
$$
For a $\Gamma(\alpha,\beta)$
$$
\begin{align}
E(X) & =\alpha \beta, &  var(X) & =\alpha \beta^ 2  \\
\hat{\beta} & =\frac{S_{0}^2}{\bar{X}} & \hat{\alpha} & =\frac{\bar{X}}{\hat{\beta}}=\frac{(\bar{X})^2}{S_{0}^ 2}
\end{align}
$$
Using moments does not guarantee unbiasedness, seen as we used the second central moment $S_{0}^ 2$ instead of the sample variance $S_{1}^ 2$ to find the estimators


