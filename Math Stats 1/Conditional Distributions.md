
$$
\begin{align}
f_{X|Y}(x|y)  =P(A|B) & =\frac{P(A\cap B)}{P(B)} \\
   & =\frac{P(X=x,Y=y)}{P(Y=y)} \\
   f_{X|Y}(x|y)& =\frac{f_{X,Y}(x,y)}{f_{Y}(y)}
\end{align}
$$
And:
$$
f_{Y|X}(y|x)=\frac{f_{X,Y}(x,y)}{f_{X}(x)}
$$

- $f_{X,Y}(x,y)$ is the [[Multivariable Distributions|joint pmf/pdf]] of $X$ and $Y$
- $f_{Y}(y)$ is the [[Marginal Distributions|marginal distribution]] of  $Y$
- $f_{X}(x)$ is the marginal distribution of $X$

$$
f(x,y)=\frac{\partial F(x)}{\partial x} \frac{\partial F(y)}{\partial y}
$$
# [[Independency]]

If $X$ and $Y$ are independent:

$$
\begin{align}
f_{X,Y}=
\end{align}
$$
# Conditional Cumulative Distribution Functions
The conditional cumulative distributions of $X$ given $y$ 
$$
\begin{align}
F_{X|Y}(x|y) & =P(X\leq x|Y=y) \\
 & =\begin{cases}
\sum_{t\leq x}f_{X|Y}(t|y) \, \,\,\, \,\,\,\, \,  \text{ discrete case} \\
\int_{-\infty}^xf_{X|Y}(t|y)dt \, \, \, \, \,\,\, \text{ continuous case}
\end{cases}
\end{align}
$$

