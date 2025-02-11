*"To understand the power of finite automata, you must also understand their limitations" - Sipser (Introduction to the Theory of Computation)*

>[!Warning]- Permissive Patterns
>Sometimes, you'll have a language like $L = \{0^{k}u0^{k} \; | \; u \in \Sigma^{*}\}$.
>
>$L$ *looks* non-regular, because it seems to require unbounded counting (counts that can go up to infinity).
>
>However, $u$ is a highly permissive pattern which means that it allows 
>
>**tl;dr:** Be vary careful of permissive patterns


## Myhill-Nerode Theorem

### Indistinguishability

Two words $a, b \in L$ are said to be indistinguishable iff

### Intuition for Myhill-Nerode

Consider a regular language $L$. Since it is regular, there must exist a DFA $A$ for it. 

If the run of two words $x, y$ lead to the same final state (not necessarily an accepting state) in the DFA $A$, then those two words cannot be distinguished. Whenever you add the same word to the end of $x$ and to the end of $y$, it will lead to the exact same state.

Therefore, two indistinguishable words $x, y$ must have runs leading to different final states. Thus we have that:

$|\text{states}| \geq |\text{indistinguishable words}|$

So if we can prove there are an infinite number of words that are indistinguishable from one another, then we prove there are at least an infinite number of states in $A$. So any DFA for the language $L$ must have a non-finite number of states hence no DFA for $L$ exists (DFAs must have a finite number of states), so $L$ is non-regular.





























## Shitposting Notes

*CATCH UP ON THE FIRST 10 MINS OF THIS LECTURE*

***Pumping Lemma🥵*** 