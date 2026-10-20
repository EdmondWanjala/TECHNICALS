                ROBOT DYNAMICS 
Robot dynamics studies the forces, torques, masses, and moments of inertia that cause robot motion. 
It relates the motion of robot links and joints to the forces and torques required to produce that motion.

Main objectives:
- Determine the torque or force required to move a robot.
- Predict robot motion under applied forces.
- Model gravity, inertia, friction, and external loads.
- Support trajectory planning, motor selection, and control-system design.
- Improve robot stability, accuracy, and energy efficiency.
Robot kinematics vs. dynamics:
- Kinematics: describes position, velocity, and acceleration without considering forces.
- Dynamics: relates forces and torques to motion.

FUNDAMENTAL MECHANICAL QUANTITIES:
- Mass (m): resistance to linear acceleration, measured in kg.
- Moment of inertia (I): resistance to angular acceleration, measured in kg·m².
- Force (F): causes linear acceleration, measured in newtons (N).
- Torque (τ): rotational effect of a force, measured in N·m.
- Position (q): generalized coordinates describing joint configurations.
- Velocity (q̇): rate of change of joint position.
- Acceleration (q̈): rate of change of joint velocity.
- Potential energy (V): energy due to position, especially in a gravitational field.
- Kinetic energy (T): energy due to translational and rotational motion.
Newton's laws;
First law: A body remains at rest or in uniform motion unless acted upon by a net external force.
Second law:F = ma
Rotational form:τ = Iα
For a rigid body rotating about a fixed axis, τ = Iα applies when I is constant and the net torque is taken about that axis.
Third law: Every action has an equal and opposite reaction.
General force and torque relationships
Linear momentum:
    p = mv
Angular momentum about a fixed axis:
    L = Iω
Power in linear motion:
    P = Fv
Power in rotational motion:
    P = τω
Work done by a constant torque:
    W = τΔθ
For a variable torque:
    W = ∫τ dθ

DEGREES OF FREEDOM AND GENERALIZED COORDINATES:
A robot's degree of freedom (DOF) is the number of independent coordinates needed to describe its configuration.
- Revolute joint: permits rotation; coordinate is angle θ.
- Prismatic joint: permits translation; coordinate is displacement d.
For a robot with n independent joints:
    q = [q₁, q₂, ..., qₙ]ᵀ
Joint velocity:
    q̇ = dq/dt
Joint acceleration:
    q̈ = d²q/dt²
The vector q is the generalized coordinate vector. Its elements may be joint angles or linear displacements.

ROBOT DYNAMICS EQUATION:
The standard manipulator dynamics equation is:
    M(q)q̈ + C(q,q̇)q̇ + G(q) + F(q̇) = τ + Jᵀ(q)Fₑₓₜ
Where:
- M(q): inertia or mass matrix.
- q̈: joint acceleration vector.
- C(q,q̇)q̇: Coriolis and centrifugal effects.
- G(q): gravity torque or force vector.
- F(q̇): joint friction effects.
- τ: actuator torque or force vector.
- J(q): robot Jacobian matrix.
- Fₑₓₜ: external wrench applied to the robot, expressed in a compatible coordinate frame and with a consistent sign convention.
If external forces and friction are neglected:
    M(q)q̈ + C(q,q̇)q̇ + G(q) = τ
The equation predicts motion when actuator inputs are known, or calculates required actuator inputs when the desired motion is specified.
Important properties;
- M(q) is symmetric and, for a properly modeled robot with positive link masses and inertias, positive definite.
- Inertia depends on robot configuration because the links change their relative orientations.
- Coriolis and centrifugal terms depend on joint positions and velocities.
- Gravity effects depend on configuration and gravitational acceleration.
- Friction may include viscous, Coulomb, and more complex nonlinear effects.

FORWARD AND INVERSE DYNAMICS:
Forward dynamics
Determines joint acceleration from known actuator inputs and robot state.
    q̈ = M⁻¹(q)[τ − C(q,q̇)q̇ − G(q) − F(q̇) + JᵀFₑₓₜ]
The external-force sign shown assumes the dynamics equation in Section 4.
Applications: physics simulation, motion prediction, and evaluating robot response to motor commands.
Inverse dynamics;
Calculates the actuator torque or force required for a specified trajectory q(t).
    τ = M(q)q̈ + C(q,q̇)q̇ + G(q) + F(q̇) − JᵀFₑₓₜ
Applications: trajectory tracking, feedforward control, actuator sizing, and energy estimation.
Remember:
- Forward dynamics: input torque → acceleration.
- Inverse dynamics: desired motion → required torque.

KINETIC AND POTENTIAL ENERGY:
Robot dynamics can be derived using energy methods.
Translational kinetic energy
    T_trans = ½mv²
Rotational kinetic energy
    T_rot = ½Iω²
For a rigid body in three-dimensional motion:
    T = ½mvᵀv + ½ωᵀIω
Here, I is the inertia tensor about the center of mass, expressed in the same frame as ω.
Gravitational potential energy
    V = mgh
Where:
- m = mass (kg)
- g = gravitational acceleration (approximately 9.81 m/s²)
- h = height above a chosen reference level (m)
For a multi-link robot:
    T = ΣTᵢ
    V = Σmᵢghᵢ
Each link's kinetic energy must account for its translational and rotational motion, and each link's height is measured consistently relative to the chosen reference.

LAGRANGIAN FORMULATION:
The Lagrangian method derives robot equations using kinetic and potential energy.
    L(q,q̇) = T(q,q̇) − V(q)
For each generalized coordinate qᵢ:
    d/dt(∂L/∂q̇ᵢ) − ∂L/∂qᵢ = Qᵢ
Where Qᵢ is the generalized nonconservative force, including actuator input and applicable friction or external-force contributions.
For a robot with n joints, apply the equation to every coordinate q₁, q₂, ..., qₙ.
The resulting equations can be arranged into:
    M(q)q̈ + C(q,q̇)q̇ + G(q) = τ
when nonconservative effects are omitted.
Advantages:
- Systematic for multi-joint robots.
- Uses energy rather than resolving every internal force.
- Convenient for deriving equations symbolically.
Limitation: Derivations can become algebraically complex as the number of links increases.

NEWTON–EULER FORMULATION:
The Newton–Euler method applies force and moment balance to individual robot links.
Newton's equation
    ΣF = ma
Euler's rotational equation
For a rigid body about its center of mass, expressed in a body-fixed frame:
    Στ = Iα + ω × (Iω)
Where:
- I = inertia tensor.
- α = angular acceleration.
- ω × (Iω) = gyroscopic term.
For a serial robot, the recursive Newton–Euler algorithm uses:
1. Forward recursion: calculate link velocities and accelerations from the base toward the end effector.
2. Backward recursion: calculate forces and moments from the end effector back toward the base.
3. Project the resulting joint forces or moments onto each joint axis to obtain actuator effort.
Advantages:
- Computationally efficient for inverse dynamics.
- Well suited to real-time control of multi-link robots.
- Commonly used in robot dynamics libraries.

INERTIA AND THE MASS MATRIX:
The mass matrix describes how the robot's mass distribution affects joint accelerations and required actuator effort.
    M(q) = [Mᵢⱼ(q)]
For an n-joint robot, M is an n × n matrix.
The diagonal elements represent individual joint inertia contributions; off-diagonal elements describe dynamic coupling between joints.
A torque at one joint may influence the acceleration of other joints because the links are mechanically coupled.
The matrix is configuration-dependent in general, and its calculation uses each link's mass, center of mass, and inertia tensor.

CORIOLIS AND CENTRIFUGAL EFFECTS:
These terms arise from motion in a configuration-dependent mechanical system.
- Centrifugal effects: velocity-dependent effects associated with motion around a rotational path.
- Coriolis effects: coupling effects involving the velocities of multiple moving coordinates.
The combined vector is commonly represented by:
    h(q,q̇) = C(q,q̇)q̇
The matrix C is not unique; different valid formulations can produce the same vector h.
For an appropriate choice of C, the matrix Ṁ − 2C is skew-symmetric. This property is useful in robot-control stability analysis.
These effects become particularly important at high joint speeds.

GRAVITY COMPENSATION:
Gravity produces joint torques that depend on the robot's configuration and link mass distribution.
For a stationary robot:
    q̇ = 0, q̈ = 0
Ignoring friction and external loads:
    τ = G(q)
This is the gravity-compensation torque needed to hold the robot stationary.
In practical robots, gravity compensation reduces the effort required from the controller to maintain a pose and improves tracking performance.

JOINT FRICTION AND ACTUATORS:
Common friction models include:
Viscous friction
    τᵥ = bq̇
Where b is the viscous friction coefficient.
Coulomb friction;
    τ꜀ ≈ τ₀ sign(q̇)
Where τ₀ is the Coulomb friction magnitude. This approximation is discontinuous at zero velocity; real systems may exhibit stiction and more complex behavior near zero speed.
Combined simple model;
    τ_f = bq̇ + τ₀ sign(q̇)
Actuators must supply torque to overcome gravity, accelerate the robot, counter dynamic coupling, and compensate for friction and external loads.
For a rotary motor:
    P_mech = τω
For a linear actuator:
    P_mech = Fv
Mechanical power is not the same as electrical input power. Motor losses, gearbox efficiency, and drive electronics must also be considered.

JACOBIAN AND EXTERNAL FORCES:
The Jacobian maps joint velocities to end-effector velocity:
    vₑ = J(q)q̇
For a spatial robot, the Jacobian typically maps joint velocities to a six-dimensional twist containing linear and angular velocity.
The corresponding force/torque relationship is:
    τₑₓₜ = Jᵀ(q)Fₑₓₜ
This maps an end-effector wrench into equivalent joint efforts, subject to a consistent wrench and sign convention.
A wrench includes:
- Force components (N).
- Moment or torque components (N·m).
This relationship is essential for contact tasks, gripping, pushing, and force control.

ROBOT DYNAMIC SIMULATION AND CONTROL:
A typical workflow is:
1. Define robot geometry, joint types, masses, centers of mass, and inertia tensors.
2. Define joint coordinates and reference frames.
3. Derive or obtain the dynamics model.
4. Specify actuator inputs and external loads.
5. Solve the forward-dynamics equations for acceleration.
6. Numerically integrate acceleration to update velocity and position.
7. Compare the simulated response with the desired trajectory.
8. Tune the controller and validate the model against real robot data.
Common control strategies;
PID control: uses position, velocity, or other feedback errors to calculate corrective actuator commands.
Computed-torque control: uses a dynamics model to compensate for inertia, coupling, and gravity.
Impedance control: regulates the dynamic relationship between position error and interaction force, useful for compliant contact.
Force control: regulates contact force rather than relying solely on position tracking.
A practical controller must consider actuator saturation, sensor noise, model errors, and safety limits.

SIMPLE EXAMPLE: SINGLE ROTATIONAL JOINT:
Consider a rigid link rotating about a fixed horizontal axis, with its center of mass a distance l_c from the joint.
Let:
- m = link mass.
- I = moment of inertia about the joint axis.
- θ = joint angle measured from the downward vertical.
- τ = applied motor torque.
- b = viscous friction coefficient.
The equation of motion is:
    Iθ̈ + bθ̇ + mgl_c sinθ = τ
Therefore:
    θ̈ = [τ − bθ̇ − mgl_c sinθ]/I
At rest, θ̇ = 0 and θ̈ = 0, so:      
    τ = mgl_c sinθ
The motor must supply the torque needed to balance gravity at the specified angle. The sign of the gravity term depends on the chosen angle convention.

PRACTICAL ENGINEERING APPLICATIONS:
Robot dynamics is used in:
- Industrial robotic arms for accurate high-speed movement.
- Autonomous robots for predicting motion and responding to disturbances.
- Humanoid robots for balance, walking, and whole-body coordination.
- Collaborative robots for safe physical interaction with humans.
- Robotic surgery for controlled movement and force application.
- Mobile robots for wheel torque and traction analysis.
- Space robotics for manipulating objects under low-gravity conditions.
- Simulation and digital twins for testing motion before physical deployment.

IMPORTANT EXAM AND DESIGN TIPS:
1. Always define coordinate frames, positive directions, and angle conventions before deriving equations.
2. Use SI units consistently: kg, m, s, N, and N·m.
3. Distinguish joint coordinates from end-effector coordinates.
4. Include gravity when the robot operates in a gravitational field.
5. Include friction and external loads when the application requires realistic predictions.
6. Use inverse dynamics to estimate actuator torque for a desired trajectory.
7. Use forward dynamics to predict acceleration from known torques.
8. Do not confuse moment of inertia with mass; they describe resistance to angular and linear acceleration, respectively.
9. Check dimensional consistency: every term in a joint torque equation must have units of N·m for a revolute joint or N for a prismatic joint.
10. Validate dynamic models experimentally; inaccurate masses, friction estimates, and actuator models can cause substantial prediction errors.

KEY FORMULA SUMMARY:
Newton's second law:
    F = ma
Rotational dynamics:
    τ = Iα  (fixed axis, constant I)
Translational kinetic energy:
    T = ½mv²
Rotational kinetic energy:
    T = ½Iω²
Gravitational potential energy:
    V = mgh
Lagrangian:
    L = T − V
Euler–Lagrange equation:
    d/dt(∂L/∂q̇ᵢ) − ∂L/∂qᵢ = Qᵢ
Robot dynamics:
    M(q)q̈ + C(q,q̇)q̇ + G(q) + F(q̇) = τ
Forward dynamics:
    q̈ = M⁻¹(q)[τ − C(q,q̇)q̇ − G(q) − F(q̇)]
Inverse dynamics:
    τ = M(q)q̈ + C(q,q̇)q̇ + G(q) + F(q̇)
Jacobian velocity relation:
    vₑ = J(q)q̇
External wrench mapping:
    τₑₓₜ = Jᵀ(q)Fₑₓₜ
Mechanical power:
    P = τω  or  P = Fv
CORE IDEA: Robot dynamics connects joint motion to the forces and torques that produce it. 
The central equation is M(q)q̈ + C(q,q̇)q̇ + G(q) + F(q̇) = τ, which captures inertia, velocity-dependent effects, gravity, friction, and actuator effort.