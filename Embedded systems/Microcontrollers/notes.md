                    MICROCONTROLLERS
A microcontroller (MCU) is a compact integrated circuit containing a processor (CPU), memory, input/output peripherals, timers, and other control hardware on a single chip. It is designed to control specific tasks within an embedded system.
An embedded system is a computer-based system designed to perform a dedicated function within a larger device or product.
Examples: washing machines, traffic lights, digital thermometers, smart meters, robots, automotive control units, and IoT devices.
Main characteristics
- Designed for a specific application.
- Usually operates in real time or under timing constraints.
- Often has limited memory, processing power, and energy.
- Interacts with physical devices through sensors and actuators.
- Can operate independently or communicate with other systems.
Applications
- Automotive: engine control, airbags, parking systems.
- Industrial: process control, motor control, automation.
- Medical: patient monitors and measurement devices.
- Consumer electronics: appliances, remote controls.
- IoT: smart agriculture, environmental monitoring, home automation.

MICROCONTROLLER ARCHITECTURE:
The main components of a microcontroller are
Central Processing Unit (CPU);
Executes instructions and controls system operations.
Its major components include:
- ALU (Arithmetic Logic Unit): Performs arithmetic and logical operations.
- Control unit: Decodes instructions and coordinates execution.
- Registers: Small, fast storage locations inside the CPU.
- Program counter (PC): Holds the address of the next instruction to execute.
- Stack pointer (SP): Points to the current stack location.
- Status register: Stores flags such as zero, carry, negative, and overflow.
Memory;
 Program memory (Flash/ROM)
- Stores firmware and executable instructions.
- Flash memory is electrically programmable and typically non-volatile.
 RAM (Random Access Memory)
- Stores temporary variables, stack data, and runtime information.
- Volatile: data is generally lost when power is removed.

EEPROM or other non-volatile data memory:
- Stores configuration settings and persistent data.
- Available only on some microcontrollers; external or Flash-based alternatives may be used.
Input/Output (I/O) Ports;
Connect the microcontroller to external devices.
- Digital input: Reads HIGH or LOW logic levels.
- Digital output: Controls devices such as LEDs and driver circuits.
- Analog input: Receives varying voltages through an ADC where available.
- Alternate-function pins: Serve as communication, timer, or other peripheral signals.
Timers and Counters;
Used for:
- Generating accurate delays and periodic interrupts.
- Measuring pulse duration and frequency.
- Counting external events.
- Generating PWM signals.
Interrupt Controller;
Allows the CPU to respond to important events without continuously polling every device.
Examples include timer overflows, incoming data, and external pin changes.
Communication Peripherals;
- UART/USART: serial communication.
- SPI: synchronous, high-speed peripheral communication.
- I²C: two-wire communication with multiple devices.
- CAN: robust communication commonly used in vehicles and industrial systems.
- USB, Ethernet, or wireless interfaces: available on selected MCUs or through external modules.
Other Peripherals;
- ADC: Converts analog voltage into a digital value.
- DAC: Converts a digital value into an analog signal, if provided.
- PWM unit: Generates pulse-width-modulated signals.
- Watchdog timer: Resets or interrupts the system if software fails to service it as required.
- RTC: Maintains time and date, often with a suitable clock source.

MICROCONTROLLER VS MICROPROCESSOR:
Microcontroller (MCU);
- Integrates CPU, memory, and peripherals on one chip.
- Designed mainly for dedicated control applications.
- Usually has lower system cost and power consumption.
- Common in appliances, sensors, and control equipment.
Microprocessor (MPU);
- Primarily provides processing capability; external memory and peripherals may be required.
- Often supports more powerful operating systems and complex applications.
- Common in computers, advanced multimedia devices, and application processors.
The distinction is not absolute: modern microcontrollers can be powerful, while some microprocessors integrate additional peripherals.

TYPES OF MICROCONTROLLERS:
By data width;
- 8-bit: Processes 8-bit data efficiently; common in simple control systems.
- 16-bit: Offers greater arithmetic capability and precision.
- 32-bit: Supports wider data operations and often higher performance.
Bit width describes the processor architecture, not necessarily every peripheral's resolution.
By instruction architecture;
- RISC: Uses a relatively simple instruction set designed for efficient execution.
- CISC: Uses a more complex instruction set with varied instruction operations.
Modern processors may combine features, so the distinction is not always strict.
By memory architecture;
- Harvard architecture: Separates program and data memory paths.
- Von Neumann architecture: Uses a shared memory/address path for instructions and data.
Examples of MCU families
- 8051: classic 8-bit microcontroller family.
- PIC: Microchip microcontroller families.
- AVR: used in many Arduino-compatible boards.
- ARM Cortex-M: widely used 32-bit MCU processor cores.
- ESP32: microcontroller family commonly used for Wi-Fi/Bluetooth-enabled applications.
- STM32: broad family of microcontrollers based on ARM Cortex-M cores.

CLOCK AND INSTRUCTION EXECUTION:
The clock provides timing signals that coordinate processor and peripheral operations.
Clock frequency:
    f = 1/T
Where:
- f = frequency in hertz (Hz).
- T = clock period in seconds.
Therefore:
    T = 1/f
For example, a 16 MHz clock has a period of:
    T = 1/(16 × 10⁶) = 62.5 ns
The CPU executes instructions through a sequence commonly involving;
1. Fetch: obtain the instruction.
2. Decode: determine the required operation.
3. Execute: perform the operation.
4. Store/write back: save the result when required.
Actual pipelines and instruction stages depend on the processor architecture.
Important: Clock frequency is not always equal to instruction execution rate. Some instructions require multiple clock cycles, while pipelined processors may execute parts of several instructions concurrently.

DIGITAL INPUT AND OUTPUT:
Digital systems represent information using binary logic levels.
- Logic 0: LOW voltage range.
- Logic 1: HIGH voltage range.
The exact voltage limits depend on the microcontroller's electrical specifications.
GPIO (General-Purpose Input/Output)
GPIO pins are programmable pins used to read digital signals or  control external circuits.
 Input configuration:
- Reads switches, digital sensors, and logic signals.
- May use internal pull-up or pull-down resistors.
- Floating inputs can produce unpredictable readings.
 Output configuration:
- Controls LEDs, logic inputs, and driver circuits.
- Must remain within the pin's voltage and current ratings.
- High-current loads require suitable driver transistors, MOSFETs,  or driver ICs.
LED current-limiting resistor
For a series LED circuit:
    R = (VCC − VF)/I
Where:
- R = resistor resistance in ohms.
- VCC = supply voltage.
- VF = LED forward voltage.
- I = desired LED current in amperes.
Example: VCC = 5 V, VF = 2 V, I = 10 mA.
    R = (5 − 2)/0.01 = 300 Ω
A standard resistor near 300 Ω may be selected after checking component ratings and the available resistor series.

ANALOG-TO-DIGITAL CONVERSION (ADC):
An ADC converts an analog voltage into a digital number that a microcontroller can process.
For an ideal n-bit ADC:
    Number of levels = 2ⁿ
For an ideal unipolar ADC with input range 0 to VREF, the approximate quantization step is:
    LSB = VREF/2ⁿ
The ideal conversion result is approximately:
    Digital code = floor[(Vin/VREF) × 2ⁿ]
The code is limited to the range 0 to 2ⁿ − 1.
Example: A 10-bit ADC with VREF = 5 V has:
Number of levels = 2¹⁰ = 1024
    LSB = 5/1024 ≈ 4.88 mV
For Vin = 2.5 V:
    Digital code ≈ (2.5/5) × 1024 = 512
The actual ADC code is affected by quantization, offset, gain error, noise, and the converter's implementation.
Applications: Reading temperature sensors, light sensors, potentiometers, battery voltages, and other analog signals.

DIGITAL-TO-ANALOG CONVERSION (DAC):
A DAC converts a digital number into an analog voltage or current.
For an ideal n-bit unipolar voltage DAC:
    Vout ≈ (D/2ⁿ) × VREF
Where:
- D = digital input code.
- VREF = reference voltage.
- n = DAC resolution in bits.
For a 10-bit DAC with VREF = 5 V and D = 512:
    Vout ≈ (512/1024) × 5 = 2.5 V   
The exact transfer function depends on the DAC design and output range.
If a DAC is unavailable, an MCU may generate an approximate analog voltage using PWM and a low-pass filter.

TIMERS, COUNTERS AND PWM:
Timers;
A timer counts clock pulses to measure time or generate periodic events.
For a timer clock derived using a prescaler P:
    f_timer = f_clock/P
For a timer that counts from 0 through ARR inclusive:
    f_update = f_timer/(ARR + 1)
Where ARR is the auto-reload value.
If the timer generates an interrupt every N counts:
    T_interrupt = N/f_timer
These equations assume the stated timer counting mode and clock configuration.
Counters;
Counters count external pulses or internal events. They are used for frequency measurement, object counting, and encoder processing.
PWM (Pulse-Width Modulation);
PWM controls the average power delivered to a load by changing the fraction of time a signal stays HIGH.
Duty cycle:
    D = (TON/T) × 100%
Where:
- TON = HIGH duration.
- T = total period.
For an ideal PWM signal switching between 0 V and VCC:
    Vaverage = (D/100) × VCC
Example: VCC = 5 V and duty cycle = 40%.
        Vaverage = 0.40 × 5 = 2 V
This is the average of the switching waveform, not necessarily the instantaneous output voltage.
Applications: LED brightness control, DC motor speed control, power conversion, and signal generation.

INTERRUPTS:
An interrupt temporarily diverts the CPU to an interrupt service routine (ISR) when an event requires attention.
Interrupt sequence;
1. An interrupt event occurs.
2. The CPU recognizes and accepts it, subject to priority and masking.
3. The current execution context is saved as required.
4. The ISR executes.
5. The CPU restores the context and resumes the interrupted program.
Types
- External interrupts: triggered by external pins or signals.
- Timer interrupts: generated by timer events.
- Peripheral interrupts: generated by UART, ADC, SPI, and similar peripherals.
- Software interrupts: initiated by software or processor mechanisms.
Interrupt Service Routine (ISR);
An ISR should
- Execute quickly.
- Avoid long delays and blocking operations.
- Clear or acknowledge the interrupt source when required.
- Avoid unsafe access to shared data.
- Defer lengthy processing to the main program or a task.
Polling vs interrupts;
- Polling repeatedly checks a device's status; it is simple but can waste CPU time or miss events.
- Interrupts notify the CPU when events occur; they improve responsiveness but require careful handling of priorities and shared data.

SERIAL COMMUNICATION:
UART;
- Asynchronous serial communication.
- Commonly uses TX and RX lines.
- Both devices must agree on baud rate and framing.
- Typical settings include data bits, parity, and stop bits.
- Logic voltage levels must be compatible.
SPI;
- Synchronous communication.
- Common signals: SCLK, MOSI, MISO, and CS/SS.
- Supports high-speed communication with peripherals.
- Often uses separate chip-select signals for different devices.
I²C;
- Two-wire synchronous bus using SDA (data) and SCL (clock).
- Supports addressing of multiple devices.
- Uses pull-up resistors on the bus.
- Common in sensors, RTCs, and configuration ICs.
CAN;
- Message-based, robust communication bus.
- Supports arbitration and error detection.
- Widely used in automotive and industrial control systems.
Selection tip: UART is simple for point-to-point links; SPI is useful for high-speed peripheral communication; I²C reduces signal-wire count; CAN is useful in electrically noisy, multi-node systems.

RESET, WATCHDOG AND POWER MANAGEMENT:
Reset;
Returns the microcontroller to a defined startup state.
Common reset sources
- Power-on reset.
- External reset pin.
- Software reset.
- Watchdog reset.
- Brown-out detection.
Watchdog timer;
A watchdog monitors whether software continues to operate correctly. If the program fails to service it within the configured interval, the watchdog can reset the system or trigger another configured response.
It should be serviced only after confirming that the system is functioning correctly, rather than blindly refreshing it from a timer.
Power management;
Methods include
- Sleep and low-power modes.
- Reducing clock frequency when appropriate.
- Disabling unused peripherals.
- Using interrupts to wake the processor.
- Minimizing unnecessary switching and sensor activity.
Always consult the specific MCU datasheet for sleep behavior, wake-up sources, and power limits.

EMBEDDED SOFTWARE AND FIRMWARE:
Firmware is software stored in non-volatile memory that controls the embedded hardware.
Common programming languages;
- C and C++: widely used for MCU firmware.
- Assembly: used where low-level control or optimization is required.
- Rust and other languages: supported by selected platforms and toolchains.
Typical development workflow;
1. Define system requirements.
2. Select an MCU based on performance, memory, peripherals, cost, and power.
3. Design the hardware circuit.
4. Write and compile the firmware.
5. Program the MCU using a programmer/debugger or bootloader.
6. Test the hardware and software.
7. Debug timing, communication, and electrical problems.
8. Validate reliability and maintain the firmware.
Bare-metal superloop;
A simple embedded program repeatedly performs tasks:
- Initialize hardware.
- Read inputs.
- Process data.
- Update outputs.
- Repeat continuously.
Example structure:
while (1) {
read_inputs();
process_data();
update_outputs();
}
In a real implementation, these functions must be defined, and timing-sensitive tasks may need interrupts, hardware timers, or a real-time operating system (RTOS).
RTOS;
A Real-Time Operating System schedules tasks and provides services such as synchronization, queues, timers, and inter-task communication.
Useful when an application has multiple concurrent activities and defined timing requirements.
A real-time system must meet its required deadlines; real-time does not simply mean fast.

REAL-TIME SYSTEMS:
A real-time system produces results within specified timing constraints.
- Hard real-time: Missing a deadline constitutes system failure.
- Firm real-time: A late result has no useful value, although an occasional miss may not cause catastrophic failure.
- Soft real-time: Late results reduce quality or usefulness but may still be valuable.
Important concepts:
- Latency: Time between an event and the system's response.
- Jitter: Variation in timing or latency.
- Deadline: Latest acceptable completion time.
- Response time: Time from a task's release or triggering event until it completes.
Timing-sensitive embedded systems must account for interrupt latency, execution time, communication delays, and task scheduling.

SENSORS AND ACTUATORS:
Sensors;
Convert physical quantities into electrical signals.
Examples:
- Thermistor: temperature.
- LDR: light intensity.
- Accelerometer: acceleration.
- Pressure sensor: pressure.
- Ultrasonic sensor: distance.
Sensor signals may require amplification, filtering, calibration, or analog-to-digital conversion.

Actuators;
Convert electrical control signals into physical action.
Examples:
- DC motor: rotational motion.
- Servo motor: controlled angular position.
- Relay: electrical switching.
- Solenoid: linear movement.
- LED: light output.
Microcontroller pins generally cannot drive high-power actuators directly. Use appropriate drivers, power supplies, and protection components.
Closed-loop control;
A feedback system measures the output and adjusts the control action to reduce the difference between desired and actual output.
Error:
    e(t) = r(t) − y(t)
Where:
- r(t) = reference or setpoint.
- y(t) = measured output.
- e(t) = control error.
Example: A temperature controller reads a sensor, compares the measurement with the desired temperature, and adjusts a heater.

MEMORY AND REGISTER OPERATIONS:
Registers;
Registers control peripherals and store data or status information.
Examples:
- GPIO direction register.
- GPIO input/output data register.
- Timer control and count registers.
- UART status and data registers.
- ADC control and result registers.
Bit manipulation;
Embedded software often changes individual register bits.
- Set bit n: "REG |= (1U << n);"
- Clear bit n: "REG &= ~(1U << n);"
- Toggle bit n: "REG ^= (1U << n);"
- Test bit n: "if (REG & (1U << n))"
These operations assume a suitable unsigned integer type and a valid bit position. Hardware registers may have special write semantics, so follow the datasheet.
Important: "volatile" is commonly required for memory-mapped hardware registers and certain variables modified by interrupts. It prevents certain compiler optimizations but does not, by itself, make an operation atomic or provide thread synchronization.

IMPORTANT EQUATIONS SUMMARY:
1. Clock period: T = 1/f
2. Clock frequency: f = 1/T
3. ADC levels: L = 2ⁿ
4. Ideal ADC step: LSB = VREF/2ⁿ
5. Approximate ADC code: D = floor[(Vin/VREF) × 2ⁿ]
6. Ideal DAC output: Vout ≈ (D/2ⁿ) × VREF
7. LED resistor: R = (VCC − VF)/I
8. Timer frequency after prescaling: f_timer = f_clock/P
9. Timer update frequency: f_update = f_timer/(ARR + 1)
10. PWM duty cycle: D = (TON/T) × 100%
11. Ideal PWM average voltage: Vaverage = (D/100) × VCC
12. Ohm's law: V = IR
13. Electrical power: P = VI = I²R = V²/R
14. Binary storage capacity of n bits: 2ⁿ distinct bit patterns.
Always verify assumptions, units, timer counting modes, and peripheral-specific transfer functions before applying these equations.

PRACTICAL DESIGN AND EXAM TIPS:
- Read the datasheet and reference manual before configuring unfamiliar hardware.
- Check the operating voltage, clock limits, pin functions, current ratings, and memory capacity.
- Do not assume all MCU pins are 5 V tolerant.
- Use pull-up or pull-down resistors where required; mechanical switches may need debouncing.
- Add appropriate current-limiting and driver circuits for LEDs, motors, relays, and other loads.
- Use flyback protection for inductive loads when required by the driver topology.
- Avoid long delays in interrupt service routines.
- Protect shared data between interrupts and main code using suitable atomic or synchronization techniques.
- Use a watchdog and defined fault-handling behavior where reliability is important.
- Test boundary conditions, power interruptions, sensor failures, and communication timeouts.
- Distinguish MCU hardware features from features provided by a development board or external module.
- In numerical questions, identify the formula, substitute values with correct units, calculate, and state the result clearly.

SUMMARY:
A microcontroller integrates processing, memory, and peripherals to control an embedded system. Its CPU executes firmware; memory stores instructions and data; GPIO connects external hardware; timers provide precise timing; ADCs and DACs interface with analog signals; interrupts support responsive operation; and communication peripherals exchange data with other devices.
Effective microcontroller design requires understanding both software and hardware, including timing, electrical limits, memory, peripheral configuration, power consumption, reliability, and real-time requirements.