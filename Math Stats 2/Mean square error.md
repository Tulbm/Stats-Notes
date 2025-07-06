The mean square error of an estimator $\hat{\theta}$ of the parameter $\theta$ is given by
$$\begin{align}
MSE(\hat{\theta}) & =E[(\hat{\theta}-\theta)^2] \\
 & = E[(\hat{\theta}-E(\hat{\theta})+E(\hat{\theta})-\hat{\theta})^2] \\
 & = E[(\hat{\theta}-E(\hat{\theta})^2+ 2(\hat{\theta}-E(\hat{\theta}))(E(\hat{\theta}-\theta))+(E(\hat{\theta})-\theta)^2)] \\
 & =E((\hat{\theta}-E(\hat{\theta}))^2)+2E((\hat{\theta}-E(\hat{\theta}))(E(\hat{\theta})-\theta))+E((E(\hat{\theta}-\theta))^2) \\
 & =var(\hat{\theta})+2(E(\hat{\theta})-\theta)(E(\hat{\theta})-E(\hat{\theta}))+bias^2(\hat{\theta}) \\
 & =var(\hat{\theta})+0+bias^2(\hat{\theta}) \\
 & =var(\hat{\theta})+[E(\hat{\theta})-\theta]^2
\end{align}
$$
