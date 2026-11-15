            WIRELESS COMMUNICATION
Wireless communication is the transfer of information between two or more devices using electromagnetic waves without requiring a physical cable connection.
Information is transmitted through free space using radio waves, microwaves, infrared or other electromagnetic radiation.
  Main objectives:
- Enable communication without physical connections.
- Support mobility and remote connectivity.
- Transmit information over short or long distances.
- Provide reliable communication with efficient use of spectrum and power.
  Applications:
- Mobile cellular networks (2G, 3G, 4G and 5G).
- Wi-Fi and Bluetooth.
- Satellite communication.
- GPS and navigation.
- Wireless sensor networks.
- Internet of Things (IoT).
- Radar and remote sensing.
- Wireless industrial automation.

 BASIC WIRELESS COMMUNICATION SYSTEM
A typical wireless communication system consists of:
Information Source → Transmitter → Transmitting Antenna → Wireless Channel → Receiving Antenna → Receiver → Destination
  Main components:
a) Information source
- Generates the information to be transmitted.
- Examples: microphone, camera, computer or sensor.
b) Transmitter
- Converts information into a suitable electrical or radio-frequency signal.
- Performs encoding, modulation, filtering and amplification.
c) Transmitting antenna
- Converts electrical signals into electromagnetic waves.
- Radiates the waves into free space.
d) Wireless channel
- The environment through which electromagnetic waves propagate.
- May introduce attenuation, noise, interference, reflection and fading.
e) Receiving antenna
- Captures electromagnetic waves and converts them into electrical signals.
f) Receiver
- Amplifies, filters, demodulates and decodes the received signal.
- Recovers the original information.

 ELECTROMAGNETIC WAVES AND RADIO FREQUENCY
Wireless communication mainly uses electromagnetic waves to transport information.
An electromagnetic wave consists of changing electric and magnetic fields that propagate through space.
  Important properties:
- Frequency (f): Number of wave cycles per second, measured in hertz (Hz).
- Wavelength (λ): Distance between successive corresponding points of a wave.
- Amplitude: Magnitude of the wave.
- Phase: Position of a wave within its cycle.
- Propagation speed: Speed at which the wave travels.
Relationship between wavelength, frequency and propagation speed:
    λ = c/f
Where:
λ = wavelength (m)
c = speed of light ≈ 3 × 10⁸ m/s in free space
f = frequency (Hz)
  Important relationship:
- Higher frequency means shorter wavelength.
- Lower frequency means longer wavelength.
  Radio frequency spectrum:
- LF: 30–300 kHz
- MF: 300 kHz–3 MHz
- HF: 3–30 MHz
- VHF: 30–300 MHz
- UHF: 300 MHz–3 GHz
- SHF: 3–30 GHz
- EHF: 30–300 GHz
Different frequency ranges have different propagation, coverage, bandwidth and penetration characteristics.

 WIRELESS FREQUENCY BANDS AND APPLICATIONS
  Common applications include:
- AM broadcasting: Uses medium-frequency bands.
- FM broadcasting: Uses VHF bands.
- Television broadcasting: Uses VHF and UHF bands.
- Cellular communication: Uses various licensed bands, depending on the generation and country.
- Wi-Fi: Commonly operates in 2.4 GHz, 5 GHz and 6 GHz bands, subject to regional regulations.
- Bluetooth: Operates in the 2.4 GHz ISM band.
- Satellite communication: Uses several microwave frequency bands.
- Millimetre-wave communication: Uses frequencies such as 24 GHz and above for high-capacity links.
  Important:
Frequency allocation is regulated nationally and internationally. A frequency band being technically suitable does not automatically mean it is available for unrestricted use.

 WIRELESS TRANSMISSION MODES
Wireless systems can be classified according to the direction of communication.
a) Simplex
- Information travels in one direction only.
- Example: conventional radio broadcasting.
b) Half-duplex
- Communication occurs in both directions, but not simultaneously.
- Example: walkie-talkies.
c) Full-duplex
- Communication occurs in both directions simultaneously.
- Example: cellular voice communication.
Wireless links can also be classified by their communication arrangement:
- Point-to-point: Direct connection between two communication endpoints.
- Point-to-multipoint: One central transmitter communicates with multiple receivers.
- Broadcast: One transmitter distributes information to many receivers.
- Mesh: Devices communicate through multiple interconnected wireless nodes.

 WIRELESS PROPAGATION MECHANISMS
Wireless signals interact with objects and the environment as they travel.
a) Reflection
- Occurs when electromagnetic waves encounter large surfaces such as buildings, walls or the ground.
- Can create multiple signal paths.
b) Diffraction
- Occurs when waves bend around obstacles or edges.
- Allows signals to reach areas without a direct line of sight.
c) Scattering
- Occurs when waves encounter objects with dimensions comparable to or smaller than their wavelength.
- Examples include foliage, rough surfaces and small structures.
d) Absorption
- Occurs when materials absorb electromagnetic energy.
- Can reduce signal strength.
e) Refraction
- Occurs when waves change direction due to changes in propagation medium or its properties.
These mechanisms influence signal strength, coverage and reliability.

 TYPES OF WIRELESS PROPAGATION
a) Ground-wave propagation
- Radio waves travel along or near the Earth's surface.
- Commonly associated with lower-frequency communication.
b) Sky-wave propagation
- Radio waves are refracted by ionized regions of the upper atmosphere.
- Can support long-distance HF communication.
c) Line-of-sight (LOS) propagation
- Communication occurs through a relatively unobstructed path between antennas.
- Common in microwave, satellite and many high-frequency wireless links.
d) Non-line-of-sight (NLOS) propagation
- Communication occurs without a direct unobstructed path.
- Relies on reflection, diffraction and scattering.

 FREE-SPACE PATH LOSS
As a radio signal travels away from a transmitting antenna, its power spreads over a larger area, reducing the received power density.
Free-space path loss (FSPL) is:
    FSPL = (4πd/λ)²
In decibels:
    FSPL(dB) = 20log₁₀(4πd/λ)
A commonly used practical formula is:
    FSPL(dB) = 32.44 + 20log₁₀(f_MHz) + 20log₁₀(d_km)
Where:
f_MHz = frequency in MHz
d_km = distance in kilometres
  Important:
- Increasing distance increases path loss.
- Increasing frequency increases free-space path loss for the same distance when antenna gains are held constant.
- This formula assumes ideal free-space propagation, not real environments with obstacles or multipath.

 ANTENNAS IN WIRELESS COMMUNICATION
An antenna is a device that converts electrical energy into electromagnetic waves during transmission and electromagnetic waves into electrical signals during reception.
  Important antenna parameters:
a) Antenna gain
- Measures how effectively an antenna concentrates energy in a particular direction relative to a reference antenna.
- Expressed in dBi when referenced to an isotropic radiator.
b) Directivity
- Describes how concentrated the antenna radiation is in a particular direction.
c) Radiation pattern
- Shows how an antenna radiates or receives energy in different directions.
d) Polarization
- Describes the orientation of the electric field.
- Common types: vertical, horizontal and circular polarization.
e) Bandwidth
- The frequency range over which an antenna operates effectively.
f) Impedance
- Electrical opposition presented by an antenna.
- Proper impedance matching reduces reflections and improves power transfer.
  Common antenna types:
- Dipole antenna.
- Monopole antenna.
- Yagi-Uda antenna.
- Patch antenna.
- Helical antenna.
- Parabolic reflector.
- Horn antenna.
- Phased-array antenna.

 MODULATION IN WIRELESS COMMUNICATION
Modulation is the process of varying a carrier signal according to the information being transmitted.
It makes information suitable for radio-frequency transmission.
 Analog modulation
1. Amplitude Modulation (AM)
- Carrier amplitude changes according to the message signal.
- Used in conventional AM broadcasting.
2. Frequency Modulation (FM)
- Carrier frequency varies according to the message signal.
- Used in FM broadcasting and other radio systems.
3. Phase Modulation (PM)
- Carrier phase varies according to the message signal.
 Digital modulation
1. ASK (Amplitude Shift Keying)
- Represents digital symbols through changes in carrier amplitude.
2. FSK (Frequency Shift Keying)
- Represents digital symbols using different carrier frequencies.
3. PSK (Phase Shift Keying)
- Represents digital symbols using different carrier phases.
- Examples: BPSK and QPSK.
4. QAM (Quadrature Amplitude Modulation)
- Uses combinations of amplitude and phase changes.
- Examples: 16-QAM, 64-QAM and 256-QAM.
5. OFDM (Orthogonal Frequency Division Multiplexing)
- Divides data across many closely spaced, mathematically orthogonal subcarriers.
- Improves resistance to frequency-selective fading and multipath.
- Used in Wi-Fi, 4G LTE and 5G NR.

 MULTIPLE ACCESS TECHNIQUES
Multiple access techniques allow several users to share wireless communication resources.
a) FDMA (Frequency Division Multiple Access)
- Each user is allocated a separate frequency channel.
- Used in early cellular systems.
b) TDMA (Time Division Multiple Access)
- Users share a frequency channel but transmit in different time slots.
- Used in GSM.
c) CDMA (Code Division Multiple Access)
- Users share frequency and time resources but use different spreading codes.
- Used in IS-95 and certain 3G systems.
d) OFDMA (Orthogonal Frequency Division Multiple Access)
- Allocates groups of orthogonal subcarriers to different users.
- Used in 4G LTE downlink and 5G NR.
e) SDMA (Space Division Multiple Access)
- Separates users spatially using directional antennas or beamforming.
- Important in modern multi-antenna wireless systems.

 MULTIPATH PROPAGATION AND FADING
Multipath propagation occurs when a transmitted signal reaches a receiver through multiple paths due to reflection, diffraction and scattering.
The different signal copies may arrive with different:
- Amplitudes.
- Phases.
- Delays.
This can cause constructive or destructive interference.
Fading is the variation in received signal strength over time, frequency or position.
  Types of fading:
a) Large-scale fading
- Signal variation over relatively large distances.
- Mainly caused by path loss and shadowing.
b) Small-scale fading
- Rapid signal variation over short distances or time intervals.
- Mainly caused by multipath propagation.
c) Flat fading
- Affects approximately all frequency components of a signal similarly.
d) Frequency-selective fading
- Affects different frequency components differently.
e) Rayleigh fading
- Common model for multipath environments without a dominant direct path.
f) Rician fading
- Common model when a dominant direct path exists alongside scattered paths.
  Methods of reducing fading:
- Diversity reception.
- MIMO techniques.
- Antenna placement optimization.
- Equalization.
- OFDM.
- Beamforming and suitable channel coding.

 NOISE AND INTERFERENCE
Noise is unwanted random disturbance that affects a received signal.
  Common types:
a) Thermal noise
- Produced by random motion of charge carriers in electronic components.
- Present in all systems above absolute zero.
Thermal noise power:
    P_n = kTB
Where:
k = Boltzmann constant (1.38 × 10⁻²³ J/K)
T = absolute temperature in kelvin
B = bandwidth in hertz
b) Shot noise
- Caused by the discrete nature of electric charge and random carrier movement.
c) Atmospheric noise
- Caused by natural electrical phenomena such as lightning.
d) Impulse noise
- Short-duration, high-amplitude disturbances.
e) Co-channel interference
- Caused by other transmitters using the same frequency channel.
f) Adjacent-channel interference
- Caused by signals from nearby frequency channels.
Signal-to-Noise Ratio:
    SNR = P_signal/P_noise
In decibels:
    SNR(dB) = 10log₁₀(P_signal/P_noise)
A higher SNR generally improves the reliability of signal detection.

 LINK BUDGET
A link budget calculates the expected received signal power by accounting for transmitter power, antenna gains and losses along the communication path.
Basic link budget equation:
    P_r(dBm) = P_t(dBm) + G_t(dBi) + G_r(dBi) - L_t(dB) - L_r(dB) - L_p(dB)
Where:
P_r = received power
P_t = transmitted power
G_t = transmitting antenna gain
G_r = receiving antenna gain
L_t = transmitter-side losses
L_r = receiver-side losses
L_p = propagation path loss
Link margin:
    Link Margin = Received Power - Receiver Sensitivity
All quantities must be expressed in compatible units, normally dB or dBm as appropriate.
A positive link margin indicates that received power exceeds the receiver's sensitivity threshold. A practical design also allows margin for fading, interference and implementation losses.

 CELLULAR COMMUNICATION SYSTEMS
A cellular network divides a geographical area into smaller regions called cells.
Each cell is served by a base station that communicates with mobile devices.
  Main components:
a) Mobile station / User Equipment (UE)
- A mobile phone, modem or other wireless device.
b) Base station
- Provides radio communication between mobile devices and the network.
- Examples include BTS, NodeB, eNodeB and gNodeB in different generations.
c) Core network
- Manages communication, authentication, mobility and connections to external networks.
d) Backhaul
- Connects base stations to the wider network infrastructure.
  Important concepts:
Cell
- A geographical coverage area served by a base station.
Frequency reuse
- Reusing the same frequency resources in sufficiently separated cells to increase network capacity.
Handover
- Transfer of an active connection from one cell or base station to another as a user moves.
Roaming
- Allows a subscriber to use services through another network under an agreement.
Small cells
- Low-power base stations used to improve capacity and coverage in targeted areas.

 GENERATIONS OF CELLULAR NETWORKS
1G:
- First-generation analogue cellular communication.
- Mainly supported voice calls.
2G:
- Digital cellular communication.
- Introduced improved voice quality, encryption and SMS.
- Examples: GSM and IS-95.
2.5G / 2.75G:
- Added packet-data capabilities.
- Examples: GPRS and EDGE.
3G:
- Improved mobile internet and multimedia services.
- Examples: UMTS/WCDMA and CDMA2000.
4G:
- High-speed, all-IP mobile broadband.
- LTE is the major technology family.
- Supports high-quality streaming and VoLTE.
5G:
- Designed for higher capacity, lower latency in suitable deployments and massive device connectivity.
- Uses technologies such as massive MIMO, beamforming, OFDM and network slicing.
- Supports enhanced mobile broadband, massive machine-type communication and ultra-reliable low-latency communication use cases.

 WI-FI AND BLUETOOTH
A. Wi-Fi
Wi-Fi is a wireless local area networking technology based on IEEE 802.11 standards.
Characteristics:
- Provides wireless access to local networks and the internet.
- Operates in frequency bands including 2.4 GHz, 5 GHz and 6 GHz, depending on standard and regional rules.
- Uses technologies including OFDM/OFDMA and MIMO in modern versions.
- Commonly uses an access point to connect devices.
Applications:
- Homes and offices.
- Universities and public hotspots.
- Industrial wireless networks.
- IoT connectivity.
B. Bluetooth
Bluetooth is a short-range wireless technology operating in the 2.4 GHz ISM band.
Characteristics:
- Low power consumption in many implementations.
- Supports device-to-device communication.
- Bluetooth Low Energy (BLE) is designed for low-power devices.
- Uses frequency hopping to help manage interference.
Applications:
- Wireless headphones.
- Smart watches.
- Sensors.
- Keyboards and mice.
- Embedded systems and IoT.

 SATELLITE COMMUNICATION
Satellite communication uses artificial satellites to relay radio signals between geographically separated locations.
  Basic operation:
1. An earth station transmits a signal to the satellite (uplink).
2. The satellite receives and processes or relays the signal.
3. The signal is transmitted back to an earth station (downlink).
  Important terms:
Uplink:
- Transmission from an earth station to a satellite.
Downlink:
- Transmission from a satellite to an earth station.
Transponder:
- Satellite subsystem that receives, processes and retransmits signals.
  Satellite orbit types:
a) GEO (Geostationary Earth Orbit)
- Approximately 35,786 km above the equator.
- Satellite appears stationary relative to the Earth's surface.
- Useful for broadcasting and fixed communication links.
- Has relatively high propagation delay.
b) MEO (Medium Earth Orbit)
- Used by several navigation and communication satellite systems.
c) LEO (Low Earth Orbit)
- Lower altitude than GEO.
- Can provide lower propagation delay.
- Often requires multiple satellites for continuous coverage.
Applications:
- Television broadcasting.
- Satellite internet.
- GPS and navigation.
- Weather monitoring.
- Remote-area connectivity.

 MIMO AND BEAMFORMING
A. MIMO (Multiple Input Multiple Output)
MIMO uses multiple transmitting and receiving antennas to improve wireless communication.
Benefits:
- Higher data throughput.
- Improved link reliability.
- Better spectral efficiency.
- Improved coverage under suitable conditions.
Main techniques:
Spatial multiplexing:
- Transmits multiple independent data streams through the same time-frequency resources.
Diversity:
- Uses multiple signal paths or antennas to improve reliability.
Massive MIMO:
- Uses a large number of antenna elements, particularly in modern cellular systems.
B. Beamforming
Beamforming controls the phase and amplitude of signals from multiple antenna elements to direct radio energy toward particular users or directions.
Benefits:
- Improves received signal strength.
- Reduces interference in unwanted directions.
- Improves spatial coverage and capacity.

 WIRELESS SENSOR NETWORKS AND IoT
A Wireless Sensor Network (WSN) consists of multiple sensor nodes that communicate wirelessly to monitor physical or environmental conditions.
  Typical sensor node components:
- Sensors.
- Microcontroller.
- Wireless transceiver.
- Power supply or battery.
- Antenna.
Operation:
  1. Sensors measure physical parameters.
2. The microcontroller processes the measurements.
3. The wireless module transmits data.
4. A gateway or receiver collects the data.
5. A monitoring system stores, displays or analyzes the information.
  Common wireless technologies:
Wi-Fi:
- Suitable for relatively high data rates and network connectivity.
Bluetooth Low Energy:
- Suitable for low-power, short-range devices.
Zigbee:
- Low-power mesh networking based on IEEE 802.15.4.
LoRa/LoRaWAN:
- Designed for long-range, low-data-rate IoT communication.
NB-IoT:
- Cellular technology designed for low-power wide-area IoT connectivity.
Applications:
- Smart agriculture.
- Environmental monitoring.
- Smart homes.
- Industrial automation.
- Asset tracking.
- Smart metering.

 WIRELESS SECURITY
Wireless signals travel through open environments, making security essential.
  Common threats:
- Eavesdropping.
- Unauthorized access.
- Spoofing and impersonation.
- Replay attacks.
- Denial-of-service attacks.
- Rogue access points.
  Security measures:
- Strong encryption.
- Secure authentication.
- Proper access control.
- Regular firmware and software updates.
- Secure key management.
- Network monitoring and segmentation.
  Examples:
- WPA2 and WPA3 for Wi-Fi security.
- Encryption and authentication in cellular networks.
- Secure pairing and application-level protection for Bluetooth devices.

 WIRELESS COMMUNICATION PERFORMANCE PARAMETERS
  Important parameters:
Bandwidth:
- Frequency range available for communication.
Data rate:
- Number of bits transmitted per second.
Throughput:
- Actual successful data delivery rate.
Latency:
- Time taken for data to travel from source to destination.
SNR:
- Ratio of signal power to noise power.
BER:
- Ratio of erroneous received bits to total received bits.
RSSI:
- Received Signal Strength Indicator; a measure or estimate of received signal strength.
Spectral efficiency:
- Data rate per unit bandwidth, measured in bit/s/Hz.
Coverage:
- Geographical area in which a wireless service is available.
Reliability:
- Ability to maintain communication with an acceptable error rate and availability.

 IMPORTANT FORMULAS SUMMARY
1. Wavelength:
   λ = c/f
2. Frequency:
   f = c/λ
3. Free-space path loss:
   FSPL = (4πd/λ)²
4. Free-space path loss in dB:
   FSPL(dB) = 32.44 + 20log₁₀(f_MHz) + 20log₁₀(d_km)
5. Thermal noise power:
   P_n = kTB
6. Signal-to-noise ratio:
   SNR = P_signal/P_noise
7. SNR in dB:
   SNR(dB) = 10log₁₀(S/N)
8. Link budget:
   P_r = P_t + G_t + G_r - L_t - L_r - L_p
9. Link margin:
   Link Margin = P_r - Receiver Sensitivity
10. Shannon channel capacity:
    C = B log₂(1 + S/N)
11. Doppler frequency shift (for radial motion):
    f_d = (v/c)f_c
Where:
v = relative radial speed
c = propagation speed
f_c = carrier frequency
For motion toward the transmitter, the received frequency increases; for motion away, it decreases.

 PRACTICAL ENGINEERING PROJECTS
1. Wireless temperature monitoring:
   Use an ESP32 to transmit temperature readings to a computer or mobile dashboard.
2. Bluetooth-controlled robot:
   Control a robot wirelessly using a smartphone and Bluetooth module.
3. Wi-Fi-based home automation:
   Use an ESP32 to control lights and monitor sensors over a local network.
4. LoRa-based agricultural monitoring:
   Transmit soil moisture and environmental data over long distances.
5. Wireless signal-strength measurement:
   Measure RSSI at different distances and investigate path loss.
6. Antenna design and testing:
   Build a dipole antenna and study its radiation and reception characteristics.
7. Digital modulation simulation:
   Use Python or MATLAB to simulate BPSK, QPSK and QAM under noisy channel conditions.
8. Wireless communication channel simulation:
   Model path loss, Rayleigh fading, noise and bit error rate.

 STUDY AND EXAMINATION TIPS
- Understand the complete wireless communication block diagram.
- Know the electromagnetic spectrum and frequency bands.
- Understand the relationship between frequency and wavelength.
- Distinguish reflection, diffraction, scattering and absorption.
- Understand line-of-sight and non-line-of-sight propagation.
- Practise free-space path-loss and link-budget calculations.
- Understand antenna gain, directivity, polarization and radiation patterns.
- Differentiate AM, FM, PSK, FSK, QAM and OFDM.
- Understand FDMA, TDMA, CDMA and OFDMA.
- Study multipath propagation, fading and diversity techniques.
- Understand cellular architecture, frequency reuse and handover.
- Compare Wi-Fi, Bluetooth, cellular, satellite and IoT communication.
- Relate MIMO and beamforming to modern wireless systems.
- Practise numerical problems involving SNR, thermal noise, wavelength and channel capacity.