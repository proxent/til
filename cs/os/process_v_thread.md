# Process v Thread

Processes are running binaries and threads are the smallest unit of execution schedulable by an operating system's process scheduler.
![image](https://github.com/proxent/til/assets/50007186/b2b01441-e55a-4fa9-932a-58bee1859e18)

As the figure above indicates, a process contains text(code), and data(stores global variables and static variables), and stack(call stack, local variables), heap(dynamic memory allocation).

The typical difference is that threads (of the same process) run in a shared memory space, while processes run in separate memory spaces

Each thread shares the same page table, but owns a private set of registers and a seperate stack.

Why Thread? We could use multi-thread approach instead.

- It is easier to make a new thread, because when you create a new process, you create its code, data, and resources. Also processes are isolated from each other and in order to communicate it requires inter-process communication mechanisms like pipes, sockets or shared memory.

What is context switching? How does it work?

1. It uses Process Control Block(PCB).
2. stores the values of CPU registers, program counter, stack pointers.
3. Selecting the next process.
4. Restores the values.
5. Resumes execution.
