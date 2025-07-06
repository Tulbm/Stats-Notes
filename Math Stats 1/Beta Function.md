$$
\begin{align}
M_{X}(t)=E(e^{tX}) & =\int_{-\infty}^\infty e^{tx}\frac{1}{\beta^\alpha \Gamma(\alpha)} x^{\alpha-1}e^{ -x/\beta}dx \\
 & =\frac{1}{\beta^\alpha\Gamma(\alpha)}\int_{0}^\infty e^{tx-x/\beta}x^{\alpha-1}dx\left. \right|_{t=0}\\
 & =\frac{1}{\beta^\alpha\Gamma(\alpha)}\quad\int_{0}^\infty e^{-x(1/\beta-t)}x^{\alpha-1}dx \quad \left( u=x\left( \frac{1}{\beta}-t \right) \right)\\ 
 & =\frac{1}{\beta^\alpha\Gamma(\alpha)}\int_{0}^\infty e^{ -u}\left( \frac{u}{\frac{1}{\beta}-t} \right)^{\alpha-1} \frac{du}{\frac{1}{\beta}-t} \quad \left( x=\frac{u}{\frac{1}{\beta}-t}, dx = \frac{du}{\left( \frac{1}{\beta}-t \right)} \right) \\
 & =\frac{1}{\beta^\alpha \Gamma(\alpha)}\left( \frac{1}{\frac{1}{\beta}-t} \right)^\alpha \int_{0}^\infty e^{-u}u^{\alpha-1}du \\
 & =\left( \frac{1}{\beta}-t \right)^{-\alpha} \frac{1}{\beta^\alpha \Gamma(\alpha)}\Gamma(\alpha) \\
 & =\left( \left( \frac{1}{\beta}-t \right)\beta \right)^{-\alpha} \\
 M_{X}(t)& =(1-t\beta){^{ -\alpha}} \\
\end{align}
$$

$$
B(\alpha,\beta)=\left[ \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \right]^{-1}
$$

Inverse to denote the relationship with [[Counting Theorems|combinatorics]], [[Gamma function]] is the continuous factorial, so it is like the inverse of ${ n\choose k }$ 

If the gamma function was not weirdly shifted by one, it would look like

$$
B(\alpha,\beta)=\frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)(\alpha+\beta+1)}
$$

which is one argument for the weird gamma function. Another one is the fact that $\Gamma(0)=-1!=\infty$
