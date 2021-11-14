---
title: Project 2 DesignDoc 模板
weight: 5
---

# Project 2 Design Document

## QUESTION 1: ARGUMENT PASSING

### DATA STRUCTURES

> A1: Copy here the declaration of each new or changed `struct` or `struct` member, global or static variable, `typedef`, or enumeration. Identify the purpose of each in 25 words or less.

### ALGORITHMS

> A2: Briefly describe how you implemented argument parsing. How do you arrange for the elements of argv[] to be in the right order? How do you avoid overflowing the stack page?
>
> A2: 简要描述你是怎么实现 Argument parsing 的。你是如何安排 argv[]中的 elements，使其在正确的顺序的？你是如何避免 stack page 的溢出的？

### RATIONALE

> A3: Why does Pintos implement strtok_r() but not strtok()?
>
> A3: 为什么 Pintos 中实现 strtok_r()而不是 strtok()？

> A4: In Pintos, the kernel separates commands into a executable name and arguments. In Unix-like systems, the shell does this separation. Identify at least two advantages of the Unix approach.
>
> A4: 在 Pintos 中，kernel 将命令分成了可执行文件的 name 以及参数。在 Unix-like 的系统中，shell 完成这部分的分隔。列举至少 2 种 Unix 这样做的好处。

## QUESTION 2: SYSTEM CALLS

### DATA STRUCTURES

> B1: Copy here the declaration of each new or changed `struct` or `struct` member, global or static variable, `typedef`, or enumeration. Identify the purpose of each in 25 words or less.

> B2: Describe how file descriptors are associated with open files. Are file descriptors unique within the entire OS or just within a single process?
>
> B2: 描述文件描述符是如何与打开文件相联系的。文件描述符是在整个中唯一还是仅在单个进程中唯一？

### ALGORITHMS

> B3: Describe your code for reading and writing user data from the kernel.
>
> B3: 描述你用来从 kernel 中读写文件的代码。

> B4: Suppose a system call causes a full page (4,096 bytes) of data to be copied from user space into the kernel. What is the least and the greatest possible number of inspections of the page table (e.g. calls to pagedir_get_page()) that might result? What about for a system call that only copies 2 bytes of data? Is there room for improvement in these numbers, and how much?
>
> B4: 假设一个系统调用造成一整页的数据(4096 bytes)从用户空间复制到 kernel。
>
> 求可能造成的最小和最大的页表的检查次数。(e.g. 对 pagedir_get_page()的调用)。如果系统调用只 copy 了 2 bytes 的数据呢？还有没有空间优化？可以优化多少？

> B5: Briefly describe your implementation of the "wait" system call and how it interacts with process termination.
>
> B5: 简要描述你"wait"系统调用的实现以及它是如何与进程停止交互的。

> B6: Any access to user program memory at a user-specified address can fail due to a bad pointer value. Such accesses must cause the process to be terminated. System calls are fraught with such accesses, e.g. a "write" system call requires reading the system call number from the user stack, then each of the call's three arguments, then an arbitrary amount of user memory, and any of these can fail at any point. This poses a design and error-handling problem: how do you best avoid obscuring the primary function of code in a morass of error-handling? Furthermore, when an error is detected, how do you ensure that all temporarily allocated resources (locks, buffers, etc.) are freed? In a few paragraphs, describe the strategy or strategies you adopted for managing these issues. Give an example.
>
> 任何在用户指定的地址上对用户程序的内存的访问可能因为指针错误而失败。此类访问一定导致进程终止。系统调用充满了这样的访问。如一个“写”系统调用需要先从用户栈中读系统调用号，然后每一个调用的 3 个参数，然后是任意数量的用户内存。任何这些都可能造成失败。这构成一个设计错误处理的问题：如何最好地避免混淆主要错误处理的烦恼？此外，当错误被检查到，你如何保证所有的临时开出的资源（锁、缓冲区等）都被释放？用几段话来描述你处理这些问题的策略。

### SYNCHRONIZATION

> B7: The "exec" system call returns -1 if loading the new executable fails, so it cannot return before the new executable has completed loading. How does your code ensure this? How is the load success/failure status passed back to the thread that calls "exec"?
>
> B7: 如果新的可执行文件加载失败，"exec"系统调用会返回-1，所以它不能够在该新的可执行文件成功加载之前返回。你的代码是如何保证这一点的？加载成功/失败的状态是如何传递回调用"exec"的线程的？

> B8: Consider parent process P with child process C. How do you ensure proper synchronization and avoid race conditions when P calls wait(C) before C exits? After C exits? How do you ensure that all resources are freed in each case? How about when P terminates without waiting, before C exits? After C exits? Are there any special cases?
>
> B8: 考虑有父进程 P 和它的子进程 C。当 P 在 C exit 之前调用 wait(C)时，你如何确保同步以及如何避免争用的情况？你如何确保在每种情况下，所有的资源都被释放？如果 P 在 C exit 之前，没有 waiting 便终止？如果在 C exit 之后？有什么特殊情况吗？

### RATIONALE

> B9: Why did you choose to implement access to user memory from the kernel in the way that you did?
>
> B9: 为什么你使用这种方式来实现从内核对用户内存的访问？

> B10: What advantages or disadvantages can you see to your design for file descriptors?
>
> B10: 你对文件描述符的设计有什么优劣吗？

> B11: The default tid_t to pid_t mapping is the identity mapping. If you changed it, what advantages are there to your approach?
>
> B11: 默认的 tid_t 到 pid_t 的映射是 identity mapping。如果你进行了更改，那么你的方法有什么优点？

## 空白模板

```markdown
# Project 2 Design Document

## QUESTION 1: ARGUMENT PASSING

### DATA STRUCTURES

> A1: Copy here the declaration of each new or changed `struct` or `struct` member, global or static variable, `typedef`, or enumeration. Identify the purpose of each in 25 words or less.

### ALGORITHMS

> A2: Briefly describe how you implemented argument parsing. How do you arrange for the elements of argv[] to be in the right order? How do you avoid overflowing the stack page?
>
> A2: 简要描述你是怎么实现 Argument parsing 的。你是如何安排 argv[]中的 elements，使其在正确的顺序的？你是如何避免 stack page 的溢出的？

### RATIONALE

> A3: Why does Pintos implement strtok_r() but not strtok()?
>
> A3: 为什么 Pintos 中实现 strtok_r()而不是 strtok()？

> A4: In Pintos, the kernel separates commands into a executable name and arguments. In Unix-like systems, the shell does this separation. Identify at least two advantages of the Unix approach.
>
> A4: 在 Pintos 中，kernel 将命令分成了可执行文件的 name 以及参数。在 Unix-like 的系统中，shell 完成这部分的分隔。列举至少 2 种 Unix 这样做的好处。

## QUESTION 2: SYSTEM CALLS

### DATA STRUCTURES

> B1: Copy here the declaration of each new or changed `struct` or `struct` member, global or static variable, `typedef`, or enumeration. Identify the purpose of each in 25 words or less.

> B2: Describe how file descriptors are associated with open files. Are file descriptors unique within the entire OS or just within a single process?
>
> B2: 描述文件描述符是如何与打开文件相联系的。文件描述符是在整个中唯一还是仅在单个进程中唯一？

### ALGORITHMS

> B3: Describe your code for reading and writing user data from the kernel.
>
> B3: 描述你用来从 kernel 中读写文件的代码。

> B4: Suppose a system call causes a full page (4,096 bytes) of data to be copied from user space into the kernel. What is the least and the greatest possible number of inspections of the page table (e.g. calls to pagedir_get_page()) that might result? What about for a system call that only copies 2 bytes of data? Is there room for improvement in these numbers, and how much?
>
> B4: 假设一个系统调用造成一整页的数据(4096 bytes)从用户空间复制到 kernel。
>
> 求可能造成的最小和最大的页表的检查次数。(e.g. 对 pagedir_get_page()的调用)。如果系统调用只 copy 了 2 bytes 的数据呢？还有没有空间优化？可以优化多少？

> B5: Briefly describe your implementation of the "wait" system call and how it interacts with process termination.
>
> B5: 简要描述你"wait"系统调用的实现以及它是如何与进程停止交互的。

> B6: Any access to user program memory at a user-specified address can fail due to a bad pointer value. Such accesses must cause the process to be terminated. System calls are fraught with such accesses, e.g. a "write" system call requires reading the system call number from the user stack, then each of the call's three arguments, then an arbitrary amount of user memory, and any of these can fail at any point. This poses a design and error-handling problem: how do you best avoid obscuring the primary function of code in a morass of error-handling? Furthermore, when an error is detected, how do you ensure that all temporarily allocated resources (locks, buffers, etc.) are freed? In a few paragraphs, describe the strategy or strategies you adopted for managing these issues. Give an example.
>
> 任何在用户指定的地址上对用户程序的内存的访问可能因为指针错误而失败。此类访问一定导致进程终止。系统调用充满了这样的访问。如一个“写”系统调用需要先从用户栈中读系统调用号，然后每一个调用的 3 个参数，然后是任意数量的用户内存。任何这些都可能造成失败。这构成一个设计错误处理的问题：如何最好地避免混淆主要错误处理的烦恼？此外，当错误被检查到，你如何保证所有的临时开出的资源（锁、缓冲区等）都被释放？用几段话来描述你处理这些问题的策略。

### SYNCHRONIZATION

> B7: The "exec" system call returns -1 if loading the new executable fails, so it cannot return before the new executable has completed loading. How does your code ensure this? How is the load success/failure status passed back to the thread that calls "exec"?
>
> B7: 如果新的可执行文件加载失败，"exec"系统调用会返回-1，所以它不能够在该新的可执行文件成功加载之前返回。你的代码是如何保证这一点的？加载成功/失败的状态是如何传递回调用"exec"的线程的？

> B8: Consider parent process P with child process C. How do you ensure proper synchronization and avoid race conditions when P calls wait(C) before C exits? After C exits? How do you ensure that all resources are freed in each case? How about when P terminates without waiting, before C exits? After C exits? Are there any special cases?
>
> B8: 考虑有父进程 P 和它的子进程 C。当 P 在 C exit 之前调用 wait(C)时，你如何确保同步以及如何避免争用的情况？你如何确保在每种情况下，所有的资源都被释放？如果 P 在 C exit 之前，没有 waiting 便终止？如果在 C exit 之后？有什么特殊情况吗？

### RATIONALE

> B9: Why did you choose to implement access to user memory from the kernel in the way that you did?
>
> B9: 为什么你使用这种方式来实现从内核对用户内存的访问？

> B10: What advantages or disadvantages can you see to your design for file descriptors?
>
> B10: 你对文件描述符的设计有什么优劣吗？

> B11: The default tid_t to pid_t mapping is the identity mapping. If you changed it, what advantages are there to your approach?
>
> B11: 默认的 tid_t 到 pid_t 的映射是 identity mapping。如果你进行了更改，那么你的方法有什么优点？
```
