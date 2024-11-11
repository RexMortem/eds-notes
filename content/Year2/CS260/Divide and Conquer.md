# Divide and Conquer

Break problems into smaller problems:
- solve these smaller problems
- divide, conquer, combine 


## Revisiting Merge Sort 

1) Divide array into two halves
2) Solve each half 
3) Merge them together

## Number of operations 

T(n) = 0
T(n) ≤ T(n/2) + T(n/2) + n

### Proof by Recursion Tree

### Proof by Telescoping 

T(n) = 2T(n/2) + n
T(n)/n = 2T(n/2)/2 + 1
= T(n/2)/(n/2) + 1
= T(n/4)/(n/2) + 1 + 1 
= T(n/n)/(n/2) + 1 + 1 + … + 1 (n times)

### Proof by Induction 


## Master Theorem