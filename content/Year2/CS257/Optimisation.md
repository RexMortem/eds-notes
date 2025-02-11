The goal in this module is to optimise using: 
- efficient cache use
	- spatial locality
	- temporal locality
- spamming pragmas

>[!Warning]- Operation Commutativity
>Operations which are meant to be commutative may not be with floating-point operations! 
>
>This means that $(1.01 + 2.03)/3.0 = (1.01)/3.0 + (2.03)/3.0$ may not necessarily be true.


## Pipelining
Instruction-level Parallelism. 

Lay out the process into an assembly line/pipeline. Clearly, while later stages are being worked on, you can concurrently work on earlier stages. 

***Example:*** The linear approach to instruction fetch-and-execute is to fetch an instruction, and then execute it. 2 stages.

The pipelined approach is to fetch the next instruction while executing an instruction. 

Sometimes, you can't apply pipelining to every stage because some stages depend on the result of other stages. 
### Data Dependencies


## Loop Optimisations 

Be careful about loop dependencies. 
### Loop Peeling

If all loops depend on some constant number of initial elements, then just do those initial elements first and then parallelise later iterations.

### Loop Interchange

Doing iterations in a certain order to optimise for spatial locality. 

- If entire dataset fits in cache -> little impact