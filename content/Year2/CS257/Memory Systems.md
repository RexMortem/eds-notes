## The Designer's Dilemma 

Refer to [[Memory|CS132]]. 

## Memory Hierarchy

Memory hierarchy is the same as in [[Memory|CS132]], but we go more into detail on *why* we have one. 

### Why have a hierarchy?

- Economics: we don't have infinite money, so we can't build ultra-fast ultra-high capacity memory. Therefore, we have a hierarchy with trade-offs between capacity and access times. 
- Temporal Locality & Spatial Locality lead to cache-based devices in the memory hierarchy having very good access times
	- **Temporal Locality:** Memory location being referenced means it's likely it'll be referenced again 
	- **Spatial Locality:** Memory location being referenced means it's likely nearby memory will be referenced again
	- arrays have good spatial locality because it is a contiguous block of memory

## Organisation of a Memory Chip

Array is organised in words of $B$ bits. 
![[Pasted image 20250108103133.png]] 
If $B = 8$, then each word above will contains 8 bits. 
***Example 1:*** $W_{0}$ will contain 8 bits 
***Example 2:*** The entire block of memory contains $8 \times 16 = 128$ bits of memory. 

## Choices in Memory Chip Organisation

***Example:*** Consider a 1 kilobit device, that reads in 1 byte at a time. 

First, know that 
- 1 kilobit = 1024 bits 
- 1 byte = 8 bits

**How many output pins do we have?** 
**How many rows/words do we have?** 
**How many addressing bits do we need?** 
>[!note]- Exam
>This is often an exam question. 

## Minimising Address Decoding Space 

Row Buffer is a cache for storing the entire row that is retrieved from the array. 

## Holes 

Grounding chips? Why required?

- Look at DRAM chip from W. Stallings 
