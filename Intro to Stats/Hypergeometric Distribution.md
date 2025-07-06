
Similar to the [[Binomial Distribution]] but samples without replacement 
- probability of success is not constant from trial to trial


- for the geometric distribution:
	- finite population correction function
# Probability Distribution Function
A random variable $X$ has a hypergeometric distribution $X\sim \text{ hypergeometric}(n,N,M)$ if and only if its probability distribution is

$$P(X=x)=f(x;n,N,M)=\frac{\begin{pmatrix}M\\x\end{pmatrix}\begin{pmatrix}   N-M\\ n-  x   \end{pmatrix}}{\begin{pmatrix}N\\n\end{pmatrix}}$$
for $x=0,1,2,\dots,n,$ $x\leq n,\, x\leq M$ and $n-x\leq N-M$
- $N=$ population size
- $n =$ sample size
- $M=$ size of one group in the population
- $x=$ number of successes in one group among $n$ samples

$$\begin{align}
E(X) & =\sum_{x=0}^n x \frac{\begin{pmatrix}M\\x\end{pmatrix}\begin{pmatrix}   N-M\\ n-  x   \end{pmatrix}}{\begin{pmatrix}N\\n\end{pmatrix}}  \\
 & =\frac{1}{{N\choose n}}\sum_{x=0}^n x \frac{M!}{x!(M-x)!} {N-M\choose n-x} \\
 & =\frac{1}{{N\choose n}}\sum_{x=1}^n \frac{xM(M-1)!}{x(x-1)!(M-1-(x-1))!}  {N-M\choose n-x} \\
 & =\frac{M}{{N\choose n}} \sum_{x=0}^{n-1} \frac{(M-1)!}{x!(M-1-x)!} {N-M\choose n-(x+1)} \\
 & =\frac{M}{{N\choose n}} \sum_{x=0}^{ n-1}{M-1\choose x} {N-M\choose n-1-x} \\
 & =\frac{M}{{N\choose n}} {N-1\choose n-1} \quad \quad \text{vandermondes} \\
 E(X)& =\frac{nM}{N}
\end{align}
$$
[[Counting Theorems#Vandermonde's (Zhu Shijie's) Identity]]
$$
\sigma^2= \frac{nM(N-M)(N-n)}{N^2(N-1)}
$$
$$

$$
# examples
- taking 3 balls from a urn with 10 balls, we want only 2 red ones(4 red in total)
$$ P(X=2) = \frac {\begin{pmatrix}   4\\ 2 \end{pmatrix}\begin{pmatrix}   6\\1 \end{pmatrix}} {\begin{pmatrix}   10\\3 \end{pmatrix}} = 0.3$$
- with replacement (binomial)
$$P(X=2) = \begin{pmatrix}   3\\2   \end{pmatrix}4^20.6^{1} = 0.288 $$
