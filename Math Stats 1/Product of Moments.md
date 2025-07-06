The *rth* and *sth* product of [[Moments]] about the means on the random variables $X$ and $Y$ ($\mu_{r,s}$) is
$$
\begin{align}
\mu_{r,s} & =E[(X-\mu_{X})^r(Y-\mu_{Y})] \\
 & =\sum_{x}\sum_{y}(x-\mu_{X})^r(y-\mu_{Y})^s\cdot f_{X,Y}(x,y) \\ \\
 & \text{ or for continuous:} \\ \\
\mu_{r,s} & =\int_{-\infty}^\infty \int_{-\infty}^\infty(x-\mu_{x})^r(y-\mu_{y})^s\cdot f_{X,Y}(x,y)\,dx\,dy \\
 & (r,s)\in N^2
\end{align}
$$

When $r=s=1, \mu_{1,1}=E[(X-\mu_{X})(Y-\mu_{Y})]$ is the [[Covariance]] of $X$ and $Y$, $cov(X,Y)$ or $\sigma_{XY}$

The *rth* and *sth* product of moment (about the origin) of the random variables $X$ and $Y$ ($\mu'_{r,s}$) is
$$
\begin{align}
\mu_{r,s}' & =  \sum_x\sum_yx^ry^s\cdot f_{X,Y}(x,y)=E[X^rY^s] \\ \\

 & \text{or for continuous:} \\ \\

\mu_{r,s}' & =\int_{-\infty}^\infty\int_{-\infty}^\infty x^ry^s\cdot f_{X,Y}(x,y)dxdy \\
  &  (r,s)  \in N^2
\end{align}
$$
- $\mu'_{1,0}=E(X^1Y^0)=E(X)=\mu_{X}$
- $\mu'_{0,1}=E(X^0Y^1)=E(Y)=\mu_{Y}$
- $\mu'_{1,1}=E(X^1Y^1)=E(XY)=\mu_{XY}$

If $X$ and $Y$ are [[Independency|independent]]:
- $E(XY)=E(X)E(Y)$
- $cov(X,Y)=\sigma_{XY}=0$
- $Var(X+Y)=var(X)+var(Y)$, as the $2cov(X,Y)$ term $=0$




