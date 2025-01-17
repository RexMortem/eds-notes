## Representing Graphs 

We typically represent graphs as a set of vertices (V) and a set of edges (E).

**Problem:** This is quite slow for certain tasks e.g. finding what vertices a given vertex $v$ has an edge to
**Solution:** We have other ways of representing graphs
### Adjacency Matrix

We have an $n \times n$ matrix $A$ where $A_{i,j} = 1$ iff there is an edge $(i, j) \in E$. 
Otherwise, $A_{i,j} = 0$.
$$
\begin{bmatrix}

\end{bmatrix}
$$

>[!Note]- Time Complexities 
>**Checking all edges for a given node:** $\theta(n)$
>**Checking all edges:** $\theta(n^{2})$
>**Checking a node is connected to another node:** $\theta(1)$
>**Space:** $\theta(n^{2})$
### Adjacency List 

Linked List for each node in the graph, which contains the nodes connected to the original node. 

>![Note]- Time/Space Complexities
>Space is $O(n+m)$
## Graph Search (unweighted)

### BFS 

**Theorem:** $\forall i, L_{i}$ we have that $L_{i}$ consists of nodes at a distance $i$ from $s$. 
>[!Note]- Let's use an inductive argument.
>***Base case i=0:*** Node $s$ is at a distance of $0$ from $s$
>***Assume true for i=k:*** For each node $x \in L_{k}$ we have that $x$ is at a distance $k$ from $s$.
>***Induction for i=k+1:*** Let's consider $L_{k+1}$, which consists of unexplored nodes that are neighbours to some $x \in L_{k}$. 
>For each $a \in L_{k+1}$, $a$ has an edge to some $b \in L_{k}$ and $b$ is at a distance $k$ from $s$. Since $a$ is a distance 1 from $b$, we now know there is a path with distance $k+1$ from $s$ to $a$. We know there is no smaller path from $s$ to $a$ because otherwise $a$ would have been explored previously. Hence, $a$ is at a distance $k+1$ from $s$.

#### BFS Time Complexity

$O(1) + \sum{}$


## Dijkstra's 

## Dijkstra Proof 

Note that $w$ is the length of a single step. $c$ is the length of the path so far (defined for all explored points $S$ so far)