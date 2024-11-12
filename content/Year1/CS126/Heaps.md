
## HeapSort
### Implementation (Python)

It's important to be able to use standard libraries; this is using **heapq** which is the standard library in Python for heaps.

```py
import heapq

def heapsort(arr):
    # first, make the arr a min-heap
    heapq.heapify(arr)

    # now, we need to remove min elements and put into a new array
    toReturn = [None] * len(arr)

    for i in range(len(arr)):
        currentMinElement = heapq.heappop(arr)
        toReturn[i] = currentMinElement

    return toReturn

# note that we created a new array; if we coded the heap from scratch, then we can actually do this sort in-place. How?

# Leave a space at the start of the array, and shuffle the newly popped elements to there

sortedArray = heapsort([5, 3, 2, 6, 1, 4, 3, 2, 7, 8])
print(sortedArray)
```