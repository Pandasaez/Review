# QUIZ 1

* Mac OS X Lion: 2011
* UNIX: Late 1970 
* Windows 98: 1998
* Windows NT: 1993
* Red Hat (Linux distribution): 1994
* Linux: 1991 
* IBM PC DOS: 1981
* DOS (Microsoft Disk Operating System): 1981
* Mac OS: System 1 - 1984
* Berkeley  1970s
* Android: 2008
* Ubuntu: 2004
* IBSYS: 1960s 
* MIT's Tape Director: 1960s 


# QUIZ 2
Determine the function of each computer system component.

1. dictates how the memory, input-output devices, arithmetic logic unit, etc. should behave. - Control Unit
2. It transfers data throughout the computer as required, including from the storage unit to the central processing unit and vice versa. - Bus
3. The control unit transfers data from the storage unit to ___________________ when calculations need to be performed. - Arithmetic Unit
4. provides the results of the computer process to the users, i.e., it links the computer with the external environment. - Output Unit
5. It can perform operations like addition, subtraction, multiplication, division, etc. - Arithmetic Unit
6. It is traditionally divided into primary storage and secondary storage. - Memory
7. It takes data from the input devices, converts it into machine language, and then loads it into the computer system. - Input Unit
8. Contains many computer components that are used to store data. - Storage Unit
9. Keyboard, mouse, etc., are the most commonly used input devices. - Input Unit
10. This unit controls all the other units of the computer system and so is known as its central nervous system. - Control Unit
11. All the calculations related to the computer system are performed by the arithmetic logic unit. - Arithmetic Unit
12. The different devices are monitors, printers, speakers, headphones, etc. - Output Unit
13. It takes data from the input devices, converts it into machine language, and then loads it into the computer system. - Input Unit
14. It can perform operations like addition, subtraction, multiplication, division, etc. - Arithmetic Unit
15. Dictates how the memory, input-output devices, arithmetic logic unit, etc. should behave. - Control Unit


### Q1
    refers to an early type of processing in which the user would
    submit a job (program, data, and control information about the nature
    of the job (usually on cards)) to an operator [Batch]

### Q2
    Similar to simple batch except that the computer
    executes jobs from a pool of jobs that have been loaded into the memory. [Multi-programmed batch]

### Q3
    Stores data and programs.[main memory]

### Q4
    Moves data between system and external environment
    (secondary memory devices - disks, terminals, etc) [i/o Module]

### Q5
    Carries out the operation of the computer. [processor]

### Q6
     Provides communication among system components. [system bus]

### Q7
    consists of at least one Arithmetic Logic Unit (ALU) and several
    registers. [Pro]

### Q8
    contains the address of the next instruction to be fetched from memory. [PC – Program Counter]

### Q9
    Address in I/O buffer of data to be moved [I/O BR]

### Q10 
    contains the instruction most recently fetched. [R – Instruction Register, ]

# QUIZ 3

### Q1
    What is the process state where PCB is being created and initialized? [New]

### Q2
    What states is where the process is waiting for some event to occur (such as I/O completion or receiving a signal). [Waiting (Blocked)]

### Q3
    What is the address of the next instruction to be executed in the process?[Program Counter ]

### Q4
    What is a PCB component where states like new, running, waiting, ready, or terminated are included? [Process State]

### Q5
    What term is used for CPU time, elapsed time, run time limit, etc? [Accounting Information]

### Q6
     When a program is loaded into the memory and it becomes a process, it can be divided into how many sections? [4]

### Q7
    What is the dynamically allocated memory to process during its run time? [Heap]

### Q8
    Which of the following includes the current activity represented by the value of Program Counter and the contents of the processor's registers? [Stack]

### Q9
    Which of the following contains the temporary data such as method/function parameters, return address, and local variables? [Stack]

### Q10 
    What PCB information indicates the address of the next instruction to be executed for this process? [Program Counter]

# QUIZ 4

### Q1
    Scheduler does not wait for an I/O request or an interrupt to move a job from the running queue to the ready queue. [Preemptive]

### Q2
    When the CPU becomes idle, a job from the Ready Queue is selected to run. [Short Term]

### Q3
    The following are the jobs of short term scheduler, except one, which is it?.[Because it is called infrequently, it can take time to decide which processes should be selected for execution]

### Q4
    Which of the following is one of the job of Long Term Scheduler? [Operates less frequently. ]

### Q5
    The amount of time that from submission of the job to its first response to the user. Good response time is important in time sharing systems. [Response time]

### Q6
    Keep the CPU as busy as possible. In a real system a light load is about 40%, heavy 90%. [CPU Utilization]

### Q7
    The job in the ready queue with the shortest next CPU burst is selected [Shortest Job First]

### Q8
    FCFS algorithm in which each process in the ready queue is preempted after a short time (time quantum). [Round Robin]

### Q9
    Processes are served in the order they are received. Can be implemented with a FIFO queue. [First Come First Serve ]

### Q10 
    Process execution alternates between periods of CPU use and I/O waiting. [CPU - I/O burst]

### Q11
    This is a measure of how long a process spends in the system. It is the time from when the process is submitted to completion. [Turnaround time]

### Q12
    The scheduling algorithm does not effect the amount of time spent executing or doing I/O; it only affects the time spent in the ready queue. Waiting time is the sum of time periods waiting in the ready queue. [Waiting time]

### Q13
    Which of the following puts intense load on CPU? [Simulation]

### Q14
    Which of the following has intense usage in a game? [Both CPU and I/O]

### Q15
    what is the changing of process states? [Context Switching]

# QUIZ 5

### Q1
    A _____ is a flow of execution through the process code, with its own program counter that keeps track of which instruction to execute next, system registers that hold its current working variables, and a stack that contains the execution history. [Thread]

### Q2 
    Advantages of Thread except; [It is more economical to create and context switch threads.]

### Q3
    Thread is light weight, taking lesser resources than a process.
    Process is heavy weight or resource intensive. [True]

### Q4
    In multiple processing environments, each process executes the same code but has its own memory and file resources. Multiple threaded processes use fewer resources.[True]

### Q5
    In this case, the thread management kernel is not aware of the existence of threads. The thread library contains code for creating and destroying threads, for passing message and data between threads, for scheduling thread execution and for saving and restoring thread contexts. The application starts with a single thread. [User Level Threads ]

### Q6 
    In this case, thread management is done by the Kernel. There is no thread management code in the application area. Kernel threads are supported directly by the operating system. Any application can be programmed to be multithreaded. All of the threads within an application are supported within a single process. [Kernel Level Threads]

### Q7
    Multithreading Models except; [One to Many relationship ]

### Q8
    User-level threads are slower to create and manage.
    Kernel-level threads are faster to create and manage. [ False ]

### Q9 
    User-level thread is generic and can run on any operating system.
    Kernel-level thread is specific to the operating system. [True]

### Q10
    Multi-threaded applications cannot take advantage of multiprocessing.
    Kernel routines themselves can be multithreaded. [True]

# QUIZ 6

### Q1
    _____ is the functionality of an operating system that handles or manages primary memory and moves processes back and forth between main memory and disk during execution. [Memory management]

### Q2
    The set of all logical addresses generated by a program is referred to as a logical address space.[True]    

### Q3
    The set of all symbolic addresses corresponding to these logical addresses is referred to as a physical address space. [False]

### Q4
    _____ is a mechanism in which a process can be interchanged temporarily out of main memory (or move) to secondary storage (disk) and make that memory available to other processes. At some later time, the system swaps back the process from the secondary storage to main memory.[Swapping]

### Q5
    As processes are loaded and removed from memory, the free memory space is broken into little pieces. It happens after sometimes that processes cannot be allocated to memory blocks considering their small size and memory blocks remains unused. This problem is known as _____. [Fragmentation]

### Q6
    External fragmentation: Total memory space is enough to satisfy a request or to reside a process in it, but it is not contiguous, so it cannot be used. [True]

### Q7
    _____ is a memory management technique in which process address space is broken into blocks of the same size called pages [Paging]

### Q8
    Internal fragmentation: Memory block assigned to process is bigger. Some portion of memory is left unused, as it cannot be used by another process. [True]
    
### Q9
    _____ is a memory management technique in which each job is divided into several segments of different sizes, one for each module that contains pieces that perform related functions. Each segment is actually a different logical address space of the program. [Segmentation]

### Q10
    When _____ is used, it is not required to link the actual module or library with the program, rather a reference to the dynamic module is provided at the time of compilation and linking. [Dynamic Linking]

# QUIZ 7

### Q1
    _____ is one with which the driver communicates by sending and receiving single characters (bytes, octets). For example, serial ports, parallel ports, sounds cards etc. [Character Device]

### Q2
    The process of periodically checking status of the device to see if it is time for the next I/O operation, is called Interrupt. [False]

### Q3
    Device drivers are software modules that can be plugged into an OS to handle a particular device. Operating System takes help from device drivers to handle all I/O devices. [True]

### Q4
    An _____ is required to take an application I/O request and send it to the physical device, then take whatever response comes back from the device and send it to the application. [I/O system]
    
### Q5
    This uses CPU instructions that are specifically made for controlling I/O devices. These instructions typically allow data to be sent to an I/O device or read from an I/O device. [Special Instruction I/O]

### Q6
    Synchronous I/O − I/O proceeds concurrently with CPU execution
    Asynchronous I/O − In this scheme CPU execution waits while I/O proceed [False]

### Q7
    When using _____, the same address space is shared by memory and I/O devices. The device is connected directly to certain main memory locations so that I/O device can transfer block of data to/from memory without going through CPU. [Memory-mapped I/O]

### Q8
    A _____ is one with which the driver communicates by sending entire blocks of data. For example, Hard disks, USB cameras, Disk-On-Key etc.[Block Device ]

### Q9
    The Device Controller works like a processor between a device and a device driver. I/O units (Keyboard, mouse, printer, etc.) typically consist of a mechanical component and an electronic component where electronic component is called the device controller. [False]

### Q10
    _____ means CPU grants I/O module authority to read from or write to memory without involvement. _____ module itself controls exchange of data between main memory and the I/O device. [Direct Memory Access]


# May we all Pass Our Finals 
    

