Robot sensors and perception bridge the gap between physical machinery and intelligent, autonomous behavior. 
Sensors collect raw data from the robot's interior and surroundings, while perception systems process, filter, and interpret that data to build a meaningful model of the world.

Overview;
• Sensation vs. Perception: Sensation is the raw physical measurement (e.g., a camera recording pixels or a laser measuring distance). Perception is the cognitive process of organizing, identifying, and contextualizing those measurements into actionable knowledge (e.g., recognizing an approaching pedestrian or mapping a room).
• Classification of Sensors:
	• Proprioceptive Sensors: Measure the internal state and physical configuration of the robot itself (e.g., joint angles, motor speeds, battery levels, and orientation).
	• Exteroceptive Sensors: Gather information about the external environment (e.g., light, sound, obstacles, temperature, and proximity).
	• Active vs. Passive: Active sensors emit energy into the environment (like LiDAR or ultrasound) and measure the return, whereas passive sensors only measure ambient energy present in the environment (like standard RGB cameras).
• Sensor Fusion: Combining data streams from multiple distinct sensors (such as cameras, LiDAR, radar, and inertial measurement units) to create a single, reliable environmental model that overcomes the blind spots or weaknesses of any single sensor.

Key Topics;
• Proprioception & Kinematics:
	• Encoders: Track rotational or linear displacement of motors and joints.
	• Inertial Measurement Units (IMUs): Combine accelerometers, gyroscopes, and sometimes magnetometers to track motion, tilt, and rotational acceleration.
• Exteroceptive Sensing & Range Finding:
	• LiDAR (Light Detection and Ranging): Uses laser pulses to generate high-resolution 3D point clouds and depth maps.
	• Ultrasonic and Infrared Sensors: Emit sound or light waves to detect close-range obstacles and measure short distances.
• Computer Vision and Image Processing:
	• RGB, Stereo, and Depth (RGB-D) Cameras: Capture color, surface texture, and stereoscopic depth cues for scene understanding.
	• Feature Extraction & Segmentation: Algorithms that isolate objects, track motion over time, and segment foregrounds from backgrounds.
• Tactile and Force Sensing:
	• Touch/Electronic Skin Sensors: Measure contact pressure, surface texture, and slip to enable delicate manipulation.
• Simultaneous Localization and Mapping (SLAM):
	• The computational pipeline where a robot uses real-time sensor data to build a map of an unknown space while simultaneously keeping track of its own position within it.

Applications;
• Autonomous Vehicles and Drones: Rely on dense sensor fusion (LiDAR, radar, GPS, cameras) for lane tracking, pedestrian avoidance, and dynamic path planning.
• Industrial Automation & Collaborative Robots ("Cobots"): Use torque sensors, vision systems, and tactile skins to assemble components safely alongside human workers.
• Service and Domestic Robots: Robotic vacuum cleaners and delivery units use infrared, sonar, and bump sensors to map household layouts and clear obstacles.
• Search and Rescue: Thermal cameras, gas sensors, and acoustic arrays help locate survivors in hazardous or collapsed structures.
• Healthcare and Assistive Robotics: Tactile and vision sensors guide prosthetic limbs or patient-care robots with fine motor precision.