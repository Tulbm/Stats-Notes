Type 1 error rate = $\alpha$ = $P(\text{Type 1 error})=P(\text{reject }H_{0}|H_{0} \text{ is true})$
Type 2 error rate = $\beta$ = $P(\text{Type 2 error})=P(\text{do not reject }H_{0}|H_{0} \text{ is false})$
$\text{Power}=1-P(\text{Type 2 error})=1-\beta= P(\text{reject }H_{0}|H_{0}\text{ is false})$

Trying to decrease one of the error rates by changing the [[Critical Region]] increases the other one

$$
\begin{align}
0.05 & = P(\text{reject }H_{0}|\mu=2) \\
0.05 & = P(\bar{X}>C^ *|\mu =2) \\
0.05 & =P\left( \frac{\bar{X}-2}{\sqrt{ 1.2 /n}} > \frac{C^*-2}{\sqrt{ 1.2 /n }}|\, \mu=2\right) \\
\rightarrow pag97
\end{align}
$$

![](https://i.imgur.com/DvJq87j.png)




- $\beta$ depends on the choice of $\alpha$, sample size, the true value of the parameter, etc
- the greater the value of $\alpha$ or $\beta$, the higher the probability that the other test errors occur
- type 1 errors are worst case scenario, so we normally choose a small value for $\alpha$ and let $\beta$ be