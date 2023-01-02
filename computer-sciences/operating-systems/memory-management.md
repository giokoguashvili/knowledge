# [Memory Management](https://en.wikipedia.org/wiki/Memory_management)

![Memory Management in OS](https://user-images.githubusercontent.com/8178412/210232701-760f0baa-84d6-4ad6-ae7a-787acc5e5757.png)

## Types of Memory Addresses

- **Physical addresses** <br/>
is the memory location within system RAM
- **Logical addresses** <br/>
virtual memory, is what operating systems and applications access to execute code, as an abstraction of physical address space

## Memory Allocation
- **Static Loading** <br/>
code is loaded into memory, before it is executed. Used in structured programming languages including C
- **Dynamic Loading** <br/>
Code is loaded into memory as needed. Used in object oriented programming languages, such as Java

## Memory Fragmentation

- **Internal Fragmentation** <br/> 
Memory is allocated to a process or application and isn’t used, leaving un-allocated or fragmented memory
- **External Fragmentation** <br/> 
As memory is allocated and then deallocated, there can be small spaces of memory leftover, leaving memory holes or “fragments” that aren’t suitable for other processes

## Paging

## Segmentation

## Swapping


# Sources

- [What is Memory Management?](https://www.enterprisestorageforum.com/hardware/memory-management/) - enterprisestorageforum.com
- [What every programmer should know about memory](https://lwn.net/Articles/250967/) - lwn.net
