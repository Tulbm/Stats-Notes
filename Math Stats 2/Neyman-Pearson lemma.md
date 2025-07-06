Used to derive the most powerful test, by finding the optimal critical region

Concept of fixing $\alpha$ and then maximizing the [[Error types|power]], instead of having $\alpha$ and $\beta$ balancing each other out

Suppose $X_{1},\dots,X_{n}\sim iid f(x;\theta)$. To test $H_{0}:\theta=\theta_{0}\, vs \,H_{a}:\theta=\theta_{1}$, let $C$ be the critical region such that:
$$
P(\underset{\sim}{x}\in C\,|\,H_{0}\text{ is true})= \alpha
$$
If $\forall$ $C^*$ such that $P(\underset{\sim}{x}\in C^* | H_{0}\text{ is true})= \alpha$ we have that the power of $C>$ power of $C^*$ 
$$
P(\underset{\sim}{x}\in C\, |\, H_{0} \text{ is false}) \geq P(\underset{\sim}{x} \in C^*\, |\, H_{0}\text{ is false})
$$
Then we say that $C$ is the best [[Critical Region]] / most powerful test

100-101?

NP provides a method for testing two simple hypothesis, for a more general method of composite hypothesis we use the [[Likelihood ratio test]]


# Examples
$X_{1},\dots,X_{n}\sim N(\mu,1)$ To test $H_{0}:\mu=\mu_{0}\, vs\,H_{a}:\mu=\mu_{1},\, \mu_{1}>\mu_{0}$
$$\begin{align}
L_{0} & =f(x_{1},\dots,x_{n};\mu_{0},1) \\
 & =\prod \frac{1}{\sqrt{ 2\pi }}e^{-(x_{i}-\mu_{0})^2/2}=(2\pi)^{-n/2} e^{-\sum (x_{i}-\mu_{0})^2/2} \\
L_{1} & =f(x_{1},\dots,x_{n};\mu_{1},1) \\
 & =(2\pi)^{-n/2} e^{-\sum (x_{i}-\mu_{1})^2/2} \\
\frac{L_{0}}{L_{1}} & =\frac{(2\pi)^{-n/2}e^{-\sum(x_{i}-\mu_{0})^2/2}}{(2\pi)^{-n/2} e^{-\sum (x_{i}-\mu_{1})^2/2}} \\
 & =\exp\left\{ - \frac{1}{2} \left( \sum x_{i}^2 -2\mu_{0}\sum x_{i}+n\mu_{0}^2 - \sum x_{i}^2 + 2\mu_{1}\sum x_{i} - n\mu_{1}^2 \right) \right\} \\
 & =\exp\left( n\bar{x}(\mu_{0}-\mu_{1})- \frac{n}{2}(\mu_{0}^2-\mu_{1}^2) \right) \\
 & \text{now to find a region and }K: \\
\frac{L_{0}}{L_{1}} & = e^{n\bar{x}(\mu_{0}-\mu_{1})- \frac{n}{2}(\mu_{0}^2-\mu_{1}^2) } \leq k \quad st (x_{1},\dots,x_{n})\in C \\
 & \to n\bar{x}(\mu_{0}-\mu_{1})- \frac{n}{2}(\mu_{0}^2-\mu_{1}^2)\leq \ln k  \\
 & \bar{x} \geq \frac{1}{n(\mu_{0}-m_{1})}\left[ \ln k+ \frac{n}{2}(\mu_{0}^2 -\mu_{1}^2) \right] = k^* \\
 \to  & \begin{cases}
\bar{x} > k^*, \quad (x_{1},\dots,x_{n})\in C \\
\bar{x} \leq k^*, \quad (x_{1},\dots,x_{n}) \notin C
\end{cases} \\
 \alpha & = P(\text{reject }H_{0}|H_{0}\text{ is true}), \quad \bar{x} \sim N\left( \mu_{0}, \frac{1}{n} \right) \\
\alpha & =P(\bar{x} \geq k^* | \mu= \mu_{0}) \\
\alpha & =P \left( \frac{\bar{x}-\mu_{0}}{\sqrt{ 1 /n }} \geq \frac{k^*-\mu_{0}}{\sqrt{  1 /n }}\right) \\
k^* & = \mu_{0}+Z_{1-\alpha}\sqrt{ \frac{1}{n} } \\
 & \text{The most powerful critical region for the test is}: \\
C & =\left\{ (x_{1},\dots,x_{n}); \bar{x}\geq \mu_{0}+Z_{1-\alpha} \sqrt{ \frac{1}{n} }) \right\}
\end{align}
$$
When $\bar{x}$ increases, it favors $H_{a}$
When $\bar{x}$ decreases, it favors $H_{0}$

The most powerful test at $\alpha$-level of significance is
$$
\phi(x_{1},\dots,x_{n})= \begin{cases}
 1, \quad \text{if }Z\geq Z_{1-\alpha} \\
0, \quad \text{o.w.}
\end{cases}
$$
