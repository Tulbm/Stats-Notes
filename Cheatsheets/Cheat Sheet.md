**Discrete** 
$$
F(x,y)=P(X\leq x,Y\leq y)=\sum_{s\leq x}\sum_{t\leq y}f(s,t)\ \ \ \ \text{ for }x,y\in R
$$
Marginals
- $f_{X}(x)=P(x=x)=\sum _yf(x,y),f_{Y}(y)=P(Y=y)=\sum_{x}f(x,y)$
For $n$ discrete random variables $X_{1},X_{2},\dots ,X_{n}$ with a joint probability distribution $f(x_{1},x_{2},\dots,x_{n})$ and marginals distributions $f_{X_{i}}(x_{i})$:
$$
f_{X}(x_{1},x_{2},\dots x_{n})=f_{X_{1}}(x_{1})\cdot f_{X_{2}}(x_{2})\dots f_{X_{n}}(x_{n}) \, \, \, \,\forall(x_{1},x_{2},\dots,x_{n})
$$
if and only if the $n$ random variables are independent
**uniform**
$$
f(x)=\frac{1}{k},\quad \mu=\frac{n+1}{2}, \quad \sigma^2 = \frac{n^2-1}{12}
$$
**Bernoulli**
$$
f(x)=p^x(1-p)^{ 1-x}, \quad \mu=p, \quad \sigma^2 = p(1-p) 
$$
**binomial**
$$
f(x)={n\choose x}p^x(1-p)^{n-x},\quad \mu = np,\quad \sigma^2=np(1-p),\quad M_{X}(t)=[1+p(e^t-1)]^n
$$
**negative binomial** (geometric when k =1)
$$
f(x;k,p)={x-1\choose k-1}p^k(1-p)^{x-k}, \quad \mu = \frac{k}{p}, \quad \sigma^2 = \frac{k}{p}\left( \frac{1}{p}-1 \right)
$$
**hypergeometric**  (sampling without replacement)
$$
f(x;n,N,M)=\frac{\begin{pmatrix}M\\x\end{pmatrix}\begin{pmatrix}   N-M\\ n-  x   \end{pmatrix}}{\begin{pmatrix}N\\n\end{pmatrix}},\quad \mu=\frac{nM}{N},\quad \sigma^2= \frac{nM(N-M)(N-n)}{N^2(N-1)}
$$
**poisson**
$$
f(x;\lambda)=\frac{\lambda ^xe^{-\lambda}}{x!}, \mu =\sigma^2=\lambda, \quad M_{X}(t)=e^{\lambda(e^t-1)}
$$
**Continuous**
**Joint Cumulative Density**
$$
F(X,Y)=P(X\leq x,Y\leq y)=\int_{-\infty}^y\int_{-\infty}^xf(s,t)dsdt\ \ \ x,y \in (-\infty,\infty)
$$
$$
f(x,y)=\frac{\partial^2}{\partial x\partial y}F(x,y)
$$
$$
\text{marginals}\quad \quad \quad \quad \, \,f_X(x)=\int_{-\infty}^\infty f(x,y)dy\quad and\quad f_Y(y)=\int_{-\infty}^\infty f(x,y)dx
$$
For $n$ continuous random variables $X_{1},X_{2},\dots ,X_{n}$ with a joint probability densities $f(x_{1},x_{2},\dots,x_{n})$ and marginals densities $f_{X_{i}}(x_{i})$:
$$
f_{X}(x_{1},x_{2},\dots x_{n})=f_{X_{1}}(x_{1})\cdot f_{X_{2}}(x_{2})\dots f_{X_{n}}(x_{n}) \, \, \, \,\forall(x_{1},x_{2},\dots,x_{n})
$$
if and only if the $n$ random variables are independent
**uniform**
$$
f(x;\alpha,\beta)=\frac{1}{\beta-\alpha}, \quad \mu = \frac{\alpha+\beta}{2}, \quad \sigma^2=\frac{1}{12}(\alpha-\beta)^2
$$
**gamma function** (continuous factorial)
$$
\Gamma(\alpha)=\int_{0}^\infty y^ {\alpha-1}e^{-y}dy, \quad \Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi }
$$
**Gamma Distribution**
$$
f(x;\alpha,\beta)= \frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-x/\beta},\quad \mu = \beta \alpha,\quad \sigma^2=\beta^2 \alpha 
$$
[[Exponential Distribution]] is a gamma distribution when $\alpha=1$
The [[Chi-Squared Distribution]] is a gamma distribution with $\alpha=\frac{v}{2}$ and $\beta=2$, $v$ = df
**beta distribution**
$$
f(x;\alpha,\beta)=\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1},\quad \mu=\frac{\alpha}{\alpha+\beta}, \quad \sigma^2 =\frac{\alpha \beta}{(\alpha +\beta)^2(\alpha+\beta+1)}
$$
**normal distribution**
$$
\huge f(x;\mu,\sigma^2)= \frac{1}{\sqrt{ 2\pi \sigma^2 }}e^{-(x-\mu)^2/2\sigma^2}, \quad M_{X}(t)=e^{\mu t+\frac{1}{2}\sigma^2t^2}
$$
If $X\sim Bin(n,p)$ then the moment-generating function of 
$$
Z=\frac{X-np}{\sqrt{ np(1-p) }}=\frac{X-\mu}{\sigma}
$$

$$P(A|B) = \frac{P(B|A)P(A)}{P(B)}=\frac {P(A\cap B)}{P(B)}$$
 **Conditional**
$$\begin{align}f_{X|Y}(x|y)   =P(A|B)   & =\frac{P(A\cap B)}{P(B)}=\frac{f(x,y)}{f_{Y}(y)} \\
E[g(X)|Y=y]  &  =\sum_{x}g(x)f_{X|Y}(x|y) \\
E[g(X)|Y=y] & =\int_{-\infty}^\infty g(x)f_{X|Y}(x|y)  \\
Var(X|Y=y) & =E(X^2|Y=y)-[E(X|Y=y)]^2 \\
\end{align}
$$
**Expectation** 
$$\begin{align} E[g(X,Y)] & =\int_{-\infty}^\infty\int_{-\infty}^\infty g(x,y)\cdot f_{X,Y}(x,y)dx \\
E[g(X,Y)]  & =\sum_x\sum_yg(x,y)\cdot f_{X,Y}(x,y) \\
\end{align}
$$
**properties**
$$
\begin{align}
  E\left[ \sum_{i=1}^nc_{i}g_{i}(X) \right] & =\sum_{i=1}^n c_{i}E[g_{i}(x)] \\
E[(aX+b)^n]    & = \sum_{i=0}^n {n\choose i}a^{n-i} b^iE(X^{n-1})   \\
E[aX+b] & =aE[X]+b \\
\text{var}(aX+b) & =a^2[E(X^2)-[E(X)]^2]=a^2\sigma^2=a^2\text{var}(X)
\end{align}
$$
**Moments**
$$
\begin{align}
\mu_{r}^{\prime}=E(X^{r})  =\sum_{x}x^{r}f(x) & \quad(discrete)\\ 
\mu_{r}^{\prime}=E(X^{r})  =\int_{-\infty}^{\infty}x^{r}f(x)dx & \quad(continuous) \\
\end{align}
$$
Central moments
$$
\begin{align}
\mu_r & =E[(X-\mu)^r]=\sum_x(x-\mu)^r\cdot f(x) & \quad (discrete)\\
\mu_r & =E[(X-\mu)^r]=\int_{-\infty}^\infty(x-\mu)^r\cdot f(x)dx & \quad(continuous) \\
\text{var}(X) & =\sigma^2=\mu_{2}=E[(X-\mu)^2]=E(X^2)-[E(X)]^2
\end{align}
$$
Moment generating functions are a bijection between functions
$$
\begin{align}
M_{X}(t)=E(e^{ tX}) & =\sum_{x}e^{ tx}f(x)\quad \quad  & \text{discrete} \\
M_{X}(t)=E(e^{ tX}) & =\int_{-\infty}^\infty e^{ tx}f(x)\,dx\quad \quad  & \text{continuous}  \\
\mu_{r}'=E(X^r) & =\left. \frac{d^rM_{X}(t)}{dt^r} \right|_{t=0} \\
\end{align}
$$
$$
\begin{align}
1. &\quad  M_{X+a}(t)=E[e^{(X+a)t}]=e^{at}\cdot M_{X}(t) \\
2. &\quad M_{bX}(t)=E[e^{bXt}]=M_{X}(bt) \\
3. &\quad M_{\frac{X+a}{b}}(t)=E\left[ e^\left( \frac{x+a}{b} \right)t \right] =E\left[ e^{\frac{a}{b}t} \right]M_{X}\left( \frac{t}{b} \right) 
\end{align}
$$
Product of Moments
$$
\begin{align}
\mu_{r,s}' & =  \sum_x\sum_yx^ry^s\cdot f_{X,Y}(x,y)=E[X^rY^s] \\ 
\mu_{r,s}' & =\int_{-\infty}^\infty\int_{-\infty}^\infty x^ry^s\cdot f_{X,Y}(x,y)dxdy  \\
P(|X-\mu|<k\sigma) & \geq1- \frac{1}{k^2}, \quad \sigma\neq 0
\end{align}
$$
The covariance of $X$ and $Y$ is the  [[Product of Moments]] about the mean, expectations are inversely related when covariance is negative, and directly related when it is positive
$$
\mu_{1,1}=\sigma_{XY}=cov(X,Y)  =E((X-\mu_{X})^1(Y-\mu_{Y})^1) =E(XY)-E(X)E(Y)
$$
If $X$ and $Y$ are [[Independency|independent]]:
- $E(XY)=E(X)E(Y), \quad cov(X,Y)=\sigma_{XY}=0$

If $A_{1},A_{2},A_{3},\dots A_{n}$ are in a sample space such that $P(A_{1})\neq0, P(A_{1}A_{2})\neq0,\dots P(A_{1}A_{2}\dots A_{{n-1}})\neq0$ then $P(A_{1}A_{2}\dots A_{n})=P(A_{1})P(A_{2}|A_{1})P(A_{3}|A_{1}A_{2})\dots P(A_{n}|A_{1}A_{2}\dots A_{n-1})$
If $A$ and $B$ are independent $\to (A$ and $\overline{B})$ and $(\overline{A}$ and $B)$ are also independent
If the sample space S can be partitioned into events $B_{1},B_{2},\dots B_{k}$  and $P(B_{k})\neq 0$ $\forall i=1,2\dots k$ 
Then for any event A in S $P(A)=\sum_{i=1}^kP(A|B_{i})P(B_{i})$
**Independence**
If $X$ and $Y$ are independent:
$$
\begin{align}
  f(x,y) & = P(X=x,Y=y) \\
 & =P(X=x)P(Y=y)  \\
 f(x,y)& =f_{X}(x)f_{Y}(y) \, \, \, \,\ \forall \text{(x,y)  }
\end{align}
$$
$$
\begin{align}
F(x,y) & =P(X\leq x,Y\leq y) \\
 & =P(X\leq x)P(Y\leq y) \\
 & =F_{X}(x)F_{Y}(y) \, \, \, \, \, \, \, \, \, \,\forall \text{  (x,y)}
\end{align}
$$
The cdfs can be used instead to determine the dependency of the variables
$$
\begin{align}
f(x,y)  & = f_{X}(x)f_{Y}(y) \\
F(x,y) & =F_{X}(x)F_{Y}(y)
\end{align}
$$
