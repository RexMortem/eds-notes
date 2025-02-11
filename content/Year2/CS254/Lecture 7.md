**DFS numbering:** we assign numbers in the order with which nodes "finish". 
- A node is finished when it backtracks; with a stack, it would be when the value is popped off the stack

## DAG 

- Topological Sort
	- *"the point of this exercise is that you're completely drunk"*

***Theorem:*** A digraph $G$ has a topological sort iff $G$ is a DAG.
**Proof:** FTSOC assume $G$ has a cycle $C = (x_{0}, \dots, x_{k})$.

We have $(x_{0}, x_{k}) \in E$ and so $d$

We have proven if $G$ has a topological sort, then $G$ must be a DAG. 


