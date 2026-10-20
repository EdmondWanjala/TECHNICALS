Robot kinematics is the branch of robotics that studies the geometric motion of a robot’s structure (links and joints) with respect to a reference coordinate frame, without considering the forces, torques, or masses that cause the motion.
• Links: Rigid bodies that make up the robot arm or structure.
• Joints: Connections between links (such as revolute/rotary or prismatic/sliding joints) that allow relative motion.
• Degrees of Freedom (DoF): The number of independent parameters or joint variables that define the configuration of the robot.

Key Topics;
• Forward Kinematics:
	• Given the values of the robot's joint variables (e.g., joint angles or extension lengths), calculate the spatial position and orientation of the robot's end-effector (tool, gripper, or hand).
• Inverse Kinematics:
	• Given a desired position and orientation for the end-effector in Cartesian space, calculate the required joint angles or displacements. This often yields multiple mathematical solutions or singularities.
• Coordinate Transformations & Homogeneous Matrices:
	• Mathematical tools (such as 4 × 4 homogeneous transformation matrices, rotation matrices, Euler angles, and quaternions) used to combine rotation and translation across different frames of reference (world frame, base frame, end-effector frame).
• Denavit-Hartenberg (DH) Convention:
	• A systematic method of attaching reference frames to the links of a serial manipulator to derive its kinematic equations.
• Differential Kinematics & the Jacobian Matrix:
	• Relates joint-space velocities to Cartesian-space velocities of the end-effector via the Jacobian matrix, which is crucial for real-time velocity control and identifying singularities.
• Singularities & Workspace:
	• Singularities are configurations where the robot loses one or more degrees of freedom, causing erratic joint speeds or loss of control. The workspace is the total volume of space that the robot's end-effector can physically reach.

Applications;
• Industrial Manufacturing:
	• Guiding robotic arms for welding, pick-and-place assembly, painting, and material handling with high precision.
• Path Planning and Navigation:
	• Computing collision-free trajectories for mobile robots, drones, and robotic manipulators moving through cluttered environments.
• Medical and Surgical Robotics:
	• Enabling high-accuracy movement for minimally invasive surgical instruments or prosthetic limbs.
• Computer Animation and Biomechanics:
	• Modeling articulated human skeletons, character rigging, and joint movements in virtual environments.
• Aerospace and Space Exploration:
	• Controlling satellite arms, rovers, and multi-jointed exploratory mechanisms.