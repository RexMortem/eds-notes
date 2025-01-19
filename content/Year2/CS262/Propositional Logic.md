As in [[Year1/CS130/Logic|CS130]], propositions are composed from smaller propositions joined together with logical operators or are atomic propositions. 

## Propositional Formulas 

- Propositional **variables** are the atomic building blocks; they are **atomic formulas** 
	- ***Example:*** in $((p \land q) \lor r)$, we have $p, q, r$ as propositional variables 
- Formulas can also be formed from negating a formula
	- ***Example 1:*** $\neg x$ is a formula if $x$ is a formula 
	- ***Example 2:*** $\neg((p \lor q) \land r)$ is a formula if $((p \lor q) \land r)$ is a formula
- Formulas can be formed from binary 

>![Warning]- Strict Syntax
>In this module, we have to be very careful about forming valid formulas. 
>
>For example, 

### Degree 

The ***degree*** of a formula is the number of logical operators used in the formula. 

***Example 1:*** $x$ has degree of 0 
***Example 2:*** $\neg x$ has degree of 1
***Example 3:*** $x \lor y$ has degree of 1
***Example 4:*** $(x \land y) \lor (y \land z)$ has degree of 3
### Induction 

We can derive recursive functions from the recursive structure of propositional formulas. 

For instance, we define the *degree* of a formula recursively.
- **Atomic Formulas:** $deg(x) = 0$ if $x$ is an atomic formula 
- **:**

### Parse Trees 

#### Inner nodes (parse trees)

Inner nodes are nodes that are not leaf nodes i.e. $x$ is an inner node if $deg(x) > 0$.

**Theorem:** The degree of a formula is the number of inner nodes in the formula's parse tree. 
***Proof:*** 

### Valuation 
A valuation is a function that maps from the set of formulas to the set of truth values $\{T,F\}$, that satisfies the following properties: 

### Tautologies, Contradictions, & Satisfiability

Tautologies evaluate to **true** regardless of the values of its atomic formulas.
Contradictions evaluate to **false** regardless of the values of its atomic formulas. 

Satisfiability can be thought of as a weaker version of a tautology: a formula is satisfiable if it can evaluate to **true** under some values of its atomic formulas.

### Propositional Consequence 

A formula $X$ is a consequence of some set $S$ of formulas if $X$ evaluates to true when all the formulas in $S$ are set to true. 

We denote this by $S|X$ which reads "$X$ is a consequence of $S$". 

