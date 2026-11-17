            AUTONOMOUS SYSTEMS
An autonomous system is a machine or computational system capable of performing tasks, making decisions and controlling its operations with minimal or no continuous human intervention.
In robotics, autonomous systems enable robots to perceive their environment, interpret information, make decisions, plan actions and execute tasks independently.
  Examples include:
- Self-driving vehicles.
- Autonomous mobile robots (AMRs).
- Unmanned aerial vehicles (UAVs).
- Agricultural robots.
- Industrial inspection robots.
- Planetary exploration rovers.
  Main Characteristics
1. Autonomy: Ability to operate independently.
2. Perception: Ability to sense and interpret the environment.
3. Decision-making: Ability to select appropriate actions.
4. Planning: Ability to determine actions required to achieve objectives.
5. Adaptability: Ability to respond to changing conditions.
6. Learning: Ability to improve performance using experience or data.
7. Navigation: Ability to determine position and move toward destinations.
8. Fault tolerance: Ability to detect, manage or recover from certain failures.

 Levels of Autonomy
Autonomous systems can be classified according to their level of independence.
1. Manual operation: A human directly controls the system.
2. Remote-controlled operation: A human controls the system from a distance.
3. Assisted operation: The system performs specific functions automatically while a human supervises.
4. Semi-autonomous operation: The system independently performs certain tasks but requires human intervention in some situations.
5. Highly autonomous operation: The system independently performs complex tasks within defined operational conditions.
6. Fully autonomous operation: The system operates independently within its intended operational domain without requiring routine human intervention.
Note: 
Autonomy is task- and environment-dependent. 
A robot may be highly autonomous in a controlled factory but less autonomous in an unpredictable outdoor environment.

 Architecture of an Autonomous Robotic System
An autonomous robot generally consists of the following interconnected subsystems:
  A. Perception System
Collects and interprets information about the environment using sensors.
Examples:
- Cameras.
- LiDAR.
- Radar.
- Ultrasonic sensors.
- Infrared sensors.
- IMUs.
- GPS/GNSS receivers.
  B. Localization System
Determines the robot's position and orientation within its environment.
  C. Mapping System
Builds or updates a representation of the surrounding environment.
  D. Planning System
Determines the robot's route, trajectory and actions required to achieve its objective.
  E. Decision-Making System
Selects appropriate actions based on the robot's goals, observations and environmental conditions.
  F. Control System
Converts planned actions into motor commands and regulates the robot's movement.
  G. Communication System
Allows information exchange between the robot, other robots, remote operators and external systems.
  H. Power Management System
Monitors and manages energy consumption, battery condition and power distribution.

 Sense–Think–Act Cycle
Autonomous robots operate through a continuous cycle known as the sense–think–act loop.
1. Sense: Sensors collect information about the environment.
2. Perceive: The robot processes sensor data to identify objects, obstacles and environmental conditions.
3. Localize: The robot estimates its position and orientation.
4. Think: The decision-making system interprets the situation and selects an appropriate action.
5. Plan: The robot calculates a suitable path or sequence of actions.
6. Act: Motors and actuators execute the planned movement.
7. Evaluate: Feedback is used to determine whether the action achieved the intended result.
This cycle repeats continuously as the robot interacts with its environment.

 Sensors Used in Autonomous Systems
Sensors enable robots to observe their surroundings and monitor their internal conditions.
  A. Cameras
Capture visual information about the environment.
Applications:
- Object recognition.
- Lane detection.
- Facial and gesture recognition.
- Visual navigation.
- Defect inspection.
Types:
- Monocular cameras.
- Stereo cameras.
- RGB cameras.
- Depth cameras.
- Thermal cameras.
  B. LiDAR (Light Detection and Ranging)
Uses laser pulses to measure distances and generate information about surrounding objects.
Applications:
- 3D mapping.
- Obstacle detection.
- Robot localization.
- Autonomous vehicle navigation.
  C. Radar
Uses radio waves to detect objects and estimate their distance and relative velocity.
Applications:
- Vehicle detection.
- Collision avoidance.
- Long-range object detection.
  D. Ultrasonic Sensors
Use high-frequency sound waves to measure distances.
Applications:
- Short-range obstacle detection.
- Robotic parking.
- Collision prevention.
  E. IMU (Inertial Measurement Unit)
Measures the robot's linear acceleration and angular velocity using accelerometers and gyroscopes. Some IMUs also include magnetometers.
Applications:
- Orientation estimation.
- Motion tracking.
- Drone stabilization.
- Dead reckoning.
  F. GPS/GNSS
Provides geographical position and, with suitable receivers, velocity and timing information.
Applications:
- Outdoor navigation.
- Autonomous vehicles.
- Agricultural robots.
- Drone navigation.
  G. Encoders
Measure motor or joint rotation and provide position and velocity feedback.
Applications:
- Wheel odometry.
- Joint position control.
- Robot movement estimation.

 Sensor Fusion
Sensor fusion is the process of combining information from multiple sensors to obtain a more reliable and accurate estimate of the robot's environment or internal state.
For example, an autonomous vehicle can combine:
- Camera data for object classification.
- LiDAR data for accurate distance measurements.
- Radar data for relative speed.
- GPS data for geographical positioning.
- IMU data for motion and orientation estimation.
  Sensor Fusion Methods
1. Kalman Filter: Estimates system states using prediction and measurement updates under suitable probabilistic assumptions.
2. Extended Kalman Filter (EKF): Applies Kalman filtering to nonlinear systems through local linearization.
3. Unscented Kalman Filter (UKF): Uses selected sigma points to approximate nonlinear state transformations.
4. Particle Filter: Represents uncertain states using a collection of weighted samples.
5. Complementary Filter: Combines measurements with different frequency characteristics, commonly accelerometer and gyroscope data.
Sensor fusion improves robustness, reduces uncertainty and compensates for individual sensor limitations.

 Localization and Position Estimation
Localization is the process through which a robot determines its position and orientation relative to a reference coordinate system or map.
A robot's 2D pose is commonly represented as:
    ξ = [x, y, θ]ᵀ
Where:
- x = position along the X-axis.
- y = position along the Y-axis.
- θ = orientation or heading angle.
  Localization Techniques
A. GPS/GNSS Localization
Uses satellite signals to estimate geographical position.
B. Odometry
Estimates movement by measuring wheel rotations or joint displacement.
C. Inertial Navigation
Uses accelerometer and gyroscope measurements to estimate motion and orientation.
D. Visual Odometry
Estimates camera movement by tracking visual features across consecutive images.
E. LiDAR Localization
Matches laser scan measurements against a map or previous scans.
F. Landmark-Based Localization
Uses identifiable environmental features as reference points.
  Dead Reckoning
Dead reckoning estimates the current position using a previously known position and measured movement.
For a simple robot moving in 2D:
    x(t) = x₀ + ∫v cosθ dt
    y(t) = y₀ + ∫v sinθ dt
Where:
- x₀, y₀ = initial position.
- v = linear velocity.
- θ = heading angle.
Dead reckoning accumulates errors over time, making periodic corrections important.

 Mapping and Environmental Representation
Mapping involves constructing a representation of the environment for navigation, planning and obstacle avoidance.
 Types of Maps
A. Occupancy Grid Maps
Divide the environment into cells, each representing the probability of being occupied by an obstacle.
B. Topological Maps
Represent locations as nodes and connections between them as edges.
C. Metric Maps
Represent the environment using geometric measurements and spatial relationships.
D. Feature-Based Maps
Represent the environment using identifiable landmarks or geometric features.
E. 3D Maps
Represent environmental structures in three dimensions, commonly using LiDAR point clouds or depth information.
  Occupancy Probability
Each grid cell can be assigned an occupancy probability:
    P(occupied | measurements)
A high probability indicates that a cell is likely occupied, while a low probability indicates that it is likely free.

 SLAM (Simultaneous Localization and Mapping)
SLAM is a technique that allows a robot to estimate its position while simultaneously constructing or updating a map of an initially unknown environment.
It solves two interconnected problems:
1. Where is the robot?
2. What does the surrounding environment look like?
  SLAM Process
1. Collect sensor measurements.
2. Identify environmental features.
3. Estimate robot movement.
4. Match current observations with previously observed features.
5. Update the estimated robot position.
6. Update the environmental map.
7. Correct accumulated localization errors.
Types of SLAM
- Visual SLAM: Uses camera images.
- LiDAR SLAM: Uses laser scanning measurements.
- Visual-inertial SLAM: Combines cameras and IMU data.
- RGB-D SLAM: Uses colour and depth information.
Applications
- Autonomous mobile robots.
- Indoor navigation.
- Warehouse automation.
- Drone navigation.
- Robotic exploration.

 Path Planning and Motion Planning
Path planning determines a route from the robot's starting position to its destination while avoiding obstacles.
Motion planning determines a feasible movement sequence that also considers the robot's physical and dynamic constraints.
  Path Planning Algorithms
A. Dijkstra's Algorithm
Finds the shortest path in a graph with non-negative edge costs.
B. A Algorithm*
Uses actual path cost and a heuristic estimate of the remaining cost.
    f(n) = g(n) + h(n)
Where:
- g(n) = cost from the starting node to the current node.
- h(n) = estimated cost from the current node to the goal.
- f(n) = estimated total path cost.
C. Rapidly Exploring Random Trees (RRT)
Uses randomly sampled configurations to explore a robot's configuration space and construct feasible paths.
D. Probabilistic Roadmaps (PRM)
Builds a graph of collision-free sampled configurations and searches it for a route.
E. Potential Field Method
Uses attractive forces toward the goal and repulsive forces away from obstacles.
F. Dynamic Window Approach (DWA)
Evaluates feasible short-term velocity commands and selects one based on safety and motion objectives.
  Path Planning Considerations
- Shortest distance.
- Obstacle avoidance.
- Energy consumption.
- Robot dimensions.
- Maximum speed.
- Acceleration constraints.
- Terrain conditions.
- Dynamic obstacles.

 Obstacle Detection and Avoidance
Obstacle avoidance enables a robot to detect potential collisions and select safe movement actions.
  Main Stages
1. Detect obstacles using sensors.
2. Estimate their position and dimensions.
3. Determine their movement where applicable.
4. Calculate collision risk.
5. Select an avoidance manoeuvre.
6. Adjust the robot's trajectory.
7. Resume navigation when safe.
  Obstacle Avoidance Methods
- Reactive obstacle avoidance.
- Potential field methods.
- Vector Field Histogram (VFH).
- Dynamic Window Approach.
- Model Predictive Control (MPC).
- Vision-based obstacle avoidance.
Reactive avoidance: Responds directly to current sensor measurements.
Predictive avoidance: Estimates future motion and potential collisions before selecting an action.

 Decision-Making in Autonomous Systems
Decision-making determines which action an autonomous robot should perform based on its goals, current state and available information.
  Common Decision-Making Approaches
A. Rule-Based Systems
Use predefined IF–THEN rules.
Example:
- IF an obstacle is detected within a critical distance, THEN stop.
- IF the path is clear, THEN continue moving.
B. Finite State Machines (FSM)
Represent behaviour using a finite number of states and transitions.
Example states:
- Idle.
- Navigate.
- Detect obstacle.
- Avoid obstacle.
- Reach destination.
- Emergency stop.
C. Behaviour-Based Control
Uses multiple interacting behaviours, such as obstacle avoidance, target seeking and wall following.
D. Probabilistic Decision-Making
Uses probabilities to make decisions under uncertainty.
E. Reinforcement Learning
Learns suitable actions through interaction with an environment and feedback in the form of rewards or penalties.

 Artificial Intelligence in Autonomous Systems
Artificial intelligence enables robots to perform tasks that require perception, recognition, prediction, learning and decision-making.
  Important AI Technologies
A. Machine Learning (ML)
Allows systems to learn patterns from data.
Applications:
- Object classification.
- Predictive maintenance.
- Behaviour prediction.
B. Deep Learning
Uses multi-layer neural networks to learn complex representations.
Applications:
- Visual recognition.
- Scene understanding.
- Object detection.
C. Computer Vision
Enables robots to extract useful information from images and videos.
Applications:
- Object detection.
- Tracking.
- Segmentation.
- Visual navigation.
D. Reinforcement Learning
Allows an agent to learn actions through interaction with an environment.
The objective is to maximize cumulative reward.
E. Natural Language Processing
Allows robots to interpret and respond to human language.
  Important Distinction
AI is not a requirement for every autonomous system. Many autonomous robots operate effectively using conventional control algorithms, predefined rules and deterministic planning methods.

 Autonomous Navigation
Autonomous navigation is the ability of a robot to determine where it is, where it needs to go and how to reach its destination safely.
  Navigation Process
1. Determine the robot's current location.
2. Identify the destination.
3. Construct or obtain an environmental map.
4. Plan a suitable route.
5. Detect obstacles.
6. Execute the route using motion control.
7. Continuously update localization and navigation decisions.
   Navigation Types
- Indoor navigation.
- Outdoor navigation.
- GPS-based navigation.
- Vision-based navigation.
- LiDAR-based navigation.
- Landmark-based navigation.
- Terrain-based navigation.

 Communication in Autonomous Systems
Communication enables autonomous robots to exchange information with external devices, infrastructure, other robots and human operators.
  Communication Technologies;
- Wi-Fi.
- Bluetooth.
- Zigbee.
- Cellular networks (4G/5G).
- Ethernet.
- CAN bus.
- Serial communication.
- ROS 2 middleware using DDS.
Applications
- Remote monitoring.
- Fleet coordination.
- Multi-robot collaboration.
- Sensor data sharing.
- Remote software updates.
- Supervisory control.
Communication is not always necessary for basic autonomy. 
A robot can perform autonomous tasks without a continuous network connection.

 Multi-Robot Autonomous Systems
A multi-robot system consists of two or more robots cooperating or coordinating to accomplish tasks.
  Common Coordination Approaches
A. Centralized Coordination
A central controller assigns tasks and coordinates the robots.
B. Decentralized Coordination
Individual robots make local decisions and communicate when necessary.
C. Distributed Coordination
Decision-making and task execution are distributed across multiple robots.
 Important Concepts
- Task allocation.
- Cooperative navigation.
- Collision avoidance.
- Communication protocols.
- Formation control.
- Cooperative mapping.
- Resource sharing.
Applications
- Warehouse fleets.
- Search and rescue.
- Agricultural automation.
- Swarm robotics.
- Environmental monitoring.

 Autonomous Systems and Real-Time Computing
Autonomous robots must process sensor information and generate control commands within appropriate time limits.
Real-time computing ensures that critical operations are completed within their required deadlines.
  Important Concepts
A. Sampling Rate
The frequency at which sensor measurements or control updates are obtained.
B. Latency
The time delay between an event, its processing and the resulting response.
C. Jitter
Variation in timing or latency.
D. Processing Throughput
The amount of data or computation processed within a given period.
E. Real-Time Operating System (RTOS)
An operating system designed to provide predictable task scheduling and timing behaviour.
Examples:
- FreeRTOS.
- Zephyr.
- QNX.
- VxWorks.
A missed deadline in a safety-critical control task can cause system failure even when the computed result is mathematically correct.

 Autonomous Systems Hardware and Software
Hardware Components
- Microcontrollers.
- Microprocessors.
- Embedded computers.
- GPU-equipped computing platforms.
- Sensors.
- Motor drivers.
- Actuators.
- Communication modules.
- Battery and power management systems.
Software Components
- Embedded firmware.
- Robot operating middleware.
- Sensor-processing algorithms.
- Localization software.
- Mapping algorithms.
- Path planners.
- AI models.
- Motion controllers.
- Safety-monitoring software.
  Common Development Platforms
ROS 2 (Robot Operating System 2):
A robotics middleware framework that supports communication, hardware integration, sensor processing, navigation and distributed robotic applications.
Python:
Commonly used for AI, data processing, prototyping and robotics development.
C/C++:
Widely used for performance-critical robotics software, embedded systems and real-time processing.
Linux/Ubuntu:
Commonly used as the development and deployment environment for robotics applications.

 Safety, Reliability and Fault Tolerance
Autonomous robots must operate safely even when unexpected events or component failures occur.
Common Risks
- Sensor malfunction.
- Communication failure.
- Battery depletion.
- Software errors.
- Navigation failure.
- Unexpected obstacles.
- Actuator failure.
- Incorrect environmental interpretation.
Safety Mechanisms
1. Emergency stop systems.
2. Collision detection.
3. Speed and force limits.
4. Sensor redundancy.
5. Watchdog timers.
6. Fault detection and diagnosis.
7. Safe shutdown procedures.
8. Restricted operating zones.
9. Human supervision where necessary.
Fault Tolerance
Fault tolerance is the ability of a system to continue operating safely or recover appropriately when some components fail.
It may involve:
- Redundant sensors.
- Backup controllers.
- Error detection.
- Recovery procedures.
- Graceful degradation.

 Applications of Autonomous Systems
1. Industrial robotics: Autonomous material handling, inspection and manufacturing.
2. Transportation: Self-driving vehicles and autonomous delivery systems.
3. Agriculture: Crop monitoring, precision spraying and automated harvesting.
4. Healthcare: Assistive robots and autonomous hospital logistics.
5. Aerospace: UAVs, autonomous spacecraft and planetary rovers.
6. Military and security: Unmanned surveillance and reconnaissance systems.
7. Logistics: Automated warehouses and delivery robots.
8. Environmental monitoring: Autonomous underwater vehicles and field-monitoring robots.
9. Domestic applications: Cleaning robots and intelligent home systems.
10. Disaster response: Search-and-rescue robots operating in hazardous environments.

 Challenges Facing Autonomous Systems
- Unpredictable environmental conditions.
- Sensor noise and uncertainty.
- Localization errors.
- Dynamic obstacles.
- Limited battery capacity.
- Computational limitations.
- Communication delays.
- Cybersecurity threats.
- High development costs.
- Safety and ethical concerns.
- Difficulties in generalizing AI models to unfamiliar environments.

 Important Engineering Considerations
When designing an autonomous robotic system, consider:
1. Operating environment: Indoor, outdoor, underwater or aerial.
2. Required autonomy level.
3. Sensor selection and placement.
4. Localization accuracy.
5. Mapping and navigation requirements.
6. Processing power and memory.
7. Communication requirements.
8. Actuator and motor specifications.
9. Energy efficiency.
10. Real-time performance.
11. Safety and reliability.
12. Testing under realistic operating conditions.

 Key Revision Points
- Autonomous systems perform tasks with minimal continuous human intervention.
- Perception enables robots to understand their surroundings.
- Localization estimates position and orientation.
- Mapping constructs a representation of the environment.
- SLAM combines localization and mapping.
- Sensor fusion combines information from multiple sensors.
- Path planning determines a suitable route.
- Motion planning considers robot movement constraints.
- Obstacle avoidance prevents collisions.
- Decision-making selects suitable actions.
- AI enables learning, recognition and intelligent decision-making but is not essential for all autonomous systems.
- ROS 2 is widely used in robotics software development.
- Real-time computing supports timely control and decision-making.
- Fault tolerance and safety mechanisms improve operational reliability.

Central idea: 
An autonomous robotic system integrates sensing, perception, localization, mapping, planning, decision-making and control to perform tasks independently while responding to changes in its environment.