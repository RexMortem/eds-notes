# Overview of Operating Systems

What's the point of the syscall interface in a monolithic kernel, if a monolithic kernel is always in kernel mode i.e. users directly interact? 
-> could be hole in understanding of what a "syscall" is; previous understanding is that a syscall has a transition between user and kernel mode because safety
Previous understanding from "When a user process requires a service from the kernel (e.g., reading from a file or writing to a file) it invokes a system call"


- MS-DOS is an old OS by Microsoft 

## Operating System Structures 

### Monolithic Kernels

### Layered Approach 

Advantages: 
- Simplicity of construction
- Ease of debugging (and therefore safety)
- Clear interfaces between layers 
	- ease of use 

Disadvantages: 
- Defining layers (separation) is difficult 
- Efficiency: adds a bit of overhead to go between the layers 

## Microkernels

Mach OS is one of the earliest examples of a **microkernel**. 
As the name suggests:
- Removes all non-essential components from the kernel → smaller kernel 
- contrasts against monolithic kernels, which are generally MASSIVE (do everything)

***Advantages:***
- Extending from the OS is easy 
	- We'll see how you can use Loadable Kernel Modules 
- Safe and reliable

***Disadvantages:***
- Performance overhead (syscall overhead)
- 