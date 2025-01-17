This is for solving the Maximum Subarray problem, so we'll investigate what approaches we can take to solve it.
## Bruteforce

```py
# bruteforce

maxSum = -1000000

for i in range(len(nums)):
	subArraySum = 0
	
	for j in range(i, len(nums)):
		subArraySum += nums[j]
		maxSum = max(maxSum, subArraySum) # careful; this is on this indent level

return maxSum
```

## Kadane's Algorithm
*"Don't add a negative if we don't have to."*

```py
subArraySum = -1000000
currentSum = 0

for i in range(len(nums)):
	currentSum = nums[i] + max(currentSum, 0)
	subArraySum = max(subArraySum, currentSum)

return subArraySum

```
This calculates it in the opposite direction to the DP solution I give; it calculates the max subarray *ending* with a given $i$. 
## DP Solution 

We can create a DP solution. 

First, we'll look at basic memoisation then go on further to optimise it. We will arrive at an algorithm which is essentially Kadane's Algorithm but in the opposite direction; if you wrote the DP solution in the opposite direction, then you would derive Kadane's Algorithm. 

### Approach

Generate an OPT function which gives us the max subarray starting from a given index $i$. 
We then ask ourselves, "do we include any more elements?" 

We can answer this question by checking if the max subarray for the next element is greater than 0 or not. If it's not, then there's no point including it. 

$$
OPT(i) = \begin{cases}
arr[i] + max(0, OPT(i+1)) & i<len(arr), \\
0 & otherwise
\end{cases}
$$
### Memoisation 

```py
OPT = [0] * len(nums) # value (0) doesn't matter since it'll be replaced

  

        OPT[len(nums)-1] =nums[len(nums)-1]

  

        for i in range(len(nums)-2, -1, -1):

            OPT[i] = nums[i] + max(0, OPT[i+1])

  

        maxSubarray = -1000000

  

        for i in range(0, len(OPT)):

            maxSubarray = max(maxSubarray, OPT[i])

  

        return maxSubarray
```

Only need to keep track of the OPT value immediately above. 
### Previous Pointer

```py
prevMax = nums[len(nums)-1]
maxSubarray = prevMax

for i in range(len(nums)-2, -1, -1):
	prevMax = nums[i] + max(0, prevMax)
	maxSubarray = max(maxSubarray, prevMax)

return maxSubarray
```