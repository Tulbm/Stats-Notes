Suppose $X_{1},\dots,X_{n}$ is a set of continuous random variables with a known joint pdf $f_{X_{1},\dots X_{n}}(x_{1},\dots,x_{n})$ and
$$
Y=h(X_{1},\dots X_{n})
$$
Given that $X_{1},\dots X_{n}$ are continuous, $Y$ is continuous, we can find the pdf of $Y$ by first getting its cdf 
$$
F_{Y}(y)=P(Y\leq y)=P(h(X_{1},\dots ,X_{n})\leq y)
$$and then derivating it to get the pdf
$$
f_{Y}(y)= \frac{\partial F_{Y}(y)}{\partial y}
$$
When working with discrete variables, we usually work on the pmf directly

# Examples


Example with $U=1-e^{-x/\beta}$, $X\sim Exponential$ 
$$
x\in(0,\infty), \quad e^{-x/\beta}\in(0,1), \quad 1-e^{-x/\beta}\in(0,1)
$$
$$\begin{align}
F_{U}(u) & =P(U\leq u )  =P(1-e^{-x/\beta}\leq u) \\
 & = P(e^{-x/\beta}\geq 1-u) \\
  & =P\left( \frac{-x}{\beta}\geq \ln(1-u) \right) \\
 & =P(x \leq -\beta \ln(1-u)) \\
 & =\int_{0}^{-\beta \ln(1-u)} \frac{1}{\beta} e^{-x/\beta} dx \\
 & = \left[-e^{-x/\beta}\right|_{0}^{-\beta \ln(1-u)} \\
 & =1 - e^{- -\beta \ln(1-u)/\beta} \\
 & =1-e^{\ln(1-u)} \\
 & =1-(1-u) \\
 & =u \\
f_{U}(u) =\frac{\partial F_{U}}{\partial u} & = \frac{\partial}{\partial u} u  \\
 f_{U}(u)& =1,\quad 0<u<1
\end{align}
$$
The random variable $U$ follows a uniform distribution, in the interval $(0,1)$