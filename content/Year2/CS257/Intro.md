Repeated content, such as Moore's Law, omitted. 
## Logistics
Recordings available for limited time, and will be removed if attendance of lectures drops below 50%. 

## Design Goals
*"Computer Architecture is the science and art of designing computer platforms... to achieve a set of specific goals." - O. Mutlu*

Keep design goals in mind when designing platforms and components.
Different platforms will have different goals.

## RISC 

**RISC** - Restricted Instruction Set Computers

### The Alternative 

Much of early hardware development was to ensure as few instructions executed as possible, by creating many instructions doing more and more niche things. 

This led to increasingly complicated architecture. 

### Enter RISC

- f

## Growth in Processor Performance

Massive contributor: use of instruction-set parallelism, and the use of caches. 

### Slowing Down


- Practical limit to multiprocessing: some tasks can't be multithreaded (or not known to be). These are serial tasks. 

## Current Trends in CA

New models in performance based on parallelism: 

- f

## Further Growth in Processor Performance

## Reducing Power Consumption 

- Inactive cores -> turn off
- Low activity cores -> reduce clock frequency 

## Flynn's Taxonomy

Different classifications based on:
- one or many data streams
- one or many instruction streams 

### SISD (Single Instruction, Single Data)

### SIMD (Single Instruction, Multiple Data)


### MISD ()

### MIMD 

Tightly-coupled is on a single machine (so shared memory)
Loosely-coupled is on many machines (so distributed memory)

## Measuring Performance

### Benchmarks
Many benchmark tasks
	- Kernels
	- "Toy" programs (e.g. sorting)
	- Synthetic Benchmarks
	- Benchmark Suites (e.g. SPEC benchmarks (SPEC2017, SPEC2006, ... , SPEC89))

Many benchmarks **discredited** due to systems able to optimise to solve benchmarks.
***Example:*** You can have a system optimised to solve 7x7 matrix multiplications *really fast*, but which can't do much else quickly. 

So standardised benchmark suites are preferred because: 
- the tests 

## Current Research

Specification is key for the future.
### New paradigms 

- Processing in memory devices, and near data
- Neuromorphic Computing (GTech)
- Secure and Dependable Computers
	- Design with security in mind through all levels of the hierarchy 