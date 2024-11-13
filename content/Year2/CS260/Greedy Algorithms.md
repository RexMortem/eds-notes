
A greedy algorithm is an algorithm that, in each step, picks the "obvious" choice. If your algorithm is maximising some value, then in each step, it would pick the choice with the largest value. In other words, the locally optimal choice is chosen. 

Sometimes, there are multiple measures to be greedy towards and the difficulty is often choosing which measure. 

We will look at some classic problems with greedy algorithm solutions:
- <a href="#IntervalScheduling"> Testing </a>
## <a name="IntervalScheduling"> Interval Scheduling Problem </a>

The interval scheduling problem is choosing a maximum subset of compatible tasks (jobs). 

**Explain this more:** If you're looking for the related but harder problem: [[DP]]

By building up this subset, we consider whether to add a compatible job to the subset. But by which measure should we greedily choose the next job:
- Earliest start time
- Earliest finish time
- Shortest duration
- Fewest conflicts 

### Solution

It turns out that the measure for the optimal algorithm is **earliest finish time**. 

#### Implementation (Python)

```py
def solve(jobs):
    # sort by end-duration
    jobs.sort(key=lambda x: x[1])

    # build a list of elements to be included
    toReturn = [jobs[0]]

    # add non-conflicting jobs to the list of elements
    for i in range(1, len(jobs)):
        # check the latest element included; could also keep a variable for it
        latestJob = toReturn[len(toReturn)-1]

        # if start time is AFTER end-time of latest job --> we can add
        if jobs[i][0] >= latestJob[1]:
            toReturn.append(jobs[i])

    return toReturn

sol = solve([(0, 6),(1, 4), (3, 5), (3, 8), (4, 7), (5, 9), (6, 10), (8, 11)])

print(sol) # [(1, 4), (4, 7), (8, 11)]
```

### Proving Earliest Finish Time is Optimal

## Interval Partitioning Problem

## Coin Changing Problem

## Optimal Offline Caching Problem

## Selecting Breakpoints Problem

