Two events are independent if and only if
$$
\begin{align}
P(A|B)=P(A) &  &  &  & P(B|A)=P(B)
\end{align}
$$
If $X$ and $Y$ are independent:
$$
\begin{align}
  f(x,y) & = P(X=x,Y=y) \\
 & =P(X=x)P(Y=y)  \\
 f(x,y)& =f_{X}(x)f_{Y}(y) \, \, \, \,\ \forall \text{(x,y)  }
\end{align}
$$
[[Multi-variable Functions|Joint probability]] is equal to the product of the [[Marginal Distributions]]

$$
\begin{align}
F(x,y) & =P(X\leq x,Y\leq y) \\
 & =P(X\leq x)P(Y\leq y) \\
 & =F_{X}(x)F_{Y}(y) \, \, \, \, \, \, \, \, \, \,\forall \text{  (x,y)}
\end{align}
$$
[[Multi-variable Functions|Joint cumulative probability]] is equal to the product of the [[Marginal Distributions]]

If $\exists x_{0},y_{0}$ such that $f_{X,Y}(x_{0},y_{0})\neq f_{X}(x_{0})f_{Y}(y_{0})$ then $X$ and $Y$ are not independent
# Discrete
For $n$ discrete random variables $X_{1},X_{2},\dots ,X_{n}$ with a joint probability distribution $f(x_{1},x_{2},\dots,x_{n})$ and marginals distributions $f_{X_{i}}(x_{i})$:
$$
f_{X}(x_{1},x_{2},\dots x_{n})=f_{X_{1}}(x_{1})\cdot f_{X_{2}}(x_{2})\dots f_{X_{n}}(x_{n}) \, \, \, \,\forall(x_{1},x_{2},\dots,x_{n})
$$
if and only if the $n$ random variables are independent

Three of more random variables can still be pairwise independent without being completely independent among all of them

$$
\text{Total independency} \Longrightarrow \text{pairwise independency}
$$
$$
f_{X,Y,Z}(x,y,z)=f_{X}(x)f_{Y}(y)f_{Z}(z)\Longrightarrow {\begin{cases}
f_{X,Y}=f_{X}(x)f_{Y}(y) \\
f_{X,Z}=f_{X}(x)f_{Z}(z)\\
f_{Y,Z}=f_{Y}(y)f_{Z}(z)
\end{cases}}
$$
# Continuous
For $n$ continuous random variables $X_{1},X_{2},\dots ,X_{n}$ with a joint probability densities $f(x_{1},x_{2},\dots,x_{n})$ and marginals densities $f_{X_{i}}(x_{i})$:
$$
f_{X}(x_{1},x_{2},\dots x_{n})=f_{X_{1}}(x_{1})\cdot f_{X_{2}}(x_{2})\dots f_{X_{n}}(x_{n}) \, \, \, \,\forall(x_{1},x_{2},\dots,x_{n})
$$
if and only if the $n$ random variables are independent

The cdfs can be used instead to determine the dependency of the variables
$$
\begin{align}
f(x,y)  & = f_{X}(x)f_{Y}(y) \\
F(x,y) & =F_{X}(x)F_{Y}(y)
\end{align}
$$
# Measures
- $E(XY)=E(X)E(Y)$
- $Var(X+Y)=var(X)+var(Y)$
- $cov(X,Y)=\sigma_{XY}=0$