            ROBOT KINEMATICS
Robot kinematics is the branch of robotics that studies the motion of robots without considering the forces and torques responsible for producing that motion.
It describes the relationship between the positions, orientations, velocities, and accelerations of robot links and joints.
Kinematics is essential for determining where a robot's end effector is located, how it moves, and how its joints must move to achieve a desired position or trajectory.
  Main objectives;
- Determine the position and orientation of robot links.
- Calculate the position and orientation of the end effector.
- Establish relationships between joint variables and end-effector motion.
- Determine joint angles or displacements required to reach a target.
- Calculate joint and end-effector velocities and accelerations.
- Analyze robot workspace and movement limitations.
- Support trajectory planning and motion control.
  Kinematics vs. dynamics;
- Kinematics: studies motion without considering forces and torques.
- Dynamics: studies the relationship between motion, forces, torques, and mass.
  Two major branches;
1. Forward kinematics.
2. Inverse kinematics.

 BASIC KINEMATIC CONCEPTS
A. Position;
Position describes the location of a point relative to a reference coordinate frame.
In three-dimensional Cartesian coordinates:
    P = [x, y, z]ᵀ
Where x, y, and z represent distances along the three coordinate axes.
B. Orientation;
Orientation describes the rotational alignment of a robot link or end effector.
Common representations include:
- Euler angles.
- Rotation matrices.
- Quaternions.
- Axis-angle representation.
C. Configuration;
A robot configuration describes the complete arrangement of its joints.
For a robot with n joints:
    q = [q₁, q₂, ..., qₙ]ᵀ
Joint variables may represent:
- Angular displacement for revolute joints.
- Linear displacement for prismatic joints.
D. Trajectory;
A trajectory describes the path and timing of robot movement.
It specifies how robot position, orientation, or joint variables change over time.
E. Degrees of freedom (DOF);
The number of independent variables required to describe a robot's configuration.
A free rigid body in 3D space has six degrees of freedom:
- Three translational: X, Y, Z.
- Three rotational: roll, pitch, yaw.
A robot's actual mobility depends on its joint arrangement and mechanical constraints.

 COORDINATE SYSTEMS IN ROBOTICS
Coordinate systems provide reference frames for describing the positions and orientations of robot components.
A. Cartesian coordinate system;
Uses three perpendicular axes:
- X-axis: horizontal direction.
- Y-axis: lateral direction.
- Z-axis: vertical direction.
A point is represented as:
    P = [x, y, z]ᵀ
B. Joint coordinate system;
Describes robot configuration using joint variables.
For example:
    q = [θ₁, θ₂, d₃]ᵀ
This represents two revolute joints and one prismatic joint.
C. Base coordinate frame;
A reference frame fixed to the robot's base.
It provides the primary reference for calculating the position of robot links and the end effector.
D. Link coordinate frame;
A coordinate system attached to an individual robot link.
It helps describe the position and orientation of neighboring links.
E. End-effector coordinate frame;
A coordinate system attached to the robot's tool or end effector.
It is useful for describing the position and orientation required to perform a task.
F. World coordinate frame;
A global reference frame used to describe the robot relative to its environment.

 TYPES OF ROBOT JOINTS
Joint types determine the possible relative movements between robot links.
1. Revolute joint (R)
- Allows rotation about a fixed axis.
- Joint variable: θ.
- Unit: radians or degrees.
2. Prismatic joint (P)
- Allows linear translation along an axis.
- Joint variable: d.
- Unit: metres or millimetres.
3. Cylindrical joint (C)
- Allows rotation and translation along the same axis.
- Two degrees of freedom.
4. Spherical joint (S)
- Allows three rotational degrees of freedom about a common point.
5. Helical joint
- Combines rotation and translation through a screw relationship.
- Has one degree of freedom because the two motions are coupled.

 FORWARD KINEMATICS (FK)
Forward kinematics determines the position and orientation of a robot's end effector from known joint variables.
It answers:
"Given the joint angles or displacements, where is the end effector?"
  General procedure
1. Identify the robot's joint types.
2. Assign coordinate frames to the links.
3. Determine the geometric parameters.
4. Construct the transformation matrix for each joint.
5. Multiply the transformations in sequence.
6. Extract the final end-effector position and orientation.
Example: Two-link planar robot arm
Consider a two-link robot arm moving in a horizontal plane.
Parameters:
- L₁ = length of link 1.
- L₂ = length of link 2.
- θ₁ = angle of joint 1.
- θ₂ = relative angle of joint 2.
<pre>       End effector (x,y)
              *
             /
         L₂ /
           /
          * Joint 2
         /
     L₁ /
       /
      O  Base
</pre>The end-effector coordinates are:
Horizontal position:
    x = L₁cosθ₁ + L₂cos(θ₁ + θ₂)
Vertical position:
    y = L₁sinθ₁ + L₂sin(θ₁ + θ₂)
The end-effector orientation is:
    φ = θ₁ + θ₂
These equations are fundamental in planar robot-arm analysis.

 HOMOGENEOUS TRANSFORMATION MATRICES
Homogeneous transformations combine rotation and translation into a single matrix operation.
They are widely used to describe the position and orientation of robot links relative to one another.
A. Rotation matrix in 2D
    R(θ) =[ cosθ  -sinθ ]
          [ sinθ   cosθ ]
B. Rotation matrices in 3D
Rotation about X-axis:
    Rx(θ) =[ 1      0       0    ]
           [ 0    cosθ   -sinθ   ]
           [ 0    sinθ    cosθ   ]
Rotation about Y-axis:
    Ry(θ) =[ cosθ    0    sinθ  ]
          [ 0       1     0    ]
          [ -sinθ   0    cosθ  ]
Rotation about Z-axis:
    Rz(θ) =[ cosθ  -sinθ   0 ]
           [ sinθ   cosθ   0 ]
           [ 0       0     1 ]
Rotation matrices must be used with a consistent coordinate-frame and multiplication convention.
C. Homogeneous transformation matrix
A general rigid-body transformation is:
    T =[ R₃ₓ₃   p₃ₓ₁ ]
       [ 0 0 0    1  ]
Where:
- R = 3 × 3 rotation matrix.
- p = 3 × 1 translation vector.
- T = 4 × 4 homogeneous transformation matrix.
In expanded form:
    T =[ r₁₁ r₁₂ r₁₃ x ]
       [ r₂₁ r₂₂ r₂₃ y ]
       [ r₃₁ r₃₂ r₃₃ z ]    
       [  0   0   0  1 ]
D. Transformation of a point
A point in homogeneous coordinates is:
    P = [x, y, z, 1]ᵀ
Its transformed coordinates are:
    P' = TP
E. Combining transformations
For a serial robot with multiple links:
    ⁰Tₙ = ⁰T₁ × ¹T₂ × ²T₃ × ... × ⁿ⁻¹Tₙ
This gives the end-effector pose relative to the robot base.
The order of multiplication matters.

 DENAVIT–HARTENBERG (D-H) PARAMETERS
The Denavit–Hartenberg convention is a systematic method for assigning coordinate frames and describing the geometry of serial robot manipulators.
It reduces the complexity of deriving transformation matrices.
  Four D-H parameters;
1. Link length (aᵢ)
- Distance between consecutive joint axes measured along the common normal.
- Unit: metres.
2. Link twist (αᵢ)
- Angle between consecutive joint axes measured about the common normal.
- Unit: radians or degrees.
3. Link offset (dᵢ)
- Distance along the joint axis.
- For a revolute joint, this is usually constant.
4. Joint angle (θᵢ)
- Rotation about the joint axis.
- For a prismatic joint, this is usually constant.
For the standard D-H convention, the transformation matrix is:
    Aᵢ =[ cosθᵢ  -sinθᵢcosαᵢ   sinθᵢsinαᵢ   aᵢcosθᵢ ]
        [ sinθᵢ   cosθᵢcosαᵢ  -cosθᵢsinαᵢ   aᵢsinθᵢ ]
        [ 0        sinαᵢ        cosαᵢ        dᵢ       ]
        [ 0        0             0            1       ]
The complete transformation is:
    ⁰Tₙ = A₁A₂A₃...Aₙ
  D-H procedure;
1. Identify all joint axes.
2. Assign the Z-axis along each joint axis.
3. Identify common normals between successive joint axes.
4. Assign X- and Y-axes consistently.
5. Determine aᵢ, αᵢ, dᵢ, and θᵢ.
6. Construct each transformation matrix.
7. Multiply the matrices to obtain the end-effector pose.
Important: 
There are standard and modified D-H conventions. Their frame assignments and transformation matrices differ. 
Do not mix their parameter tables and formulas.

 INVERSE KINEMATICS (IK)
Inverse kinematics determines the joint variables required to place a robot's end effector at a specified position and orientation.
It answers:
"Given the desired end-effector position and orientation, what joint angles or displacements are required?"
  General procedure;
1. Specify the desired end-effector position and orientation.
2. Establish the robot's geometric equations.
3. Form the inverse kinematic equations.
4. Solve for the unknown joint variables.
5. Check joint limits and mechanical constraints.
6. Select a feasible solution.
Example: Two-link planar robot arm
Forward kinematics:
    x = L₁cosθ₁ + L₂cos(θ₁ + θ₂)
    y = L₁sinθ₁ + L₂sin(θ₁ + θ₂)
First calculate θ₂:
    cosθ₂ = (x² + y² − L₁² − L₂²)/(2L₁L₂)
Therefore:
    θ₂ = ±cos⁻¹[(x² + y² − L₁² − L₂²)/(2L₁L₂)]
Next calculate θ₁:
    θ₁ = atan2(y,x) − atan2(L₂sinθ₂, L₁ + L₂cosθ₂)
The ± sign generally produces two configurations:
- Elbow-up configuration.
- Elbow-down configuration.
  Important IK characteristics;
Multiple solutions: A target may be reached through different joint configurations.
No solution: A target may lie outside the robot's reachable workspace or violate joint constraints.
Singular configurations: Certain joint arrangements cause loss of independent end-effector motion directions.
Redundancy: A robot with more independent joints than required for a specified task may have multiple solutions even after satisfying the target pose.

 ROBOT VELOCITY KINEMATICS
Velocity kinematics studies the relationship between joint velocities and end-effector velocities.
  Joint velocity;
For joint coordinate q:
    q̇ = dq/dt
  End-effector velocity;
The end-effector velocity is related to joint velocity through the Jacobian matrix.
    v = J(q)q̇
Where:
- v = end-effector velocity or twist.
- J(q) = Jacobian matrix.
- q̇ = joint velocity vector.
For a spatial robot, the end-effector twist typically contains three linear and three angular velocity components.
Example: Two-link planar robot
From:
    x = L₁cosθ₁ + L₂cos(θ₁ + θ₂)
    y = L₁sinθ₁ + L₂sin(θ₁ + θ₂)
Differentiate with respect to time:
    ẋ = −L₁sinθ₁ θ̇₁ − L₂sin(θ₁ + θ₂)(θ̇₁ + θ̇₂)
    ẏ = L₁cosθ₁ θ̇₁ + L₂cos(θ₁ + θ₂)(θ̇₁ + θ̇₂)
The Jacobian is:
    J =[ −L₁sinθ₁ − L₂sin(θ₁+θ₂)   −L₂sin(θ₁+θ₂) ]
       [  L₁cosθ₁ + L₂cos(θ₁+θ₂)    L₂cos(θ₁+θ₂) ]
Therefore:
    [ẋ]       [θ̇₁]
    [ẏ] = J  [θ̇₂]
The Jacobian is useful for calculating the joint speeds required to produce a desired end-effector velocity.

 ROBOT JACOBIAN MATRIX
The Jacobian describes how changes in joint variables affect end-effector motion.
General relationship:
    ẋ = J(q)q̇
For a square, nonsingular Jacobian:
    q̇ = J⁻¹(q)ẋ
For non-square or singular Jacobians, a suitable pseudoinverse or numerical method may be required.
 Applications;
- End-effector velocity control.
- Joint velocity calculation.
- Force and torque mapping.
- Singularity analysis.
- Motion planning.
- Robot manipulation.
  Jacobian and force relationship;
The relationship between end-effector wrench and joint torque is:
    τ = JᵀF
Where:
- τ = joint torque vector.
- Jᵀ = transpose of the Jacobian.
- F = end-effector wrench.
The wrench and Jacobian must use compatible coordinate frames and conventions.

 ROBOT ACCELERATION KINEMATICS
Acceleration kinematics studies the relationship between joint accelerations and end-effector accelerations.
Starting with:
    ẋ = J(q)q̇
Differentiate with respect to time:
    ẍ = J(q)q̈ + J̇(q)q̇
Where:
- ẍ = end-effector acceleration.
- q̈ = joint acceleration.
- J̇ = time derivative of the Jacobian.
This equation is important for high-speed robot movement and smooth trajectory execution.
It accounts for both joint acceleration and changes in the Jacobian as the robot moves.

 ROBOT WORKSPACE
Workspace is the region in space that a robot's end effector can reach.
  Types of workspace;
1. Reachable workspace
- All points the end effector can reach in at least one feasible configuration.
2. Dexterous workspace
- Region where the end effector can achieve all required orientations, according to the robot's orientation constraints.
3. Restricted workspace
- Region limited by joint limits, physical obstructions, and mechanical constraints.
Workspace of a two-link planar robot
For link lengths L₁ and L₂:
Maximum reach:
    R_max = L₁ + L₂
Minimum radial reach:
    R_min = |L₁ − L₂|
For unrestricted full rotation of both joints, the reachable workspace is an annular region:
    |L₁ − L₂| ≤ √(x² + y²) ≤ L₁ + L₂
Actual workspace may be smaller because of joint limits and collisions.
  Factors affecting workspace;
- Number of joints.
- Link lengths.
- Joint types.
- Joint limits.
- Robot configuration.
- Physical interference and obstacles.

 ROBOT SINGULARITIES
A singularity is a robot configuration in which the Jacobian loses rank.
At a singularity, the robot loses the ability to produce certain instantaneous end-effector motion directions.
For a square Jacobian, a singularity occurs when:
    det(J) = 0
For a non-square Jacobian, rank deficiency is the more general condition.
  Types of singularities;
1. Boundary singularity
- Occurs near the limits of the robot's workspace.
2. Internal singularity
- Occurs within the workspace due to a particular arrangement of robot joints.
Effects;
- Loss of one or more independent motion directions.
- Large joint velocities may be required for certain end-effector velocities.
- Reduced controllability in affected directions.
- Increased difficulty in motion planning.
  Singularity avoidance;
- Avoid problematic joint configurations.
- Use redundancy where available.
- Apply damped least-squares inverse kinematics.
- Plan trajectories that maintain adequate distance from singular configurations.

 TRAJECTORY PLANNING
Trajectory planning determines how a robot moves from an initial configuration to a target configuration over time.
It considers position, velocity, acceleration, and sometimes jerk.
A. Joint-space trajectory planning;
Motion is planned directly using joint coordinates.
q(t) describes the movement of each joint over time.
Advantages:
- Convenient for joint control.
- Easy to respect joint limits.
- Often computationally efficient.
B. Cartesian-space trajectory planning;
Motion is planned in the end-effector coordinate space.
x(t) describes the desired end-effector path.
Advantages:
- Useful for straight-line tool motion.
- Suitable for welding, painting, and precision assembly.
C. Cubic polynomial trajectory;
A cubic polynomial is commonly used to connect initial and final positions with specified velocities.
    q(t) = a₀ + a₁t + a₂t² + a₃t³
Velocity:
    q̇(t) = a₁ + 2a₂t + 3a₃t²
Acceleration:
    q̈(t) = 2a₂ + 6a₃t
The four coefficients are determined using four boundary conditions, typically initial and final positions and velocities.
D. Quintic polynomial trajectory;
A fifth-order polynomial can satisfy six boundary conditions, usually:
- Initial position.
- Final position.
- Initial velocity.
- Final velocity.
- Initial acceleration.
- Final acceleration.
    q(t) = a₀ + a₁t + a₂t² + a₃t³ + a₄t⁴ + a₅t⁵
It is useful when smooth acceleration transitions are required.

 ROBOT MOTION REPRESENTATIONS
Cartesian representation;
Describes movement along X, Y, and Z axes.
Joint-space representation;
Describes motion using joint angles and displacements.
Polar representation;
Uses radial distance and angular coordinates.
Cylindrical representation;
Uses radial, angular, and vertical coordinates.
Spherical representation;
Uses radial distance and two angular coordinates.
The choice of representation depends on robot geometry, the task, and the motion-planning requirements.

 PRACTICAL APPLICATIONS OF ROBOT KINEMATICS
Industrial robotic arms;
- Calculating end-effector positions.
- Performing assembly and welding.
- Positioning tools accurately.
Mobile robots;
- Calculating wheel motion.
- Estimating robot position and orientation.
- Planning movement paths.
Humanoid robots;
- Calculating limb positions.
- Coordinating arm and leg movements.
- Supporting walking and balance control.
Robotic surgery;
- Precise tool positioning.
- Controlled movement within restricted workspaces.
Autonomous robots;
- Navigation.
- Obstacle avoidance.
- Path tracking.
Robotic manufacturing;
- Tool-path generation.
- Automated material handling.
- Repetitive positioning operations.

 IMPORTANT ENGINEERING AND EXAM TIPS
1. Clearly identify all joint variables before solving a kinematics problem.
2. Distinguish absolute joint angles from relative joint angles.
3. Draw a clear robot diagram and label link lengths and joint axes.
4. Use consistent coordinate frames and transformation conventions.
5. Remember that revolute joints use angular variables while prismatic joints use linear variables.
6. Use forward kinematics when joint variables are known.
7. Use inverse kinematics when the desired end-effector pose is known.
8. Check whether the target position lies within the robot's reachable workspace.
9. Remember that inverse kinematics may have multiple solutions or no feasible solution.
10. Use atan2(y,x) rather than a basic inverse tangent when calculating angles to preserve quadrant information.
11. Check whether angles are in degrees or radians before evaluating trigonometric functions.
12. Pay attention to transformation multiplication order.
13. Differentiate position equations carefully when deriving velocity equations.
14. Check the Jacobian for singularities before attempting inverse velocity calculations.
15. Verify results by substituting calculated joint variables back into the forward kinematics equations.

 KEY FORMULA SUMMARY
Position and orientation;
- Position: P = [x, y, z]ᵀ
- Configuration: q = [q₁, q₂, ..., qₙ]ᵀ
Two-link planar forward kinematics;
- x = L₁cosθ₁ + L₂cos(θ₁ + θ₂)
- y = L₁sinθ₁ + L₂sin(θ₁ + θ₂)
- φ = θ₁ + θ₂
Two-link planar inverse kinematics;
- cosθ₂ = (x² + y² − L₁² − L₂²)/(2L₁L₂)
- θ₂ = ±cos⁻¹[(x² + y² − L₁² − L₂²)/(2L₁L₂)]
- θ₁ = atan2(y,x) − atan2(L₂sinθ₂,L₁ + L₂cosθ₂)
Homogeneous transformation;
- P' = TP
- ⁰Tₙ = ⁰T₁ × ¹T₂ × ... × ⁿ⁻¹Tₙ
Velocity kinematics;
- q̇ = dq/dt
- ẋ = J(q)q̇
Acceleration kinematics;
- ẍ = J(q)q̈ + J̇(q)q̇
Jacobian force relationship;
- τ = JᵀF
Workspace;
- R_max = L₁ + L₂
- R_min = |L₁ − L₂|
Singularity;
- det(J) = 0 (for a square Jacobian)
Trajectory planning;
- Cubic: q(t) = a₀ + a₁t + a₂t² + a₃t³
- Quintic: q(t) = a₀ + a₁t + a₂t² + a₃t³ + a₄t⁴ + a₅t⁵

CORE IDEA
Robot kinematics establishes the mathematical relationship between joint movements and the position, orientation, velocity, and acceleration of a robot's end effector.
The two fundamental problems are:
- Forward kinematics: joint variables → end-effector pose.
- Inverse kinematics: desired end-effector pose → joint variables.
Transformation matrices describe link positions and orientations, while the Jacobian relates joint motion to end-effector velocity and force.