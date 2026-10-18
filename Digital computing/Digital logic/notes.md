                DIGITAL LOGIC
Digital logic is the study of circuits that operate using discrete binary values, usually represented by 0 and 1. It forms the foundation of digital computers, processors, memory systems, calculators, and digital control systems.
- Logic 0 (LOW): represents a LOW voltage range.
- Logic 1 (HIGH): represents a HIGH voltage range.
- Binary signal: a signal with two distinct logical states.
- Logic gate: an electronic circuit that performs a Boolean operation on one or more binary inputs to produce an output.
- Boolean algebra: a mathematical system used to analyze and simplify digital logic circuits.
Applications include computer processors, digital clocks, communication systems, embedded systems, and industrial automation.

BINARY LOGIC AND BOOLEAN VARIABLES
A Boolean variable can have only two possible values: 0 or 1.
Common symbols:
- A, B, C: input variables.
- Y or F: output variable.
- AND: multiplication, represented by A·B or AB.
- OR: addition, represented by A + B.
- NOT: complement, represented by A̅ or ¬A.
- XOR: exclusive OR, represented by A ⊕ B.
- XNOR: exclusive NOR, represented by (A ⊕ B)̅.
Important distinction: Boolean addition and multiplication are logical operations, not ordinary arithmetic operations.

BASIC LOGIC GATES
NOT Gate (Inverter)
Produces the opposite of its input.
Equation: Y = A̅
A| Y
0| 1
1| 0
Application: generating complementary signals.
AND Gate
The output is 1 only when all inputs are 1.
Equation: Y = A·B
A| B| Y
0| 0| 0
0| 1| 0
1| 0| 0
1| 1| 1
Application: enabling a device only when all required conditions are satisfied.
OR Gate
The output is 1 when at least one input is 1.
Equation: Y = A + B
A| B| Y
0| 0| 0
0| 1| 1
1| 0| 1
1| 1| 1
Application: activating an alarm when any one of several conditions occurs.
NAND Gate
The opposite of AND.
Equation: Y = (A·B)̅
A| B| Y
0| 0| 1
0| 1| 1
1| 0| 1
1| 1| 0
Application: general-purpose digital circuit design. NAND is a universal gate.
NOR Gate
The opposite of OR.
Equation: Y = (A + B)̅
A| B| Y
0| 0| 1
0| 1| 0
1| 0| 0
1| 1| 0
Application: control and logic circuits. NOR is also a universal gate.
XOR Gate (Exclusive OR)
The output is 1 when the inputs are different.
Equation: Y = A ⊕ B = A̅B + AB̅
A| B| Y
0| 0| 0
0| 1| 1
1| 0| 1
1| 1| 0
Application: binary addition and parity generation.
XNOR Gate (Exclusive NOR)
The output is 1 when the inputs are equal.
Equation: Y = (A ⊕ B)̅ = AB + A̅B̅
A| B| Y
0| 0| 1
0| 1| 0
1| 0| 0
1| 1| 1
Application: equality comparison in digital systems.

SUMMARY OF LOGIC GATES
Gate| Boolean expression| Output is 1 when
NOT| A̅| A = 0
AND| AB| All inputs are 1
OR| A + B| At least one input is 1
NAND| (AB)̅| At least one input is 0
NOR| (A + B)̅| All inputs are 0
XOR| A ⊕ B| Inputs differ
XNOR| (A ⊕ B)̅| Inputs are equal
For n binary inputs, the number of possible input combinations is 2ⁿ. Therefore, a truth table with two inputs has 4 rows, while one with three inputs has 8 rows.

BOOLEAN ALGEBRA LAWS
Boolean algebra simplifies logical expressions and reduces the number of gates required to implement a circuit.
Identity laws
- A + 0 = A
- A·1 = A
Null or domination laws
- A + 1 = 1
- A·0 = 0
Idempotent laws
- A + A = A
- A·A = A
Complement laws
- A + A̅ = 1
- A·A̅ = 0
Involution law
- (A̅)̅ = A
Commutative laws
- A + B = B + A
- AB = BA
Associative laws
- (A + B) + C = A + (B + C)
- (AB)C = A(BC)
Distributive laws
- A(B + C) = AB + AC
- A + BC = (A + B)(A + C)
Absorption laws
- A + AB = A
- A(A + B) = A
De Morgan's theorems
- (AB)̅ = A̅ + B̅
- (A + B)̅ = A̅B̅
De Morgan's theorems are especially useful when converting AND/OR logic into NAND/NOR implementations.

SIMPLIFICATION OF BOOLEAN EXPRESSIONS
Boolean simplification reduces a logic expression to an equivalent, simpler form.
Example 1:
F = A + AB
Using the absorption law:
F = A
Example 2:
F = AB + AB̅
Taking A as a common factor:
F = A(B + B̅)
Since B + B̅ = 1:
F = A·1 = A
Example 3:
F = (A + B)̅
Using De Morgan's theorem:
F = A̅B̅
Simplification can reduce circuit complexity, component count, power consumption, propagation delay, and cost.

LOGIC CIRCUITS AND LOGIC DIAGRAMS
A logic circuit consists of interconnected logic gates that implement a Boolean function.
To design a logic circuit:
1. Identify the inputs and desired output.
2. Define the conditions under which the output is 1.
3. Construct a truth table.
4. Derive a Boolean expression.
5. Simplify the expression.
6. Draw the corresponding logic-gate diagram.
7. Verify the output for every input combination.
Example:
A warning light turns ON when both a power signal P and a fault signal F are active.
Boolean expression: Y = P·F
The circuit uses one AND gate. The warning light is ON only when P = 1 and F = 1.

COMBINATIONAL AND SEQUENTIAL LOGIC
Combinational logic
The output depends only on the current input values. It has no stored state.
Examples:
- Adders and subtractors
- Multiplexers and demultiplexers
- Encoders and decoders
- Comparators
Sequential logic
The output depends on current inputs and the circuit's previous state. It uses memory elements to store information.
Examples:
- Flip-flops
- Registers
- Counters
- Shift registers
- Memory circuits
Sequential circuits often use a clock signal to control when state changes occur.

IMPORTANT COMBINATIONAL CIRCUITS
Half adder
Adds two binary bits A and B.
Sum: S = A ⊕ B
Carry: C = AB
A| B| S| C
0| 0| 0| 0
0| 1| 1| 0
1| 0| 1| 0
1| 1| 0| 1
A half adder cannot accept a carry input from a previous stage.
Full adder
Adds A, B, and an input carry Cᵢₙ.
Sum: S = A ⊕ B ⊕ Cᵢₙ
Carry output: Cₒᵤₜ = AB + ACᵢₙ + BCᵢₙ
It is used in multi-bit binary addition.
Multiplexer (MUX)
Selects one of several inputs and forwards it to a single output.
A 2-to-1 multiplexer has inputs I₀ and I₁, select input S, and output Y.
Equation: Y = S̅I₀ + SI₁
- S = 0 selects I₀.
- S = 1 selects I₁.
Demultiplexer (DEMUX)
Routes one input to one of several outputs according to select signals.
Application: data distribution and communication systems.
Encoder and decoder
- Encoder: converts an active input among several input lines into a binary code.
- Decoder: converts a binary input code into one or more activated output lines.
Applications include keyboard encoding, address decoding, and display control.
Comparator
Compares binary values and determines whether one is greater than, equal to, or less than the other.
Application: processors, sorting circuits, and digital control systems.

FLIP-FLOPS AND MEMORY
A flip-flop is a bistable sequential circuit that stores one bit.
Common types:
- SR flip-flop: Set and Reset.
- D flip-flop: stores the value present at D at the active clock edge.
- JK flip-flop: supports set, reset, hold, and toggle operations.
- T flip-flop: toggles its state when enabled.
A register is a group of flip-flops used to store multiple bits.
An n-bit register can store 2ⁿ distinct bit patterns.
Counters use sequential logic to move through a defined sequence of states, often in response to clock pulses.

KARNAUGH MAPS (K-MAPS)
A Karnaugh map is a graphical method of simplifying Boolean expressions.
Procedure:
1. Construct the truth table.
2. Transfer output values into the corresponding K-map cells.
3. Group adjacent 1s in powers of two: 1, 2, 4, 8, and so on.
4. Make the largest useful groups, allowing overlap where beneficial.
5. Write the simplified expression from the variables that remain constant within each group.
Rules:
- Groups may wrap around map edges.
- Diagonal cells are not adjacent.
- Every required 1 must be covered.
- In sum-of-products simplification, group 1s; for product-of-sums, group 0s.
- Don't-care conditions may be used when they help simplify the circuit.
K-maps are most practical for functions with a small number of variables, commonly two to four and sometimes five or six.

STANDARD FORMS OF BOOLEAN EXPRESSIONS
Sum of Products (SOP);
An OR combination of AND terms.
    Example: F = A̅B + AB̅
Each AND term is called a product term.
Product of Sums (POS);
An AND combination of OR terms.
    Example: F = (A + B)(A̅ + B̅)
Each OR term is called a sum term.
Minterms and maxterms;
- Minterm: a product term containing every variable exactly once, complemented or uncomplemented. It corresponds to one truth-table row where the output is 1.
- Maxterm: a sum term containing every variable exactly once, complemented or uncomplemented. It corresponds to one truth-table row where the output is 0.
Canonical notation:
- F = Σm(indices) represents the sum of minterms.
- F = ΠM(indices) represents the product of maxterms.
Use a consistent variable ordering when assigning binary row indices.

UNIVERSAL GATES
NAND and NOR are universal gates because any Boolean function can be implemented using only NAND gates or only NOR gates.
Using NAND:
- NOT: A NAND A = A̅
- AND: (A NAND B) NAND (A NAND B) = AB
- OR: (A NAND A) NAND (B NAND B) = A + B
Using NOR:
- NOT: A NOR A = A̅
- OR: (A NOR B) NOR (A NOR B) = A + B
- AND: (A NOR A) NOR (B NOR B) = AB
Universal gates are valuable because a circuit can be implemented using a single gate family.

TIMING AND PRACTICAL CONSIDERATIONS
- Propagation delay: time taken for a change at an input to affect the output.
- Fan-in: number of inputs a gate can accept.
- Fan-out: number of standard input loads that an output can drive reliably.
- Logic level: one stage of logic through which a signal passes.
- Clock frequency: number of clock cycles per second, measured in hertz (Hz).
- Setup time: minimum time data must be stable before the active clock edge.
- Hold time: minimum time data must remain stable after the active clock edge.
- Glitch: an unintended temporary output transition caused by unequal signal delays.
- Noise margin: the voltage range over which a signal can vary without being interpreted incorrectly.
Practical circuit design must consider voltage levels, timing constraints, loading, power consumption, and the electrical specifications of the chosen logic family.

QUICK FORMULA SUMMARY
NOT: Y = A̅
AND: Y = AB
OR: Y = A + B
NAND: Y = (AB)̅
NOR: Y = (A + B)̅
XOR: Y = A̅B + AB̅
XNOR: Y = AB + A̅B̅
Half-adder sum: S = A ⊕ B
Half-adder carry: C = AB
Full-adder sum: S = A ⊕ B ⊕ Cᵢₙ
Full-adder carry: Cₒᵤₜ = AB + ACᵢₙ + BCᵢₙ
2-to-1 MUX: Y = S̅I₀ + SI₁
Number of input combinations: N = 2ⁿ
Number of patterns storable in n bits: 2ⁿ
Core principle: Digital logic uses Boolean algebra and logic gates to process binary information. 
Combinational circuits process current inputs, while sequential circuits also retain information about previous states.