# Class Notes August 27

Summary:
    [1. History of Computing](#1.-history-of-computing)
    2. Moore's Law and Rock's Law
    3.

## 1. History of Computing

    1st: Vacuum Tubes (1940 - 1956)
        - Large, high power, heat, hardware failures
        - Machine language only

    2nd: Transistors (1956 - 1963)
        - Smaller, less heat and power, faster
        - Assembly and early high-level (FORTRAN, COBOL)

    3rd: Integrated Circuit ICs (1964 - 1971)
        - Much smaller, higher speed, reduced cost
        - Operating Systems, multiprogramming, high-level languages

    4th: Microprocessors (1971 - Now)
        - Entire CPU on a single chip
        - PCs, very high speed, low cost and portable
        - High level and object oriented languages
        - GUI-based systems

    5th: AI and Quantum (Now - Future)
        - ULSI (ultra-large-scale integration)
        - Nanotechnology

## 2. Moore's Law and Rock's Law

    Moore's Law (1965): ICs transistors doubles every 18-24 months -> empirical observation.

    Rock's Law (Moore's Second Law): cost of building semiconductor fabrication plants doubles every 4 years.

## 3. What is a Modern Computer

    Electronic, digital, general purpose computing machine that automatically follows a step-by-step list of instructions (algorithm or computer program) to solve a problem.

    Three pieces:

    - Processor: interprets and executes
        - Registers and ALU (arithmetic and logic unit)
        - Control unit

    - Memory: store data and programs

    - Data input and output (I/O)

## 4. Measures of Computer Storage Capacity

    1 byte = 8 bits
    
    Kibibyte, mebibyte, gibibyte, tebibyte, etc
    Pebi, Exbi, zebi, yobi

## 5. Mearures of Processor Speed

    Clock Speed (Frequency) is measured in Hertz

    Hertz = clock cicles / second

    Primarily measured in GHz (10^9 Hz)

    Cycle time = 1/Cycle frequency

## 6. Measures of Time and Space

    Time: ms, µs, ns

    Space: mm, µm, nm
    
    Mili, Micro, Nano, Pico, Femto, Atto, Zepto, Yocto

## 7. Compiler Assembler, Linker, and Loader

    - **Compiler:** translates HLL code into assembly language or object (machine) code

    - **Assembler:** converts assembly into machine code
        Produces .o (object) file

    - **Linker:** combines multiple .o files into a single executable
        - Static Linking: libraries copied into executable.
        - Dynamic linking: libraries linked at runtime (slight runtime overhead, but smaller executables, easier library updates and shared memory usage).

    - **Loader:** part of the OS, loads the executable into memory for the CPU to run -> sequential pipeline for human-readable code to a running program

## 8. Computer Level Hierarchy

    Levels of abstraction: from phycical hardware (Digital Logic) up to User Level
    Each level hides the details of the level below it.
    Changes in lower levels do not affect upper levels if ISA is preserved.
    ISA: Instruction Set Architecture

    - Level 6: User
        Program execution and UI.
    - Level 5: HLL
        C, C++, Python, etc -> human-readable.
        Translated by compilers/interpreters.
    - Level 4: Assembly
        Translated by an assembler.
    - Level 3: System Software
        OS: manages hardware resources (CPU, memory, I/O) and provides a platform for applications.
        Compilers.
    - Level 2: Machine (ISA)
        Interface between hardware and software.
        Defines intructions, registers, data types, addressing modes, etc.

    - Level 1: Control
        How the ISA is implemented.
        Microprogram: program written in LLL that is implemented by the hardware.
        Hardwired: directly executes machine instructions.
    - Level 0: Digital Logic
        Transistors, logic gates, flip-flops.
        Circuits performing basic operations and implementing datapath and control.

## 9. von Neumann Modal

    Computer Architecture
    1945 John von Neumann

    - Main Components:
        - **CPU (Central Processing Unit):**
            - Arithmetic Logic Unit (ALU): performs arithmetic and logical operations
            - Control Unit (CU): interpret instructions and generates control signals
            - Registers: high-speed storage
                - Program Counter (PC): keeps track of the address of the next instruction to be executed
                - Instruction Register (IR): holds the current instruction being executed
                - Stack pointer (SP): holds the memory address of the "top" of the stack
                - General-purpose: temporary storage of data during processing

        - **Main Meory:**
            Stores both instructions and data.

        - **I/O Devices:**
            External hardware like keyboards, monitors, or storage devices.

        - **Bus:**
            Communication system -> transfers data, addresse, and control signals between the CPU, memory, and I/O devices.

        - **I/O Bus**: connects CPU and memory to I/O devices.

    - Major Limitation: von Neumann Bottleneck
        Single path between the CPU and main memory.

    - Program execution:
        Sequential instruction processing.
        Each instruction: fetch - decode - execute.

    - Key Characteristics:
        Single memory for data and instructions.
        Shared Bus (transferring data, addresses, and control signals, which can limit performance).
        Sequential Execution: one at a time in a sequential manner.

    - System Bus
        Data Bus: transfers actual data or instructions between components (bidirectional).
        Address Bus: carries the address to be accessed from the CPU to the memory or I/O controller (unidirectional).
        Control Bus: transmits control signals from CPU to other components and status signals back to the CPU, controlling and coordinating operations (read/write signals, interrupt requests, etc) (bidirectional).
