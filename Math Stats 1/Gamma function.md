$$
\Gamma(\alpha)=\int_{0}^\infty y^ {\alpha-1}e^{-y}dy, \quad \text{for } y>0
$$
Pi function brings it back to the right factorial
$$
\Gamma(x)=\Pi(x-1)=\int_{0}^\infty t^x e^{-t}dt =\int_{0}^\infty (-\ln(t))^xdt = \lim_{ N \to \infty } N^x \prod_{k=1}^N \frac{k}{x+k}
$$

# Properties
1. $\Gamma(\alpha)=(\alpha-1)\Gamma(\alpha-1)$ for $\alpha>1$
$$\begin{align}
\Gamma(\alpha) & =\int_{0}^\infty y^{\alpha-1}e^{-y} \,dy\quad \text{(integration by parts)}\\
 & = \left[y^{\alpha-1}(-e^{-y})\right|_{0}^\infty-\int_{0}^\infty-e^{-y}(\alpha-1)y^{\alpha-2}dy \\
 & = 0-0+(\alpha-1)\int_{0}^\infty y^{\alpha-1 -1}e^{-y}dy \\
 & =(\alpha-1)\Gamma(\alpha-1)
\end{align}
$$
1. $\Gamma(1)=\int_{0}^\infty e^{-y}dy=1$
2. $\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi }=- \frac{1}{2}!$ 
3. $\Gamma\left( \frac{3}{2} \right)=\frac{1}{2}! =\frac{\sqrt{ \pi }}{2}$
