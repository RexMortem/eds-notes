This is a model of computation; there are many other models of computation (such as turing machines, [[PDAs]] etc).

The basic gist of a DFA is that it's a machine with a *finite* number of states ($Q$) and each state can be **accepting** or not accepting. You put an input string into the DFA and the string will either be accepted or rejected, depending on whether the state the DFA is at is an accepting state, when the entire string has been read. 

Before reading the first symbol in the input string, the DFA starts at an **initial** state ($q_{0}$). 

The set of input strings that are accepted by a DFA is called the language of the DFA. We might also say that the DFA recognises that language. 
## Background

DFAs are often referred to as finite state machines; this property of having a finite number of states is essential as it means you can only model computers with limited memory. 

In other words, a DFA with an infinite number of states cannot exist. If you could have such DFAs with an infinite number of states, then they could model pretty much anything.

In this module, we also discuss [[NFAs]]. In other modules, such as (Data Analytics??), we discuss Markov chains which are the probabilistic version of DFAs. 

Used for lexical analysis. 
*To me: double-check the details of lexing and DFAs vs other models in lexing*

## Definitions

A DFA is a 5-tuple $(Q, \Sigma, q_{0}, F, \delta)$.

- $Q$ is a set of states
-  $\Sigma$ is the alphabet (explained in [[Intro to Formal Languages]])
- $q_{0} \in Q$ is the initial state 
- $F \subseteq Q$ is the set of accepting states
- $\delta : Q \times \Sigma \rightarrow Q$ is the transition function which maps from state & input to a state (the next state)


>[!Note]- Syntax & Semantics
> Sipser's book offers a beginner-friendly specification of a DFA; the definition doesn't really explain the semantics of a DFA and what it's used for. 
> 
> Dmitry says a full definition of a DFA has Syntax and Semantics, rather than just Syntax.
-> Semantics is more important than Syntax


***Example 1:*** 

Note that, in DFAs, for each state there must be exactly one transition for every symbol in the alphabet. Otherwise, the DFA doesn't know what to do if it reads that symbol :(

***Example 2:*** Empty language DFA

No accept states? Empty language :(

## Extended Transition Function 


## Regular Languages

A language $L$ is said to be regular if there exists a DFA that recognises $L$. 

We'd like to discuss Closure Operations on languages which are operations which, when applied to regular languages, give you a regular language. However, we don't have a machine expressive enough to easily prove it yet! Look at the operations in [[NFAs]].