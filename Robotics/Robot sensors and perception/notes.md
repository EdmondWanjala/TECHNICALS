            ROBOT SENSORS AND PERCEPTION
Robot sensors and perception deal with how robots collect information about their internal condition and surrounding environment, process that information, and use it to make decisions and perform tasks.
Robot sensing is the process of detecting and measuring physical quantities using sensors.
Robot perception is the process of interpreting sensor measurements to understand the robot's environment, identify objects, estimate positions, recognize patterns, and determine relevant environmental conditions.
  Main objectives;
- Detect objects and obstacles.
- Measure distance, position, orientation, and motion.
- Monitor internal robot conditions.
- Recognize and classify objects.
- Estimate the robot's location and orientation.
- Understand environmental conditions.
- Support navigation and obstacle avoidance.
- Enable autonomous decision-making.
- Improve accuracy, safety, and operational efficiency.
  Basic perception pipeline;
1. Sensing: collect information from the environment.
2. Signal acquisition: convert physical measurements into usable signals.
3. Signal processing: remove noise and improve measurement quality.
4. Feature extraction: identify useful information from sensor data.
5. Interpretation: recognize objects, surfaces, motion, and environmental conditions.
6. State estimation: estimate the robot's position and environmental state.
7. Decision-making: determine appropriate actions.
8. Control: execute the selected actions.

 CLASSIFICATION OF ROBOT SENSORS
Robot sensors can be classified according to what they measure, where they are installed, and how they interact with the environment.
  A. Proprioceptive sensors
Measure the internal state of the robot.
Examples:
- Encoders: measure joint or wheel rotation.
- Potentiometers: measure angular or linear displacement.
- IMUs: measure acceleration and angular velocity.
- Current sensors: measure motor current.
- Force sensors: measure applied mechanical forces.
- Temperature sensors: monitor component temperature.
Applications:
- Joint position control.
- Motor monitoring.
- Robot motion estimation.
- Internal condition monitoring.
  B. Exteroceptive sensors
Measure information about the external environment.
Examples:
- Cameras.
- LiDAR.
- Ultrasonic sensors.
- Infrared sensors.
- Radar.
- Depth cameras.
- External force and tactile sensors.
Applications:
- Obstacle detection.
- Object recognition.
- Environment mapping.
- Navigation.
- Object manipulation.
  C. Contact sensors
Detect physical contact between a robot and an object or surface.
Examples:
- Touch sensors.
- Tactile sensors.
- Contact switches.
- Force sensors.
Applications:
- Robotic gripping.
- Collision detection.
- Assembly operations.
- Surface interaction.
  D. Non-contact sensors
Detect objects or physical quantities without requiring direct contact.
Examples:
- Optical sensors.
- Ultrasonic sensors.
- Infrared sensors.
- LiDAR.
- Radar.
Applications:
- Distance measurement.
- Object detection.
- Navigation.
- Collision avoidance.

 POSITION AND DISPLACEMENT SENSORS
These sensors measure the position or movement of robot components.
  A. Rotary encoders
Measure angular position or rotation of a shaft.
 Two common types:
Incremental encoder
- Generates electrical pulses as a shaft rotates.
- Position is calculated by counting pulses.
- Often provides two quadrature signals for direction detection.
- Requires a reference or homing procedure to establish absolute position after startup.
Angular displacement:
    θ = (2πN)/(PPR)
Where:
- θ = angular displacement (rad).
- N = number of counted pulses.
- PPR = pulses per revolution, using the effective counting convention.
Angular velocity:
    ω = Δθ/Δt
Absolute encoder
- Provides a unique digital position value for each angular position.
- Retains position information without requiring pulse counting from a reference after power-up, provided its position information is preserved.
Applications:
- Robotic joint positioning.
- Servo motor feedback.
- Industrial automation.
B. Linear encoders
Measure linear displacement along a straight path.
Applications:
- Cartesian robots.
- CNC systems.
- Linear actuator positioning.
C. Potentiometers
Convert displacement into a corresponding change in electrical resistance and output voltage.
For a simple voltage-divider arrangement:
    V_out = V_in × (R₂/(R₁ + R₂))
Their output can represent angular or linear position.
Applications:
- Joint position measurement.
- Low-cost robotic mechanisms.
- Joystick position sensing.
D. LVDT (Linear Variable Differential Transformer)
Measures linear displacement using electromagnetic induction.
Working principle:
- An AC excitation is applied to the primary winding.
- A movable magnetic core changes the coupling to two secondary windings.
- The differential output indicates displacement and direction relative to a null position.
Applications:
- Precision linear position measurement.
- Industrial robotic systems.
- Hydraulic actuator feedback.

4. PROXIMITY AND DISTANCE SENSORS
These sensors detect nearby objects or measure the distance between a robot and an object.
  A. Ultrasonic sensors
Use high-frequency sound waves to measure distance.
Working principle:
1. The transmitter emits an ultrasonic pulse.
2. The pulse travels through the air.
3. The sound reflects from an object.
4. The receiver detects the echo.
5. The system calculates distance using the travel time.
Distance equation:
    d = vt/2
Where:
- d = distance to object (m).
- v = speed of sound (approximately 343 m/s in air at 20°C).
- t = round-trip travel time (s).
The division by two accounts for the outgoing and returning sound wave.
Advantages:
- Relatively inexpensive.
- Simple implementation.
- Useful for short-range obstacle detection.
Limitations:
- Affected by temperature and environmental conditions.
- Soft or angled surfaces may produce weak echoes.
- Limited angular resolution.
Applications:
- Mobile robot obstacle detection.
- Parking robots.
- Object distance measurement.
B. Infrared (IR) sensors
Use infrared radiation to detect objects or estimate distance.
Common types:
- Reflective infrared sensors.
- Infrared proximity sensors.
- Infrared distance sensors.
- Thermal infrared sensors.
Working principle:
- An IR emitter transmits infrared radiation.
- An object reflects some radiation.
- A receiver detects the reflected energy.
- The system determines object presence or estimates distance.
Applications:
- Line-following robots.
- Proximity detection.
- Object detection.
- Short-range navigation.
Limitations:
- Surface colour and reflectivity affect readings.
- Ambient infrared radiation can interfere.
- Performance depends on sensor design and range.
C. Inductive proximity sensors
Detect metallic objects using electromagnetic induction.
Working principle:
- An internal coil produces an alternating magnetic field.
- A nearby metal object develops eddy currents.
- These currents change the sensor's electromagnetic characteristics.
- The sensor detects the change.
Applications:
- Industrial robotic automation.
- Metal object detection.
- Position and limit detection.
D. Capacitive proximity sensors
Detect objects by measuring changes in capacitance.
Capacitance:
    C = εA/d
Where:
- C = capacitance (F).
- ε = permittivity of the dielectric.
- A = overlapping plate area (m²).
- d = separation between plates (m).
The presence of an object changes the effective electric field and capacitance.
Applications:
- Detecting metallic and non-metallic materials.
- Liquid-level detection.
- Object presence detection.

 OPTICAL AND VISION SENSORS
Optical sensors use light to detect, measure, and interpret objects or environmental features.
  A. Cameras
Capture images that allow robots to recognize and locate objects.
Types:
Monocular camera
- Uses one camera.
- Captures two-dimensional images.
- Depth can be estimated using additional information, motion, or learned models.
Stereo camer
- Uses two cameras positioned at a known separation.
- Estimates depth by comparing corresponding image points.
RGB camera
- Captures colour information.
- Useful for object recognition and classification.
Depth camera
- Produces depth measurements for image pixels.
- Can use structured light, time-of-flight, or stereo techniques.
Applications:
- Object recognition.
- Visual inspection.
- Robotic manipulation.
- Navigation.
- Quality control.
  B. Computer vision
Computer vision is the field concerned with enabling machines to extract meaningful information from images and videos.
Important processes:
1. Image acquisition.
2. Image preprocessing.
3. Image enhancement.
4. Image segmentation.
5. Feature extraction.
6. Object detection.
7. Object classification.
8. Object tracking.
  C. Image processing techniques
Grayscale conversion: Converts colour images into intensity images.
Thresholding: Separates image regions based on intensity values.
Edge detection: Identifies boundaries and changes in image intensity.
Filtering: Reduces noise or enhances image features.
Segmentation: Divides an image into meaningful regions.
Feature extraction: Identifies useful characteristics such as edges, corners, textures, and shapes.
  D. Object detection and recognition
Object detection identifies objects and estimates their locations within an image.
Object recognition determines what an object is.
Common approaches:
- Template matching.
- Feature-based recognition.
- Machine learning.
- Deep learning.
- Convolutional neural networks (CNNs).
Applications:
- Identifying components during assembly.
- Recognizing people and objects.
- Sorting products.
- Detecting defective products.

 LiDAR SENSORS
LiDAR stands for Light Detection and Ranging.
It uses laser light to measure distances and generate spatial information about the environment.
Working principle
1. A laser pulse is emitted.
2. The light reflects from an object.
3. The reflected light is detected.
4. The travel time is measured.
5. Distance is calculated.
6. Multiple measurements produce a point cloud.
Distance equation:
    d = ct/2
Where:
- d = distance to the object (m).
- c = speed of light (approximately 3 × 10⁸ m/s).
- t = round-trip travel time (s).
Types of LiDAR
- 2D LiDAR.
- 3D LiDAR.
- Mechanical LiDAR.
- Solid-state LiDAR.
  Point clouds
A point cloud is a collection of three-dimensional points representing surfaces and objects in an environment.
Each point may contain:
- X coordinate.
- Y coordinate.
- Z coordinate.
- Intensity or reflectivity information.
Advantages
- Accurate distance measurement.
- Provides spatial information.
- Useful in mapping and navigation.
- Works in low visible-light conditions.
Limitations
- Cost can be high.
- Performance can be affected by weather and reflective surfaces.
- Some objects and materials may produce weak or unreliable returns.
Applications:
- Autonomous mobile robots.
- Self-driving vehicles.
- Mapping and localization.
- Obstacle detection.
- Industrial automation.

 INERTIAL MEASUREMENT UNIT (IMU)
An IMU is a sensor system that measures the motion and orientation-related dynamics of a robot.
  A typical IMU contains:
Accelerometer
- Measures specific force along three axes.
- Used to estimate linear acceleration and orientation relative to gravity when suitable conditions apply.
Gyroscope
- Measures angular velocity about three axes.
- Used to estimate rotational motion and orientation changes.
Magnetometer
- Measures the surrounding magnetic field.
- Can provide a heading reference when magnetic disturbances are controlled.
A six-axis IMU contains a three-axis accelerometer and a three-axis gyroscope.
A nine-axis system adds a three-axis magnetometer.
Accelerometer
Measures specific force, not simply gravitational acceleration.
In a simplified inertial-navigation model, acceleration can be estimated after accounting for gravity and transforming measurements into the appropriate reference frame.
Velocity:
    v(t) = v₀ + ∫a(t)dt
Position:
    x(t) = x₀ + ∫v(t)dt
Repeated integration causes errors to accumulate.
Gyroscope
Measures angular velocity.
Angular displacement for constant angular velocity:
    θ = ωt
For variable angular velocity:
    θ(t) = θ₀ + ∫ω(t)dt
IMU applications
- Robot orientation estimation.
- Balancing robots.
- Drone stabilization.
- Humanoid robot movement.
- Motion tracking.
- Inertial navigation.
IMU limitations
- Sensor noise.
- Bias drift.
- Accumulated integration errors.
- Magnetic interference in magnetometer measurements.

 FORCE AND TORQUE SENSORS
These sensors measure mechanical interaction forces and rotational moments.
  A. Force sensors
Measure applied forces.
Types:
- Strain-gauge force sensors.
- Piezoelectric force sensors.
- Load cells.
- Capacitive force sensors.
  B. Torque sensors
Measure rotational moments applied to a shaft or joint.
Torque:
    τ = F × r
Magnitude:
    τ = Fr sinθ
  C. Six-axis force/torque sensors
Measure:
- Three force components: Fx, Fy, Fz.
- Three torque components: Mx, My, Mz.
Applications:
- Robotic gripping.
- Assembly operations.
- Contact detection.
- Collaborative robotics.
- Surface polishing.
- Force-controlled manipulation.
  D. Tactile sensors
Detect physical contact and pressure distribution across a surface.
They can provide information about:
- Contact location.
- Pressure.
- Contact area.
- Slip.
- Surface characteristics.
Applications:
- Robotic hands.
- Adaptive gripping.
- Object manipulation.
- Human-robot interaction.

 TEMPERATURE AND ENVIRONMENTAL SENSORS
These sensors monitor environmental and operating conditions.
  A. Temperature sensors
Examples:
- Thermistors.
- RTDs.
- Thermocouples.
- Infrared temperature sensors.
Applications:
- Motor temperature monitoring.
- Battery monitoring.
- Industrial process control.
- Overheating protection.
  B. Humidity sensors
Measure moisture content in the air.
Applications:
- Agricultural robots.
- Environmental monitoring.
- Storage and processing systems.
  C. Pressure sensors
Measure pressure in gases or liquids.
Applications:
- Pneumatic systems.
- Hydraulic robots.
- Industrial process monitoring.
  D. Gas sensors
Detect specific gases or changes in gas concentration.
Applications:
- Environmental monitoring.
- Hazard detection.
- Industrial inspection.

 ROBOT LOCALIZATION
Localization is the process of determining a robot's position and orientation within its environment.
A robot may use:
- Wheel encoders.
- IMUs.
- GPS/GNSS.
- Cameras.
- LiDAR.
- External positioning systems.
  Types of localization
1. Relative localization
- Estimates movement relative to a previous position.
- Often uses odometry and inertial measurements.
2. Absolute localization
- Estimates position relative to a known global or mapped reference.
- May use GNSS, landmarks, or known reference points.
3. Landmark-based localization
- Identifies known environmental features and uses them to estimate robot position.
4. Visual localization
- Uses camera images to estimate robot movement and location.
Odometry
Odometry estimates robot movement by measuring the motion of its wheels or joints.
For a differential-drive robot with wheel radius r:
Linear velocity:
    v = r(ωᵣ + ωₗ)/2
Angular velocity:
    ω = r(ωᵣ − ωₗ)/L
Where:
- ωᵣ = right wheel angular velocity.
- ωₗ = left wheel angular velocity.
- L = distance between the wheels.
For a small time interval Δt:
    Δx ≈ v cosθ Δt
    Δy ≈ v sinθ Δt
    Δθ ≈ ωΔt
Odometry is useful but accumulates errors due to wheel slip, uneven surfaces, and measurement inaccuracies.

 SENSOR FUSION
Sensor fusion combines information from multiple sensors to produce a more reliable estimate of the robot's state or environment.
For example:
- Camera + LiDAR: object recognition and accurate spatial information.
- IMU + wheel encoders: improved motion estimation.
- GPS + IMU: navigation and orientation estimation.
- Force sensor + camera: controlled object manipulation.
Benefits
- Improves measurement reliability.
- Reduces dependence on individual sensors.
- Compensates for some sensor limitations.
- Improves localization accuracy.
- Provides more complete environmental information.
  Common sensor fusion methods;
1. Complementary filter
- Combines measurements with different frequency characteristics.
- Often combines gyroscope measurements with accelerometer-based orientation estimates.
2. Kalman filter
- Estimates the state of a dynamic system using a mathematical model and noisy measurements.
- Commonly used for robot localization and tracking.
3. Extended Kalman filter (EKF)
- Applies Kalman filtering to nonlinear systems through local linearization.
4. Unscented Kalman filter (UKF)
- Uses selected sigma points to approximate the propagation of nonlinear state distributions.
5. Particle filter
- Represents possible states using a collection of weighted samples.
- Useful for nonlinear and non-Gaussian estimation problems.

 ROBOT ENVIRONMENT PERCEPTION
Environmental perception enables robots to interpret surrounding objects, surfaces, obstacles, and movement.
  Major tasks
1. Obstacle detection
Identifies objects that may interfere with robot movement.
2. Object recognition 
Determines the identity or category of detected objects.
3. Object tracking
Follows an object's position and movement over time.
4. Scene understanding
Interprets the arrangement and relationships between objects in the environment.
5. Free-space detection
Identifies regions where a robot can safely move.
6. Mapping
Creates a representation of the environment.
  Environment representations
- Occupancy grids: divide the environment into cells representing occupied, free, or unknown space.
- Point clouds: represent surfaces using 3D points.
- Feature maps: represent important visual or geometric landmarks.
- Topological maps: represent places and connections between them.
- Semantic maps: represent objects and their meanings, such as roads, doors, and furniture.

 SIMULTANEOUS LOCALIZATION AND MAPPING (SLAM)
SLAM stands for Simultaneous Localization and Mapping.
It is a process through which a robot estimates its position while simultaneously constructing or updating a map of an unknown environment.
  Basic SLAM process
1. Collect sensor measurements.
2. Detect environmental features.
3. Estimate robot movement.
4. Match current observations with previously observed features.
5. Update the robot's estimated position.
6. Update the environmental map.
7. Correct accumulated errors using loop closure and optimization where applicable.
  Types of SLAM
- Visual SLAM.
- LiDAR SLAM.
- Visual-inertial SLAM.
- RGB-D SLAM.
  Important concepts
Feature extraction: Identifies distinctive environmental points or structures.
Data association: Determines whether current observations correspond to previously observed landmarks.
Loop closure: Recognizes a previously visited location and uses it to correct accumulated localization and mapping errors.
Pose estimation: Estimates the position and orientation of the robot.
  Applications
- Autonomous navigation.
- Warehouse robots.
- Self-driving vehicles.
- Drone navigation.
- Exploration robots.
- Indoor mapping.

 ARTIFICIAL INTELLIGENCE IN ROBOT PERCEPTION
AI enables robots to interpret complex sensor data and recognize patterns that may be difficult to process using traditional algorithms.
  Machine learning
Allows robots to learn patterns from collected data.
Applications:
- Object classification.
- Fault detection.
- Sensor data interpretation.
- Activity recognition.
  Deep learning
Uses multilayer neural networks to learn complex representations from data.
 Common techniques:
Convolutional Neural Networks (CNNs)
- Primarily used for image-related tasks.
- Useful for object recognition, classification, and detection.
Recurrent Neural Networks (RNNs)
- Process sequential data.
- Can be used for time-series sensor information.
Transformers
- Use attention mechanisms to process relationships in data.
- Applied to vision, multimodal perception, and sequential sensor processing.
Point-cloud neural networks
- Process 3D spatial data.
- Useful for object recognition and scene understanding.
Computer vision AI applications
- Face and object detection.
- Human pose estimation.
- Defect detection.
- Gesture recognition.
- Autonomous navigation.
Edge AI
Edge AI processes AI workloads locally on or near the robot rather than relying entirely on remote cloud computing.
Advantages:
- Reduced communication latency.
- Lower dependence on internet connectivity.
- Faster local responses.
- Improved operational autonomy.
Limitations:
- Limited processing power.
- Memory and energy constraints.
- Model optimization requirements.

 SENSOR CHARACTERISTICS AND PERFORMANCE
Sensor selection depends on measurement quality, operating conditions, and application requirements.
1. Accuracy
Closeness of a measurement to the true value.
2. Precision
Closeness of repeated measurements to one another.
3. Resolution
Smallest detectable change in the measured quantity.
4. Sensitivity
Change in sensor output per unit change in input.
    Sensitivity = ΔOutput/ΔInput
5. Range
Minimum and maximum values that a sensor can measure reliably.
6. Linearity
How closely the relationship between input and output follows a straight line.
7. Repeatability
Ability to produce consistent readings under the same conditions.
8. Response time
Time required for a sensor to respond to a change in the measured quantity.
9. Hysteresis
Difference in output depending on whether the input is increasing or decreasing.
10. Noise
Unwanted variations in sensor measurements.
11. Drift
Gradual change in sensor output over time under constant input conditions.
12. Sampling frequency
Number of measurements taken per second.
    fₛ = 1/Tₛ
Where:
- fₛ = sampling frequency (Hz).
- Tₛ = sampling period (s).
For a properly band-limited signal, the Nyquist sampling criterion requires:
    fₛ > 2f_max
In practical systems, higher sampling rates and suitable anti-aliasing filters may be necessary.

 SENSOR CALIBRATION AND SIGNAL CONDITIONING
  Sensor calibration
Calibration establishes the relationship between sensor output and the actual physical quantity being measured.
It helps correct measurement errors and improve accuracy.
 Common calibration procedures:
1. Apply known reference inputs.
2. Record sensor outputs.
3. Compare measured and reference values.
4. Determine calibration coefficients.
5. Apply corrections to subsequent measurements.
  Signal conditioning
Signal conditioning prepares sensor signals for processing by a controller or computer.
 Common operations:
Amplification: Increases signal amplitude.
Filtering: Removes unwanted frequency components and noise.
Isolation: Protects circuits from unwanted electrical interactions.
Linearization: Corrects nonlinear sensor responses.
Analog-to-digital conversion (ADC): Converts analog signals into digital values.
For an ideal n-bit ADC with input range Vref:
    Resolution ≈ Vref/2ⁿ
The exact quantization step depends on the ADC's coding convention.
 Common signal-processing filters
- Low-pass filter: allows low-frequency components and attenuates high-frequency components.
- High-pass filter: allows high-frequency components and attenuates low-frequency components.
- Band-pass filter: allows a selected frequency range.
- Notch filter: suppresses a particular frequency, such as electrical interference.

 PRACTICAL APPLICATIONS OF ROBOT SENSORS AND PERCEPTION
Industrial robotics
- Position feedback.
- Product inspection.
- Object identification.
- Force-controlled assembly.
Autonomous mobile robots
- Obstacle detection.
- Localization.
- Navigation.
- Mapping.
Drones
- Altitude measurement.
- Orientation estimation.
- Visual navigation.
- Obstacle avoidance.
Humanoid robots
- Balance estimation.
- Joint position measurement.
- Tactile interaction.
- Human activity recognition.
Agricultural robots
- Soil and moisture sensing.
- Crop detection.
- Fruit recognition.
- Environmental monitoring.
Medical robots
- Force sensing.
- Tool positioning.
- Image-guided procedures.
- Precision manipulation.
Space robots
- Visual navigation.
- Distance measurement.
- Terrain perception.
- Autonomous exploration.

 IMPORTANT ENGINEERING AND EXAM TIPS
1. Distinguish proprioceptive sensors from exteroceptive sensors.
2. Understand the working principle of each sensor, not just its name.
3. Select sensors according to range, accuracy, resolution, response time, and environmental conditions.
4. Remember that an accelerometer measures specific force, not simply linear acceleration.
5. Understand the difference between incremental and absolute encoders.
6. Remember to divide round-trip ultrasonic and LiDAR travel time by two when calculating distance.
7. Use sensor calibration to reduce systematic measurement errors.
8. Account for noise and drift when processing IMU data.
9. Understand that odometry errors accumulate over time.
10. Use sensor fusion to improve state estimation and reliability.
11. Distinguish object detection, object recognition, object tracking, and scene understanding.
12. Understand how SLAM combines localization and mapping.
13. Consider processing power, memory, latency, and energy requirements when deploying AI perception on robots.
14. Use appropriate coordinate frames when combining measurements from different sensors.
15. Validate perception systems under realistic operating conditions.

 KEY FORMULA SUMMARY
  Distance and position sensing
Ultrasonic distance:
    d = vt/2
LiDAR distance:
    d = ct/2
  Encoder measurements
Angular displacement:
    θ = 2πN/PPR
Angular velocity:
    ω = Δθ/Δt
  Mechanical sensing
Torque:
    τ = r × F
  IMU and motion estimation
Velocity:
    v(t) = v₀ + ∫a(t)dt
Position:
    x(t) = x₀ + ∫v(t)dt
Angular displacement:
    θ(t) = θ₀ + ∫ω(t)dt
Capacitive sensing
    C = εA/d
  Odometry: differential-drive robot
Linear velocity:
    v = r(ωᵣ + ωₗ)/2
Angular velocity:
    ω = r(ωᵣ − ωₗ)/L
  Sensor performance
Sensitivity:
    S = ΔOutput/ΔInput
Sampling frequency:
    fₛ = 1/Tₛ
Nyquist criterion:
    fₛ > 2f_max
Ideal ADC resolution:
    ΔV ≈ Vref/2ⁿ

CORE IDEA
Robot sensors collect information about the robot's internal state and external environment, while robot perception processes and interprets that information to understand the surroundings and estimate the robot's state.
  The fundamental relationship is:
Physical environment → Sensors → Signal processing → Perception → State estimation → Decision-making → Robot action.
Sensors provide the measurements; perception transforms those measurements into useful knowledge that enables robots to operate intelligently, accurately, and autonomously.