
A set of processes is in a deadlock 

## Necessary (but not sufficient) conditions for deadlock

- **Mutual exclusion:** Only one can use an instance of a resource (Ed: or a finite n processes?)
- **Hold and wait:** Must be a process holding resources, while waiting for other resources (which are mutually exclusive)
- **No preemption:** Mutually exclusive resource can only be voluntarily released from a process
- **Circular wait:** Must exist a circular wait. This is not a sufficient condition as resources can have more than one "slots".

## Deadlock Prevention

We discuss potential solutions for each necessary condition to deadlock. 

**However** 

## Deadlock Avoidance

Less restrictive approach.

A request is allowed if it leaves the system in a **"safe state"**.

### Deadlock Avoidance Algorithm

Naive algorithm: 

- Banker's Safety Algorithm
## Resource Allocation Graph

Edge from **resource $\rightarrow$ process**: allocating a resource to the process
Edge from **process $\rightarrow$ resource**: requesting a resource from the resource

**Heuristic 1:** A node with no out-edges can finish without a problem. 

**Heuristic 2:** A cycle is a necessary (but not sufficient) condition for deadlock.

Generally, you can use **Heuristic 2** to identify cycles and examine each cycle (and use **Heuristic 1**) to check whether the cycle leads to a deadlock. 

## Deadlock Detection Algorithm

While loop:
- If Currently Available has any non-zero elements, then assign resources to requests.
- Check across allocation table and request table for processes that can now finish. 
	- Update currently available if a process can now finish! 
- Terminate loop if no processes were finished 