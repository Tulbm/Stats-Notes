- for continuous random variables only
Suppose $X\sim f_{X}(x)$ where $f_{X}(x)$ is the pdf of $X$

Let $Y=h(X)$
# Bijective transformation
If $h(x)$ is differentiable at all values of $x$ and is either a decreasing/increasing function such that there is a unique inverse function $X=h^{-1}(Y)$, then the pdf of $Y$ is
$$
f_{y}(y)=f_{X}(h^{-1}(y))\cdot \left|  \frac{\partial h^{-1}(y)}{\partial y}\right|
$$
if $\frac{\partial h(x)}{\partial x}=0, f_{Y}(y)=0$ 
# Non-bijective transformation
If the transformation is not one-to-one, for example $Y=X^2$, we can divide the domain of the random variable $X$ into multiple non-overlapping regions. Then we find the pdf of $Y$ in each of the regions
$$
f_{Y}(y)=f_{X}(h_{1}^{-1}(y)) \left| \frac{dh_{1}^{-1}(y)}{dy}\right| + f_{x}(h_{2}^{-1}(y)) \left|\frac{|dh_{2}^{-1}(y)}{dy}\right|
$$
# Multivariable (joint) distributions
Suppose $X_{1},\dots,X_{n}$ is a set of **continuous** random variables with joint pdf $f_{X_{1},\dots,X_{n}}(x_{1},\dots,x_{n})$ and let $Y_{1}=h_{1}(X_{1},\dots,X_{n}),$ $Y_{2}=h_{2}(X_{1},\dots,X_{n}),\dots$ $Y_{n}=h_{n}(X_{1},\dots,X_{n})$ be another set of random variables. 

If the $h_{i}$ functions are differentiable with respect to each of $X_{1},\dots,X_{n}$ and and are one-to-one correspondent within the range of $X_{1},\dots,X_{n}$ for which $f_{X_{1},\dots,X_{n}}(x_{1},\dots,x_{n})\neq0$, then the joint pdf of $Y_{1},\dots,Y_{n}$ is given by
$$f_{Y_1,...,Y_n}(y_1,...,y_n)=f_{X_1,...,X_n}(g_1(y_1,...,y_n),...,g_n(y_1,...,y_n))\cdot|J|$$
where the $g_{i}$ functions are the inverse transformations

If we have less transformations ($Y$) than random variables $(X)$, we create new pointless transformations to ensure the Jacobian is a square matrix.
Then we can remove the leftover transformations from the pdf by integrating its marginal.
$$
f_{Y_{1},\dots ,Y_{r}}(y_{1},\dots,y_{r})=\int \int \int f_{Y_{1},\dots,Y_{r},\dots Y_{n}}(y_{1},\dots,y_{r},\dots,y_{n}) dy_{n-2}\,dy_{n-1} \,  dy_{n}
$$


# Examples
$X_{1},X_{2}\sim Exponential$
$$\begin{align}
  Y_{1}  &=X_{1}+X_{2},   &  X_{1}  &=Y_{2}\\ 
Y_{2}    & = X_{1},  &X_{2}   & =Y_{1}-Y_{2}
\end{align}
$$
As both random variables are independent:
$$\begin{align}
f_{X_{1},X_{2}}(x_{1},x_{2}) & = \frac{1}{\beta}e^{-x_{1}/\beta} \cdot \frac{1}{\beta}e^{-x_{2}/\beta} \\
f_{X_{1},X_{2}}(x_{1},x_{2}) & =\frac{1}{\beta^2}e^{-(x_{1}+x_{2})/\beta}
\end{align}
$$
Jacobian:
$$
|J|= \det
\begin{bmatrix}
\frac{\partial X_1 }{\partial Y_{1}} & \frac{\partial X_{1}}{\partial Y_{2}} \\
\frac{\partial X_{2}}{\partial Y_{1}} & \frac{\partial X_{2}}{\partial Y_{2}}
\end{bmatrix}=\det
\begin{bmatrix}
0 & 1 \\
1 & -1
\end{bmatrix} = |-1|=1
$$
Joint pdf of $Y_{1},Y_{2}:$
$$\begin{align}
f_{Y_{1},Y_{2}}(y_{1},y_{2}) & = f_{X_{1},X_{2}}(Y_{2},Y_{1}-Y_{2})\cdot 1\\
 & =\frac{1}{\beta^2}e^{-(y_{2}+y_{1}-y_{2})/\beta} \\
 & =\frac{1}{\beta^2}e^{-y_{1}/\beta} \quad 0\leq y_{2}\leq y_{1}
\end{align}
$$
Marginalizing:
$$\begin{align}
f_{Y_{1}}(y) & =\int_{0}^{y_{1}} \frac{1}{\beta^2}e^{-y_{1}/\beta} dy_{2} \\
 & =  \frac{1}{\beta^2}e^{-y_{1}/\beta}  \int_{0}^{y_{1}}1\,dy_{2} \\
 f_{Y_{1}}(y) & = \frac{1}{\beta^2}y_{1}e^{-y_{1}/\beta}, \quad y_{1}\geq 0
\end{align}
$$
The transformation $Y_{1}$ follows a Gamma distribution with parameters $\alpha=2, \beta =\beta$


Finding the pdf of a cdf
$$
\begin{align}
Y & =g(x)  =F_{X}(x) & 0 \leq F_{X}(x)\leq 1,\quad    0\leq y\leq1 \\
X & =h^{-1}(Y)  &  \frac{dx}{dy}=\frac{1}{\frac{dy}{dx}}=\frac{1}{\frac{dF_{X}(x)}{dx}}  & = \frac{1}{f_{X}(x)}= \frac{dh^{-1}(y)}{dy}  \\
f_{Y}(y) & =f_{X}(h^ {-1}(y)) \cdot \left|\frac{dh^{-1}(y)}{dy}\right| \\
 & =1, \quad Y=F_{X}(x) \sim unif[0,1]
\end{align}
$$
The cdf for any pdf follows a [[Uniform Distribution]]
