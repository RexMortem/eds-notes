NFAs are DFAs but with a less restricted transition function:
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

Case $|w| > 0$: $w = w^{\prime}a$ and $\delta^{hat}(q, w^{\prime}) = \{s_{1}, \dots, s_{k}\}$. Then $\delta^{hat}(q, w) =$ 
***Example:*** $\delta^{hat}(q_{0},110) = \{q_{0}, q_{1}\}$
$\delta^{hat}(q_{0}, 1101) = \delta(q_{0}, 1) \cup \delta(q_{2}, 1) = \{q_{0}, q_{1}\} \cup \emptyset = \{q_{0}, q_{1}\}$.

