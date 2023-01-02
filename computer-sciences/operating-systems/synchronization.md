# [Process Synchronization](https://en.wikipedia.org/wiki/Synchronization_(computer_science)#:~:text=Process%20synchronization%20refers%20to%20the,a%20certain%20sequence%20of%20action.)

Classic problems of synchronization
The following are some classic problems of synchronization:

    - The Producer–Consumer Problem (also called The Bounded Buffer Problem)
    - The Readers–Writers Problem
    - The Dining Philosophers Problem

- Implementation of Synchronization
  - Spinlock
  - Barriers
  - [Semaphores](https://en.wikipedia.org/wiki/Semaphore_(programming))
    - Binary Semaphore
    - Counting Semaphore
- Synchronization in Windows
  - Interrupt masks <br/>
    which protect access to global resources (critical section) on uniprocessor systems
  - Spinlocks <br/>
    which prevent, in multiprocessor systems, spinlocking-thread from being preempted
  - Dynamic Dispatchers <br/>
    which act like mutexes, semaphores, events, and timers
- Synchronization in Linux
  - Semaphores
  - Spinlock
  - Barriers
  - **Mutex** <br/>
    readers–writer locks, for the longer section of codes which are accessed very frequently but don't change very often
  - Read-Copy-Update (RCU)
- [POSIX Threads](https://en.wikipedia.org/wiki/Pthreads) <br/>
is a platform-independent API that provides
  - Mutexes
  - Condition variables
  - Readers–Writer Locks
  - Spinlocks
  - Barriers