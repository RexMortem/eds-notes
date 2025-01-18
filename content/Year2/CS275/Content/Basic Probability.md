# Basic Probability

See [Probability](../../../Year%201/CS130/Probability.md) for a recap of probability. 

### Intuition 

1) An unbiased coin is flipped twice. Given that at least one of the tosses is a head, what is the chance that the other is a head?

Analysing this, we have two events:

- $A =$ at least one head
- $B =$ both are heads 

It should be clear that these events affect each other and therefore are not independent. 
So it should make sense that the answer might not be $\frac{1}{2}$. 

We can calculate the answer ($P(B|A)$) like so:

$A = \{HH, TH, HT\}.$
$B = \{HH\}.$

$P(B|A) = \frac{P(A \cap B)}{P(A)}= \frac{P(\{HH\})}{P(\{HH, TH, HT\})} = \frac{1}{3}.$

2) Similarly, consider the following: An unbiased coin is flipped twice. Given that at least one of the tosses is a head, what is the chance that the other is a tail? 

$A =$ at least one head 
$B =$ the other is a tail 

Evidently, these events also affect each other and therefore are not independent. 
Again, it should then make sense if the answer is not $\frac{1}{2}$. 
It may very well be, but let's see what the answer is. 

$A = \{HH, TH, HT\}.$
$B = \{TH, HT\}.$

$P(B|A) = \frac{P(A \cap B)}{P(A)}= \frac{P(\{TH, HT\})}{P(\{HH, TH, HT\})} = \frac{2}{3}.$

