# Discrete
Marginal Distributions (marginal pdfs) of $X$ and $Y$:
- $f_{X}(x)=P(x=x)=\sum _yf(x,y)$
- $f_{Y}(y)=P(Y=y)=\sum_{x}f(x,y)$

where $f(x,y)$ is their joint pmf 



box with 9 balls, 2 white, 4 black (Y), 3 red (X)

| $P(X=x,Y=y)$   | x = 0 | x = 1 | x = 2 | $f_{y}(y)=P(Y=y)$ |
| -------------- | ----- | ----- | ----- | ----------------- |
| y = 0          | 1/36  | 6/36  | 3/36  | 10/36             |
| y = 1          | 8/36  | 12/36 | 0     | 20/36             |
| y = 2          | 6/36  | 0     | 0     | 6/36              |
| $f_{x}=P(X=x)$ | 15/36 | 18/36 | 3/36  |                   |
# Continuous
If X and Y are continuous random variables and $f(x,y)$ is the value of their joint pdf at $(x,y)$, the functions given by
$$
\begin{align}\\&f_X(x)=\int_{-\infty}^\infty f_{X,Y}(x,y)dy\quad and\quad f_Y(y)=\int_{-\infty}^\infty f_{X,Y}(x,y)dx\\&\end{align}
$$
are called the marginal distributions (marginal pdfs) of X and Y respectively.
