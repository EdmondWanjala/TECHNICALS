                    SENSORS
A sensor is a device that detects a physical, chemical or biological quantity (measurand) and converts it into a measurable signal, usually electrical.
A sensor allows electronic systems to detect and respond to changes in their environment.
  Examples of measured quantities:
- Temperature
- Pressure
- Force and weight
- Displacement and position
- Speed and acceleration
- Light intensity
- Humidity
- Gas concentration
- Sound and vibration
- Magnetic fields
  Sensor vs Transducer;
- Sensor: Detects a physical quantity or change.
- Transducer: Converts energy from one form into another.
- Actuator: Converts an electrical control signal into physical action.
A sensor is often part of a transducer system.
  Basic sensor measurement system;
1. Measurand: Physical quantity being measured.
2. Sensing element: Detects the physical change.
3. Transduction element: Converts the change into a usable signal.
4. Signal conditioning: Amplifies, filters or linearizes the signal.
5. Data acquisition: Converts the signal into digital data where necessary.
6. Processing and display: Interprets and presents the measurement.

 CLASSIFICATION OF SENSORS
  Based on power requirement;
Active sensors
- Generate their own electrical output from the measured quantity.
- Do not require external excitation for the basic sensing mechanism.
- Examples: Thermocouples, photovoltaic cells and piezoelectric sensors.
Passive sensors
- Require external excitation or electrical power.
- The measurand changes an electrical property such as resistance, capacitance or inductance.
- Examples: RTDs, thermistors, strain gauges and LDRs.
  Based on output;
Analog sensors
- Produce continuously varying output signals.
- Example: Analog temperature sensor producing a voltage proportional to temperature.
Digital sensors
- Produce discrete digital signals or data.
- Examples: Digital temperature sensors, digital encoders and digital humidity sensors.
  Based on contact;
- Contact sensors: Must physically touch the object being measured.
- Non-contact sensors: Detect objects or quantities without physical contact.
Examples of non-contact sensors include infrared, ultrasonic, inductive and capacitive proximity sensors.

 IMPORTANT SENSOR CHARACTERISTICS
  Sensitivity;
The change in output per unit change in input.
    Sensitivity = ΔOutput / ΔInput
Example: A temperature sensor produces a 10 mV change for every 1°C change.
    Sensitivity = 10 mV/°C.
  Accuracy
How close a measured value is to the true or accepted value.
  Precision
How close repeated measurements are to one another.
  Resolution
The smallest change in input that a sensor can detect.
  Range
The minimum and maximum values a sensor can measure.
  Linearity
The degree to which the sensor output follows a straight-line relationship with its input.
  Repeatability
Ability to produce the same output under identical measurement conditions.
  Hysteresis
Difference in output for the same input depending on whether the input is increasing or decreasing.
  Response time
Time required for the sensor output to respond to a change in input.
  Drift
Gradual change in sensor output over time despite a constant input.
  Stability
Ability to maintain consistent performance over time.

 TEMPERATURE SENSORS
Temperature sensors measure the thermal condition of an object or environment.
  Thermocouple;
- Works on the Seebeck effect.
- Two dissimilar metals joined together generate a voltage when their junctions are at different temperatures.
- Suitable for a wide temperature range.
- Rugged and commonly used in industrial applications.
Seebeck relationship (approximately):
    V = S × ΔT
Where:
- V = thermoelectric voltage.
- S = Seebeck coefficient.
- ΔT = temperature difference between junctions.
  RTD (Resistance Temperature Detector);
- Measures temperature through the change in electrical resistance of a metal.
- Platinum is commonly used (e.g. Pt100).
- Offers good accuracy and stability.
Approximate relationship:
    Rt = R₀[1 + α(T − T₀)]
Where:
- Rt = resistance at temperature T.
- R₀ = resistance at reference temperature T₀.
- α = temperature coefficient of resistance.
  Thermistor;
A temperature-sensitive resistor.
Types:
- NTC: Resistance decreases as temperature increases.
- PTC: Resistance increases as temperature increases.
NTC thermistors are widely used in temperature measurement and compensation.
  Infrared temperature sensor;
- Detects infrared radiation emitted by an object.
- Allows non-contact temperature measurement.
- Used in industrial monitoring, thermal imaging and medical thermometers.

 PRESSURE SENSORS
Measure the force exerted by a fluid or gas per unit area.
Pressure = Force / Area
    P = F/A
Types:
  Strain-gauge pressure sensor;
- Pressure deforms a diaphragm.
- Strain gauges detect the resulting mechanical deformation.
- Resistance changes with strain.
  Capacitive pressure sensor;
- Pressure changes the distance between capacitor plates or their effective geometry.
- This changes capacitance.
    C = εA/d
Where:
- C = capacitance.
- ε = permittivity.
- A = overlapping plate area.
- d = separation between plates.
  Piezoelectric pressure sensor;
- Uses piezoelectric materials to generate electrical charge under mechanical stress.
- Suitable for dynamic pressure measurements.
Applications: Hydraulic systems, pneumatic systems, automotive engines and industrial process control.

 POSITION AND DISPLACEMENT SENSORS
Measure the location or movement of an object.
  Potentiometer;
- Converts linear or angular displacement into a change in resistance.
- Produces a variable voltage when used as a voltage divider.
    Vout = Vin × (R₂/R₁ + R₂)
  Linear Variable Differential Transformer (LVDT);
- Measures linear displacement using electromagnetic induction.
- Contains one primary coil and two secondary coils.
- Movement of a magnetic core changes the induced secondary voltages.
- Provides accurate, frictionless displacement measurement.
  Rotary encoder;
Converts angular movement into electrical pulses or digital position data.
Types:
- Incremental encoder: Measures relative movement.
- Absolute encoder: Provides a unique digital code for each angular position.
Applications: Robotics, CNC machines, motor control and automation.

 PROXIMITY SENSORS
Detect the presence or absence of objects without requiring physical contact.
  Inductive proximity sensor;
- Detects metallic objects.
- Generates an electromagnetic field.
- Metal objects cause changes in the field, triggering detection.
Applications: Metal detection, industrial automation and machine positioning.
  Capacitive proximity sensor;
- Detects changes in capacitance caused by nearby objects.
- Can detect metallic and non-metallic materials.
- Used for liquid-level detection and object sensing.
  Photoelectric sensor;
- Uses light to detect objects.
- Commonly uses an LED or laser transmitter and a photodetector.
Types:
- Through-beam.
- Retro-reflective.
- Diffuse-reflective.
  Ultrasonic sensor
- Uses high-frequency sound waves.
- Measures distance using the time taken for an echo to return.
    Distance = (Speed of sound × Echo time)/2
    d = vt/2
Applications: Obstacle detection, parking systems and liquid-level measurement.

 LIGHT SENSORS
Measure light intensity or radiation.
  LDR (Light Dependent Resistor);
- Resistance decreases as light intensity increases.
- Used in automatic lighting systems.
  Photodiode;
- Converts light into electrical current.
- Often operated in reverse bias for photodetection.
- Offers fast response.
  Phototransistor;
- Uses light to control transistor current.
- Generally provides higher sensitivity than a photodiode but may be slower.
  Photovoltaic sensor;
- Converts incident light directly into electrical energy.
- Used in solar cells and light detection systems.

 FORCE, WEIGHT AND STRAIN SENSORS
  Strain gauge;
Measures mechanical deformation by detecting changes in electrical resistance.
Gauge factor:
    GF = (ΔR/R)/ε
Where:
- GF = Gauge factor.
- ΔR = Change in resistance.
- R = Original resistance.
- ε = Mechanical strain.
Strain:
    ε = ΔL/L
  Load cell;
Converts applied force or weight into an electrical signal.
- Commonly uses strain gauges.
- Strain gauges are often connected in a Wheatstone bridge.
- Used in electronic weighing scales and industrial weighing systems.
  Piezoelectric sensor;
Generates electrical charge when mechanical stress is applied.
    Q = dF
Where:
- Q = Generated charge.
- d = Piezoelectric charge coefficient.
- F = Applied force.
Used in vibration, impact and dynamic force measurement.

 SPEED AND MOTION SENSORS
  Tachometer;
Measures rotational speed.
Angular velocity:
    ω = 2πN/60
Where:
- ω = Angular velocity (rad/s).
- N = Rotational speed (rpm).
  Hall-effect sensor;
- Detects magnetic fields.
- Produces an electrical output based on magnetic field strength and polarity.
- Used for speed measurement, position detection and current sensing.
  Accelerometer;
Measures acceleration along one or more axes.
Applications:
- Motion detection.
- Vehicle crash detection.
- Smartphone orientation.
- Vibration monitoring.
- Robotics.
  Gyroscope;
Measures angular velocity around one or more axes.
Used in:
- Drones.
- Robotics.
- Navigation systems.
- Stabilization systems.
  IMU (Inertial Measurement Unit);
Combines sensors such as:
- Accelerometer.
- Gyroscope.
- Sometimes magnetometer.
Used to estimate orientation, motion and movement.

 HUMIDITY AND GAS SENSORS
  Humidity sensor;
Measures the amount of water vapour in air.
Types:
- Capacitive humidity sensor.
- Resistive humidity sensor.
- Thermal humidity sensor.
Relative humidity:
    RH = (Actual vapour pressure / Saturation vapour pressure) × 100%
  Gas sensors;
Detect the presence or concentration of specific gases.
Types:
- Metal oxide semiconductor (MOS) sensors.
- Electrochemical sensors.
- Infrared gas sensors.
- Catalytic gas sensors.
Applications:
- Carbon monoxide detection.
- Methane and LPG leakage detection.
- Industrial safety.
- Air-quality monitoring.

 MAGNETIC SENSORS
Detect magnetic fields and changes in magnetic flux.
Important types:
1. Hall-effect sensor: Detects magnetic field strength and polarity.
2. Reed switch: Uses magnetic force to open or close electrical contacts.
3. Magnetoresistive sensor: Detects magnetic fields through changes in electrical resistance.
4. Fluxgate sensor: Measures magnetic fields using magnetic core behaviour.
Applications include electronic compasses, motor position sensing and current measurement.

 SENSOR SIGNAL CONDITIONING
Sensor outputs are often weak, noisy or unsuitable for direct processing. Signal conditioning prepares them for measurement and control systems.
Main techniques:
  Amplification;
Increases weak sensor signals using operational amplifiers.
Voltage gain:
    Av = Vout/Vin
For an ideal non-inverting op-amp:
    Av = 1 + (Rf/Rin)
  Filtering;
Removes unwanted noise and frequency components.
Types:
- Low-pass filter: Allows low frequencies and attenuates high frequencies.
- High-pass filter: Allows high frequencies and attenuates low frequencies.
- Band-pass filter: Allows a selected frequency range.
- Notch filter: Rejects a particular frequency range.
  Linearization;
Corrects nonlinear sensor output to obtain a more proportional relationship with the measured quantity.
  Isolation;
Protects circuits by electrically separating sensor and processing sections.
  Analog-to-Digital Conversion (ADC);
Converts analog sensor signals into digital values.
For an ideal n-bit ADC:
    Number of levels = 2ⁿ
Approximate voltage resolution:
    Resolution = Vref/2ⁿ
Where Vref is the ADC reference voltage.
  Wheatstone bridge;
A circuit used to measure small resistance changes, especially in strain gauges and RTDs.
For a balanced bridge:
    R₁/R₂ = R₃/R₄

 SENSOR INTERFACING WITH MICROCONTROLLERS
Sensors are commonly connected to microcontrollers such as Arduino, ESP32 and STM32.
  Analog interfacing;
- Connect analog sensor output to an ADC input.
- Configure the reference voltage and resolution.
- Read the digital value.
- Convert the ADC reading into the required physical unit.
For an n-bit ADC:
    Vin ≈ ADC reading × Vref/(2ⁿ − 1)
  Digital interfacing;
Common communication protocols:
 GPIO
- Reads HIGH or LOW signals.
- Used with switches and digital output sensors.
 I²C
- Uses SDA and SCL lines.
- Supports multiple addressed devices.
- Common in temperature sensors, accelerometers and displays.
 SPI
- Uses clock, data and chip-select signals.
- Generally supports high-speed communication.
- Common in precision ADCs and digital sensors.
 UART
- Uses TX and RX communication lines.
- Common in GPS modules and some sensor modules.
  Important interfacing considerations;
- Supply voltage compatibility.
- Current requirements.
- ADC resolution.
- Sensor output range.
- Pull-up or pull-down resistors.
- Ground reference.
- Noise and electromagnetic interference.
- Calibration and measurement accuracy.

 SENSOR CALIBRATION
Calibration is the process of comparing a sensor's output with a known reference standard and adjusting or correcting its measurements.
  Important terms:
- Zero calibration: Corrects output offset at a reference point.
- Span calibration: Adjusts the output range.
- Two-point calibration: Uses two known reference values.
- Multi-point calibration: Uses several reference values to correct nonlinear behaviour.
A simple linear calibration model:
    y = mx + c
Where:
- y = Sensor output.
- x = Measured quantity.
- m = Sensitivity or slope.
- c = Offset.
Calibration improves measurement accuracy and reliability.

 SENSOR ERRORS AND NOISE
Common sources of measurement errors:
1. Environmental temperature changes.
2. Electrical and electromagnetic interference.
3. Mechanical vibration.
4. Sensor ageing and drift.
5. Incorrect calibration.
6. Poor electrical connections.
7. Supply voltage fluctuations.
8. Quantization errors in ADCs.
9. Nonlinearity and hysteresis.
Methods of reducing errors:
- Proper shielding and grounding.
- Signal filtering.
- Regular calibration.
- Temperature compensation.
- Stable power supplies.
- Correct sensor placement.
- Averaging repeated measurements where appropriate.

17. INDUSTRIAL SENSOR APPLICATIONS
Industry/application| Sensors used
Robotics| Encoders, IMUs, proximity sensors
Automotive| Pressure, temperature, speed, oxygen sensors
Agriculture| Soil moisture, humidity, temperature
Healthcare| Temperature, pressure, pulse oximetry sensors
Manufacturing| Proximity, position, force sensors
Environmental monitoring| Gas, humidity, temperature sensors
Aerospace| Accelerometers, gyroscopes, pressure sensors
Smart homes| PIR, light, gas and temperature sensors
Renewable energy| Irradiance, current and temperature sensors

18. IMPORTANT FORMULAS SUMMARY
Quantity| Formula
Sensitivity| ΔOutput/ΔInput
Pressure| P = F/A
Strain| ε = ΔL/L
Gauge factor| GF = (ΔR/R)/ε
Capacitance| C = εA/d
Thermocouple voltage| V ≈ SΔT
RTD resistance| Rt = R₀[1 + α(T−T₀)]
Ultrasonic distance| d = vt/2
Angular velocity| ω = 2πN/60
Relative humidity| RH = (Pv/Psat) × 100%
Op-amp non-inverting gain| Av = 1 + Rf/Rin
ADC levels| 2ⁿ
ADC resolution| Vref/2ⁿ
Linear calibration| y = mx + c
Piezoelectric charge| Q = dF

19. IMPORTANT STUDY AND EXAM TIPS
1. Understand the difference between sensors, transducers and actuators.
2. Classify sensors according to their operating principle and output.
3. Know which sensors require external excitation and which generate their own output.
4. Understand the operating principles of thermocouples, RTDs, thermistors and strain gauges.
5. Practise ultrasonic distance and ADC resolution calculations.
6. Distinguish between accuracy, precision, sensitivity and resolution.
7. Understand Wheatstone bridge operation and its applications.
8. Learn how analog sensors interface with microcontrollers.
9. Understand I²C, SPI, UART and GPIO communication.
10. Always consider calibration, noise, response time and environmental effects when selecting a sensor.

KEY IDEA: Sensors are the foundation of measurement, automation and intelligent electronic systems. 
They convert real-world physical quantities into signals that electronic circuits, microcontrollers and computers can process to monitor, analyse and control the environment.