
A set of functions is complete if you can represent *all* truth functions using these connectives. For boolean logic, the truth functions are of the form $f: \{T,F\}^{n} \rightarrow \{T,F\}$. 

For each $n$, there are $2^{2^{n}}$ such functions. This comes from the fact that for a function $g: X \rightarrow Y$, there are $|Y|^{|X|}$ such functions. 


## DNF 

**Fact:** $\{\land, \lor, \neg\}$ is complete.
***Proof Sketch:*** Construct a DNF for each function.
- For every possible set of inputs that map to $T$, create a conjunction of all the input variables. If an input variable is set to $F$, then write the negation of that input variable 
- Create a disjunction of all conjunctions constructed in the above bullet point 

***Example 1:*** For the 

***Example 2:*** For the function $\lor : \{T, F\}^{2} \rightarrow \{T,F\}$, we have the following truth table:

| a   | b   | $a \lor b$ |
| --- | --- | ---------- |
| F   | F   | F          |
| F   | T   | T          |
| T   | F   | T          |
| T   | T   | T          |

**Theorem:** Every Boolean function has a DNF. 
(Proof is same construction as above; the completeness fact is a corollary of every boolean function having a DNF)
## CNF

**Theorem:** Every Boolean function has a CNF. 


## Generalized disjunctions/conjunctions

$[X_{1}, X_{2}, \dots, X_{n}] = X_{1} \lor X_{2} \lor \dots \lor X_{n}$ 
$<X_{1}, X_{2}, \dots, X_{n}> = X_{1} \land X_{2} \land \dots \land X_{n}$


>![Note]- Tip for remembering brackets to disjunction/conjunction
>
>- Square brackets form the start of a capital '**D**', so square brackets for **Disjunction (OR)**
>- Angled brackets form the start of a capital '**C**', so angled brackets for **Conjunction (AND)**

Disjunction valuates to $T$ if any $X_{i} = T$.
Conjunction valuates to $T$ if for all $X_{i}$ we have $X_{i} = T$.

## Normal Form Algorithms


### Alpha, Beta Formulas

### Correctness of NF Algorithms

**Proposition:** Throughout running algorithm, we produce a sequence of logically equivalent formulas. 
***Proof:*** First 3 cases are trivial. 

**Case - Alpha Expansion:** $D_{i} = [\alpha, X_{2}, \dots, X_{n}]$
$= [\alpha_{1} \land \alpha_{2}, X_{2}, \dots, X_{n}]$
$= []$

**Case - Beta Expansion:** 

### Termination


**Konig's Lemma:** A tree that is *finitely branching* but infinite must have an infinite branch.  


### Rank

We define rank as a measure of how "simple" a formula is. 