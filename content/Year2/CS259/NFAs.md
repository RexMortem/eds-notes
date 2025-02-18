NFAs are [[DFAs & Regular Languages|DFAs]] but with a less restricted transition function:
- it can accept the empty string as an input i.e. it can transition without reading a symbol
- its output is a set of states i.e. it can transition to a number of states

A 5-tuple $(Q, \Sigma, q_{0}, F, \delta)$ where $\delta : Q \times \Sigma_{E} \rightarrow 2^{Q}$ where $\Sigma_{E} = \Sigma \cup \{E\}$

## Runs

Informal: Given an NFA and a ...

Given NFA $A$ and $w \in \Sigma^{*}$, a run of $A$ on $w$ is a sequence $a_{0}a_{1}\dots a_{n} \in Q$ s.t. there exists $y_{1}, \dots, y_{n} \in \Sigma_{\epsilon}$ s.t. $w = y_{1} \dots y_{n}$ and:
1) $a_{0}$ is the initial state ($q_{0}$) of $A$ 
2) $a_{i} \in \delta(a_{i-1}, y_{i})$

A run is accepting if it ends in a final state i.e. $a_{n} \in F$.

### Tree
You can draw a tree for determining whether there is an NFA accepting run.
### Extended Transition Function
$\delta^{hat} : Q \times \Sigma^{*} \rightarrow 2^{Q}$.

Case $|w| = 0$: $\delta^{hat}(q, w) = \delta^{hat}(q, \epsilon) = \{q\}$

Case $|w| > 0$: $w = w^{\prime}a$ and $\delta^{hat}(q, w^{\prime}) = \{s_{1}, \dots, s_{k}\}$. Then $\delta^{hat}(q, w) = \bigcup^{k}_{i=1} \delta(s_{i}, a)$

***Example:*** $\delta^{hat}(q_{0},110) = \{q_{0}, q_{1}\}$
$\delta^{hat}(q_{0}, 1101) = \delta(q_{0}, 1) \cup \delta(q_{2}, 1) = \{q_{0}, q_{1}\} \cup \emptyset = \{q_{0}, q_{1}\}$.

NFA $A$ has an accepting run on $w$ iff $\delta^{hat}(q_{0}, w) \cap F \neq \emptyset$

**Theorem:** For every $\epsilon$-free NFA $N=(Q, \Sigma, q_{0}, F, \delta)$, there exists a DFA $D = (2^{Q}, \Sigma, \{q_{0}\}, F_{D}, \delta_{D})$ s.t. $L(N) = L(D)$.

***Proof Sketch:*** The NFA essentially has a transition function that goes from some set of states, to some other set of states. 

The DFA will encode these possible sets of states as elements of a single set. Then, the transition function will tell you how to go from one element to another element i.e. how to go from one set of states to another set of states (just like in the NFA). 

Then, any accepting state in the DFA is any subset with an accepting state from the NFA. 

***Proof:*** Let $F_{D} = \{A \subseteq Q : \;  A \cap F = \emptyset \}$.

Now, to adapt the proof for epsilon transitions.

--- 

**Def:** The $\epsilon$-closure of $q \in Q$, notated $EClose(q)$, is the set of states that can be reached from $q$ by following only $\epsilon$-transitions. 

We also define $EClose$ for sets. 

$EClose(S) = \bigcup_{q \in S} EClose(q)$

- Call EClose at the start
- Call EClose after w=0 transition
- Call EClose on set from w > 1 transition 
- Call EClose in DFA-NFA proof 

## Converting NFAs into DFAs

This is sometimes called the "powerset construction".

**Intuition:** AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

## Closure Properties

Languages are closed under certain operations, and we can see why using NFAs!

Since we've proved that NFAs have the same expressive power as DFAs (since every DFA can be trivially converted into an NFA, and every NFA can be converted into a DFA), we can prove that these properties hold for regular languages by using NFAs. 

### Complementation 

If a language $L$ is regular, then $\Sigma \setminus L$ is also regular. 

>[!Warning]- Empty String
>Be careful about what the complement of a language actually is.
>
>For instance, if $L = \{w | \; \text{w ends with a 1}\}$.
>It's tempting to say that obviously $\Sigma \setminus L =  \{w | \; \text{w ends with a 0}\}$.
>
>However, this is **WRONG**!
>
>The complement of $L$ includes everything not in $L$; this specific $L$ does not include the empty string, and so its complement $\Sigma \setminus L$ includes $\epsilon$. 
>
>It's very easy to forget about $\epsilon$, so please be careful!
