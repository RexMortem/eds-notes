
Might merge with [[Context-Free Languages]]

## Transitions
*A key thing to remember is that PDAs work non-deterministically*

With PDAs, our transitions need to capture reading in symbols *but also* modifying a stack. We will introduce a notation which may seem unrelated at first :)

Transitions are written as $a, b \rightarrow c$. 
This means "when reading $a$, we can replace $b$ on the stack with $c$ by taking this transition".
Of course, we can only take this transition if the symbol on top of the stack is $b$.

At first, it's not obvious that this encapsulates how a stack works. How do we push? How do we pop? How might we check the state of the stack before accepting or more generally, allowing passage to another state in the machine?

**Intuition:** For pushes/pops, we can view $a, b \rightarrow c$ as meaning "when reading $a$, we pop $b$ off the stack and push $c$ onto the stack by taking this transition".

**Pushing:** We can represent just pushing as $a, \epsilon \rightarrow b$ which means "when reading $a$, we can push $b$ onto the stack" 

**Popping:** We can represent just popping as $a, b \rightarrow \epsilon$ which means "when reading $a$, we can pop a $b$ off the stack"

**Checking state:** We can enforce needing a certain symbol on the top of the stack with $a, b \rightarrow b$ which means "when reading $a$, we require a $b$ to take this transition and don't change the stack" (since $b$ replacing $b$ doesn't do anything).

### Using the empty string

Our transitions are quite strong. For $a, b \rightarrow c$, we're saying that to take this transition:
-  $a$ must be the next symbol read **AND**
- $b$ must be on top of the stack 

We might want a transition with only one of these conditions; we can use $\epsilon$ for this!

#### Only reading

To ignore the stack part and just check 

#### Neither

Analogous to $\epsilon$-transitions in NFAs.

$\epsilon, \epsilon \rightarrow \epsilon$
### Bottom

Often, we also need the power to check whether the stack is empty. We can do this by pushing on a symbol (we will choose $\bot$) at the very start, so that it will be the first symbol pushed onto the stack. 

We can then check whether the stack is empty with a transition $a, \bot \rightarrow \bot$ which means "when reading $a$, we can take this transition if the stack is empty". 

Of course, we might choose to replace "$\bot$" with another symbol at the same time as checking whether the stack is empty. 

## CFGs and PDAs 

$G$ is in Chomsky normal form if all rules:
$A \rightarrow BC$ where $B,C \neq S$
$A \rightarrow a$

**Theorem:** For every CFG G, there is a CFG $G^{\prime}$ in CNF s.t. $L(G) = L(G^{\prime})$

HMU 7.1.5

Cooke-Younger-Kasami propose a DP algorithm 