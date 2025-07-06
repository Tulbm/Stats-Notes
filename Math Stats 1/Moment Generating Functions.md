$$
\begin{align}
M_{X}(t)=E(e^{ tX})=\sum_{x}e^{ tx}f(x)\quad \quad  & \text{discrete} \\
M_{X}(t)=E(e^{ tX})=\int_{-\infty}^\infty e^{ tx}f(x)\,dx\quad \quad  & \text{continuous} \\
\end{align}
$$
The function can be used to find an specific moment:
$$
\mu_{r}'=E(X^r)=\left. \frac{d^rM_{X}(t)}{dt^r} \right|_{t=0}
$$
as we want to evaluate at $t=0$, we handle the function considering t to be a very small value, $t\in(-\delta,\delta)$

Using the series expansion for $e^{tx}$ we arrive at a form for the function that resembles a [[Taylor Series]]
$$
m(t)=1+t\mu_{1}'+ \frac{t^2}{2!}\mu_{2}'+ \frac{t^3}{3!}\mu_{3}'+\dots
$$
Derivating removes the unwanted terms from the left, evaluating at $t=0$ eliminates everything from the right

If $a$ and $b$ are constants:
$$
\begin{align}
1. &\quad  M_{X+a}(t)=E[e^{(X+a)t}]=e^{at}\cdot M_{X}(t) \\
2. &\quad M_{bX}(t)=E[e^{bXt}]=M_{X}(bt) \\
3. &\quad M_{\frac{X+a}{b}}(t)=E\left[ e^\left( \frac{x+a}{b} \right)t \right] =E\left[ e^{\frac{a}{b}t} \right]M_{X}\left( \frac{t}{b} \right) 
\end{align}
$$
The problem with MGFs is that they don't always exist
- sum/integral may not converge for the expectation
In that case, the characteristic function
$$
\varphi_{X}(t)= E(e^{itX}), \quad i=\sqrt{ -1 }
$$
always exists for any distribution
# Properties

If $X$ and $Y$ have the same MGF $\to$ they must have the same pdf 

1. Suppose $X\sim f(x)$, if $M_{X}(t)$ exists then $M_{X}(t)$ and $f(x)$ have a one-to-one correspondence

2. Suppose $X$ and $Y$ are two random variables such that
$$\begin{align}
M_{X}  (t) & \longrightarrow M_{Y}(t) \\
  & \text{ then} \\
f_{X} (x) & \longrightarrow f_{Y}(y)  \quad \forall x ,\forall y
\end{align}
$$

If $Y=aX+b$ then
$$
M_{Y}(t)=e^{bt} M_{X}(at)
$$

If $X$ and $Y$ are independent then
$$
M_{X+Y}(t)=M_{X}(t)M_{Y}(t)
$$

# [[Binomial Distribution]]
$X\sim binom(n,p)$
$$\begin{align}
M_{X}(t)=E(e^{ xt}) & =\sum e^{xt}f(x) \\
 & = \sum_{x=0}^ne^{xt}{n\choose x}p^x(1-p)^{ n-x} \\
 & =\sum_{x=0}^n{n\choose x} (e^tp)^x(1-p)^{ n-x} \quad \text{(binomial expansion)}\\ 
 & =[e^tp+(1-p)]^n = [1+p(e^t-1)]^n
\end{align}
$$

# Factorial 
$$
FM_{X}(t)=E(t^X)= \sum_{x}t^xf(x)
$$
rth factorial [[Moments|moment]] 
$$
\mu'_{(r)}=E[X(X-1)(X-2)\dots(X-r+1)] = \left.\frac{d^r}{dt^r}  FM_{X}(t) \right|_{t=1}
$$

# [[Poisson Distribution]]
$$\begin{align}M_{X}(t)=E(e^{xt}) & =\sum_{x=0}^\infty e^{ xt} \frac{e^{-\lambda}\lambda^x}{x!} \\
 e^{e^t\lambda}\text{ is a constant} \quad \quad& =e^{-\lambda} e^{e^t\lambda} \sum_{x=0}^\infty \frac{e^{ -e^t\lambda}(e^t\lambda)^x}{x!}  \\
 & =e^{-\lambda}e^{e^t\lambda} \cdot 1 \quad \text{(pmf of poisson)} \\
 & =e^{\lambda(e^t-1)}
\end{align}

$$
# [[Gamma Distribution]]
$$
\begin{align}
M_{X}(t)=E(e^{tX}) & =\int_{-\infty}^\infty e^{tx}\frac{1}{\beta^\alpha \Gamma(\alpha)} x^{\alpha-1}e^{ -x/\beta}dx \\
 & =\frac{1}{\beta^\alpha\Gamma(\alpha)}\int_{0}^\infty e^{tx-x/\beta}x^{\alpha-1}dx\left. \right|_{t=0}\\
& =\frac{1}{\beta^\alpha\Gamma(\alpha)}\int_{0}^\infty e^{-x(1/\beta-t)}x^{\alpha-1}dx \quad \left( u=x\left( \frac{1}{\beta}-t \right) \right)\\ 
 & =\frac{1}{\beta^\alpha\Gamma(\alpha)}\int_{0}^\infty e^{ -u}\left( \frac{u}{\frac{1}{\beta}-t} \right)^{\alpha-1} \frac{du}{\frac{1}{\beta}-t} \quad \left( x=\frac{u}{\frac{1}{\beta}-t}, dx = \frac{du}{\left( \frac{1}{\beta}-t \right)} \right) \\
 & =\frac{1}{\beta^\alpha \Gamma(\alpha)}\left( \frac{1}{\frac{1}{\beta}-t} \right)^\alpha \int_{0}^\infty e^{-u}u^{\alpha-1}du \\
 & =\left( \frac{1}{\beta}-t \right)^{-\alpha} \frac{1}{\beta^\alpha \Gamma(\alpha)}\Gamma(\alpha) \\
 & =\left( \left( \frac{1}{\beta}-t \right)\beta \right)^{-\alpha} \\
 M_{X}(t)& =(1-t\beta){^{ -\alpha}} \\
\end{align}
$$
# [[Exponential Distribution]]
$$
\begin{align}
M_{X}(t)=E(e^{tX}) & =\int_{0}^\infty e^{tx} \frac{1}{\lambda}e^{-x/\lambda}dx \\
 & =\frac{1}{\lambda} \int_{0} ^\infty e^{-(1/\lambda-t)x}dx \\
 & =\frac{1}{\lambda} \frac{1}{\frac{1}{\lambda}-t}\int_{0}^\infty \left( \frac{1}{\lambda}-t \right)e^{-(1/\lambda-t)x}dx \\
 & =\frac{1}{1-\lambda t} \cdot 1 \quad \quad \text{(pdf of }\exp(0) )
\end{align}
$$
