# ISTE-190 - Operating Systems

## Basics
* Operating system (OS) provides hardware resources and management services to applications
* Hardware includes:
 * Processor
 * Main memory
 * External memory (disk)
 * Attached devices (mouse, keyboard, touchpads, displays, printers, etc.)

## Common operating systems
* Windows (Microsoft)
* OS X, iOS (Apple)
 * Based on UNIX (developed at AT&T Bell Labs)
* Linux
 * UNIX-like
 * Open source
 * Google Chrome based on Linux
 * [The best Linux operating system of all time?](https://fedoraproject.org)
* Android
 * Based on Linux kernel (Linux for mobile devices)
 * Open source
 * Kernel is central module of operating system
* IBM mainframe (server) operating systems
 * Also run Linux

## Principle contributions
* Abstractions
 * Hide details of hardware from user (including some, but not all, application developers) and from programs
 * Some types of programming requires detailed knowledge of hardware
* Examples of abstraction
 * Running a Java program requires no knowledge of how program is initiated, executed, and terminated
 * Developing program to read record requires no knowledge of how disks operate or the record's physical location on the disk
 * Sending a file to a printer requires no knowledge of how printer reads the file and prints the file's contents
* Big picture: OS overlaps in time as many computing operations as possible
 * Classic example is executing program B while program A is waiting for data from disk read operation
* Resource allocation
 * Processor resources (instruction execution)
 * Memory resources (main memory for instructions and data)
* Resource scheduling
* Resource sharing
 * Multiple users
 * Multiple programs
 * Multiple cores

## Device drivers
* Example of abstraction
* Software that provides interface between operating system and device connected to computing system
* Integrated into operating system
 * Many device drivers present in operating system out of the box
 * Others added in automatically by OS or by users as new devices are added to system over time
* Operating system specific
* Hardware specific
* Translates operating system instructions into format device understands
 * When program needs to use connected device, program instruction is intercepted by the OS (e.g. PRINT)
 * OS then sends information and instructions to device driver
* Physical details of the device are hidden

### Example: Print driver
* Program wants to print to specific printer
* Program executes print request that is intercepted by the OS
* OS locates the print file and sends file to printer driver
* Printer driver translates the file contents with accompanying formatting codes and printing instructions into print commands
 * Such as: black and white, greyscale, color; single or double-sided; stapled; number of copies; etc.
* Print commands sent to printer controller, which is hardware component of device
* Programmer (and the program) are not concerned with the physical operating details of the printer

## Resource allocation
* Program needs to reside in main memory to eventually be executed
* OS allocates main memory to a program
* Executing program is a process
* Process composed of tasks
 * Application program specific tasks
 * Generic tasks that support the execution of programs

## Resource scheduling
* OS schedules the execution of tasks
 * Maintains a task queue (an ordered list)
 * Selects tasks for execution by assigning the task to the CPU
* When process is complete, the OS de-allocates memory (returns memory to available main memory pool)

## Resource sharing
* Added OS complexity
* Multiple users of same system
 * Users need to be authenticated
 * Programs need to be assigned file privileges (read, write, execute, delete)
* Concurrent examples of programs
 * *Concurrent*: Sharing a processor's cycles and execution resources among several active processes and their tasks
 * Provides an illusion that processes and tasks are being executed in parallel
* Parallel execution
 * *Parallel*: Sharing the cycles and execution resources of several processors among several active processes and their tasks
 * Provides for true, simultaneous execution of processes and tasks
* Resource sharing in multi-core systems
 * OS assigns processes and their tasks to cores for parallel execution

## Threads
* *Thread*: Independence sequence of instructions
* Belongs to one and only one process
* Multi-threaded application contains several copies of a particular thread
* Threads can be executed concurrently or in parallel
* Multi-threading is an approach to increase the speed of process execution
* Can take advantage of multicore processors

## Threading example
* Program is written to develop a sum of a list of 1,000 numbers
* Single-threaded approach
 * For 1000 times...
 * ...read the next number in the list...
 * ...add to SUM.
* Multi-threaded approach
 * Create four threads
 * Each thread will develop a sum for 250 numbers
 * Each thread is identical, except a beginning and end position in the list
 * Thread:
 * > begin position
 * > end position
 * > read next number in list starting at beginning until end
 * > add to SUM
* When all four threads have completed execution, then program executes
* Grand total = thread 1 (SUM) + thread 2 (SUM) + thread 3 (SUM) + thread 4 (SUM)