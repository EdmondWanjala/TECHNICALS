                    MEMORY
Computer memory is the storage system used to hold data, instructions and results required by a computer or digital system.
  It stores:
- Program instructions.
- Input data.
- Intermediate processing results.
- Final output data.
- System configuration and firmware.
Memory is essential because the CPU needs fast access to instructions and data during execution.
  Basic memory operations:
1. Read: Retrieve stored information.
2. Write: Store new information.
3. Addressing: Identify a specific memory location.
4. Storage: Retain information in binary form.
  Memory stores information using binary digits (bits):
- Bit: Smallest unit of information (0 or 1).
- Nibble: 4 bits.
- Byte: 8 bits.
- Word: A group of bits processed as a unit by a processor.

 MEMORY ORGANIZATION
Memory consists of multiple storage locations, each identified by a unique address.
 Important terms:
- Memory cell: Basic unit capable of storing one bit.
- Memory location: A group of bits stored at one address.
- Address: Unique identifier of a memory location.
- Word length: Number of bits stored or processed as one word.
- Capacity: Total amount of information a memory can store.
- Access time: Time required to read or write data.
- Memory bandwidth: Amount of data transferred per unit time.
  Memory capacity:
If a memory has n address lines:
    Number of addressable locations = 2^n
If each location stores m bits:
    Total capacity = 2^n × m bits
Example:
A memory with 12 address lines and 8 bits per location:
    Number of locations = 2^12 = 4096
Capacity = 4096 × 8
         = 32768 bits
         = 4096 bytes
         = 4 KB
Memory units:
- 1 nibble = 4 bits
- 1 byte = 8 bits
- 1 KB = 1024 bytes (binary convention)
- 1 MB = 1024 KB
- 1 GB = 1024 MB
- 1 TB = 1024 GB
Note: In some storage specifications, KB, MB and GB use decimal multiples of 1000. KiB, MiB and GiB represent binary multiples of 1024.

 MEMORY CLASSIFICATION
Computer memory is broadly classified into:
-Primary Memory
-Secondary Memory
  PRIMARY MEMORY;
Primary memory is directly accessible by the CPU or its memory controller and is used to hold data and instructions currently needed by the system.
Types:
i. RAM (Random Access Memory)
RAM is a read-and-write memory that temporarily stores programs and data during computer operation.
Characteristics:
- Usually volatile.
- Supports both reading and writing.
- Provides relatively fast access.
- Stores active programs and working data.
- Contents are generally lost when power is removed.
Types of RAM:
a) SRAM (Static RAM)
Stores data using bistable flip-flop circuits.
Characteristics:
- Does not require periodic refreshing.
- Very fast.
- More expensive per bit.
- Lower storage density.
- Requires more transistors per bit.
Applications:
- CPU cache memory.
- High-speed buffers.
- Registers and specialized memory circuits.
b) DRAM (Dynamic RAM)
Stores data as electrical charge in capacitors, controlled by transistors.
Characteristics:
- Requires periodic refreshing because capacitor charge leaks.
- Slower than SRAM.
- Cheaper per bit.
- Higher storage density.
- Commonly used as main memory.
Applications:
- Computer main memory.
- Smartphones.
- Graphics memory (specialized DRAM variants).
SRAM vs DRAM:
SRAM:
- Flip-flop-based.
- No periodic refresh.
- Faster.
- More expensive.
- Lower density.
- Commonly used in cache.
DRAM:
- Capacitor-based.
- Requires refresh.
- Slower.
- Cheaper.
- Higher density.
- Commonly used in main memory.
ii. ROM (Read Only Memory)
ROM is non-volatile memory used to store data and instructions that must be retained without power.
Characteristics:
- Retains information without electrical power.
- Commonly stores firmware and boot instructions.
- Generally used for permanent or semi-permanent storage.
Types of ROM:
a) Mask ROM:
Programmed during manufacturing and cannot normally be modified.
b) PROM (Programmable ROM):
Can be programmed once by the user.
c) EPROM (Erasable Programmable ROM):
Can be erased using ultraviolet light and reprogrammed.
d) EEPROM (Electrically Erasable Programmable ROM):
Can be electrically erased and reprogrammed.
e) Flash Memory:
A type of electrically erasable non-volatile memory that erases and writes data in blocks.
Applications:
- BIOS/UEFI firmware.
- Embedded system firmware.
- Microcontrollers.
- USB flash drives.
- Memory cards and SSDs.
  SECONDARY MEMORY
Secondary memory provides long-term data storage.
Characteristics:
- Non-volatile.
- Larger capacity than primary memory.
- Generally slower than RAM.
- Stores files, applications and operating systems.
Types:
i. Magnetic Storage
Uses magnetic fields to store data.
Examples:
- Hard Disk Drives (HDDs).
- Magnetic tapes.
Applications:
- Large-scale data storage.
- Backups.
- Archiving.
ii. Optical Storage
Uses laser technology to read and write data.
Examples:
- CD.
- DVD.
- Blu-ray Disc.
iii. Solid-State Storage
Uses semiconductor memory, usually NAND flash.
Examples:
- SSDs.
- USB drives.
- SD cards.
Advantages:
- No moving mechanical parts.
- Fast access.
- Low power consumption.
- Resistant to mechanical shock compared with HDDs.

 MEMORY HIERARCHY
Memory hierarchy organizes storage according to speed, capacity, cost and proximity to the CPU.
Typical arrangement, from fastest to slowest:
1. CPU Registers
2. Cache Memory
3. Main Memory (RAM)
4. Secondary Storage (SSD/HDD)
5. Archival Storage
Characteristics:
Registers:
- Located inside the CPU.
- Extremely fast.
- Very small capacity.
- Hold operands, addresses and intermediate results.
Cache:
- Very fast memory between the CPU and main memory.
- Stores frequently or recently accessed instructions and data.
- Reduces average memory access time.
Main Memory:
- Holds currently executing programs and data.
- Usually implemented using DRAM.
- Larger but slower than cache.
Secondary Storage:
- Provides persistent storage.
- Has much larger capacity.
- Slower than RAM.
General hierarchy relationship:
Moving upward:
- Speed increases.
- Cost per bit increases.
- Capacity decreases.
Moving downward:
- Speed decreases.
- Cost per bit decreases.
- Capacity increases.

 CACHE MEMORY
Cache is a small, high-speed memory that stores copies of frequently accessed data and instructions from main memory.
Purpose:
- Reduce CPU waiting time.
- Improve processing speed.
- Reduce average memory access time.
Cache levels:
L1 Cache:
- Smallest and fastest.
- Usually dedicated to individual CPU cores.
- Often divided into instruction cache and data cache.
L2 Cache:
- Larger than L1.
- Usually slower than L1.
- May be private to a core or shared.
L3 Cache:
- Usually larger than L2.
- Generally slower than L1 and L2.
- Often shared among CPU cores.
  Cache operations:
1. Cache Hit:
Requested data is found in cache.
2. Cache Miss:
Requested data is not found in cache and must be fetched from a lower memory level.
3. Hit Rate:
Fraction of memory accesses found in cache.
Hit Rate = Cache Hits / Total Memory Accesses
4. Miss Rate:
Miss Rate = 1 - Hit Rate
Average Memory Access Time (AMAT):
AMAT = Hit Time + (Miss Rate × Miss Penalty)
Where:
- Hit Time = Time to access cache.
- Miss Penalty = Additional time required to obtain data after a miss.
Example:
Hit time = 2 ns
Miss rate = 5%
Miss penalty = 40 ns
AMAT = 2 + (0.05 × 40)
     = 4 ns
Therefore, average memory access time is 4 ns.
Cache mapping techniques:
a) Direct Mapping:
Each memory block maps to exactly one cache line.
Advantages:
- Simple.
- Low cost.
- Fast lookup.
Disadvantage:
- More conflict misses.
b) Fully Associative Mapping:
A memory block can be placed in any cache line.
Advantages:
- Flexible placement.
- Reduces conflict misses.
Disadvantage:
- More complex hardware.
c) Set-Associative Mapping:
Cache is divided into sets, and a block can occupy any line within its assigned set.
Advantages:
- Balances flexibility and hardware complexity.
Cache replacement policies:
- LRU (Least Recently Used).
- FIFO (First In, First Out).
- Random replacement.
Write policies:
- Write-through: Updates cache and lower memory simultaneously.
- Write-back: Updates cache first and writes to lower memory when the cache block is replaced.

 VIRTUAL MEMORY
Virtual memory is a memory management technique that allows programs to use a virtual address space larger than the available physical RAM.
It uses secondary storage to support the illusion of a large memory space.
Important concepts:
- Virtual Address: Address generated by the CPU.
- Physical Address: Actual location in RAM.
- Page: Fixed-size block of virtual memory.
- Frame: Fixed-size block of physical memory.
- Page Table: Maps virtual pages to physical frames.
- Page Fault: Occurs when a requested page is not currently available in physical memory.
- TLB (Translation Lookaside Buffer): A small, fast cache storing recent address translations.
Advantages:
- Allows large programs to execute.
- Supports process isolation.
- Improves memory utilization.
- Enables multitasking.
Disadvantages:
- Page faults cause delays.
- Excessive paging reduces performance.
- Requires memory management hardware and software.
Page replacement algorithms:
- FIFO: Replaces the oldest loaded page.
- LRU: Replaces the least recently used page.
- Optimal: Replaces the page whose next use is farthest in the future; mainly theoretical because future references are unknown.
Thrashing:
A condition in which excessive page faults cause the system to spend more time transferring pages than executing instructions.

 MEMORY ADDRESSING AND ACCESS METHODS
Memory addressing identifies the location where data is stored.
Addressing capacity:
With n address bits:
Number of unique addresses = 2^n
Example:
A 16-bit address can identify:
2^16 = 65,536 locations.
Memory access methods:
a) Random Access:
Any address can be accessed directly with approximately equal access time.
Examples: RAM and ROM.
b) Sequential Access:
Data is accessed in sequence.
Example: Magnetic tape.
c) Direct Access:
Data is accessed using a physical location or block, with access time depending partly on location.
Example: HDD.
d) Associative Access:
Data is searched by content rather than only by a specified address.
Example: Content-addressable memory (CAM).

 MEMORY TIMING AND PERFORMANCE
Memory performance depends on several parameters.
1. Access Time:
Time between initiating a memory operation and obtaining valid data or completing the write operation.
2. Memory Cycle Time:
Minimum time between the start of two successive memory operations.
3. Transfer Rate:
Amount of data transferred per second.
4. Latency:
Delay before data transfer begins or data becomes available.
5. Bandwidth:
Maximum or effective data transfer rate.
Bandwidth:
Bandwidth = Data Transferred / Transfer Time
For a memory bus:
Bandwidth = Transfer Rate × Bus Width
For example:
A 64-bit bus operating at 100 million transfers per second:
Bandwidth = 64 × 100 × 10^6 bits/s
           = 6.4 × 10^9 bits/s
           = 800 MB/s
This assumes one 64-bit transfer per transfer event and ignores protocol overhead.

 ERROR DETECTION AND CORRECTION
Memory errors occur when stored bits change unintentionally.
Causes:
- Electrical noise.
- Radiation.
- Hardware defects.
- Power disturbances.
- Timing problems.
Types of errors:
a) Single-bit Error:
Only one bit changes.
b) Burst Error:
Two or more bits within a sequence are corrupted.
Error detection techniques:
i. Parity Bit:
An additional bit is added to make the number of 1s even or odd.
Even parity:
Total number of 1s must be even.
Odd parity:
Total number of 1s must be odd.
Limitation:
Parity detects any odd number of bit errors but cannot reliably detect an even number of errors.
ii. ECC (Error-Correcting Code):
Uses additional bits to detect and correct certain errors.
Hamming Code:
A technique that can correct single-bit errors and detect certain multiple-bit errors.
For a Hamming code with m data bits and r parity bits:
2^r >= m + r + 1
ECC memory is commonly used in servers, workstations and systems requiring high reliability.

 SEMICONDUCTOR MEMORY TECHNOLOGY
Semiconductor memory stores binary information using integrated electronic circuits.
Important memory technologies:
SRAM:
Uses bistable circuits to store data.
DRAM:
Uses capacitors and transistors.
NAND Flash:
Organized for high-density data storage, commonly used in SSDs and memory cards
NOR Flash:
Provides efficient random access for reading and is commonly used for firmware storage and code execution in embedded systems.
Memory cell concepts:
- Word Line: Selects a row of memory cells.
- Bit Line: Carries data to or from selected cells.
- Sense Amplifier: Detects and amplifies small voltage differences during reading.
- Decoder: Selects a specific memory location.
- Write Driver: Applies appropriate signals to store data.

 MEMORY IN DIGITAL SYSTEMS AND EMBEDDED SYSTEMS
Memory is essential in microprocessors, microcontrollers, FPGA systems and other digital devices.
Common memory types and uses:
- Registers: Hold immediate CPU data and control information.
- SRAM: Used in cache and fast working memory.
- DRAM: Used as main system memory.
- ROM: Stores fixed instructions.
- Flash: Stores firmware and persistent data.
- EEPROM: Stores small amounts of data that must survive power loss.
- FIFO Memory: Stores data in first-in-first-out order.
- Dual-Port RAM: Allows two independent access ports, useful for simultaneous data transfers.
Embedded system memory organization:
1. Program Memory:
Stores executable firmware, commonly Flash.
2. Data Memory:
Stores variables and temporary data, commonly SRAM.
3. Non-Volatile Data Memory:
Stores settings, calibration values and persistent information.
4. CPU Registers:
Hold immediate processing data.
Examples:
- Microcontrollers use Flash for firmware and SRAM for runtime variables.
- FPGAs use block RAM for temporary data storage.
- DSP systems use specialized memory arrangements for fast signal processing.

 IMPORTANT MEMORY EQUATIONS
1. Number of memory locations:
N = 2^n
Where n = number of address bits.
2. Total memory capacity:
C = Number of Locations × Bits per Location
3. Number of address bits:
n = log2(N)
4. Number of bytes:
Bytes = Total Bits / 8
5. Cache hit rate:
Hit Rate = Hits / Total Accesses
6. Cache miss rate:
Miss Rate = 1 - Hit Rate
7. Average memory access time:
AMAT = Hit Time + (Miss Rate × Miss Penalty)
8. Memory bandwidth:
Bandwidth = Data Transferred / Time
9. Memory transfer time:
Time = Data Size / Bandwidth
10. Hamming parity bit requirement:
2^r >= m + r + 1
Where:
m = Number of data bits
r = Number of parity bits

 IMPORTANT COMPARISONS
RAM vs ROM
RAM:
- Generally volatile.
- Read and write.
- Stores temporary working data.
- Used during program execution.
ROM:
- Non-volatile.
- Primarily stores persistent instructions.
- Used for firmware and boot information.
SRAM vs DRAM
SRAM:
- Flip-flop storage.
- No refresh.
- Faster.
- Expensive.
- Lower density.
DRAM:
- Capacitor storage.
- Requires refresh.
- Slower.
- Cheaper.
- Higher density.
Primary vs Secondary Memory
Primary:
- Directly accessible by CPU or memory controller.
- Faster.
- Smaller capacity.
- Higher cost per bit.
Secondary:
- Persistent storage.
- Larger capacity.
- Slower.
- Lower cost per bit.
Volatile vs Non-Volatile Memory
Volatile:
- Requires power to retain data.
- Example: SRAM and DRAM.
Non-Volatile:
- Retains data without power.
- Example: ROM, Flash and EEPROM.

 PRACTICAL APPLICATIONS OF MEMORY
Memory is used in almost every digital computing system.
Computers:
- RAM stores running programs.
- Cache reduces CPU access delays.
- SSDs store operating systems and files.
Smartphones:
- RAM supports active applications.
- Flash stores applications, photos and videos.
Embedded Systems:
- Flash stores firmware.
- SRAM stores variables and temporary data.
- EEPROM stores configuration information.
Networking:
- Buffer memory stores packets temporarily.
- CAM supports fast address and routing-table lookups.
Robotics:
- Memory stores control algorithms, sensor data and navigation information.
Digital Signal Processing:
- Memory stores sampled signals, coefficients and intermediate calculations.
FPGA Systems:
- Block RAM stores data and instructions.
- Distributed RAM supports small local storage structures.

 KEY EXAM TIPS
1. Always distinguish between memory capacity and memory word length.
2. When calculating memory capacity, first determine the number of addressable locations.
3. Remember:
   Number of locations = 2^n.
4. Do not confuse SRAM and DRAM:
   SRAM uses flip-flops; DRAM uses capacitors.
5. Remember that both SRAM and DRAM are volatile.
6. ROM and Flash are non-volatile.
7. Understand why cache improves CPU performance: it exploits temporal and spatial locality.
8. Temporal locality:
   Recently accessed data is likely to be accessed again.
9. Spatial locality:
   Data near recently accessed data is likely to be accessed soon.
10. A cache miss does not mean data is lost; it means the requested data is not currently in that cache.
11. Distinguish a page fault from a cache miss.
12. When calculating bandwidth, ensure that bits and bytes are not confused.
13. Remember that 1 byte = 8 bits.
14. Understand the difference between access time and cycle time.
15. In memory hierarchy questions, relate speed, capacity and cost per bit.
16. Practise memory capacity, address line, cache hit-rate and bandwidth calculations.