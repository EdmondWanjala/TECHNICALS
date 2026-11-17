            HUMAN-ROBOT INTERACTION (HRI)
Human-Robot Interaction (HRI) is the interdisciplinary field concerned with the design, development and study of interactions between humans and robots.
It focuses on enabling robots to communicate, cooperate and work safely and effectively with humans.
  HRI combines principles from:
- Robotics and mechanical engineering.
- Artificial intelligence.
- Computer science.
- Electronics and control systems.
- Psychology and cognitive science.
- Human-computer interaction.
- Ergonomics and safety engineering.
  Main Objectives;
1. Enable effective communication between humans and robots.
2. Improve human safety during robot operation.
3. Develop intuitive and user-friendly robotic systems.
4. Enable collaboration between humans and robots.
5. Improve task efficiency and productivity.
6. Build appropriate human trust in robotic systems.
7. Make robots adaptable to human behaviour and needs.

 Types of Human-Robot Interaction
  A. Direct Interaction;
A human interacts directly with a robot through physical contact, buttons, touchscreens, gestures or other input methods.
Examples:
- Operating a robotic arm through a control panel.
- Touching a robot's interface.
- Physically guiding a collaborative robot.
  B. Remote Interaction;
A human controls or supervises a robot from a distant location.
Examples:
- Teleoperated surgical robots.
- Remotely controlled inspection robots.
- Bomb-disposal robots.
- Remote exploration robots.
  C. Collaborative Interaction;
Humans and robots work together to accomplish a shared task.
Examples:
- A worker and robotic arm assembling a product.
- A robot assisting a human in material handling.
- Collaborative manufacturing.
  D. Social Interaction;
Robots communicate with humans using speech, facial expressions, gestures and socially appropriate behaviours.
Examples:
- Companion robots.
- Educational robots.
- Reception and service robots.
- Healthcare assistance robots.
  E. Physical Human-Robot Interaction (pHRI);
Involves direct physical contact or force exchange between humans and robots.
Examples:
- Rehabilitation robots.
- Wearable robotic exoskeletons.
- Collaborative robots assisting with lifting.
- Physical guidance of robotic manipulators.

 Levels of Human-Robot Interaction
Human-robot interaction can be organized according to the level of human involvement.
1. Human-controlled: The human directly controls the robot's actions.
2. Human-supervised: The robot performs tasks automatically while a human monitors its operation.
3. Human-robot collaboration: Humans and robots share tasks and coordinate their actions.
4. Human-robot cooperation: Humans and robots contribute to a common objective, potentially performing different but complementary tasks.
5. Autonomous robot operation: The robot performs tasks independently, with humans providing goals, constraints or occasional intervention.
The required level depends on task complexity, risk, reliability and the robot's capabilities.

 Human-Robot Interaction Architecture
An HRI system integrates human input, robotic perception, decision-making, control and feedback.
  A. Human Input Interface;
Receives commands or information from humans.
Examples:
- Buttons and switches.
- Touchscreens.
- Microphones.
- Cameras.
- Gesture sensors.
- Joysticks.
- Brain-computer interfaces.
  B. Perception System;
Detects and interprets human actions and environmental information.
Examples:
- Human detection.
- Face and gesture recognition.
- Voice recognition.
- Body pose estimation.
- Human movement tracking.
  C. Communication System;
Allows information exchange between humans and robots.
  D. Decision-Making System;
Interprets human commands and determines suitable robotic actions.
  E. Robot Control System;
Converts decisions into movement and actuator commands.
  F. Feedback System;
Communicates the robot's status and actions to the human.
Feedback may be:
- Visual.
- Auditory.
- Tactile or haptic.
- Text-based.

 Human-Robot Communication
Communication enables humans and robots to exchange commands, information and feedback.
  A. Speech-Based Communication;
Robots use microphones and speech-processing software to recognize spoken commands.
Main stages:
1. Audio acquisition.
2. Noise reduction.
3. Speech recognition.
4. Language interpretation.
5. Command execution.
6. Voice or other feedback.
Technologies:
- Automatic Speech Recognition (ASR).
- Natural Language Processing (NLP).
- Text-to-Speech (TTS).
- Voice activity detection.
Applications:
- Voice-controlled assistants.
- Service robots.
- Assistive robots.
- Industrial voice-command systems.
  B. Gesture-Based Communication;
Gestures allow humans to communicate commands through body movements.
Types:
- Hand gestures.
- Arm movements.
- Head gestures.
- Full-body gestures.
Technologies:
- RGB cameras.
- Depth cameras.
- Computer vision.
- Motion tracking sensors.
- Machine learning.
Applications:
- Controlling robotic arms.
- Human-robot collaboration.
- Gesture-controlled drones.
- Assistive technologies.
  C. Facial Expression Recognition
Robots use cameras and computer vision to detect facial features and estimate expressions.
Applications:
- Social robots.
- Healthcare assistance.
- Interactive educational robots.
Important limitation: 
Facial expressions are ambiguous and culturally influenced. 
They should not be treated as definitive evidence of a person's emotional state.
  D. Touch-Based Communication;
Humans communicate with robots using physical contact or touch-sensitive interfaces.
Technologies:
- Touchscreens.
- Capacitive sensors.
- Pressure sensors.
- Force sensors.
- Tactile sensors.
Applications:
- Robot teaching.
- Physical guidance.
- Medical robots.
- Interactive service robots.

 Human Detection and Tracking
Human detection involves identifying the presence and location of people within a robot's operating environment.
Human tracking involves continuously estimating a person's position and movement.
  Common Technologies;
1. RGB cameras.
2. Depth cameras.
3. LiDAR.
4. Radar.
5. Ultrasonic sensors.
6. Wearable tracking devices.
7. Infrared sensors.
  Important Concepts;
Human detection: Determines whether a person is present.
Human localization: Estimates the person's position.
Human tracking: Follows the person's movement over time.
Pose estimation: Identifies the positions of body joints and body orientation.
Activity recognition: Identifies actions such as walking, sitting, lifting or reaching.
Applications include collision prevention, collaborative manufacturing and assistive robotics.

 Collaborative Robots (Cobots)
Collaborative robots, commonly called cobots, are robots designed to work alongside humans in shared or closely coordinated work environments.
Unlike traditional industrial robots, which often operate inside safety cages, cobots are designed with features that support human collaboration.
  Main Characteristics;
- Force and torque sensing.
- Collision detection.
- Speed and separation monitoring.
- Power and force limitation.
- Hand-guiding capabilities.
- Easy programming.
- Flexible deployment.
  Applications
1. Assembly operations.
2. Material handling.
3. Machine tending.
4. Quality inspection.
5. Packaging.
6. Laboratory automation.
  Traditional Industrial Robots vs Cobots
Traditional industrial robots:
- Often operate in restricted workspaces.
- Commonly use physical safety barriers.
- Can operate at high speeds and forces.
- May require more complex safety integration.
Collaborative robots:
- Designed for collaborative applications.
- May operate in shared workspaces after a risk assessment.
- Often include integrated sensing and safety functions.
- Can be programmed for flexible tasks.
Important: 
A cobot is not automatically safe for unrestricted human contact. 
A complete risk assessment and appropriate safeguarding are still necessary.

 Physical Human-Robot Interaction
Physical HRI involves mechanical interaction between a human and a robot through contact forces and movements.
  Important Concepts;
A. Force Sensing
Measures forces exerted on or by the robot.
B. Torque Sensing
Measures rotational forces acting on robot joints.
C. Compliance
Allows a robot to respond to external forces rather than behaving as an entirely rigid system.
D. Impedance Control
Regulates the relationship between robot motion and interaction forces.
    F = Mẍ + Bẋ + Kx
Where:
- F = interaction force.
- M = virtual mass.
- B = virtual damping.
- K = virtual stiffness.
- x = displacement.
E. Admittance Control
Uses measured external forces to generate desired motion.
A simplified model is:
    ẍ = (Fext - Bẋ - Kx)/M
F. Haptic Feedback
Provides tactile or force sensations to the human operator.
Applications:
- Teleoperation.
- Surgical robotics.
- Rehabilitation.
- Physical robot guidance.

 Human-Robot Safety
Safety is one of the most important considerations in HRI because robots may operate near people or make physical contact with them.
  Common Hazards;
- Collision with moving robot parts.
- Crushing and trapping.
- Pinching.
- Excessive contact forces.
- Unexpected robot movements.
- Electrical hazards.
- Mechanical failure.
- Software malfunction.
- Unsafe human actions.
  Safety Measures;
1. Emergency stop systems.
2. Force and torque limitation.
3. Collision detection.
4. Speed limitation.
5. Separation monitoring.
6. Protective sensors.
7. Safety-rated control systems.
8. Mechanical guarding where necessary.
9. Restricted operating zones.
10. Regular maintenance and inspection.
  Collaborative Robot Safety Principles;
Four commonly recognized collaborative operation methods include:
1. Safety-Rated Monitored Stop
The robot stops when a person enters the designated collaborative workspace.
2. Hand Guiding
A human physically guides the robot through its intended movement.
3. Speed and Separation Monitoring
The robot adjusts its movement or stops to maintain a safe separation from humans.
4. Power and Force Limiting
Robot design and control limit potentially hazardous contact forces and pressures.
These methods are associated with collaborative industrial robot safety guidance, particularly ISO 10218 and ISO/TS 15066.

 Human-Robot Trust
Trust refers to the extent to which a human considers a robot reliable, predictable and capable of performing its assigned tasks.
Trust influences whether people accept and use robotic systems.
  Factors Affecting Trust;
- Robot reliability.
- Accuracy.
- Safety.
- Transparency.
- Predictability.
- Consistency.
- Communication quality.
- Previous interaction experience.
  Appropriate Trust;
Under-trust: A person does not sufficiently trust a capable robot, limiting its usefulness.
Over-trust: A person relies excessively on a robot and may ignore its limitations or failures.
Calibrated trust: The human's level of trust matches the robot's actual capabilities and limitations.
  Ways to improve appropriate trust:
- Provide understandable feedback.
- Communicate system limitations.
- Explain important actions.
- Maintain consistent performance.
- Clearly indicate errors and uncertainty.

 Human-Robot Interaction Interfaces
An interface is the medium through which humans provide commands and receive information from robots.
  A. Graphical User Interface (GUI)
Uses visual elements such as buttons, menus, icons and displays.
Applications:
- Robot monitoring.
- Industrial control panels.
- Robot programming.
  B. Voice User Interface (VUI)
Allows spoken communication with a robot.
  C. Gesture Interface
Uses body or hand movements as commands.
  D. Haptic Interface
Provides tactile or force feedback.
  E. Brain-Computer Interface (BCI)
Uses measured brain activity to generate control commands.
Applications:
- Assistive robotics.
- Rehabilitation.
- Experimental prosthetic control.
  F. Teleoperation Interface
Allows a human to control a robot remotely through a control station or device.

 Human-Robot Cooperation and Collaboration
These concepts describe how humans and robots work toward common objectives.
  Cooperation
Humans and robots contribute to the same overall goal, but their activities may be separated in time or space.
Example: A robot transports materials to a workstation where a human performs assembly.
  Collaboration
Humans and robots coordinate their actions more directly while working on a shared task.
Example: A human positions a component while a robot holds or manipulates it.
  Important Requirements
- Task coordination.
- Communication.
- Shared situational awareness.
- Collision prevention.
- Appropriate task allocation.
- Predictable behaviour.
- Mutual adaptation.

 Task Allocation in Human-Robot Teams
Task allocation determines which activities should be performed by humans and which should be performed by robots.
  Human Strengths;
- Complex judgement.
- Contextual understanding.
- Adaptability.
- Creativity.
- Handling unusual situations.
  Robot Strengths;
- Repetitive operations.
- High precision.
- Heavy material handling.
- Continuous monitoring.
- Operation in hazardous environments.
  Task Allocation Methods
- Rule-based allocation.
- Optimization algorithms.
- Auction-based allocation.
- AI-based allocation.
- Capability-based allocation.
A good allocation system considers human capabilities, robot capabilities, safety, workload and task requirements.

 Shared Autonomy
Shared autonomy combines human control with autonomous robot decision-making.
The human provides goals, instructions or high-level commands, while the robot assists with low-level control and decision-making.
Example:
A person instructs a robotic wheelchair to move toward a doorway. The robot automatically adjusts its path to avoid obstacles.
Advantages;
- Reduces human workload.
- Improves control precision.
- Supports users with limited mobility.
- Reduces navigation complexity.
- Combines human judgement with robotic automation.

 Human Factors and Ergonomics in HRI
Human factors concern how people interact with robotic systems, while ergonomics focuses on designing systems that suit human physical and cognitive capabilities.
  Important Factors;
A. Physical Ergonomics
Considers posture, physical effort, reach, repetitive movement and fatigue.
B. Cognitive Ergonomics
Considers attention, memory, mental workload and decision-making.
C. Usability
Measures how easily people can learn and operate a robotic system.
D. Accessibility
Ensures that robotic systems can be used by people with different physical and cognitive abilities.
E. Workload
Examines the physical and mental demands placed on human operators.
Good HRI design should reduce unnecessary workload, confusion and physical strain.

 Artificial Intelligence in Human-Robot Interaction
AI enables robots to interpret human commands, recognize activities and adapt their responses.
Applications;
1. Speech recognition: Converts spoken instructions into machine-readable information.
2. Natural language processing: Interprets human language and intent.
3. Computer vision: Detects people, gestures and objects.
4. Emotion-related computing: Estimates possible emotional cues from available signals, subject to uncertainty.
5. Human activity recognition: Identifies human actions.
6. Predictive modelling: Estimates likely human movement.
7. Reinforcement learning: Helps robots learn suitable interaction strategies.
8. Intelligent dialogue systems: Support conversational interaction.
AI should support rather than replace safety-critical mechanisms. Important protective functions must not depend solely on probabilistic AI decisions.

 Teleoperation and Remote Human-Robot Interaction
Teleoperation is the remote operation of a robot by a human.
It allows people to control robots in environments that may be distant, inaccessible or dangerous.
  Main Components;
- Human operator.
- Input device or control station.
- Communication channel.
- Robot controller.
- Sensors and feedback devices.
- Remote robot and actuators.
  Types of Teleoperation;
A. Direct Teleoperation
The operator directly controls robot movements.
B. Supervisory Teleoperation
The operator gives high-level commands while the robot performs lower-level actions autonomously.
C. Shared-Control Teleoperation
The human and robot jointly determine control actions.
  Challenges
- Communication latency.
- Signal interruption.
- Limited visual feedback.
- Sensor uncertainty.
- Network reliability.
- Operator fatigue.
Applications include space exploration, underwater robotics, remote surgery and hazardous-environment inspection.

 Social Robotics
Social robotics focuses on designing robots capable of interacting with people in socially appropriate ways.
  Characteristics
- Speech communication.
- Gesture recognition.
- Social behaviour.
- Human-aware navigation.
- Interactive feedback.
- Adaptive responses.
  Applications
1. Education.
2. Elderly assistance.
3. Customer service.
4. Healthcare.
5. Companionship.
6. Public information services.
Social robots should be designed to communicate their actual capabilities clearly and avoid misleading users about their nature or abilities.

 Ethical and Privacy Considerations in HRI
Human-robot interaction raises important ethical, social and legal concerns.
  A. Privacy
Robots may collect audio, video, location and behavioural information.
Privacy measures include:
- Data minimization.
- Secure storage.
- Access control.
- Appropriate consent.
- Clear data retention policies.
  B. Security
Robots may be vulnerable to unauthorized access, malicious commands and software attacks.
  C. Accountability
Responsibility for robotic actions, failures and injuries must be clearly addressed.
  D. Transparency
Users should understand when they are interacting with a robot and what the robot can and cannot do.
  E. Human Autonomy
Robots should support human decision-making rather than unnecessarily removing human control.
  F. Bias and Fairness
AI systems used in HRI should be evaluated for unfair performance differences across users and operating conditions.

 Applications of Human-Robot Interaction
1. Industrial manufacturing: Human workers collaborate with robotic arms.
2. Healthcare: Surgical assistance and rehabilitation robotics.
3. Education: Interactive teaching and learning robots.
4. Agriculture: Human-supervised autonomous farming robots.
5. Domestic services: Cleaning and assistance robots.
6. Logistics: Human-robot warehouse collaboration.
7. Military and emergency response: Remote operation of robots in hazardous areas.
8. Assistive technology: Exoskeletons, prostheses and mobility assistance.
9. Hospitality: Reception, information and service robots.
10. Space exploration: Human operators remotely supervise robotic systems.

 Challenges in Human-Robot Interaction
- Understanding natural human language.
- Recognizing gestures accurately.
- Predicting human movement.
- Ensuring safe physical interaction.
- Managing communication delays.
- Maintaining appropriate trust.
- Handling unpredictable human behaviour.
- Protecting personal information.
- Reducing operator workload.
- Making interfaces accessible and intuitive.
- Integrating AI with reliable control systems.

 Engineering Considerations When Designing HRI Systems
1. Intended users and their capabilities.
2. Nature of the interaction.
3. Operating environment.
4. Robot speed, force and payload.
5. Sensor accuracy and reliability.
6. Communication interface.
7. Human detection and tracking.
8. Control architecture.
9. Safety and risk assessment.
10. Privacy and cybersecurity.
11. System usability.
12. Maintenance and reliability.

 Key Revision Points
- HRI stands for Human-Robot Interaction.
- HRI studies communication and cooperation between humans and robots.
- Physical HRI involves force exchange and physical contact.
- Cobots are designed to support human-robot collaboration.
- Speech recognition enables voice-command interaction.
- Computer vision supports human detection and gesture recognition.
- Haptic feedback communicates force or tactile information.
- Teleoperation enables remote robot control.
- Shared autonomy combines human input with autonomous robot functions.
- Impedance control regulates the relationship between movement and interaction forces.
- Human factors and ergonomics improve usability and reduce workload.
- Safety is essential in physical human-robot interaction.
- Trust should be calibrated to actual robot capabilities.
- Privacy, accountability and cybersecurity are important ethical considerations.
Central idea: Human-Robot Interaction integrates robotics, sensing, artificial intelligence, communication, control and human factors to enable safe, effective and meaningful cooperation between humans and robotic systems.