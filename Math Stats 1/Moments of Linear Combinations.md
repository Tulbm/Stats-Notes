If we have more than two random variables, $X_{1},X_{2},\dots,X_{n}$, for constants $a$:
$$
E\left( \sum_{i=1}^n a_{i}X_{i} \right) = \sum_{i=1}^na_{i}E(X_{i})
$$
$E(X+4Y+2Z)=E(X)+4E(Y)+2E(Z)$

$$
var\left( \sum_{i=1}^na_{i}X_{i} \right)=\sum_{i=1}^na_{i}^2var(X_{i})+ 2\sum_{i= 1}^{n-1}\sum_{j=i+1}^na_{i}a_{j}\cdot cov(X_{i}X_{j})
$$
$Var(X+4Y+2Z)=Var(X)+16Var(Y)+4Var(Y)+2(1)(4)cov(X,Y)+\\2(1)(2)cov(X,Z)+2(4)(2)cov(Y,Z)$
# Covariances of Linear Combinations
If
$$
Y_{1}=\sum_{i=1}^na_{i}X_{i} \quad \quad \text{and }\quad \quad Y_{2}=\sum_{i=1}^nb_{i}X_{i}
$$
then
$$
cov(Y_{1},Y_{2})=\sum_{i=1}^na_{i}b_{i}\cdot Var(X_{i}) + \sum_{i=1}^{n-1} \sum_{j=i+1}^{n}(a_{i}b_{j}+a_{j}b_{i})\cdot cov(X_{i},X_{j})
$$
$$
\begin{align}
cov(X+4Y+2Z,3X-Y-Z)  =  &(1)(3)Var(X)+4(-1)Var(Y)+2(-1)Var(Z)+ \\
   & + [(1)(-1)cov(X,Y)+4(3)cov(X,Y)]+ \\
 & +[(1)(-1)cov(X,Y)+(2)(3)cov(X,Z)]+ \\
  & + [4(-1)cov(Y,Z)+2(-1)cov(Y,Z)]
\end{align}
$$

