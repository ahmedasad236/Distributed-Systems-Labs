# RPC and Threads

## Threads

### What is a thread ?

> A thread is a single sequence stream within a process. Threads are also called lightweight processes as they possess some of the properties of processes. Each thread belongs to exactly one process. In an operating system that supports multithreading, the process can consist of many threads. But threads can be effective only if the CPU is more than 1 otherwise two threads have to context switch for that single CPU.

### Why threads ?

- Threads run in parallel improving the application performance. Each such thread has its own **CPU state and stack, but they share the address space of the process and the environment**.

- Threads can share common data so they do not need to use **inter-process communication(IPC)**. Like the processes, threads also have states like ready, executing, blocked, etc.

- Priority can be assigned to the threads just like the process, and the highest priority thread is scheduled first.

- Each thread has its own **Thread Control Block (TCB)**. Like the process, a context switch occurs for the thread, and register contents are saved in (TCB). As threads share the same address space and resources, synchronization is also required for the various activities of the thread.

### What are the thread's components ?

- Stack Space
- Register Set
- Program counter

### What is the difference Between Process and Thread

> The primary difference is that threads within the same process run in a shared memory space, while processes run in separate memory spaces. Threads are not independent of one another like processes are, and as a result, threads share with other threads their code section, data section, and OS resources (like open files and signals). But, like a process, a thread has its own program counter (PC), register set, and stack space.

### What are the threads' challenges ?

- Race conditions
- Coordination
- Deadlock
