                COMPUTER ARCHITECTURE
Computer architecture is the design and organization of a computer system, including its processor, memory, instruction set, data paths, and input/output mechanisms.
It describes how hardware components work together to execute programs and process data.
  Main objectives;
- Improve processing speed and performance.
- Optimize memory usage and data access.
- Reduce power consumption and hardware cost.
- Improve reliability and scalability.
- Support efficient execution of software.
  Computer architecture vs computer organization;
- Computer architecture: describes what a computer does from the programmer's perspective, including instruction sets, data types, registers, and addressing modes.
- Computer organization: describes how the architecture is physically implemented, including control units, buses, memory technology, and hardware connections.
Example: The instruction set is part of architecture, while the internal circuitry used to execute an instruction is part of organization.

 BASIC COMPUTER SYSTEM STRUCTURE;
A computer system consists of five major functional units:
1. Input unit: receives data and instructions.
2. Memory unit: stores programs, data, and intermediate results.
3. Arithmetic Logic Unit (ALU): performs arithmetic and logical operations.
4. Control Unit (CU): directs and coordinates processor operations.
5. Output unit: presents processed information.
The CPU consists primarily of the ALU, control unit, and registers.
  Basic computer operation;
Input → Processing → Storage → Output
The processor fetches instructions from memory, decodes them, executes them, and stores or outputs the results.

 CENTRAL PROCESSING UNIT (CPU)
The CPU is the main processing component of a computer. It executes program instructions and coordinates system operations.
  Arithmetic Logic Unit (ALU);
Performs arithmetic and logical operations.
Arithmetic operations:
- Addition and subtraction.
- Multiplication and division.
- Increment and decrement.
Logical operations:
- AND, OR, NOT, XOR.
- Comparisons (equal, greater than, less than).
- Bit shifting and rotation.
  Control Unit (CU);
Controls the execution of instructions and coordinates data movement between CPU components, memory, and I/O devices.
Functions:
- Fetches instructions from memory.
- Decodes instructions.
- Generates control signals.
- Coordinates ALU operations.
- Controls memory read/write operations.
- Manages instruction sequencing.
  CPU Registers;
Registers are small, high-speed storage locations inside the processor.
Important registers:
- Program Counter (PC): stores the address of the next instruction to be fetched.
- Instruction Register (IR): holds the current instruction being decoded or executed.
- Memory Address Register (MAR): holds the address of the memory location being accessed.
- Memory Data Register (MDR): temporarily holds data being transferred to or from memory.
- Accumulator (ACC): stores intermediate arithmetic and logical results in some architectures.
- General-Purpose Registers (GPRs): store operands, addresses, and temporary results.
- Stack Pointer (SP): points to the current top of the stack.
- Status/Flag Register: stores condition flags such as zero, carry, sign, and overflow.
Registers are generally faster than cache and main memory.

 INSTRUCTION CYCLE (FETCH–DECODE–EXECUTE)
The instruction cycle is the sequence of operations the CPU performs to execute instructions.
  Stage 1: Fetch;
- The PC contains the address of the next instruction.
- The address is transferred to the MAR.
- The instruction is read from memory into the MDR.
- The instruction is transferred to the IR.
- The PC is updated to the next instruction address, unless the architecture uses another sequencing mechanism.
  Stage 2: Decode;
The control unit interprets the instruction to determine:
- The operation to perform.
- Required operands.
- Source and destination registers.
- Addressing mode.
- Necessary control signals.
  Stage 3: Execute;
The CPU performs the required operation using the ALU, registers, memory, or other functional units.
  Stage 4: Store/Write-back;
The result is written into the destination register or memory location where required.
The cycle repeats until the program terminates or execution is interrupted.

 INSTRUCTION SET ARCHITECTURE (ISA)
An Instruction Set Architecture is the interface between software and processor hardware.
It defines the instructions a processor can execute and how software interacts with the hardware.
An ISA specifies:
- Instruction formats and operations.
- Registers and their functions.
- Data types and sizes.
- Addressing modes.
- Memory access rules.
- Exception and interrupt behavior.
- Supported execution modes.
  Common instruction categories;
1. Data transfer: MOV, LOAD, STORE.
2. Arithmetic: ADD, SUB, MUL, DIV.
3. Logical: AND, OR, XOR, NOT.
4. Control transfer: JMP, CALL, RET, conditional branches.
5. Comparison: CMP, TEST.
6. Shift operations: SHL, SHR, ASR.
  Instruction format;
A machine instruction may contain:
- Opcode: specifies the operation.
- Operand fields: identify data sources and destinations.
- Addressing information: specifies how operands are accessed.
Example:
ADD R1, R2, R3
Meaning: R1 = R2 + R3.
The exact syntax and operand ordering depend on the ISA.

 TYPES OF COMPUTER ARCHITECTURE
  Von Neumann architecture;
Uses a common memory space for both program instructions and data.
Main components:
- CPU.
- Main memory.
- Input/output units.
- Communication buses.
Advantages:
- Simple design.
- Flexible memory use.
- Programs can be stored and modified in memory.
Disadvantage:
- Instructions and data share the same memory pathway, which can create the Von Neumann bottleneck.
  Harvard architecture;
Uses separate instruction and data memories, often with separate pathways.
Advantages:
- Instructions and data can be accessed simultaneously.
- Improved throughput in suitable systems.
- Useful in microcontrollers and digital signal processors.
Disadvantages:
- More complex design.
- Separate memory spaces can reduce flexibility.
  Modified Harvard architecture;
Combines aspects of both architectures. It commonly uses separate instruction and data caches with a shared main memory.
Found in many modern processors.

 COMPUTER DATA REPRESENTATION
Computers represent information using binary digits (bits).
  Units of data;
- Bit: one binary digit (0 or 1).
- Nibble: 4 bits.
- Byte: 8 bits.
- Word: the processor's natural data-processing unit; its size depends on the architecture.
- Kilobyte (KB): commonly 1,000 bytes.
- Megabyte (MB): 1,000 KB.
- Gigabyte (GB): 1,000 MB.
- Terabyte (TB): 1,000 GB.
In binary-based memory calculations, KiB = 1,024 bytes, MiB = 1,024 KiB, and GiB = 1,024 MiB.
  Number systems;
- Binary: base 2 (0, 1).
- Octal: base 8 (0–7).
- Decimal: base 10 (0–9).
- Hexadecimal: base 16 (0–9, A–F).
Example:
Binary: 1010₂
Decimal: 10₁₀
Hexadecimal: A₁₆
  Signed number representation;
Common methods:
- Sign-magnitude representation.
- One's complement.
- Two's complement.
Two's complement is widely used for signed integer representation.
For an n-bit two's complement number, the representable range is:
- Minimum: −2⁽ⁿ⁻¹⁾
- Maximum: 2⁽ⁿ⁻¹⁾ − 1
Example: An 8-bit signed integer has a range of −128 to +127.
  Floating-point representation;
Floating-point numbers represent very large or very small real numbers.
A common IEEE 754 representation consists of:
- Sign bit.
- Exponent.
- Fraction (significand).
For a normalized binary floating-point value:
    Value = (−1)ˢ × 1.F × 2⁽ᴱ⁻ᴮ⁾
Where:
- S = sign bit.
- F = fraction.
- E = stored exponent.
- B = exponent bias.
Common formats:
- Single precision: 32 bits.
- Double precision: 64 bits.

 MEMORY HIERARCHY
Computer memory is organized according to speed, capacity, cost, and proximity to the CPU.
Typical hierarchy from fastest to slowest:
1. CPU registers.
2. Cache memory.
3. Main memory (RAM).
4. Secondary storage (SSD/HDD).
5. Archival storage.
As we move down the hierarchy:
- Storage capacity generally increases.
- Cost per bit generally decreases.
- Access time generally increases.
  Cache memory;
Cache is small, high-speed memory located in or near the processor. It stores frequently or recently accessed instructions and data.
Cache levels:
- L1: smallest and generally fastest.
- L2: larger, generally slower than L1.
- L3: generally larger and slower than L2; often shared among CPU cores.
Important concepts:
- Cache hit: requested data is found in cache.
- Cache miss: requested data is not found in cache.
- Hit rate: fraction of accesses resulting in cache hits.
- Miss rate: fraction of accesses resulting in cache misses.
Hit rate = Cache hits / Total cache accesses
Miss rate = 1 − Hit rate
  Random Access Memory (RAM);
RAM stores programs and data currently being used.
Characteristics:
- Read and write access.
- Generally volatile.
- Directly accessible by the processor through the memory system.
Types:
- SRAM: fast, expensive, commonly used in cache.
- DRAM: denser and cheaper, commonly used as main memory.
  Read Only Memory (ROM);
Non-volatile memory used to store firmware and other persistent information.
Types include:
- PROM.
- EPROM.
- EEPROM.
- Flash memory.
  Secondary storage;
Provides long-term, non-volatile data storage.
Examples:
- HDD: magnetic storage using rotating disks.
- SSD: flash-based storage with no moving mechanical parts.
- USB flash drives.
- Memory cards.

 SYSTEM BUSES
A bus is a communication pathway that transfers information between computer components.
Three main bus categories:
  Data bus;
Transfers actual data between the CPU, memory, and I/O devices.
Its width affects how much data can be transferred in parallel.
  Address bus;
Carries the address of the memory location or I/O location being accessed.
For a system with n address bits, the number of distinct addressable locations is:
    2ⁿ
For example, a 16-bit byte-addressed system can address 2¹⁶ = 65,536 bytes.
  Control bus;
Carries control and timing signals, including:
- Read.
- Write.
- Clock.
- Interrupt.
- Reset.

 ADDRESSING MODES
Addressing modes specify how an instruction locates its operands.
Common modes:
1. Immediate addressing: operand value is included directly in the instruction.
   Example: MOV R1, #10.
2. Register addressing: operand is stored in a CPU register.
   Example: ADD R1, R2.
3. Direct addressing: instruction contains the memory address of the operand.
4. Indirect addressing: instruction refers to a location or register containing the operand's address.
5. Indexed addressing: effective address is obtained by adding an index to a base address.
6. Base/displacement addressing: effective address = base register + displacement.
7. Relative addressing: target address is calculated relative to the current instruction address or program counter, according to the ISA.
Addressing modes provide flexibility in accessing variables, arrays, pointers, and program data.

 RISC AND CISC ARCHITECTURES
  RISC (Reduced Instruction Set Computer);
Designed around a relatively simple and regular instruction set.
Characteristics:
- Often uses simple, fixed-length instructions.
- Typically uses load/store architecture.
- Large register files are common.
- Designed for efficient instruction execution and pipelining.
Examples: ARM and RISC-V.
  CISC (Complex Instruction Set Computer);
Supports a rich instruction set, including instructions that can perform complex operations.
Characteristics:
- Often supports multiple addressing modes.
- May use variable-length instructions.
- Some instructions can perform multiple low-level operations.
- Instruction decoding can be more complex.
Example: x86 architecture.
Modern processors may combine features of both approaches internally.

  PIPELINING
Pipelining is a CPU technique that improves instruction throughput by overlapping the execution stages of multiple instructions.
A typical five-stage pipeline:
1. IF – Instruction Fetch.
2. ID – Instruction Decode/Register Read.
3. EX – Execute.
4. MEM – Memory Access.
5. WB – Write Back.
Instead of completing one instruction before starting another, different instructions occupy different stages simultaneously.
  Pipeline hazards;
1. Structural hazard: two instructions require the same hardware resource simultaneously.
2. Data hazard: an instruction depends on the result of a previous instruction.
3. Control hazard: caused by branches and changes in instruction flow.
Solutions include:
- Pipeline stalls.
- Forwarding/bypassing.
- Branch prediction.
- Resource duplication.
- Instruction scheduling.
Ideal pipeline speedup for k stages approaches k under suitable conditions and a sufficiently long instruction stream, but actual performance is affected by hazards and stage imbalance.

 MULTICORE AND PARALLEL PROCESSING
A multicore processor contains two or more processing cores on one chip.
Each core can execute instructions independently, allowing parallel execution.
Important concepts:
- Core: an individual processing unit within a CPU.
- Thread: a sequence of program instructions that can be scheduled for execution.
- Multithreading: supports execution of multiple threads.
- Parallel processing: performs multiple computational tasks simultaneously.
- Multiprocessing: uses multiple processing units or processors.
Advantages:
- Higher potential throughput.
- Improved multitasking.
- Better performance for parallel applications.
- Improved energy efficiency in some workloads.
Limitations:
- Not every program can be parallelized.
- Synchronization introduces overhead.
- Shared resources can cause contention.
- Communication between cores can create latency.

 INPUT/OUTPUT (I/O) ORGANIZATION
I/O systems allow the computer to communicate with external devices.
Examples:
- Keyboard and mouse.
- Display and printer.
- Sensors and actuators.
- Storage devices.
- Network interfaces.
  I/O transfer methods;
1. Programmed I/O: CPU repeatedly checks device status and transfers data.
2. Interrupt-driven I/O: device signals the CPU when it needs attention.
3. Direct Memory Access (DMA): a DMA controller transfers blocks of data between devices and memory with limited CPU involvement.
DMA is useful for high-volume data transfers.
  Interrupts;
An interrupt is a signal that temporarily causes the processor to suspend its current instruction flow and execute an interrupt service routine (ISR).
Types include:
- Hardware interrupts.
- Software interrupts.
- Exceptions.
The processor saves the necessary execution state and resumes the interrupted program after handling the event.

 COMPUTER PERFORMANCE
Computer performance measures how efficiently a system executes tasks.
  CPU execution time;
    CPU time = Instruction Count × CPI × Clock Cycle Time
Where:
- Instruction Count = number of instructions executed.
- CPI = average clock cycles per instruction.
- Clock Cycle Time = duration of one clock cycle.
Since clock cycle time = 1 / Clock Frequency:
    CPU Time = (Instruction Count × CPI) / Clock Frequency
  CPU performance;
Performance is inversely proportional to execution time.
    Performance = 1 / Execution Time
Speedup
    Speedup = Old Execution Time / New Execution Time
Example:
If a task takes 10 seconds on one system and 5 seconds on another:
    Speedup = 10/5 = 2
The second system is twice as fast for that task.
  Amdahl's Law;
Describes the maximum speedup achievable when only part of a program can be improved through parallel processing.
    Speedup = 1 / [(1 − P) + (P/N)]
Where:
- P = fraction of the program that can be parallelized.
- N = number of processing units.
The non-parallelizable part limits overall speedup.

 VIRTUAL MEMORY
Virtual memory is a memory-management technique that gives each process a virtual address space, which the operating system maps to physical memory.
Important concepts:
- Virtual address: address generated by a program.
- Physical address: actual location in RAM.
- Page: fixed-size block of virtual memory.
- Frame: fixed-size block of physical memory.
- Page table: stores mappings between virtual pages and physical frames.
- Page fault: occurs when a required page is not currently available in physical memory.
- TLB (Translation Lookaside Buffer): a small, fast cache that stores recent virtual-to-physical address translations.
Advantages:
- Supports large virtual address spaces.
- Provides process isolation.
- Improves memory utilization.
- Allows programs to operate without requiring all their pages to be resident in RAM simultaneously.
Excessive page faults can cause thrashing, significantly reducing performance.

 MULTILEVEL MEMORY AND STORAGE CONCEPTS
Important memory technologies and concepts:
- Volatile memory: loses stored information when power is removed.
- Non-volatile memory: retains information without power.
- Latency: time taken to access data.
- Bandwidth: amount of data transferred per unit time.
- Memory capacity: total amount of information that can be stored.
- Locality of reference: programs tend to reuse recently accessed data and access nearby memory locations.
Types of locality:
1. Temporal locality: recently accessed data is likely to be accessed again.
2. Spatial locality: data near recently accessed locations is likely to be accessed.
Locality is the main reason cache memory improves performance.

 MODERN PROCESSOR ARCHITECTURE
Modern processors include several advanced features:
- Superscalar execution: executes multiple instructions in one clock cycle using multiple execution units.
- Out-of-order execution: executes independent instructions when their operands and resources are ready, rather than strictly following program order.
- Branch prediction: predicts the outcome of branch instructions to keep the pipeline busy.
- Speculative execution: executes predicted instruction paths before the prediction is confirmed.
- SIMD (Single Instruction, Multiple Data): performs the same operation on multiple data elements.
- GPU (Graphics Processing Unit): contains many processing units designed for highly parallel workloads.
- System-on-Chip (SoC): integrates CPU cores, memory controllers, I/O interfaces, and other components onto one chip.
These techniques improve performance in modern computers, smartphones, embedded systems, and high-performance computing systems.

 IMPORTANT COMPUTER ARCHITECTURE FORMULAS
1. Number of binary combinations:
   N = 2ⁿ
2. Addressable memory locations:
   Locations = 2ⁿ
   (for n address bits)
3. Memory capacity:
   Capacity = Number of locations × Bits per location
4. CPU execution time:
   CPU Time = Instruction Count × CPI × Clock Cycle Time
5. Clock cycle time:
   T = 1 / f
6. CPU execution time using clock frequency:
   CPU Time = (Instruction Count × CPI) / f
7. Average CPI:
   CPI = Total clock cycles / Total instructions
8. Cache hit rate:
   Hit Rate = Cache Hits / Total Accesses
9. Cache miss rate:
   Miss Rate = 1 − Hit Rate
10. Speedup:
    Speedup = Old Execution Time / New Execution Time
11. Amdahl's Law:
    Speedup = 1 / [(1 − P) + (P/N)]
12. n-bit unsigned integer range:
    0 to 2ⁿ − 1
13. n-bit signed two's complement range:
    −2⁽ⁿ⁻¹⁾ to 2⁽ⁿ⁻¹⁾ − 1

 IMPORTANT EXAM TIPS
1. Clearly distinguish computer architecture from computer organization.
2. Know the functions of the ALU, control unit, and CPU registers.
3. Understand the fetch–decode–execute cycle in the correct order.
4. Distinguish Von Neumann architecture from Harvard architecture.
5. Memorize the memory hierarchy and understand why cache is faster than RAM.
6. Practise binary, hexadecimal, and two's complement conversions.
7. Understand the roles of data, address, and control buses.
8. Differentiate RISC and CISC architectures.
9. Understand pipeline stages and the three major pipeline hazards.
10. Practise CPU execution-time, CPI, clock-frequency, and speedup calculations.
11. Distinguish programmed I/O, interrupt-driven I/O, and DMA.
12. Understand the difference between virtual memory and physical memory.
13. Remember that increasing clock frequency alone does not guarantee better overall performance; CPI, instruction count, memory behavior, and processor design also matter.

CORE PRINCIPLE: Computer architecture explains how a computer's processor, memory, instruction set, buses, and I/O systems are designed and coordinated to execute instructions, process information, and deliver computational performance.