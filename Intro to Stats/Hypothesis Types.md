A **statistical hypothesis** is a statement about the population/its distribution

A statement that fully specifies the distribution of a population is called a simple hypothesis. Otherwise, the statement is called a composite hypothesis
- one set value vs a range of multiple values for $\mu$ for example

Null Hypothesis, $H_{0}:$ disapproves the claim
Alternative Hypothesis, $H_{a}:$ claim under investigation/research
$$
H_{0}:\theta \in \Theta_{0} \quad vs \quad H_{a}: \theta\in \Theta_{1}
$$
where parameter space $\Theta=\Theta_{0}\cup \Theta_{1}$ and $\Theta_{0}\cap \Theta_{1}=\emptyset$
- only one of the hypothesis can be accepted

[[Error types]]

# Examples

- sleep study, total sleep recorded and subjective time they thought they slept
	- $\mu _I$ = mean of the difference in the answer x reality for insoniacs
	- $\mu _N$ = mean of the difference in the answer x reality for normal people
	- $H_0 : \mu _I = \mu_N$
	- $H_a : \mu _I \neq \mu_N$
	- on average, do normal sleepers perceive sleep time correctly?
	- does the mean mismatch time 
- hand grip strenght x attractiveness
	- $H_0$ : there is no relationship
	- $H_a$ : there is a relationship
	- we might assume that if there is a relationship, it is a linear one, and test
		- $H_0$ : true slope is 0
		- $H_a$ : true slope is not 0
- company's arsenic level
	- government trying to prove that it goes over 0.30
	- $H_0:\mu = 0.30$ 
		- $H_0:\mu\leq0.30$ makes more sense, but in the end we are only gonna pick one value when proving it with formulas, and thats just gonna be the closest value to the $H_a$  (0.30)
	- $H_a:\mu>0.30$  