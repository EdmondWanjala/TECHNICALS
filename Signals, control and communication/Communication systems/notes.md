                COMMUNICATION SYSTEMS
A communication system is a system that transfers information from a source to a destination through a transmission medium or channel.
The information may be in the form of voice, audio, video, text, images or digital data.
  Main objectives:
- Transmit information accurately and reliably.
- Minimize noise, interference and distortion.
- Use available bandwidth and transmission power efficiently.
- Achieve high data rates and reliable communication.
Applications:
- Mobile and satellite communication.
- Radio and television broadcasting.
- Computer networks and the internet.
- Optical fibre communication.
- Wireless sensor networks and IoT.
- Radar, navigation and remote control systems.

 BASIC BLOCK DIAGRAM OF A COMMUNICATION SYSTEM
Information Source → Input Transducer → Transmitter → Communication Channel → Receiver → Output Transducer → Destination
  Main components:
a) Information source
- Generates the information to be transmitted.
- Examples: microphone, camera, computer or sensor.
b) Input transducer
- Converts physical information into an electrical signal.
- Example: a microphone converts sound into an electrical signal.
c) Transmitter
- Processes the message signal for transmission.
- Performs operations such as modulation, amplification, filtering and encoding.
- Produces a signal suitable for the transmission channel.
d) Communication channel
- The medium through which the signal travels.
- Guided channels: twisted-pair cables, coaxial cables and optical fibres.
- Unguided channels: radio waves, microwaves and satellite links.
e) Receiver
- Extracts the original information from the received signal.
- Performs amplification, filtering, demodulation and decoding.
f) Output transducer
- Converts the recovered electrical signal into a usable physical form.
- Example: a loudspeaker converts an electrical signal into sound.
g) Destination
- The final user or device receiving the information.

 TYPES OF COMMUNICATION SYSTEMS
  Based on signal type;
Analog communication:
- Uses continuously varying signals.
- Information is represented by continuous changes in amplitude, frequency or phase.
- Examples: conventional AM/FM radio and analog television.
- Advantages: conceptually simple and can provide continuous signal representation.
- Limitations: more susceptible to noise accumulation and degradation.
Digital communication:
- Transmits information using discrete symbols, commonly binary bits (0 and 1).
- Examples: mobile networks, computer networks, digital television and Bluetooth.
- Advantages: better noise immunity through regeneration, error detection and correction, and easier storage and processing.
- Limitations: requires sampling and quantization for analog sources, synchronization, and suitable bandwidth.
  Based on transmission medium;
Wired communication:
- Uses a physical transmission medium.
- Examples: copper cables and optical fibres.
- Generally provides controlled transmission conditions and can offer high security and reliability.
Wireless communication:
- Uses electromagnetic waves through free space.
- Examples: radio, Wi-Fi, Bluetooth, cellular and satellite communication.
- Supports mobility but may experience interference, fading and signal obstruction.
  Based on direction of communication;
Simplex:
- Communication occurs in one direction only.
- Example: conventional radio broadcasting.
Half-duplex:
- Communication occurs in both directions, but not simultaneously.
- Example: walkie-talkies.
Full-duplex:
- Communication occurs in both directions simultaneously.
- Example: telephone conversations.

 COMMUNICATION CHANNEL CHARACTERISTICS
A communication channel affects the quality and reliability of transmitted signals.
  Important characteristics:
a) Bandwidth
- The range of frequencies a channel can transmit.
- Measured in hertz (Hz).
- Greater bandwidth generally allows higher data rates.
For a band-limited channel:
    B = f_high - f_low
b) Noise
- Unwanted random electrical or electromagnetic disturbances.
- Reduces signal quality and can cause errors.
- Common types include thermal noise, shot noise, atmospheric noise and impulse noise.
c) Attenuation
- Reduction in signal amplitude or power as it travels through a medium.
- Compensated for using amplifiers or repeaters, depending on the system.
d) Distortion
- Change in the shape of a signal during transmission.
- May result from unequal attenuation or phase delay at different frequencies.
e) Interference
- Unwanted signals from other sources that affect communication.
- Examples: adjacent-channel interference and electromagnetic interference.
f) Fading
- Variation in received signal strength, especially in wireless systems.
- Caused by multipath propagation, movement and changing environmental conditions.

 MODULATION
Modulation is the process of varying a characteristic of a high-frequency carrier signal according to the information signal.
A carrier signal is commonly represented as:
    c(t) = A_c cos(2πf_ct + φ)
Where:
A_c = carrier amplitude
f_c = carrier frequency
φ = carrier phase
 Why modulation is necessary:
- Enables practical antenna sizes.
- Allows multiple signals to share the frequency spectrum.
- Improves transmission over certain channels.
- Supports frequency allocation and selective reception.
- Makes long-distance wireless transmission practical.
  ANALOG MODULATION;
1. Amplitude Modulation (AM)
- The amplitude of the carrier varies according to the message signal.
- Carrier frequency and phase remain constant in ideal conventional AM.
AM signal:
    s(t) = A_c[1 + μ cos(2πf_mt)]cos(2πf_ct)
Where:
μ = modulation index
f_m = message frequency
f_c = carrier frequency
Modulation index:
    μ = A_m/A_c
For conventional AM without overmodulation:
    0 ≤ μ ≤ 1
Bandwidth:
    BW = 2f_m(max)
Advantages:
- Simple transmitter and receiver design.
- Relatively easy demodulation.
Disadvantages:
- Susceptible to amplitude noise.
- Less power-efficient than many other modulation methods.
2. Frequency Modulation (FM);
- The instantaneous frequency of the carrier varies according to the message signal.
- Carrier amplitude remains constant in ideal FM.
FM modulation index:
    β = Δf/f_m
Where:
Δf = peak frequency deviation
f_m = modulating frequency
Carson's rule for approximate bandwidth:
    BW ≈ 2(Δf + f_m(max))
Advantages:
- Better resistance to amplitude noise than AM.
- Good audio quality in suitable systems.
Disadvantages:
- Requires more bandwidth than conventional AM.
- Transmitter and receiver designs can be more complex.
3. Phase Modulation (PM)
- The phase of the carrier varies according to the message signal.
- Used in angle-modulation systems and related digital modulation methods.
  DIGITAL MODULATION;
Digital modulation represents digital information using changes in a carrier signal.
1. Amplitude Shift Keying (ASK)
- Carrier amplitude changes according to the digital data.
- Simple but sensitive to amplitude noise.
2. Frequency Shift Keying (FSK)
- Different carrier frequencies represent different digital symbols.
- Used in some low-data-rate radio and telemetry systems.
3. Phase Shift Keying (PSK)
- Digital information is represented by changes in carrier phase.
- Examples: BPSK, QPSK and higher-order PSK.
4. Quadrature Amplitude Modulation (QAM)
- Combines amplitude and phase changes.
- Transmits multiple bits per symbol.
- Used in Wi-Fi, cellular systems and digital television.
For M-ary modulation:
    Bits per symbol = log₂(M)
Where M is the number of possible symbols.
Example:
16-QAM carries log₂(16) = 4 bits per symbol.

 MULTIPLEXING
Multiplexing allows multiple signals or data streams to share one communication channel.
A multiplexer (MUX) combines signals at the transmitter, while a demultiplexer (DEMUX) separates them at the receiver.
  Main types:
a) Frequency Division Multiplexing (FDM)
- Divides channel bandwidth into separate frequency bands.
- Different signals occupy different frequency ranges.
- Used in radio and cable communication.
b) Time Division Multiplexing (TDM)
- Assigns different time slots to different users or data streams.
- Can be synchronous or statistical.
- Used in digital communication systems.
c) Wavelength Division Multiplexing (WDM)
- Uses different wavelengths of light to carry multiple data streams through one optical fibre.
- Important in high-capacity optical networks.
d) Code Division Multiplexing (CDM/CDMA)
- Uses distinct spreading codes to allow multiple users to share the same frequency and time resources.
- Used in certain cellular systems.

 SAMPLING, QUANTIZATION AND ENCODING
These processes convert analog information into digital form.
A. Sampling
- Measures the amplitude of an analog signal at regular time intervals.
- Converts a continuous-time signal into a discrete-time sequence.
Sampling frequency:
    f_s = 1/T_s
Nyquist sampling condition:
    f_s ≥ 2f_max
Where:
f_s = sampling frequency
f_max = highest frequency component in the signal
Sampling below the required rate can cause aliasing.
B. Quantization
- Maps each sampled amplitude to one of a finite number of amplitude levels.
- Introduces quantization error.
For a uniform quantizer:
    Δ = (V_max - V_min)/L   
Where:
Δ = quantization step size
L = number of quantization levels
For an n-bit quantizer:
    L = 2^n
C. Encoding
- Converts quantized levels into binary codewords.
- Produces a digital bitstream for transmission or storage.
D. Pulse Code Modulation (PCM)
Main stages:
1. Sampling.
2. Quantization.
3. Binary encoding.
For an ideal uniform quantizer, approximate signal-to-quantization-noise ratio for a full-scale sinusoidal input is:
    SQNR ≈ 6.02n + 1.76 dB
Where n is the number of bits per sample.
PCM is used in digital telephony, audio systems and digital recording.

 DIGITAL COMMUNICATION SYSTEM
A typical digital communication system follows:
Information Source → Source Encoder → Channel Encoder → Digital Modulator → Channel → Demodulator → Channel Decoder → Source Decoder → Destination
  Main operations:
Source encoding:
- Represents information efficiently.
- Removes redundancy where appropriate.
- Examples: audio, image and video compression.
Channel encoding:
- Adds controlled redundancy to help detect or correct errors.
- Examples: Hamming, Reed-Solomon and LDPC codes.
Modulation:
- Maps bits into symbols suitable for transmission.
Demodulation:
- Estimates the transmitted symbols from the received waveform.
Channel decoding:
- Detects or corrects errors using the added redundancy.
Source decoding:
- Reconstructs the original information.

 TRANSMISSION MODES AND TECHNIQUES
Serial transmission:
- Sends bits one after another over a communication path.
- Common in USB, UART and many network interfaces.
Parallel transmission:
- Sends multiple bits simultaneously over separate lines.
- Useful over short distances but can suffer from timing skew and wiring complexity.
Synchronous transmission:
- Transmitter and receiver share timing information.
- Data is transmitted in coordinated frames or streams.
Asynchronous transmission:
- Uses start and stop bits or other framing to identify data units.
- Common in UART communication.
Baseband transmission:
- Sends a signal directly in its original or line-coded frequency range without modulating it onto a separate carrier.
- Common in wired digital links.
Passband transmission:
- Modulates information onto a carrier frequency.
- Common in radio and wireless systems.

 LINE CODING
Line coding converts binary data into electrical or optical signal patterns suitable for a physical transmission medium.
  Common line codes:
NRZ (Non-Return-to-Zero):
- Signal level represents each bit.
- Simple but may have synchronization problems with long runs of identical bits.
RZ (Return-to-Zero):
- Signal returns to a reference level within each bit period.
- Can improve timing recovery but may require more bandwidth.
Manchester encoding:
- Uses a transition in the middle of each bit period.
- Provides clock information but requires more bandwidth.
AMI (Alternate Mark Inversion):
- Binary 1s alternate between positive and negative voltage levels.
- Helps reduce DC components.
  Important considerations:
- Bandwidth efficiency.
- Clock recovery and synchronization.
- DC content.
- Error performance.

 NOISE AND SIGNAL QUALITY
Signal-to-Noise Ratio (SNR):
    SNR = P_signal/P_noise
In decibels:
    SNR(dB) = 10log₁₀(P_signal/P_noise)
For voltage measurements across the same resistance:
    SNR(dB) = 20log₁₀(V_signal/V_noise)
A higher SNR generally means a clearer received signal.
Bit Error Rate (BER):
    BER = Number of erroneous bits / Total bits received
BER is an important measure of digital communication reliability.
 Sources of errors:
- Noise.
- Interference.
- Fading.
- Distortion.
- Synchronization errors.
- Channel impairments.
  Methods of improving communication quality:
- Filtering.
- Shielding and proper grounding.
- Amplification and repeaters.
- Error detection and correction.
- Appropriate modulation and coding.
- Diversity techniques and equalization.

 CHANNEL CAPACITY AND DATA RATE
Channel capacity is the maximum theoretical rate at which information can be transmitted reliably under specified channel assumptions.
Shannon-Hartley theorem:
    C = B log₂(1 + S/N)
Where:
C = channel capacity in bits per second
B = bandwidth in hertz
S/N = linear signal-to-noise power ratio
  Important:
- Increasing bandwidth increases theoretical capacity.
- Increasing SNR also increases capacity.
- Capacity is a theoretical limit, not necessarily the actual achievable data rate.
Bit rate:
- Number of bits transmitted per second.
- Measured in bits/s.
Symbol rate (baud):
- Number of transmitted symbols per second.
For a modulation scheme carrying log₂(M) bits per symbol:
    Bit rate = Symbol rate × log₂(M)
This assumes each symbol carries the same number of bits and ignores framing and coding overhead.

 ANTENNAS AND ELECTROMAGNETIC WAVE PROPAGATION
An antenna converts electrical signals into electromagnetic waves during transmission and electromagnetic waves into electrical signals during reception.
  Important antenna parameters:
- Gain: Measures directional concentration of radiated power relative to a reference antenna.
- Directivity: Describes how concentrated radiation is in a particular direction.
- Polarization: Orientation of the electric field of the radiated wave.
- Radiation pattern: Describes how antenna radiation varies with direction.
- Bandwidth: Frequency range over which the antenna performs acceptably.
- Impedance: Electrical opposition presented by the antenna.
Wavelength:
    λ = c/f
Where:
λ = wavelength in metres
c ≈ 3 × 10⁸ m/s in free space
f = frequency in hertz
Common antenna types:
- Dipole.
- Monopole.
- Loop.
- Yagi-Uda.
- Parabolic reflector.
- Patch or microstrip antenna.
- Horn antenna.
Propagation mechanisms:
- Ground-wave propagation.
- Sky-wave propagation.
- Line-of-sight propagation.
- Reflection, diffraction and scattering.

 WIRELESS COMMUNICATION SYSTEMS
Wireless communication transfers information through electromagnetic waves without a physical cable between communicating devices.
  Important technologies:
Radio communication:
- Uses radio-frequency electromagnetic waves.
- Applied in broadcasting, telemetry and wireless links.
Microwave communication:
- Uses high-frequency radio waves.
- Applied in point-to-point links, radar and satellite systems.
Cellular communication:
- Divides geographical areas into cells served by base stations.
- Allows users to communicate while moving between cells through handover.
- Modern generations include 4G LTE and 5G NR.
Wi-Fi:
- Provides wireless local area networking.
- Commonly uses IEEE 802.11 standards.
Bluetooth:
- Provides short-range wireless communication.
- Used in peripherals, wearables and embedded devices.
Satellite communication:
- Uses satellites to relay signals over large geographical areas.
- Used in broadcasting, navigation, internet access and remote communication.

 OPTICAL FIBRE COMMUNICATION
Optical fibre communication transmits information using light through thin glass or plastic fibres.
Operating principle:
- Light is guided through the fibre core by total internal reflection.
- A transmitter converts electrical data into optical signals.
- A photodetector converts received light back into electrical signals.
  Main components:
- Optical transmitter (LED or laser diode).
- Optical fibre.
- Connectors and splices.
- Optical amplifiers or repeaters where required.
- Photodetector (PIN or avalanche photodiode).
Advantages:
- High bandwidth.
- Low attenuation over suitable distances.
- Immunity to electromagnetic interference.
- Electrical isolation.
- Difficult to tap without detection compared with many conventional cables.
Limitations:
- Installation and splicing require specialized equipment.
- Fibres can be damaged by excessive bending or mechanical stress.
- Optical components may be costly.
Applications:
- Internet backbone networks.
- Telecommunications.
- Data centres.
- Fibre-to-the-home systems.
- Industrial communication.

 SYNCHRONIZATION AND EQUALIZATION
Synchronization ensures that the transmitter and receiver agree on timing and, where necessary, carrier frequency and phase.
Types:
- Bit synchronization: Identifies individual bit boundaries.
- Frame synchronization: Identifies the beginning of data frames.
- Carrier synchronization: Recovers carrier frequency and phase.
- Clock recovery: Reconstructs timing information from the received signal.
Equalization:
- Compensates for channel effects that distort the transmitted signal.
- Reduces intersymbol interference (ISI).
- Used in high-speed wired and wireless communication.
Intersymbol interference occurs when energy from one transmitted symbol spreads into neighbouring symbol intervals, making symbol detection more difficult.

 COMMUNICATION PROTOCOLS AND NETWORKING
A communication protocol is a set of rules that governs how devices exchange information.
  Important protocols and standards:
- UART: Serial communication interface commonly used between microcontrollers and peripherals.
- SPI: High-speed synchronous serial interface.
- I²C: Two-wire synchronous communication bus.
- CAN: Robust communication bus used in vehicles and industrial systems.
- Ethernet: Wired local area networking technology.
- TCP/IP: Core protocol suite used by the internet.
- UDP: Connectionless transport protocol with low overhead.
- HTTP/HTTPS: Protocols used for web communication.
  Important concepts:
- Addressing identifies communication endpoints.
- Framing organizes data into units.
- Routing selects paths through networks.
- Flow control prevents a sender from overwhelming a receiver.
- Error control improves reliability.
- Handshaking coordinates communication.

 COMMUNICATION SYSTEM PERFORMANCE PARAMETERS
Important parameters used to evaluate communication systems:
- Bandwidth: Frequency range available for transmission.
- Data rate: Number of bits transmitted per second.
- Throughput: Actual successful data delivery rate.
- Latency: Time taken for information to travel from source to destination.
- SNR: Ratio of signal power to noise power.
- BER: Fraction of received bits that are erroneous.
- Spectral efficiency: Data rate per unit bandwidth, measured in bit/s/Hz.
- Power efficiency: How effectively transmission power is used.
- Reliability: Ability to deliver information correctly and consistently.
- Coverage: Geographical area in which communication is available.

 IMPORTANT FORMULAS SUMMARY
1. Bandwidth:
   B = f_high - f_low
2. Wavelength:
   λ = c/f
3. Sampling frequency:
   f_s = 1/T_s
4. Nyquist sampling condition:
   f_s ≥ 2f_max
5. AM modulation index:
   μ = A_m/A_c
6. FM modulation index:
   β = Δf/f_m
7. Approximate FM bandwidth (Carson's rule):
   BW ≈ 2(Δf + f_m(max))
8. AM bandwidth:
   BW = 2f_m(max)
9. Number of quantization levels:
   L = 2^n
10. PCM bit rate:
    R_b = n f_s
11. Bits per symbol:
    k = log₂(M)
12. Digital bit rate:
    R_b = R_s log₂(M)
13. Signal-to-noise ratio:
    SNR = P_signal/P_noise
14. SNR in decibels:
    SNR(dB) = 10log₁₀(S/N)
15. Bit error rate:
    BER = Error bits / Total received bits
16. Shannon channel capacity:
    C = B log₂(1 + S/N)
17. Spectral efficiency:
    η = R_b/B

20. PRACTICAL ENGINEERING APPLICATIONS
  Communication systems are used in:
- Mobile phones and cellular base stations.
- Internet and computer networks.
- Satellite navigation and communication.
- Wireless sensor networks.
- Industrial automation and remote monitoring.
- Vehicle communication systems.
- Medical telemetry and remote patient monitoring.
- Robotics and remote-control systems.
- Smart homes and IoT devices.
- Broadcasting and emergency communication.

 PRACTICAL PROJECTS FOR ENGINEERING STUDENTS
1. FM transmitter and receiver:
   Study frequency modulation, transmission and demodulation.
2. Digital data transmission using Arduino or ESP32:
   Send sensor readings between two devices using UART, Bluetooth or Wi-Fi.
3. Wireless temperature monitoring:
   Build a sensor node that transmits temperature data to a receiver.
4. Optical communication experiment:
   Transmit digital data using an LED or laser and receive it using a photodetector.
5. Digital modulation simulation:
   Generate and compare ASK, FSK, BPSK and QPSK using Python or MATLAB.
6. Software-defined radio (SDR):
   Receive and analyze radio signals using an SDR device and GNU Radio.
7. Communication channel simulation:
   Add noise to a transmitted signal and investigate its effect on SNR and BER.

22. STUDY AND EXAMINATION TIPS
- Understand the complete communication-system block diagram and the function of every component.
- Distinguish analog from digital communication.
- Clearly differentiate AM, FM and PM.
- Know the differences between ASK, FSK, PSK and QAM.
- Understand sampling, quantization and PCM.
- Practise bandwidth, modulation-index, bit-rate, wavelength and channel-capacity calculations.
- Distinguish bit rate from baud rate.
- Understand the effects of noise, attenuation, distortion, interference and fading.
- Compare FDM, TDM, WDM and CDM.
- Understand the advantages and limitations of wired, wireless and optical communication.
- Relate theoretical concepts to practical communication technologies.