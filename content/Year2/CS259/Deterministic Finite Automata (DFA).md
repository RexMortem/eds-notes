This is a model of computation; there are many other models of computation (such as turing machines, PDAs etc).

A DFA is a 5-tuple $(Q, \Sigma, q_{0}, F, \delta)$.

- $Q$ is a set of states
-  Alphabet explained in [[Intro to Formal Languages]]
- $q_{0}$ is the initial state 
- $F \subseteq Q$ is the set of accepting states
- $\delta$ is the transition function which maps from state & input to a state (the next state)

Used for lexical analysis. 
*To me: double-check the details of lexing and DFAs vs other models in lexing*

***Example 1:*** 

## Definitions

Sipser's book offers a beginner-friendly specification of a DFA; it doesn't really explain the semantics of a DFA and what it's used for. 

Dmitry says a full definition of a DFA has Syntax and Semantics, rather than just Syntax.
-> Semantics is more important than Syntax

## Empty Language DFA

