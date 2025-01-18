
## GCD 

***Example:*** GCD(15, 20) = ?

Positive divisors of 15: $15, 1, 5, 3$
Positive divisors of 20: $20, 1, 10, 2, 5, 4$
Common divisors: $1, 5$
GCD(15,20): $1 \times 5 = 5$

Manually writing out the divisors and finding the common divisors is quite slow. 

### Euclid's Algorithm 

1) Put $a_{0} = a \land b_{0} = b$
2) $b_{0} = q_{0}a_{0} + r_{0}$ where $0 \leq r_{0} < a_{0}$
3) Check $r_{0}$ value 
	- If $r_{0} = 0$ then $GCD(a,b) = a_{0}$
	- Otherwise $0 < r_{0} < a_{0}$; put $a_{1} = r_{0}$ and $b_{1} = a_{0}$ and loop

*To me: Remember to fix this algorithm description to be generic to i*

***Example:*** GCD(2024, 70) = ?

$2024 = 28 \times 70 + 64$ ($b_{0} = 2024, \; a_{0} = 70$)
$70 = 1 \times 64 + 6$ ($b_{1} = 70, a_{1} = 64$)
$64 = 10 \times 6 + 4$ ($b_{2} = 64$, $a_{2} = 6$)
$6 = 1 \times 4 + 2$ ($b_{3} = 6$, $a_{3} = 4$)
$4 = 2 \times 2 + 0$ ($b_{4} = 4$, $a_{4} = 2$)

Algorithm terminates since $r_{4} = 0$.
#### Proof of Correctness

Firstly, $a_{i} \in \mathbb{Z}_{\geq 0}$ is strictly decreasing so the process eventually terminates. 


#### Extended Euclidean Algorithm

Run Euclid's Algorithm backwards, and we get $GCD(a,b)$ as a linear combination of $a, b$. This is called the Extended Euclidean Algorithm.

2024 = 28x70 + 64
70 = 64 + 6 
64 = 10x6 + 4
6 = 1x4 + 2
4 = 2x2 + 0

2 = 6 - 4
2 = 6 - (64 - 10x6) = 11x6 - 64
2 = 11(70-64) - 64 = 11x70 - 12x64
2 = 11x70 - 12(2024 - 28x70)
2 = 347x70 - 12x2024

#### Bezout's Lemma

(Useful for solving diophantine eqs)

$f$

Proof is by induction

##### Corollary 

If $d|a$ and $d|b$ then $d|(a,b)$. This is because we can write $(a,b)$ as $xa + yb$, and $d|(xa + yb)$.

#### Euclid's Lemma

Let $m, n \in \mathbb{Z}$, and let $p$ be a prime divisor of $mn$. Then $p|m$ or $p|n$.