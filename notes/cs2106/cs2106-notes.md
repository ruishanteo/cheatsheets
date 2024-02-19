# CS2106 Notes AY23/24 Sem2

-   [CS2106 Notes AY23/24 Sem2](#cs2106-notes-ay2324-sem2)
    -   [Operating Systems](#operating-systems)
        -   [Operating System Structure](#operating-system-structure)
        -   [Running OSes](#running-oses)
    -   [Process Management](#process-management)
    -   [Process Abstraction](#process-abstraction)
        -   [Component Description](#component-description)
        -   [Basic Instruction Execution](#basic-instruction-execution)
        -   [Memory Context](#memory-context)
            -   [Function Call](#function-call)
            -   [Dynamically Allocated Memory](#dynamically-allocated-memory)
        -   [OS Context](#os-context)
            -   [Processes](#processes)
    -   [Process Scheduling](#process-scheduling)
        -   [Concurrent Execution](#concurrent-execution)
        -   [Process Scheduling Algorithms](#process-scheduling-algorithms)

## Operating Systems

-   Operating system: A program that acts as an intermediary between a computer user and the computer hardware.
-   Motivation for OS
    1. Abstraction:
        - Hide the different low level details
        - Present the common high level functionality to user
    2. Resource Allocator:
        - Manages all resources: CPU,Memory,Input/Outputdevices
        - Arbitrate potentially conflicting requests: for efficient and fair resource use
    3. Control Program:
        - Controls execution of programs: prevent errors and improper use of the computer and provides security and protection
-   ![viewOfOs](viewOfOs.png)
-   ![osComponents](osComponents.png)

### Operating System Structure

-   A **monolithic** kernel is an operating system architecture where the entire operating system is working in kernel space
    -   ![monolithicKernel](monolithicKernel.png)
-   A **microkernel** architecture is an operating system pattern where only basic functionality is provided in the core of the software system
    -   Inter-Process Communication (IPC)
    -   Address space management
    -   Thread management
    -   ![microkernelComponents](microkernelComponents.png)
-   **Layered systems**
    -   Generalization of monolithic system
    -   Organize the components into hierarchy of layers
        -   Upper layers make use of the lower layers
        -   Lowest layer is the hardware
        -   Highest layer is the user interface
-   **Client-Server Model**
    -   Variation of microkernel
    -   Two classes of processes:
        -   Client process request service from server process
        -   Server Process built on top of the microkernel
        -   Client and Server process can be on separate machine!

### Running OSes

-   Motivation
    -   Operating system assumes total control of the hardware
    -   Operating system is hard to debug/ monitor
-   Definition
    -   **Virtual machine**: a software emulation of hardware, also known as hypervisor
    -   ![type1Hypervisor](type1Hypervisor.png)
    -   ![type2Hypervisor](type2Hypervisor.png)

## Process Management

-   Process Abstraction
    -   Information describing an executing program
    -   Process/ Task/ Job is a dynamic abstracton for execution program
-   Process Scheduling
    -   Deciding which process get to execute
-   Inter-Process Communication & Synchronization
    -   Passing information between processes
-   Alternative to Process
    -   Light-weight process aka Thread

## Process Abstraction

### Component Description

-   Memory
    -   Storage for instruction and data
-   Cache
    -   Duplicate part of the memory for faster access
    -   Usually split into instruction cache and data cache
-   Fetch unit
    -   Loads instruction from memory
    -   Location indicated by a special register: Program Counter (PC)
-   Functional units
    -   Carry out the instruction execution
    -   Dedicated to different instruction type
-   Registers
    -   Internal storage for the fastest access speed
    -   General purpose registers: accessible by user program
    -   Special register: program counter

### Basic Instruction Execution

-   Instruction X is fetched
    -   Memory location indicated by Program Counter
-   Instruction X dispatched to the corresponding Functional Unit
    -   Read operands if applicable, usually from memory or GPR
-   Result computed
    -   Write value if applicable n Usually to memory or GPR
-   Instruction X is completed
    -   PC updated for the next instruction

### Memory Context

#### Function Call

-   Stack memory
    -   The new memory region to store information during function invocation
    -   Information of function invocation is described by a stack frame
    -   Stack frame contains:
        -   Return address of the caller
        -   Arguments for the function
        -   Storage for local variables
    -   Top of stack region (first unused location) is indicated by a stack pointer
        -   Stack frame is added on top when a function is invoked
        -   Stack frame is removed from top when a function call ends
-   Function call convention (example scheme)
    -   ![stackFrameSetup](stackFrameSetup.png)
    -   ![stackFrameTeardown](stackFrameTeardown.png)
-   Frame pointer
    -   To facilitate the access of various stack frame items
    -   Points to a fixed location in a stack frame
-   Saved register
    -   Number of general purpose registers on most processors are limited
    -   When GPRs are exhausted, use memory to hold the GPR value, then reuse GPR, value held can be restored afterwards (known as register spilling)

#### Dynamically Allocated Memory

-   Acquire new memory space during execution time - malloc()
-   Observations
    -   Memory is allocated only at runtime (size is not known during compilation) -> cannot place in data region
    -   No definite deallocation timing (can be explicitly freed by programmer) -> cannot place in stack region
-   Solution: set up a separate heap memory region
-   ![heapMemory](heapMemory.png)
-   Memory context: text, data, stack and heap
-   Hardware context: general purpose register, program counter, stack pointer, stack frame pointer

### OS Context

#### Processes

-   Process Identification & Process States
    -   ![processStateModel](processStateModel.png)

1. New
    - New process created
    - May still be under initialisation
2. Ready
    - Process is waiting to run
3. Running
    - Process being executed on CPU
4. Blocked
    - Process waiting for event
    - Cannot execute until event is available
5. Terminated
    - Process has finished execution, may require OS cleanup

-   Process Table & Process Control Block:

    -   Entire execution context for a process
    -   Kernel maintains PCB for all processes

-   System calls

    -   Application program interface (API) to OS
        -   Provides way of calling facilities/ services in kernel
        -   Not the same as normal function call (have to change from user mode to kernel mode)

    1. User program invokes the library call (normal function call)
    2. Library call (usually in assembly code) places the system call number in a designated location E.g. Register
    3. Library call executes a special instruction to switch from user mode to kernel mode (commonly known as TRAP)
    4. Now in kernel mode, the appropriate system call handler is determined:
        - Using the system call number as **index**
        - This step is usually handled by a **dispatcher**
    5. System call handler is executed: Carry out the actual request
    6. System call handler ended:
        - Control return to the library call
        - Switch from kernel mode to user mode
    7. Library call return to the user program: via normal function return mechanism

    -   ![systemCallMechanism](systemCallMechanism.png)

-   Exception and Interrupt
    -   Exception is **synchronous**: occur due to program execution
        -   Have to execute an exception handler
        -   Similar to a forced function call
    -   Interrupt is **asynchronous**: events that occur independent of program execution
        -   Program execution is suspended
        -   Have to execute an interrupt handler
    -   ![exceptionInterruptHandler](exceptionInterruptHandler.png)

## Process Scheduling

### Concurrent Execution

-   Concurrent processes
    -   Logical concept to cover multitasked processes
    -   ![simplisticConcurrency](simplisticConcurrency.png)
    -   ![interleavedContextSwitch](interleavedContextSwitch.png)
-   Terminology
    -   Scheduler: Part of the OS that makes scheduling decision
    -   Scheduling algorithm: The algorithm used by scheduler
-   Processing environment
    -   Batch processing
        -   No user: no interaction required, no need to be responsive
    -   Interactive
        -   With active user interacting with system
        -   Should be responsive, consistent in response time
    -   Real time processing
        -   Have deadline to meet
        -   Usually periodic process
-   Criteria for all processing environments
    -   Fairness
        -   Should get a fair share of CPU time
        -   No starvation
    -   Balance
        -   All parts of computing system should be utilised
-   Types of scheduling policies
    -   Non-preemptive (cooperative)
        -   A process stayed scheduled in running state until it blocks or gives up the CPU voluntarily
    -   Preemptive
        -   A process is given a fixed time quota to run (possible to block or give up early)

### Process Scheduling Algorithms

-   Criteria for batch processing
    n Turnaround time:
    q Total time taken, i.e. finish-arrival time
    q Related to waiting time: time spent waiting for CPU
    n Throughput:
    q Number of tasks finished per unit time q i.e. Rate of task completion
    n CPU utilization:
    q Percentage of time when CPU is working on a task
    page 16
