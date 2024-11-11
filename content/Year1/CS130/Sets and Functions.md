# Preqreq Content

Although there are no official pre-reqs for this module, there is frequent usage of set theory (covered in Sets & Numbers and also cs130).

## Sets 

A set is a mathematical object with a notion of membership i.e. whether something is in it or not. 

Since they do NOT have a notion of counting, you can only include an element *once*.
That is, $\{A, B, C\} = \{A, A, B, C\} = \{A, B, B, C, C\}$.
(sets are typically wrapped in curly braces $\{\}$)
 
We can interact with a set $S$ by asking whether an element $a$ is in the set (with $a \in S$), and asking how many (unique) elements are in the set ($|S|$).
- For example, let $A = \{1, banana, ⭐\}$
- $1 \in A$? True.
- $2 \in A$? False. 
- $|A| = 3$.
- $|\{1, 1, 2, 2, 3, 4\}| = 4$.

There are also useful operations between sets


Some common (and useful) examples of (non-finite) sets:
- the natural numbers $\mathbb{N}$
- the integers $\mathbb{Z}$
- the 

## Quantifiers 

## Relations 

## Functions

Functions are a special case of relations where each element in the first set is mapped to *exactly one* element of the second set. 
- If an element in the first set does not map, then ***existence*** is violated
- If an element in the first set maps to 2+ elements, then ***uniqueness*** is violated

So a relation $R \subseteq X \times Y$ if $\forall x \in X. \; \exists! y \in Y. \; xRy.$

### Key Properties

We will introduce *surjectivity* and *injectivity*, which are essentially the two properties required for the **inverse** relation to be a valid function.
Think about the constraint for a function ($\forall x \in X. \; \exists! y \in Y. \; xRy.$) and what this means must be true for its inverse. 

A function is ***injective*** if "no 2+ x are mapped to the same y" (i.e. each $y \in Y$ is mapped to by one $x \in X$ or not mapped to).

$\forall a, b \in X. \; (a=b) \implies f(a) \neq f(b).$ 



As all elements in the domain ($X$) map to an element in the codomain ($Y$), and no two elements are mapped to the same y, then $|X| \leq |Y|$.

A function is ***surjective*** if "no y is not mapped to". 

$\forall y \in Y. \; \exists x \in X.\; f(x) = y.$

Since every $y \in Y$ is mapped to, the size of $|X|$ must be equal to greater than $|Y|$. 

**Intuition:** which of (injectivity, surjectivity) map to (existence, uniqueness)?

A function is ***bijective*** if it's both surjective and injective. 
Since 