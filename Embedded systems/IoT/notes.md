            INTERNET OF THINGS (IoT
The Internet of Things (IoT) is a network of physical objects embedded with sensors, actuators, processors, software and communication technologies that enable them to collect, exchange and act on data over a network.
IoT allows physical devices to be monitored, controlled and automated remotely with minimal human intervention.
  Main components of an IoT system;
1. Physical devices: Objects connected to the IoT network, such as vehicles, machines and appliances.
2. Sensors: Collect environmental or physical data such as temperature, pressure, humidity and motion.
3. Actuators: Perform physical actions based on received control instructions.
4. Microcontrollers/processors: Process sensor data and execute control instructions.
5. Connectivity: Enables devices to communicate through Wi-Fi, Bluetooth, cellular networks, Ethernet and other technologies.
6. Cloud/edge computing: Stores, processes and analyses collected data.
7. User interface: Allows users to monitor and control devices through applications, dashboards and web interfaces.
  Basic IoT operation;
Physical environment → Sensors → Embedded controller → Communication network → Cloud/Edge processing → User application or automated decision → Actuator.
Example: A smart irrigation system measures soil moisture, sends the readings to an IoT platform and automatically activates a water pump when moisture falls below a specified level.

 IoT ARCHITECTURE
IoT architecture describes how devices, networks, processing systems and applications interact.
  Three-layer architecture;
Perception layer (Device layer)
Responsible for collecting information from the physical environment.
Components:
- Sensors.
- Actuators.
- RFID tags.
- Microcontrollers.
- Embedded devices.
Functions:
- Data acquisition.
- Physical environment monitoring.
- Device identification.
- Physical control.
Network layer
Responsible for transferring data between IoT devices, gateways, servers and cloud platforms.
Technologies:
- Wi-Fi.
- Bluetooth.
- Zigbee.
- LoRaWAN.
- Ethernet.
- Cellular networks (4G/5G).
- NB-IoT.
Functions:
- Data transmission.
- Device connectivity.
- Routing.
- Communication management.
Application layer
Provides services and applications to end users.
Examples:
- Smart homes.
- Smart agriculture.
- Industrial automation.
- Healthcare monitoring.
- Smart transportation.
Functions:
- Data visualization.
- Remote monitoring.
- Device management.
- Automated decision-making.
  Five-layer architecture;
1. Perception layer: Collects physical data.
2. Transport layer: Transfers data between devices and processing systems.
3. Processing layer: Stores, processes and analyses information.
4. Application layer: Provides services to users.
5. Business layer: Manages business processes, policies and overall system performance.

 IoT HARDWARE COMPONENTS
  Microcontrollers;
Microcontrollers act as the processing units of IoT devices.
Common examples:
- Arduino Uno: ATmega328P-based development board.
- ESP8266: Wi-Fi-enabled microcontroller platform.
- ESP32: Supports Wi-Fi and Bluetooth on many variants.
- STM32: Family of ARM-based microcontrollers.
- Raspberry Pi Pico: RP2040-based microcontroller board.
Functions:
- Read sensor data.
- Process inputs.
- Control actuators.
- Communicate with other devices.
- Execute embedded programs.
  Sensors;
Sensors collect physical information.
Examples:
- DHT11/DHT22: Temperature and humidity.
- HC-SR04: Ultrasonic distance measurement.
- MQ-series: Gas detection.
- LDR: Light intensity.
- BMP280: Atmospheric pressure and temperature.
- MPU6050: Acceleration and angular velocity.
- Soil moisture sensor: Soil water-content estimation.
  Actuators;
Actuators execute physical actions.
Examples:
- DC motors.
- Servo motors.
- Relays.
- Solenoid valves.
- Pumps.
- LEDs.
- Heaters.
  IoT gateways;
An IoT gateway connects devices to other networks or cloud services.
Functions:
- Protocol conversion.
- Data filtering.
- Device authentication.
- Local processing.
- Network management.
Example: A gateway can collect Zigbee sensor data and forward it to a cloud platform using Wi-Fi or Ethernet.

 IoT COMMUNICATION TECHNOLOGIES
Communication technologies determine how IoT devices exchange information.
  Wi-Fi;
- Wireless networking technology.
- Provides relatively high data rates.
- Commonly used in smart homes and connected appliances.
- Generally consumes more power than low-power sensor networking technologies.
  Bluetooth and BLE;
Bluetooth Low Energy (BLE) is designed for short-range communication with low power consumption.
Applications:
- Wearables.
- Smart health devices.
- Beacons.
- Smartphone-connected sensors.
  Zigbee;
A low-power wireless communication technology based on IEEE 802.154.
Features:
- Supports mesh networking.
- Suitable for low-data-rate applications.
- Common in smart homes and industrial monitoring.
  LoRa and LoRaWAN;
LoRa is a long-range, low-power wireless modulation technology. LoRaWAN is a networking protocol built around LoRa communication.
Features:
- Long communication range.
- Low power consumption.
- Low data rates.
- Suitable for remote monitoring.
Applications:
- Smart agriculture.
- Environmental monitoring.
- Water management.
  Cellular IoT;
Uses cellular networks to connect devices over wide geographical areas.
Examples:
- 4G LTE.
- 5G.
- NB-IoT.
- LTE-M.
Applications:
- Vehicle tracking.
- Smart meters.
- Remote industrial monitoring.
  RFID and NFC;
RFID (Radio Frequency Identification):
Uses radio waves to identify and track tagged objects.
NFC (Near Field Communication):
Enables very short-range wireless communication.
Applications:
- Access control.
- Contactless payments.
- Inventory management.
- Identification systems.
  Comparison of communication technologies;
Technology| Range| Power consumption| Typical application
Wi-Fi| Short–medium| Medium–high| Smart appliances
BLE| Short| Low| Wearables
Zigbee| Short–medium| Low| Smart homes
LoRaWAN| Long| Very low| Agriculture
Cellular| Wide area| Medium–high, varies| Tracking
RFID| Short–variable| Low for passive tags| Identification
Ethernet| Wired| Depends on device| Industrial IoT
Actual range and power consumption depend on hardware, environment, configuration and network conditions.

 IoT COMMUNICATION PROTOCOLS
Communication protocols define how devices exchange data.
  MQTT (Message Queuing Telemetry Transport);
A lightweight messaging protocol commonly used in IoT.
It uses a publish-subscribe communication model.
Main components:
- Publisher: Sends messages.
- Subscriber: Receives messages.
- Broker: Receives and distributes messages.
- Topic: Identifies the message channel.
Example:
A temperature sensor publishes readings to "farm/temperature", while a monitoring application subscribes to that topic.
MQTT QoS levels:
- QoS 0: At most once delivery.
- QoS 1: At least once delivery.
- QoS 2: Exactly once delivery.
  HTTP/HTTPS;
HTTP is used for communication between clients and web servers.
Common methods:
- GET: Retrieve information.
- POST: Send information.
- PUT: Update or replace information.
- DELETE: Remove information.
HTTPS provides encrypted communication using TLS.
  CoAP (Constrained Application Protocol);
A lightweight application protocol designed for constrained IoT devices and networks.
Features:
- Low overhead.
- Typically uses UDP.
- Supports request-response communication.
- Suitable for resource-constrained environments.
  AMQP;
Advanced Message Queuing Protocol is a messaging protocol used for reliable message exchange between applications and systems.
  WebSocket;
Provides persistent, bidirectional communication between clients and servers.
Useful for:
- Real-time dashboards.
- Live sensor monitoring.
- Remote device control.

 IoT DATA ACQUISITION AND PROCESSING
Data acquisition involves collecting information from sensors and converting it into usable digital data.
Process
1. Physical measurement.
2. Sensor signal generation.
3. Signal conditioning.
4. Analog-to-digital conversion where necessary.
5. Data processing.
6. Data transmission.
7. Data storage and analysis.
8. Visualization or automated action.
Important data concepts
Sampling: Measuring a continuous signal at regular intervals.
Sampling frequency:
    fs = 1/Ts
Where:
- fs = sampling frequency (Hz).
- Ts = sampling period (s).
Nyquist sampling theorem:
    fs ≥ 2fmax
The sampling frequency must be at least twice the highest frequency component of a band-limited signal for ideal reconstruction.
Data rate:
    Data rate = Number of bits transmitted / Time taken
Units: bits per second (bps).
Data logging: Recording sensor readings over time for analysis and monitoring.
Data filtering: Removing unwanted noise or disturbances from measurements.
Data aggregation: Combining data from multiple sensors or devices to reduce communication and storage requirements.

 EDGE COMPUTING AND CLOUD COMPUTING
  Cloud computing;
Cloud computing provides remote computing resources over the internet.
Functions:
- Data storage.
- Data processing.
- Analytics.
- Device management.
- Remote access.
- Application hosting.
Examples of cloud platforms:
- AWS IoT.
- Microsoft Azure IoT services.
- ThingsBoard.
- Blynk.
- Arduino Cloud.
  Edge computing;
Edge computing processes data close to where it is generated rather than sending everything to a remote cloud.
Advantages:
- Reduced communication latency.
- Reduced bandwidth usage.
- Improved response time.
- Continued local operation during internet outages.
- Better support for real-time control.
  Fog computing;
Fog computing distributes computing, storage and networking resources between IoT devices and centralized cloud infrastructure.
  Comparison;
Feature| Edge| Fog| Cloud
Processing location| Near device| Intermediate network layer| Remote data centre
Latency| Very low| Low–medium| Network-dependent
Resources| Limited| Moderate| High
Main purpose| Immediate processing| Distributed processing| Large-scale storage and analytics

 IoT SECURITY
IoT security protects devices, networks, applications and data against unauthorized access and attacks.
Common threats
1. Unauthorized device access.
2. Weak passwords.
3. Data interception.
4. Malware and botnets.
5. Denial-of-service attacks.
6. Firmware vulnerabilities.
7. Physical device tampering.
8. Insecure communication protocols.
  Security measures;
- Authentication: Verifies device and user identity.
- Authorization: Controls permitted actions.
- Encryption: Protects transmitted and stored data.
- Secure boot: Ensures trusted firmware is executed.
- Firmware updates: Fix security vulnerabilities.
- Access control: Limits access to authorized users.
- Network segmentation: Separates IoT devices from sensitive systems.
- TLS: Secures network communications.
- Key management: Protects cryptographic credentials.
CIA security principles;
1. Confidentiality: Prevents unauthorized disclosure of information.
2. Integrity: Prevents unauthorized modification of data.
3. Availability: Ensures systems and services remain accessible.

 IoT POWER MANAGEMENT
Many IoT devices operate using batteries and must minimize energy consumption.
Techniques include:
1. Sleep modes: Switch off unnecessary components when idle.
2. Duty cycling: Alternate between active and sleep periods.
3. Low-power microcontrollers: Use energy-efficient processors.
4. Efficient communication: Minimize unnecessary transmissions.
5. Data aggregation: Reduce the number of messages sent.
6. Event-driven operation: Activate devices only when necessary.
7. Energy harvesting: Obtain energy from sources such as solar, thermal or vibration energy.
  Battery life estimation;
Approximate battery life:
Battery life (hours) = Battery capacity (mAh) / Average current (mA)
Example:
A 2000 mAh battery powering a device with an average current consumption of 100 mA:
Battery life = 2000/100 = 20 hours.
Actual battery life is affected by battery efficiency, discharge characteristics, temperature and operating conditions.

 IoT APPLICATIONS
  Smart agriculture;
- Soil moisture monitoring.
- Automated irrigation.
- Weather monitoring.
- Livestock tracking.
- Greenhouse automation.
  Smart homes;
- Automated lighting.
- Smart security systems.
- Temperature control.
- Smart appliances.
- Energy monitoring.
  Healthcare;
- Remote patient monitoring.
- Wearable health devices.
- Smart medical equipment.
- Medication monitoring.
  Industrial IoT (IIoT);
- Machine condition monitoring.
- Predictive maintenance.
- Industrial automation.
- Production monitoring.
- Equipment tracking.
  Smart cities;
- Intelligent traffic management.
- Smart streetlights.
- Waste management.
- Water monitoring.
- Air-quality monitoring.
  Transportation;
- Vehicle tracking.
- Fleet management.
- Intelligent parking.
- Vehicle diagnostics.
- Logistics monitoring.

 PRACTICAL IoT SYSTEM DESIGN
Example: IoT-based smart irrigation system
  Required components:
- ESP32 microcontroller.
- Soil moisture sensor.
- Relay module or suitable MOSFET driver.
- Water pump.
- Power supply.
- Wi-Fi connection.
- IoT dashboard or cloud platform.
System operation:
1. The soil moisture sensor measures soil moisture.
2. The ESP32 reads the sensor value.
3. The controller compares the measurement with a predefined threshold.
4. If the soil is dry, the controller activates the pump.
5. If the soil reaches the required moisture level, the pump switches off.
6. The ESP32 transmits readings to an IoT platform.
7. The user monitors soil conditions and pump status remotely.
  Basic control algorithm:
START
Initialize ESP32, sensor and pump output.
Connect to Wi-Fi.
REPEAT:
- Read soil moisture.
- Process and calibrate the reading.
- If moisture is below the set threshold:
  - Turn pump ON.
- Otherwise:
  - Turn pump OFF.
- Send sensor reading and pump status to cloud.
- Wait for the next sampling interval.
END REPEAT
  Important design considerations;
- Calibrate the soil moisture sensor for the actual soil.
- Use hysteresis to prevent rapid pump switching.
- Include a maximum pump runtime for protection.
- Provide a manual override.
- Protect electronics against moisture.
- Use a separate suitable power supply for the pump.
- Do not drive the pump directly from an ESP32 GPIO pin.

 IMPORTANT IoT FORMULAS SUMMARY
1. Sampling frequency: 
   fs = 1/Ts
2. Nyquist criterion:   
   fs ≥ 2fmax
3. Data rate:   
   R = Data size / Transmission time
4. Battery life:   
   t = Battery capacity / Average current
5. Power:   
   P = VI
6. Energy:   
   E = Pt
7. Ohm's law:   
   V = IR
8. PWM duty cycle:   
   D = (Ton/T) × 100%
9. ADC resolution:   
   ΔV = Vref/2ⁿ
10. Sensor sensitivity:    
    S = ΔOutput/ΔInput

 KEY TAKEAWAYS
- IoT connects physical devices to networks for data exchange and intelligent control.
- Sensors collect physical information, while actuators execute physical actions.
- Microcontrollers provide local processing and device control.
- Communication technologies enable connectivity between IoT components.
- MQTT is a widely used lightweight IoT messaging protocol.
- Cloud computing supports centralized storage, analytics and remote management.
- Edge computing enables faster local processing and reduced network dependence.
- Security, power management and reliable connectivity are essential in IoT design.
- Industrial IoT applies these principles to manufacturing, automation and industrial monitoring.

Remember: IoT combines embedded systems, sensors, actuators, communication networks, data processing and software to create intelligent connected systems.