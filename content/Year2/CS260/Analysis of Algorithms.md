# Analysis of Algorithms 

## Worst-Case Analysis 
## Asymptotic Analysis

Used to describe the run-time cost of functions. 

### Big-O

Big-O means that a function is "bounded above" by another function.
For example, $f(n) \in O(g(n))$ means that f is bounded above by g. 

Formally, $f$, $f(n) \in O(g(n))$ iff $\exists A, N \geq 0. \; \forall n \geq N. \;  0 \leq f(n) \leq Ag(n)$.

For example, consider $f(n) = 3n^{2}$.
We can say:
- $f(n) \in g(n^{2})$ but we could also say…
- $f(n) \in g(n^{3})$
- $f(n) \in g(n^{4})$
- $f(n) \in g(n!)$
- $f(n) \in g(n^{n})$

### Big Omega 



## Examples of some algorithms 

### Linear Time Algorithms

- Computing the maximum (or minimum) of an unordered list of numbers 
	- Takes $\Omega(n)$ time to look at all the input 
- Merging two sorted lists 
	- For two lists of size $n$, it takes $O(2n) = O(n)$ steps because you move forward down one list each time you iterate 

### Quadratic Time Algorithms 

- Enumerate all pairs of elements
- Find the distance between the closest algorithm (though a faster solution exists)

### Input Structure Challenge

- Without taking advantage of it being sorted, just use a hashmap 
- ff

### Cubic Time Algorithms 

### Exponential Time Algorithms 

## Summary (Tips)

- Learn $O()$, $\Omega()$, $\Theta()$ notation
- Use worst-case analysis often (try to prevent the worst from happening)
- Focus on running-time 
- Polynomial good, exponential bad 