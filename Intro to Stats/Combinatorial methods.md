In [[1 - Recent/Academics/CIS/Discrete Structures/Probability]] and [[Statistics]], it is an important first step to determine all the possible outcomes of an experiment using [[Counting]] and [[Combinatorial Number Theory]] methods
- direct enumeration
- permutations
- combinations

# combination formula/binomial coefficient
- gives us the number of ways of choosing x items (w/o replacement) from n distinct items if order of selection is not important
- choose(n,x) on [[R]]
- $$  \begin{pmatrix}   n\\   x   \end{pmatrix}= \frac{n!}{x!(n-x)!}$$
- example
	- lotto 6/49, buyers pick 6 numbers from 1-49
	- how many different tickets are possible
	- $$  \begin{pmatrix}   49\\ 6 \end{pmatrix}= \frac{49!}{6!(49-6)!}$$