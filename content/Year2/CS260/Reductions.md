# Reductions

We say a problem X reduces to problem Y iff you can write an algorithm to solve X with calls to Y. In this module, we are concerned with **Polynomial-Time Reductions**.

## Polynomial-Time Reduction

We say a problem $X$ is polynomial-time reducible to $Y$ iff the reduction:
- has a polynomial number of calls to $Y$
- has a polynomial number of additional steps 

We write this as $X \leq_{P} Y$.

We treat the algorithm that solves $Y$ as a **black box** meaning we can't change the internals; we can't reduce $X$ to $Y$ with a tiny adjustment to how $Y$ internally works. Even if you understand how $Y$ would be implemented, you can't modify the internals and we call this black box an **oracle** to $Y$.

### Kinds of PT Reductions

- Explain Karp Reductions vs Cook Reductions 
### Consequences of Polynomial-Time Reduction

### (Informal) Intuition

We can informally think through the theorems by thinking about the symbol used ($\leq_{P}$). This is **not a rigorous way** to think about them, but is a nice way to remember. 

**Way 1:** We can informally think of $X \leq_{P} Y$ as meaning Y is in a "harder or equal" complexity class or just "Y is harder (or equal)". We can then think of being in P as being easy, and not being in P as being hard. 
- If $Y \in P$ then Y is easy, and since X is easier than Y, then X must also be easy: $X \in P$
- If $X \notin P$ then X is hard, and since Y is harder than X, then Y must also be hard: $Y \notin X$

**Way 2:** We can informally think of $X \leq_{P} Y$ as X, Y being "bounded" by each other
- X's complexity is upper-bounded by Y. If $Y \in P$, then $X \in P$ since Y is "above" 
- Y's complexity is lower-bounded by X. If $X \notin P$ then $Y \notin P$ since X is "below"

