Suppose $X_{1},\dots,X_{n}$ is a random sample of size $n$ from an infinite population with a continuous pdf. If we arrange the values in ascending order and 
$$
X_{(1)} \leq X_{(2)} \leq \dots \leq X_{(n)}
$$
$X_{(1)}$ = minimum, $X_{(n)}$ = maximum

For a random sample of size $n$, there are $n!$ possible arrangements of the random variables

# Distribution of minimum and maximum
Suppose $X_{1},\dots,X_{n}\sim$ iid $f_{X(x)}$ (independently identically distributed) are continuous. Let
$$
X_{(1)}=\text{min}(X_{1},X_{2},\dots,X_{n})
$$
$$
X_{(n)}=\text{max}(X_{1},X_{2},\dots X_{n})
$$
The cdf of $X$ is $F_{X}(x)=P(X\leq x)=\int f_{x}(t)dt$

The pdf of $X_{(1)}$ (min) is
$$
\begin{align}
F_{X_{(1)}} & =P(X_{(1)}\leq x)= 1-P(X_{(1)}\geq x) \\
 & =1-P(X_{1}\geq x, X_{2} \geq x, \dots X_{n}\geq x) \\
 & =1-(1-P(X_{1}\leq x))\dots(1-P(X_{n}\leq x)) \\
 & =1- (1-F_{X}(x))(1-F_{X}(x))\dots(1-F_{X}(x)) \\
 & =1-[1-F_{X}(x)]^n \\
f_{X_{(1)}} & =\frac{d}{dx}(1-[1-F_{X}(x)]^n) \\
 & =n[1-F_{X}(x)]^{n-1}f_X(x)
\end{align}
$$
And the pdf of $X_{(n)}$ (max) is
$$
\begin{align}
F_{X_{(n)}} = P(X_{n}\leq x) & = P(X_{(1)}\leq x, X_{(2)}\leq x ,\dots X_{(n)}) \\
 & =P(X_{(1)}\leq x)P(X_{(2)}\leq x)\dots P(X_{(n)}\leq x) \\
 & =[F_{X}(x)]^{n} \\
f_{X_{(n)}} & =n[F_{X}(x)]^{n-1}f_{X}(x)
\end{align}
$$
# Distribution of the rth order

$$
P(x\leq X_{(r)}\leq x+ \Delta x)=f_{X_{(r)}}(x)\Delta(x)
$$
The pdf of the $r$th order statistic $X_{(r)}$ is given by
$$
f_{X_{(r)}}=\lim_{ \Delta X \to 0 } {\frac{f_{}X_{(r)}\Delta(x)}{\Delta(x)}}
$$
pg 38

$$\begin{align}
 & P(x\leq X_{(r)}\leq x+\Delta x) \\
 & =P((r-1)\text{ x's in}(-\infty,x), \text{ one in }(x,x+\Delta(x)), (n-r) \text{ x's in }(x+\Delta x, \infty) ) \\
 & =\frac{n!}{(r-1)! 1! (n-r)!} [P(X\leq x)]^{r-1} P(x\leq X \leq x+\Delta x)[P(X\geq x+\Delta x)]^{n-r} \\
 & =\frac{n!}{(r-1)!(n-r)!}[F_{X}(x)]^{r-1}[F_{X}(x+\Delta x)-F_{X}(x)][1-F_{X}(x+\Delta x) ]^{n-r}
\end{align}
$$
Then from 
$$
\begin{align}
f_{X_{(r)}}(x) & =\lim_{ \Delta x \to 0 } \frac{P(x\leq X_{(r)}\leq x+\Delta x)}{\Delta x}  \\
 & = \lim_{ \Delta x \to 0 } \frac{n!}{(r-1)!(n-r)!} \frac{[F_{X}(x)]^{r-1}[F_{X}(x+\Delta x)-F_{X}(x)][1-F_{X}(x+\Delta x) ]^{n-r}}{\Delta x} \\
 & =\frac{n!}{(r-1)!(n-r)!} [F_{X}(x)]^{r-1} \lim_{ \Delta x \to 0 } \frac{F_{X}(x+\Delta x)-F_{X}(x)}{\Delta x} [1-F_{X}(x)]^{n-r} \\
 f_{X_{(r)}}(x) & = \frac{n!}{(r-1)!(n-r)!} [F_{X}(x)^{r-1}]f_{X}(x)[1-F_{X}(x)]^{n-r}
\end{align}
$$
From which we can derive the formula for the min $(r=1)$ and the max $(r=n)$

Applying the above result we find that the sample median $\tilde{X}$ of a random sample $X_{1},\dots X_{2n+1}$ (odd size) has the pdf
$$
f_{\tilde{X}}(x) =f_{X_{(n+1)}}(x)= \frac{(2n+1)!}{n!\cdot n!} [F_{X}(x)]^n f_{X}(x) [1-F_{X}(x)]^n
$$
$$
f_{\tilde{X}}(x) =f_{X_{(k)}}(x)= \frac{n!}{(k-1)!\cdot (n-k)!} [F_{X}(x)]^{k-1} f_{X}(x) [1-F_{X}(x)]^{n-k}
$$

For an even number of observations:
$$
\tilde{X}= \frac{X_{(n)}+X_{(n+1)}}{2}
$$
which needs to find the joint pdf of $(X_{(r)},X_{(j)})$ using [[Change of Random Variables]]:
$$
Y_{1} = \frac{X_{(n)}+X_{(n+1)}}{2},\quad Y_{2}= X_{(n)}
$$

