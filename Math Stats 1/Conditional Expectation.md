If $f_{X|Y}(x|y)$ is the conditional probability distribution/density function of $X$ given $Y=y$ at $x$, the conditional expectation of $g(X)$ given $Y=y$ is
$$
\begin{align} 
E[g(X)|Y=y] & =\sum_{x}g(x)f_{X|Y}(x|y) \\
 &  \text{ or if continuous:} \\
E[g(X)|Y=y] & =\int_{-\infty}^\infty g(x)f_{X|Y}(x|y) 
\end{align}
$$

Letting $g(X)=X$, the conditional mean of $X$ given $Y=y$ is 
$$\begin{align}
E(X|Y=y)  & = \sum_{x}xf_{X|Y}(x|y) \\
 E(X|Y=y) & = \int_{-\infty}^\infty xf_{X|Y}(x|y)dx
\end{align}
$$
and the second [[Moments|moment]]:
$$\begin{align}
E(X^2|Y=y) & =\sum_{x}x^2f_{X|Y}(x|y) \\
E(X^2|Y=y) & =\int_{-\infty}^\infty x^2f_{X|Y} \,dx
\end{align}
$$
The conditional variance of $X$ given $Y=y$ is 
$$
Var(X|Y=y)=E(X^2|Y=y)-[E(X|Y=y)]^2
$$
