Robot dynamics is the study of forces, torques, and energy and how they cause or affect the motion of robotic systems. 
While kinematics looks strictly at geometry and motion without regard to what powers it, dynamics connects actuator inputs (like motor torques) to physical movement. 
The fundamental governing equation of motion for a rigid-body robot is: 
    M(q)q̈+C(q,q̇)q̇+G(q)=τ+JT(q)Fccap M open paren q close paren q double dot plus cap C open paren q comma q dot close paren q dot plus cap G open paren q close paren equals tau plus cap J to the cap T-th power open paren q close paren cap F sub c
        𝑀(𝑞)𝑞̈+𝐶(𝑞,𝑞̇)𝑞̇+𝐺(𝑞)=𝜏+𝐽𝑇(𝑞)𝐹𝑐
• M(q): Inertia matrix (mass and moment of inertia properties)
• 𝑪(𝒒,𝒒̇): Coriolis and centrifugal forces
• G(q): Gravity vector
• τ: Actuator joint torques or forces
• 𝑱𝑻(𝒒)𝑭𝒄: Contributions from external contact forces mapped via the Jacobian 

Key Topics;
• Derivation Methods: Formulating equations of motion using Newton-Euler (recursive/computational efficiency) or Lagrangian mechanics (energy-based formulation). 
• Forward vs. Inverse Dynamics:
	• Inverse Dynamics: Given the robot's position, velocity, and acceleration, calculate the required joint torques (τ). Essential for real-time control.
	• Forward Dynamics: Given the applied joint torques, calculate the resulting accelerations, velocities, and positions. Essential for physics simulation. 
• Fixed-Base vs. Floating-Base Systems: Differentiating between grounded industrial robot arms (fixed base) and mobile platforms, humanoids, or quadrupeds whose base isn't rigidly anchored to the earth. 
• Control & Compensation: Using dynamic models for computed-torque control, gravity cancellation, and operational space control to ensure high-precision tracking. 
• Learning-Based Dynamics: Using neural networks, reinforcement learning, and data-driven approaches to handle unmodeled nonlinearities like friction, gear backlash, and flexible cables. 

Main Applications;
• Industrial Automation: Designing and tuning multi-axis robotic arms for high-speed assembly, welding, and material handling.
• Robot Simulation: Building digital twins and physics environments (such as in ROS 2 / Gazebo) to test control algorithms safely before deploying to physical hardware.
• Mobile & Humanoid Robotics: Stabilizing walking bipeds, quadrupedal dogs, and drones that must constantly manage shifting centers of mass and ground reaction forces.
• Dexterous Manipulation: Enabling robotic hands to perform complex, contact-rich tasks like turning book pages, sorting objects, or handling tools smoothly.