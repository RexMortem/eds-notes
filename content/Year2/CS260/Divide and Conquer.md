# Divide and Conquer

Break problems into smaller problems:
- solve these smaller problems
- divide, conquer, combine 


## Revisiting Merge Sort 

1) Divide array into two halves
2) Solve each half 
3) Merge them together

**CHALLENGE FOR ED:** Do MergeSort in-place, constant space. Kronrod 1969

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

## Counting Inversions

### Counting Sorted Parts 

```py
a = [3,7,10,14,18,19]
b = [2,11,16,17,23,25]

bPointer = 0
inversions = 0
finalIndexInB = len(b)-1

for i in range(len(a)):
    if a[i] > b[bPointer]:
        # iterate through b until we have greater element (no inversion)
        while (b[bPointer] <= a[i]) and (bPointer < finalIndexInB):
            bPointer += 1
    
    # bPointer is at max element
    if a[i] > b[bPointer]:
        inversions += 1
    
    inversions += bPointer

print(inversions)
```
## Master Theorem


