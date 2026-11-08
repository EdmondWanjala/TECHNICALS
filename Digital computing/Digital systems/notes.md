                DIGITAL SYSTEMS
A digital system is an electronic system that processes, stores, and communicates information using discrete values, usually binary digits (0 and 1).
Digital systems form the foundation of computers, microcontrollers, communication devices, industrial automation, embedded systems, and digital instrumentation.
  Main characteristics;
- Operate using discrete logic levels.
- Process information in binary form.
- Use logic gates and switching circuits.
- Store information using memory elements.
- Can be programmed to perform specific operations.
- Provide high reliability, speed, and repeatability.
Examples;
- Computers and smartphones.
- Digital watches and calculators.
- Microcontroller-based systems.
- Digital measuring instruments.
- Traffic light controllers.
- Industrial control systems.

 ANALOG AND DIGITAL SYSTEMS
  Analog systems;
Process continuously varying signals that can take an infinite number of values within a range.
Examples:
- Microphone audio signals.
- Temperature sensors with analog outputs.
- Analog radio receivers.
  Digital systems;
Process discrete signals represented by binary values.
Examples:
- Digital computers.
- Digital clocks.
- Microprocessors.
- Digital communication systems.
  Comparison;
Analog systems| Digital systems
Continuous signals| Discrete signals
More sensitive to accumulated noise| Better noise tolerance within logic limits
Directly represent physical variations| Require conversion for many physical signals
Often harder to reproduce exactly| Easy to store and reproduce consistently
Analog processing circuits| Logic circuits and processors

Many practical systems are mixed-signal systems, combining analog and digital components.

 NUMBER SYSTEMS;
Digital systems use different number systems to represent and process information.
  Binary number system;
- Base: 2
- Digits: 0 and 1
- Used internally by digital computers.
Example:
    1011₂ = 1(2³) + 0(2²) + 1(2¹) + 1(2⁰)= 8 + 0 + 2 + 1= 11₁₀
  Decimal number system;
- Base: 10
- Digits: 0–9
- Common human-readable number system.
  Octal number system;
- Base: 8
- Digits: 0–7
- Each octal digit represents 3 binary bits.
Example:
    101 110₂ = 56₈
  Hexadecimal number system;
- Base: 16
- Digits: 0–9 and A–F.
- Each hexadecimal digit represents 4 binary bits.
Hexadecimal| Decimal| Binary
0| 0| 0000
1| 1| 0001
2| 2| 0010
3| 3| 0011
4| 4| 0100
5| 5| 0101
6| 6| 0110
7| 7| 0111
8| 8| 1000
9| 9| 1001
A| 10| 1010
B| 11| 1011
C| 12| 1100
D| 13| 1101
E| 14| 1110
F| 15| 1111

Number conversion methods
  Binary to decimal:
Multiply each bit by its corresponding power of 2 and add the results.
  Decimal to binary:
Repeatedly divide the decimal number by 2 and read the remainders from bottom to top.
  Binary to hexadecimal:
Group binary digits into sets of four, starting from the right, and convert each group.
  Hexadecimal to binary:
Replace each hexadecimal digit with its four-bit binary equivalent.

 BINARY ARITHMETIC
Binary arithmetic is used by digital circuits and processors to perform mathematical operations.
  Binary addition;
Rules:
- 0 + 0 = 0
- 0 + 1 = 1
- 1 + 0 = 1
- 1 + 1 = 10
- 1 + 1 + 1 = 11
Example:
   1010
 + 0110
 -------
  10000
  Binary subtraction;
Rules:
- 0 − 0 = 0
- 1 − 0 = 1
- 1 − 1 = 0
- 0 − 1 requires borrowing.
Example:
   1010
 - 0011
 -------
   0111
  Binary multiplication;
Rules:
- 0 × 0 = 0
- 0 × 1 = 0
- 1 × 0 = 0
- 1 × 1 = 1
Example:
    101
  ×  10
  -----
    000
   101
  -----
   1010
  Binary division;
Binary division follows the same principles as decimal long division, but uses only 0 and 1.

 DATA REPRESENTATION AND CODING
Digital systems use binary codes to represent numbers, characters, symbols, and other information.
  Binary-coded decimal (BCD);
BCD represents each decimal digit using four binary bits.
Example:
    59₁₀ = 0101 1001 (BCD)
Note: BCD is not the same as ordinary binary representation.
  Gray code;
A binary coding system in which consecutive values differ by only one bit.
Application:
- Rotary encoders.
- Position measurement.
- Reducing transition errors in digital systems.
  ASCII;
American Standard Code for Information Interchange.
Used to represent letters, numbers, and control characters.
Traditional ASCII uses 7 bits, allowing 128 possible codes.
  Unicode
A universal character encoding standard that supports characters from many writing systems.
UTF-8 is a widely used variable-length Unicode encoding.
  Parity bits
A parity bit is added to a binary data word to help detect transmission or storage errors.
- Even parity: total number of 1s, including the parity bit, is even.
- Odd parity: total number of 1s is odd.
Parity detects any odd number of bit errors but cannot reliably detect all even-numbered bit errors.

 LOGIC GATES AND BOOLEAN OPERATIONS
Logic gates are the fundamental building blocks of digital systems.
Main gates:
1. AND: output is 1 when all inputs are 1.
2. OR: output is 1 when at least one input is 1.
3. NOT: reverses the input.
4. NAND: opposite of AND.
5. NOR: opposite of OR.
6. XOR: output is 1 when inputs differ.
7. XNOR: output is 1 when inputs are equal.
Important Boolean expressions:
- AND: Y = AB
- OR: Y = A + B
- NOT: Y = A̅
- NAND: Y = (AB)̅
- NOR: Y = (A + B)̅
- XOR: Y = A̅B + AB̅
- XNOR: Y = AB + A̅B̅
Boolean algebra is used to simplify digital circuits and reduce hardware complexity.
Important laws:
- A + 0 = A
- A·1 = A
- A + A = A
- A·A = A
- A + A̅ = 1
- A·A̅ = 0
- A + AB = A
- A(A + B) = A
De Morgan's theorems:
- (AB)̅ = A̅ + B̅
- (A + B)̅ = A̅B̅

 COMBINATIONAL DIGITAL CIRCUITS
A combinational circuit is a digital circuit whose output depends only on its current inputs.
It does not store previous input states.
  Half adder;
Adds two binary bits.
Sum: S = A ⊕ B
Carry: C = AB
  Full adder;
Adds three binary inputs: A, B, and carry-in.
Sum: S = A ⊕ B ⊕ Cᵢₙ
Carry-out: Cₒᵤₜ = AB + ACᵢₙ + BCᵢₙ
  Half subtractor;
Subtracts one binary bit B from A.
Difference: D = A ⊕ B
Borrow: Bₒᵤₜ = A̅B
  Full subtractor;
Performs subtraction using A, B, and borrow-in.
Difference:
    D = A ⊕ B ⊕ Bᵢₙ
Borrow-out:
    Bₒᵤₜ = A̅B + A̅Bᵢₙ + BBᵢₙ
  Multiplexer (MUX);
Selects one input from several inputs and transfers it to a single output.
Application: data selection and routing.
  Demultiplexer (DEMUX);
Routes one input to a selected output.
Application: data distribution.
  Encoder;
Converts an active input into a coded binary output.
  Decoder;
Converts a binary input code into a corresponding output signal.
  Digital comparator;
Compares two binary numbers and determines whether they are equal or whether one is greater or smaller.

 SEQUENTIAL DIGITAL CIRCUITS
Sequential circuits are digital circuits whose outputs depend on current inputs and previously stored states.
They contain memory elements.
  Latches;
A latch is a level-sensitive memory element that stores one bit.
Types:
- SR latch: Set and Reset.
- D latch: stores the input data while enabled.
  Flip-flops;
A flip-flop is generally an edge-triggered bistable circuit that stores one bit.
Types:
- SR flip-flop: Set and Reset.
- D flip-flop: stores data at an active clock edge.
- JK flip-flop: supports set, reset, hold, and toggle.
- T flip-flop: toggles its output when enabled.
  Registers;
A register is a group of flip-flops used to store binary data.
An n-bit register stores n bits and can represent 2ⁿ different bit patterns.
Applications:
- Temporary data storage.
- CPU registers.
- Data transfer.
- Instruction storage.
  Counters
Counters are sequential circuits that count clock pulses or follow predefined state sequences.
Types:
- Up counter.
- Down counter.
- Up/down counter.
- Ripple counter.
- Synchronous counter.
- Modulo-N counter.
- Ring counter.
- Johnson counter.
An n-bit binary counter has 2ⁿ possible states.
A modulo-N counter cycles through N distinct states before repeating.

 SHIFT REGISTERS
A shift register is a group of flip-flops that shifts stored binary data left or right in response to clock pulses.
Types:
1. SISO: Serial-In Serial-Out.
2. SIPO: Serial-In Parallel-Out.
3. PISO: Parallel-In Serial-Out.
4. PIPO: Parallel-In Parallel-Out.
Applications:
- Serial communication.
- Data conversion.
- Temporary storage.
- Digital signal processing.
- Data manipulation.

 CLOCKS AND TIMING IN DIGITAL SYSTEMS
A clock is a periodic signal used to coordinate operations in synchronous digital circuits.
Important terms:
- Clock period (T): time taken for one complete clock cycle.
- Clock frequency (f): number of cycles per second.
- Duty cycle: percentage of the period during which the clock signal is HIGH.
- Rising edge: transition from LOW to HIGH.
- Falling edge: transition from HIGH to LOW.
- Propagation delay: time taken for an input change to affect an output.
Important equations:
    f = 1/T
    T = 1/f
Duty cycle = (HIGH time / Total period) × 100%
For example, if a clock has a frequency of 1 MHz:
    T = 1/1,000,000 = 1 μs
Timing constraints
- Setup time: minimum time data must remain stable before the active clock edge.
- Hold time: minimum time data must remain stable after the active clock edge.
- Clock skew: difference in clock arrival times at different circuit components.
- Metastability: an uncertain temporary state that may occur when timing requirements are violated.
These concepts are essential for reliable synchronous circuit design.

 FINITE STATE MACHINES (FSM)
A finite state machine is a mathematical model used to design sequential digital systems that operate through a finite number of states.
An FSM consists of:
- States.
- Inputs.
- Outputs.
- Transition rules.
- Initial state.
Types of FSM
Moore machine:
Output depends only on the current state.
Mealy machine:
Output depends on the current state and current inputs.
FSM design procedure
1. Define the system requirements.
2. Identify all possible states.
3. Identify input and output conditions.
4. Draw the state diagram.
5. Construct the state transition table.
6. Assign binary codes to states.
7. Derive next-state and output logic.
8. Implement using flip-flops and logic gates.
9. Test and verify the circuit.
Applications:
- Traffic light controllers.
- Elevator systems.
- Vending machines.
- Washing machines.
- Communication protocols.
- Industrial automation.

 ANALOG-TO-DIGITAL AND DIGITAL-TO-ANALOG CONVERSION
Digital systems often interact with real-world analog signals.
  Analog-to-Digital Converter (ADC);
Converts an analog signal into a digital representation.
Main stages:
1. Sampling: measures the analog signal at discrete time intervals.
2. Quantization: assigns each sample to a discrete amplitude level.
3. Encoding: represents the quantized value in binary form.    
  Important concepts:
Sampling frequency (fₛ): number of samples taken per second.
According to the Nyquist sampling theorem:
    fₛ ≥ 2fₘₐₓ
Where fₘₐₓ is the highest frequency component of the signal, assuming ideal band-limited sampling.
In practice, anti-aliasing filtering and an appropriate sampling margin are required.
  ADC resolution;
An n-bit ADC has:
    Number of levels = 2ⁿ
For an ideal unipolar ADC with input range 0 to Vref:
    Ideal step size (LSB) ≈ Vref / 2ⁿ
Higher resolution provides finer quantization.
  Digital-to-Analog Converter (DAC);
Converts digital binary data into an analog voltage or current.
Common DAC architectures:
- Binary-weighted resistor DAC.
- R-2R ladder DAC.
- PWM-based DAC with filtering.
Applications:
- Audio output.
- Motor control.
- Signal generation.
- Instrumentation.

 DIGITAL LOGIC FAMILIES
Logic families describe the electronic technologies used to implement digital gates.
  TTL (Transistor-Transistor Logic);
Uses bipolar junction transistors.
Characteristics:
- Traditionally operates at 5 V.
- Good switching performance.
- Used in many older digital systems.
  CMOS (Complementary Metal-Oxide-Semiconductor);
Uses complementary MOS transistors.
Characteristics:
- Low static power consumption.
- High input impedance.
- High integration density.
- Widely used in modern processors, microcontrollers, and digital ICs.
Important logic-family parameters
- Supply voltage: voltage required to operate the IC.
- Logic HIGH and LOW voltage levels.
- Noise margin: tolerance to unwanted voltage variations.
- Propagation delay: switching response time.
- Fan-in: number of gate inputs.
- Fan-out: number of loads an output can drive.
- Power dissipation: power consumed during operation.
Always check voltage compatibility when connecting different logic families.

 PROGRAMMABLE DIGITAL SYSTEMS
Programmable logic devices allow digital circuits to be configured or programmed to perform specific functions.
  Programmable Logic Array (PLA);
A programmable device with programmable AND and OR arrays.
Used to implement Boolean functions.
  Programmable Array Logic (PAL);
Uses a programmable AND array and a fixed OR array.
  Complex Programmable Logic Device (CPLD);
Contains multiple programmable logic blocks connected through programmable interconnections.
  Field Programmable Gate Array (FPGA);
A reconfigurable digital integrated circuit containing:
- Configurable logic blocks.
- Programmable interconnections.
- Input/output blocks.
- Often embedded memory and specialized processing resources.
Applications:
- Digital signal processing.
- Hardware acceleration.
- Robotics.
- Communication systems.
- Embedded computing.
- Prototyping digital hardware.
Hardware Description Languages (HDLs), such as Verilog and VHDL, are commonly used to describe digital hardware.

 DIGITAL SYSTEM INTERFACING
Interfacing involves connecting digital systems to external devices and other electronic circuits.
Common interfaces include:
- GPIO: General-Purpose Input/Output pins.
- UART: asynchronous serial communication.
- SPI: synchronous serial communication.
- I²C: two-wire serial communication.
- USB: Universal Serial Bus.
- CAN: Controller Area Network.
- Ethernet: wired network communication.
Important interfacing considerations;
1. Voltage-level compatibility.
2. Input and output current limits.
3. Signal timing.
4. Noise immunity.
5. Communication speed.
6. Ground reference.
7. Electrical isolation where necessary.
For example, a 3.3 V microcontroller output must not automatically be connected to a 5 V input without checking the input's voltage requirements and compatibility.

 DIGITAL SYSTEM APPLICATIONS
Computing
- Microprocessors.
- Memory systems.
- Computers.
- Graphics processors.
Communication
- Digital signal transmission.
- Network routers.
- Wireless communication.
- Error detection and correction.
Industrial automation
- Programmable controllers.
- Motor control.
- Process monitoring.
- Digital instrumentation.
Embedded systems
- Microcontrollers.
- Smart appliances.
- Robotics.
- Automotive electronics.
Consumer electronics
- Smartphones.
- Digital cameras.
- Smart televisions.
- Gaming systems.

 IMPORTANT DIGITAL SYSTEM FORMULAS
Number of binary combinations:
    N = 2ⁿ
Binary number value:
    V = Σ bᵢ × 2ⁱ
Clock frequency:
    f = 1/T
Clock period:
    T = 1/f
Duty cycle:
    D = (Tₒₙ/T) × 100%
Number of ADC quantization levels:
    L = 2ⁿ
Ideal ADC step size:
    LSB ≈ Vref/2ⁿ
Nyquist sampling condition:
    fₛ ≥ 2fₘₐₓ
Counter states:
    N = 2ⁿ
Number of flip-flops required for at least N states:
    n = ⌈log₂N⌉
Data transmission time:
    t = Number of bits / Bit rate
Data transfer rate:
    R = Data transferred / Time taken
Memory capacity:
    Capacity = Number of addressable locations × Bits per location

IMPORTANT EXAM TIPS
1. Understand the difference between analog and digital systems.
2. Practise conversions between binary, decimal, octal, and hexadecimal.
3. Master binary addition, subtraction, multiplication, and division.
4. Know BCD, Gray code, ASCII, and parity coding.
5. Distinguish combinational circuits from sequential circuits.
6. Memorize the operation and equations of adders and subtractors.
7. Understand latches, flip-flops, registers, and counters.
8. Differentiate synchronous and asynchronous counters.
9. Understand shift-register types and their applications.
10. Practise clock frequency, period, and duty-cycle calculations.
11. Understand Moore and Mealy state machines.
12. Master ADC resolution and Nyquist sampling calculations.
13. Understand the differences between TTL and CMOS.
14. Know the applications and basic structures of PLAs, PALs, CPLDs, and FPGAs.
15. Understand common digital communication interfaces and voltage compatibility.

CORE PRINCIPLE: 
Digital systems combine binary representation, logic circuits, memory elements, timing mechanisms, and programmable hardware to process, store, transmit, and control information. 
They form the foundation of modern computing, embedded electronics, communication, and automation.