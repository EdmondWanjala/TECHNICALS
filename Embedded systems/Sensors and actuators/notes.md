            SENSORS AND ACTUATORS
Sensors and actuators are essential components of embedded systems. They enable a microcontroller or processor to interact with the physical environment.
- Sensor: Converts a physical quantity (temperature, pressure, light, motion, etc.) into an electrical signal that can be processed by a controller.
- Actuator: Converts an electrical control signal into a physical action such as movement, rotation, heating, cooling or switching.
  Basic operating principle;
Input → Sensor → Signal Conditioning → ADC → Microcontroller → Driver Circuit → Actuator → Physical Output
Example: In an automatic temperature-control system:
1. A temperature sensor measures room temperature.
2. The sensor produces an electrical signal.
3. The microcontroller reads and processes the signal.
4. The controller compares the temperature with the desired setpoint.
5. It activates a fan or heater through a driver circuit.

 SENSORS;
  Important sensor characteristics;
1. Range: Minimum and maximum values a sensor can measure.
2. Sensitivity: Change in output per unit change in input.   
   Sensitivity = ΔOutput / ΔInput
3. Accuracy: Closeness of a measurement to the true value.
4. Precision: Ability to produce consistent repeated measurements.
5. Resolution: Smallest change in input that can be detected.
6. Linearity: How closely the sensor output follows a straight-line relationship with its input.
7. Repeatability: Ability to produce the same output under identical conditions.
8. Response time: Time required for the sensor to respond to an input change.
9. Hysteresis: Difference in output for the same input depending on whether the input is increasing or decreasing.
10. Drift: Gradual change in sensor output over time despite a constant input.
  Classification of sensors;
 Based on output
- Analog sensors: Produce continuously varying electrical signals.
- Digital sensors: Produce discrete digital signals, often using communication protocols such as I²C, SPI or UART.
 Based on power requirement
- Active sensors: Generate an electrical output directly from the measured quantity, without requiring external excitation for signal generation. Example: thermocouple.
- Passive sensors: Require external excitation or power to produce a measurable output. Example: thermistor and strain gauge.
 Based on contact
- Contact sensors: Must physically touch the object being measured.
- Non-contact sensors: Measure without physical contact, e.g. infrared and ultrasonic sensors.
  Common types of sensors;
 Temperature sensors
Measure temperature.
Examples:
- Thermistor: Resistance changes with temperature.
- Thermocouple: Generates voltage due to a temperature difference between junctions.
- RTD (Resistance Temperature Detector): Resistance changes predictably with temperature.
- LM35: Analog temperature sensor with nominal sensitivity of 10 mV/°C.
- Digital sensors: DS18B20 and other integrated temperature sensors.
Thermistor equation (Steinhart–Hart simplified form):
    1/T = A + B ln(R) + C[ln(R)]³
Where:
- T = absolute temperature (K)
- R = resistance (Ω)
- A, B and C = sensor-specific constants.
 Light sensors
Measure light intensity.
Examples:
- LDR (Light Dependent Resistor): Resistance decreases as light intensity increases.
- Photodiode: Converts light into electrical current.
- Phototransistor: Uses light to control transistor current.
Applications: Automatic streetlights, brightness control and optical detection.
 Proximity sensors
Detect nearby objects without necessarily touching them.
Types:
- Inductive: Detects metallic objects using electromagnetic fields.
- Capacitive: Detects changes in capacitance; can detect metallic and non-metallic materials.
- Infrared: Detects reflected infrared radiation.
- Ultrasonic: Uses reflected sound waves to measure distance.
- Magnetic: Detects magnetic fields using Hall-effect or reed sensors.
Ultrasonic distance equation:
    d = vt/2
Where:
- d = distance to object (m)
- v = speed of sound (approximately 343 m/s in air at 20°C)
- t = round-trip time of sound (s).
The division by 2 accounts for the sound travelling to the object and back.
 Pressure sensors
Measure pressure of gases or liquids.
Types:
- Piezoresistive pressure sensors.
- Capacitive pressure sensors.
- Piezoelectric pressure sensors.
Applications: Industrial process control, automotive systems and weather monitoring.
Pressure:
    P = F/A
Where:
- P = pressure (Pa)
- F = force (N)
- A = area (m²).
 Motion and acceleration sensors
- Accelerometer: Measures linear acceleration.
- Gyroscope: Measures angular velocity.
- IMU (Inertial Measurement Unit): Combines accelerometers and gyroscopes, sometimes with a magnetometer.
- PIR sensor: Detects changes in infrared radiation caused by moving warm objects.
Applications: Robotics, drones, vehicle safety and motion detection.
 Position and displacement sensors
Measure the position or movement of an object.
Examples:
- Potentiometer.
- Rotary encoder.
- Linear encoder.
- LVDT (Linear Variable Differential Transformer).
- Hall-effect position sensor.
 Force and strain sensors
- Load cell: Measures force or weight, commonly using strain gauges.
- Strain gauge: Resistance changes when stretched or compressed.
Strain:
    ε = ΔL/L
Gauge factor:
    GF = (ΔR/R)/ε
Where:
- ε = strain (dimensionless)
- ΔL = change in length
- L = original length
- ΔR = change in resistance
- R = original resistance.
 Gas and humidity sensors
- Gas sensors: Detect gases such as CO, CO₂ and methane.
- Humidity sensors: Measure moisture content in air.
Applications: Environmental monitoring, agriculture, ventilation and safety systems.

 SIGNAL CONDITIONING AND SENSOR INTERFACING
Sensor outputs are not always suitable for direct connection to a microcontroller. Signal conditioning prepares signals for accurate processing.
  Signal conditioning operations;   
1. Amplification: Increases weak sensor signals.
2. Filtering: Removes unwanted noise and interference.
3. Attenuation: Reduces signal amplitude.
4. Linearization: Corrects nonlinear sensor responses.
5. Isolation: Protects the controller from electrical hazards and ground differences.
6. Level shifting: Adjusts voltage levels to match the controller input.
7. Excitation: Supplies power to sensors that require it.
  Analog-to-Digital Converter (ADC);
An ADC converts an analog sensor voltage into a digital value that a microcontroller can process.
For an n-bit ADC:
    Number of levels = 2ⁿ
Approximate voltage resolution:
    Resolution = Vref / 2ⁿ
For an ideal ADC:
    Digital value ≈ (Vin/Vref) × (2ⁿ − 1)
Where:
- n = ADC resolution in bits.
- Vref = reference voltage.
- Vin = analog input voltage.
Example:
For a 10-bit ADC with a 5 V reference:
    Number of levels = 2¹⁰ = 1024
    Voltage resolution = 5/1024 = 4.88 mV per step approximately.
  Sensor communication interfaces;
- GPIO: General-purpose digital input/output.
- ADC: Reads analog sensor signals.
- I²C: Two-wire serial communication using SDA and SCL.
- SPI: High-speed synchronous serial communication using clock, data and chip-select signals.
- UART: Asynchronous serial communication using TX and RX.
- 1-Wire: Single-data-wire communication used by devices such as DS18B20.

 ACTUATORS
An actuator is a device that converts electrical energy into physical action. It receives a control signal from an embedded controller and produces a desired output.
  Classification of actuators;
 Based on motion
1. Linear actuators: Produce straight-line motion.
2. Rotary actuators: Produce rotational motion.
 Based on energy source
1. Electrical actuators.
2. Hydraulic actuators.
3. Pneumatic actuators.
4. Thermal actuators.
  Common types of actuators;
 DC motors
Convert electrical energy into continuous rotational motion.
- Speed depends mainly on applied voltage and load.
- Direction can be reversed by reversing motor polarity.
- Commonly controlled using PWM and an H-bridge motor driver.
Applications: Robots, fans, pumps and conveyor systems.
 Servo motors
Provide controlled angular position.
- Contain a motor, control electronics and position feedback.
- Commonly receive a PWM control signal.
- Used where accurate positioning is required.
Applications: Robotic arms, steering mechanisms and automation.
 Stepper motors
Rotate in fixed angular steps.
- Move through discrete steps.
- Can provide precise positioning without an encoder in suitable applications.
- Require a stepper motor driver.
Applications: CNC machines, 3D printers and positioning systems.
 Solenoids
Use electromagnetic force to produce linear movement.
Applications: Electric locks, valves and switching mechanisms.
 Relays
Electrically operated switches used to control high-power circuits using low-power control signals.
Applications: Industrial control, lighting and motor switching.
A transistor or relay driver is often required between the microcontroller and relay coil.
 Heaters
Convert electrical energy into heat.
Applications: Temperature regulation, incubators and industrial heating.
 Fans and pumps
- Fans move air.
- Pumps move liquids or gases.
Applications: Cooling, irrigation and fluid-control systems.
 Pneumatic and hydraulic actuators
- Pneumatic actuators use compressed air.
- Hydraulic actuators use pressurized liquid.
They are widely used in industrial automation because they can generate substantial forces.

 ACTUATOR CONTROL METHODS
  Pulse Width Modulation (PWM);
PWM controls the average power delivered to an actuator by varying the proportion of time a signal remains HIGH during each cycle.
Duty cycle:
    D = (Ton/T) × 100%
Where:
- Ton = ON time.
- T = total period.
For an ideal switching circuit:
    Vaverage = D × Vs
Where D is expressed as a fraction between 0 and 1.
Applications:
- DC motor speed control.
- LED brightness control.
- Heater power control.
- Servo position commands (using the appropriate pulse-width timing).
  H-Bridge motor control;
An H-bridge is an electronic circuit that allows a DC motor to rotate in either direction by reversing the voltage polarity across its terminals.
Typical functions:
- Forward rotation.
- Reverse rotation.
- Braking.
- Coasting.
Motor drivers such as L293D, L298N and modern MOSFET-based drivers are commonly used.
  Transistor and MOSFET drivers
Microcontroller pins cannot normally supply the current required by motors, relays and other high-power actuators.
A transistor or MOSFET acts as an electronic switch or amplifier.
Important considerations:
- Use a suitable transistor or MOSFET.
- Select adequate voltage and current ratings.
- Include a gate/base driving arrangement where necessary.
- Use a flyback diode across inductive DC loads such as relay coils and brushed motors when the driver does not already provide an appropriate protection path.

 SENSOR–ACTUATOR INTEGRATION
Sensors and actuators work together through a microcontroller to create an automated control system.
  Basic closed-loop control system
Setpoint → Controller → Actuator → Physical System → Sensor → Feedback → Controller.
Example: Automatic water-level control.
1. A water-level sensor measures tank level.
2. The microcontroller reads the sensor output.
3. The controller compares the measured level with the desired level.
4. If the level is low, it switches on the pump.
5. When the desired level is reached, it switches off the pump.
  Open-loop versus closed-loop systems;
Open-loop system
- No feedback from the output.
- The controller operates according to predetermined instructions.
- Simple and inexpensive.
- Cannot automatically correct disturbances.
Closed-loop system
- Uses sensor feedback.
- Compares actual output with desired output.
- Automatically corrects errors.
- Generally provides better accuracy and disturbance rejection.
Control error
    e(t) = r(t) − y(t)
Where:
- e(t) = error.
- r(t) = reference or setpoint.
- y(t) = measured output.
  PID controller;
A Proportional–Integral–Derivative controller is widely used in embedded control systems.
    u(t) = Kp e(t) + Ki ∫e(t)dt + Kd de(t)/dt
Where:
- Kp = proportional gain.
- Ki = integral gain.
- Kd = derivative gain.
- e(t) = control error.
- u(t) = controller output.
Functions:
- Proportional: Responds to present error.
- Integral: Eliminates accumulated steady-state error.
- Derivative: Responds to the rate of change of error and can improve damping.
Applications: Motor speed control, temperature regulation, robotics and industrial automation.

 PRACTICAL DESIGN CONSIDERATIONS
When selecting and interfacing sensors and actuators, consider:
1. Operating voltage and current.
2. Measurement range and required accuracy.
3. Response time and sampling frequency.
4. Environmental conditions, including temperature, moisture, dust and vibration.
5. Sensor calibration requirements.
6. Electrical noise and electromagnetic interference.
7. Microcontroller input/output voltage compatibility.
8. Power consumption and battery life.
9. Actuator force, torque, speed and power requirements.
10. Electrical protection, isolation and grounding.
11. Mechanical mounting and alignment.
12. System safety and fail-safe operation.
  Common interfacing mistakes;
- Connecting a high-current motor directly to a microcontroller pin.
- Applying a voltage higher than the microcontroller's permitted input voltage.
- Forgetting a common ground when required for signal reference.
- Ignoring ADC reference voltage and resolution.
- Failing to use flyback protection for inductive loads.
- Using an incorrect PWM frequency or pulse width.
- Ignoring sensor calibration and measurement noise.

 APPLICATIONS OF SENSORS AND ACTUATORS
Application| Sensors| Actuators
Smart irrigation| Soil moisture, rain| Water pump, valve
Robotics| Ultrasonic, encoder, IMU| Motors, servos
Smart homes| Temperature, motion, light| Fans, lights, locks
Automotive| Speed, pressure, temperature| Motors, valves
Industrial automation| Proximity, pressure, temperature| Motors, relays, valves
Medical equipment| Temperature, pressure, optical| Pumps, motors
Drones| Accelerometer, gyroscope, GPS| Brushless motors

 IMPORTANT FORMULAS SUMMARY
1. Sensor sensitivity:   
   S = ΔOutput/ΔInput
2. Pressure:   
   P = F/A
3. Strain:   
   ε = ΔL/L
4. Gauge factor:   
   GF = (ΔR/R)/ε
5. Ultrasonic distance:   
   d = vt/2
6. ADC levels:   
   N = 2ⁿ
7. ADC resolution:   
   ΔV = Vref/2ⁿ
8. ADC digital output:   
   Digital value ≈ (Vin/Vref)(2ⁿ − 1)
9. PWM duty cycle:   
   D = (Ton/T) × 100%
10. Average PWM voltage:    
    Vaverage = D × Vs
11. Control error:    
    e(t) = r(t) − y(t)
12. PID control:    
    u(t) = Kp e(t) + Ki∫e(t)dt + Kd de(t)/dt

 KEY TAKEAWAYS
- Sensors detect physical quantities and convert them into electrical signals.
- Actuators convert electrical control signals into physical action.
- Signal conditioning improves sensor signals before processing.
- ADCs allow microcontrollers to process analog sensor measurements.
- PWM is widely used for controlling actuator power.
- Motor drivers protect microcontrollers and provide the current required by motors.
- Feedback allows embedded systems to monitor and correct their outputs.
- Calibration, noise reduction and electrical protection are essential for reliable operation.

Remember: Sensors provide information, microcontrollers make decisions, and actuators execute actions.