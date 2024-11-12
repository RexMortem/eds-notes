This briefly introduces random variables and discusses discrete random variables. This is prerequisite material for [[Continuous Random Variables]].
## What is a Random Variable? 

A random variable (r.v.) is simply a function from the sample space to some real number. So an r.v. $X : \Omega \rightarrow \mathbb{R}$.

Let's understand through an example!
## Dice Roll Experiment

Imagine rolling a 6-sided dice. 

***Example 1:*** You could consider an r.v. $X$ as double roll from the dice. So $X$ takes in the sample space, all the possible rolls you can get, and returns a real number - in this case, double the roll. 

$\Omega = \{1, 2, 3, 4, 5, 6\}$.

$X : \Omega \rightarrow \mathbb{R}$.

$X(1) = 2 \; \land \; X(2) = 4 \; \land \; \dots \; X(6) = 12$.

In general,
$X(a) = 2a$.

***Example 2:*** We could also consider another r.v. $Y$ as the square of the roll. 
$Y : \Omega \rightarrow \mathbb{R}$.
$Y(a) = a^{2}$.

***Example 3:*** We could consider another r.v. $Z$ as a function for whether the roll is even or not. 

$$
Z(x) = \begin{cases}
	1 & x\text{ is even}\\
	0 & x\text{ is odd}
\end{cases}
$$

These examples are to show there are **many** different random variables you can define for a single experiment; in fact, there are an uncountable number of functions that map to $\mathbb{R}$, so there are an uncountable number of random variables! 

## Discrete Random Variables