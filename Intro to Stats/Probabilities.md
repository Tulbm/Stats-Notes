The [[1 - Recent/Academics/CIS/Discrete Structures/Probability]] of an outcome is the proportion of times that outcome would occur in an infinite series of trials

It quantifies the variability of the outcome of any experiment whose outcome cannot be predicted with certainty
# Sample Space 
Set of all possible outcomes
- S = {HH, HT, TH, TT} or S = {0, 1, 2} (number of head tosses)

Each individual outcome in a sample space is called a sample point

Sample spaces are mutually exclusive
- no two sample points can occur on the same trial
	- only one sample points will occur on any individual trial

And collectively exhaustive
- the collection of sample points contains all possible outcomes

An infinite sample space contains an infinite number of elements
- outcomes can be number of fails until success

A **continuous** sample space consists of the infinite elements contained within an interval

Guidelines for sample spaces
- try to make them simple
	- no extra information unnecessary to the probability
- if possible, set it up so that the sample points are equally likely
#  Events
Subsets of the sample space
- collection of sample points (empty set is allowed)
Simple events have a single sample point and compound events have 2+

Usually represented by capital letters, A, B, C, ...
- E = {1,2,3} $\to$ represents rolling a 1,2 or 3
- F = {2,3,4}
# Probabilities of Events
Probabilities of events can be illustrated with venn diagrams, with the sample space being the total area
- P(A)
	- if all of the sample points are equally likely
		- P(A) = number of sample points that make up A / total number of sample points
			- obviously
- intersection of A and B
	- event that both A and B occur
	- if $A\cup B$ = empty set
		- they are called mutually exclusive events
- union of A and B ($A\cup B$) 
	- A or B or both occur
	- $P(A\cup B) = P(A) + P(B) - P(A\cap B)$  
- complement of $A$ = $\bar A$
	- $\bar A$ the event that A doesn't occur
		- $\bar A$ = set of all sample points that are not in A
- independent events
	- A and B are independent  if and only if $P(A\cap B) = P(A)P(B)$
		- when A and B have non-zero probabilities of occurring:
			- check if one works, if do -> independent
			- $P(A\cap B) = P(A)P(B)$
			- $P(A|B) = P(A)$
			- $P(B|A) = P(B)$
