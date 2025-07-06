
$P(A | \text{ condition})$ = Probability of A given condition
- given effectively reduces sample space
- P (Q | face card)
	- = 4/12
# Bayes Theorem
$$P(A|B) = \frac{P(B|A)P(A)}{P(B)}=\frac {P(A\cap B)}{P(B)}$$
- $P(A|B) = P(A) \to \text{A and B are independent events}$

Extended Bayes' Theorem (applying rule of total probability)
$$
P(B_{j}|A)=\frac{P(A|B_{j})P(B_{j})}{\sum_{i=1}^kP(A|B_{i})P(B_{i})}
$$


$P(A\cap B) = P(A)P(B|A)$ 
$P(A|B) = 1 - P(\bar A|B)$
$P(A\cap B) = P(A)P(B|A) = P(B)P(A|B)$
$P(A\cap B)=P(AB)$ (notation)
$P (ABC) = P (A)P (B|A)P (C|AB)$ $=P(AB)P(C|AB)$
- $P(A_{1}A_{2}A_{3}\dots)$

If $A_{1},A_{2},A_{3},\dots A_{n}$ are in a sample space such that $P(A_{1})\neq0, P(A_{1}A_{2})\neq0,\dots P(A_{1}A_{2}\dots A_{{n-1}})\neq0$ then 
- $P(A_{1}A_{2}\dots A_{n})=P(A_{1})P(A_{2}|A_{1})P(A_{3}|A_{1}A_{2})\dots P(A_{n}|A_{1}A_{2}\dots A_{n-1})$

$P(AB) = P(A)P(B|A) = P(B)P(A|B)$
$P(A)=P(A|B)+P(A|\bar{B})$
$P(A)=P(A|B)P(B)+P(A|C)P(C)+P(A|D)P(D)\dots$
- $P(A)=P(AB)+P(AC)+P(AD)\dots$ given context


If $A$ and $B$ are independent $\to (A$ and $\overline{B})$ and $(\overline{A}$ and $B)$ are also independent

$$
P(A_{1}A_{2}\dots A_{k})=P(A_{1})P(A_{2})\dots P(A_{k}) \iff A_{1},A_{2},\dots A_{k} \text{ are independent}
$$
Pairwise Independency
- 3 or more events can be independent when paired against one another (pairwise), but not when all grouped together

## Sensitivity
- ability of a test to designate an individual with the disease as positive
- $P(B\ |A)$
- sensitivity + false negative = $P(B\ | A) + P(\bar{B} |  A) = 1$
## Specificity
- ability of a test to designate an individual without the disease as negative
- $P(\bar B\ | \bar A)$
- specificity + false positive = $P(\bar B | \bar A) + P(B|\bar A) = 1$