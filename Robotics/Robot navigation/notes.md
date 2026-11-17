                    ROBOT NAVIGATION
Robot navigation is the process through which a robot determines its position, identifies its destination, plans a suitable route, and moves through an environment while avoiding obstacles and responding to changes.
It combines sensing, perception, localization, mapping, path planning, and motion control to enable autonomous or semi-autonomous movement.
  Main objectives
- Determine the robot's current position and orientation.
- Identify the destination and surrounding environment.
- Construct or use maps of the environment.
- Plan collision-free paths.
- Avoid static and moving obstacles.
- Control robot movement along a planned path.
- Correct navigation errors.
- Reach destinations safely and efficiently.
  Main components of robot navigation
1. Perception: detects obstacles, landmarks, and environmental features.
2. Localization: estimates the robot's current position and orientation.
3. Mapping: represents the surrounding environment.
4. Path planning: determines a suitable route to the destination.
5. Motion planning: generates feasible robot movements along the route.
6. Obstacle avoidance: prevents collisions.
7. Motion control: executes the planned movement.
8. Feedback: monitors movement and corrects errors.
  Basic navigation cycle
Environment → Sensors → Perception → Localization → Mapping → Path planning → Motion control → Robot movement → Feedback.

 TYPES OF ROBOT NAVIGATION
  A. Manual navigation
- A human operator controls robot movement.
- Commands may be transmitted through a remote controller or computer.
- Used in teleoperated robots and hazardous environments.
  B. Semi-autonomous navigation
- The robot performs some navigation tasks independently.
- Human operators provide commands or supervision.
- Used in industrial and service robotics.
  C. Autonomous navigation
- The robot independently determines how to reach a destination.
- Uses sensors, algorithms, maps, and feedback.
- Can adapt to environmental changes.
  D. Map-based navigation
- Uses an existing map of the environment.
- Determines the robot's position relative to known landmarks or map features.
- Common in warehouses and structured environments.
  E. Mapless navigation
- Moves using immediate sensor observations without relying on a complete pre-existing map.
- Often uses reactive obstacle avoidance and learned navigation policies.
- Useful in dynamic or unfamiliar environments.

 ROBOT LOCALIZATION
Localization is the process of estimating a robot's position and orientation within an environment.
A robot's two-dimensional pose can be represented as:
    ξ = [x, y, θ]ᵀ
Where:
- x = position along the X-axis.
- y = position along the Y-axis.
- θ = orientation or heading angle.
For three-dimensional localization, a pose includes three translational and three rotational coordinates.
  Types of localization
1. Relative localization
- Estimates movement relative to a previously known position.
- Uses wheel encoders and inertial sensors.
- Errors may accumulate over time.
2. Absolute localization
- Determines position relative to an external reference.
- May use GPS/GNSS, known landmarks, or mapped features.
3. Landmark-based localization
- Identifies recognizable environmental features.
- Compares observed landmarks with known map locations.
4. Visual localization
- Uses camera images to estimate robot position and movement.
5. Range-based localization
- Uses measured distances to known reference points.
- Can use ultrasonic sensors, LiDAR, or radio-based ranging.
  Localization challenges
- Sensor noise.
- Wheel slippage.
- Changing environmental conditions.
- Poor visibility.
- Repetitive or featureless environments.
- Accumulation of measurement errors.

 ROBOT ODOMETRY
Odometry estimates robot movement using measurements from its wheels, joints, or other motion sensors.
It is commonly used in wheeled mobile robots.
  Differential-drive robot
A differential-drive robot has two independently driven wheels.
Its movement is controlled by changing the rotational velocities of the left and right wheels.
Let:
- r = wheel radius.
- ωᵣ = right wheel angular velocity.
- ωₗ = left wheel angular velocity.
- L = distance between the two wheels.
Linear velocity:
    v = r(ωᵣ + ωₗ)/2
Angular velocity:
    ω = r(ωᵣ − ωₗ)/L
Robot motion:
    ẋ = v cosθ
    ẏ = v sinθ
    θ̇ = ω
For a sufficiently small time interval Δt:
    xₖ₊₁ ≈ xₖ + v cosθ Δt
    yₖ₊₁ ≈ yₖ + v sinθ Δt
    θₖ₊₁ ≈ θₖ + ωΔt
Differential-drive movement
- Both wheels move at the same speed: robot moves straight.
- Right wheel moves faster: robot turns left.
- Left wheel moves faster: robot turns right.
- Wheels move in opposite directions at equal speeds: robot rotates about its centre.
Limitations of odometry
- Wheel slippage.
- Uneven ground.
- Incorrect wheel radius estimates.
- Incorrect wheel separation measurements.
- Encoder errors.
Odometry is useful for short-term motion estimation but should be combined with other sensors for more reliable long-term localization.

 ROBOT MAPPING
Mapping is the process of creating a representation of an environment that a robot can use for navigation.
A map helps the robot identify obstacles, free space, landmarks, and possible routes.
  Types of maps
 A. Occupancy grid map
Divides an environment into small cells.
Each cell represents the probability that a location is:
- Occupied.
- Free.
- Unknown.
Applications:
- Indoor mobile robots.
- Autonomous navigation.
- Obstacle avoidance.
 B. Metric map
Represents the environment using measurable geometric information such as distances, coordinates, and positions.
 C. Topological map
Represents an environment as connected locations and routes.
For example:
- Room A → Corridor → Room B.
- Warehouse entrance → Storage area → Loading area.
 D. Feature-based map
Uses distinctive environmental features such as corners, edges, and landmarks.
 E. Semantic map
Adds meaning to mapped objects and locations.
Examples:
- Door.
- Road.
- Table.
- Human.
- Charging station.
 Map representation
A two-dimensional occupancy grid can be represented as:
    M(x,y) ∈ {0, 1, unknown}
Where:
- 0 = free.
- 1 = occupied.
- unknown = unobserved.
Probabilistic occupancy grids use values between 0 and 1 to represent occupancy probability.

 SIMULTANEOUS LOCALIZATION AND MAPPING (SLAM)
SLAM stands for Simultaneous Localization and Mapping.
It is a technique that allows a robot to estimate its position while simultaneously constructing or updating a map of an unfamiliar environment.
  Why SLAM is important
A robot entering an unknown environment may not have access to an existing map or a reliable external positioning system.
SLAM allows it to:
- Observe its surroundings.
- Estimate movement.
- Recognize environmental features.
- Build a map.
- Correct accumulated localization errors.
SLAM process
1. Collect sensor measurements.
2. Detect environmental features.
3. Estimate robot movement.
4. Match current observations with previous observations.
5. Update the estimated robot pose.
6. Update the environmental map.
7. Detect loop closures.
8. Optimize the estimated trajectory and map.
 Types of SLAM
1. LiDAR SLAM
- Uses laser distance measurements.
- Produces geometric maps.
- Common in warehouse and industrial robots.
2. Visual SLAM
- Uses camera images.
- Extracts and tracks visual features.
- Useful in drones and mobile robots.
3. Visual-inertial SLAM
- Combines cameras and IMUs.
- Uses visual information and inertial measurements to improve motion estimation.
4. RGB-D SLAM
- Uses colour and depth information.
- Builds three-dimensional environmental representations.
  Important SLAM concepts
Pose estimation: Determines the robot's position and orientation.
Data association: Matches newly observed features with previously identified features.
Loop closure: Recognizes a previously visited location and corrects accumulated estimation errors.
Bundle adjustment: Optimizes camera poses and observed feature positions in visual SLAM.
Pose graph optimization: Optimizes a network of robot poses and spatial constraints.
  Applications
- Autonomous vehicles.
- Warehouse robots.
- Drones.
- Exploration robots.
- Indoor service robots.

 PATH PLANNING
Path planning determines a route from the robot's starting position to its destination while avoiding obstacles.
A path can be represented as a sequence of positions:
    P = {p₀, p₁, p₂, ..., pₙ}
Where:
- p₀ = starting position.
- pₙ = destination.
- Intermediate points define the route.
  Main path-planning objectives
- Minimize travel distance.
- Reduce travel time.
- Avoid collisions.
- Minimize energy consumption.
- Maintain safe clearance from obstacles.
- Respect robot movement constraints.
  Types of path planning
A. Global path planning
- Uses a map of the environment.
- Calculates a route from start to goal.
- Usually performed before or during movement.
B. Local path planning
- Uses nearby sensor information.
- Responds to immediate obstacles.
- Adjusts the robot's movement in real time.
C. Reactive path planning
- Responds directly to sensor measurements.
- Does not necessarily construct a complete global route.
- Useful in rapidly changing environments.

 PATH-PLANNING ALGORITHMS
  A. Breadth-First Search (BFS)
Explores a graph level by level.
Characteristics:
- Finds the shortest path in an unweighted graph.
- Uses a queue.
- Can be computationally expensive for large search spaces.
Applications:
- Grid-based navigation.
- Simple maze solving.
  B. Depth-First Search (DFS)
Explores one branch as deeply as possible before backtracking.
Characteristics:
- Uses a stack or recursion.
- Requires relatively little memory in some implementations.
- Does not guarantee the shortest path.
Applications:
- Maze exploration.
- Graph traversal.
  C. Dijkstra's algorithm
Finds the shortest path in a graph with non-negative edge costs.
Characteristics:
- Considers cumulative travel cost.
- Guarantees a shortest path under its standard assumptions.
- Does not use a heuristic.
- Can explore many unnecessary nodes.
Applications:
- Warehouse navigation.
- Road networks.
- Weighted grid maps.
  D. A* (A-star) algorithm
A* combines the actual cost of reaching a node with an estimated cost to the destination.
Evaluation function:
    f(n) = g(n) + h(n)
Where:
- f(n) = estimated total path cost.
- g(n) = actual cost from the start to node n.
- h(n) = heuristic estimate from n to the goal.
Common heuristics:
Manhattan distance:
    h(n) = |x₁ − x₂| + |y₁ − y₂|
Euclidean distance:
    h(n) = √[(x₁ − x₂)² + (y₁ − y₂)²]
A* finds an optimal path when the heuristic is admissible and the algorithm's graph-search implementation handles node revisiting appropriately.
Applications:
- Autonomous mobile robots.
- Indoor navigation.
- Grid-based obstacle avoidance.
  E. D* and D* Lite
Incremental heuristic search algorithms designed to efficiently update paths when the environment changes.
Applications:
- Unknown environments.
- Dynamic obstacle navigation.
- Mobile robots operating with changing maps.
  F. Rapidly-exploring Random Tree (RRT)
A sampling-based planning algorithm that explores a configuration space by extending a tree toward randomly sampled states.
Characteristics:
- Suitable for high-dimensional configuration spaces.
- Can handle complex robot geometries.
- Basic RRT does not guarantee an optimal path.
  G. RRT*
An improved version of RRT that gradually improves path quality as more samples are added.
Under appropriate conditions, it is asymptotically optimal.
Applications:
- Robotic arm motion planning.
- Complex obstacle environments.
- High-dimensional motion planning.
  H. Probabilistic Roadmap (PRM)
Builds a graph by sampling collision-free configurations and connecting nearby configurations.
Applications:
- Robot-arm motion planning.
- Repeated navigation through known environments.

 OBSTACLE DETECTION AND AVOIDANCE
Obstacle avoidance enables robots to detect and avoid objects that could interfere with movement. 
  Types of obstacles
Static obstacles
- Walls.
- Furniture.
- Fixed machinery.
- Buildings.
Dynamic obstacles
- Moving people.
- Vehicles.
- Other robots.
- Moving equipment.
  Obstacle avoidance methods
1. Reactive obstacle avoidance
The robot responds immediately to nearby obstacles using sensor measurements.
2. Potential field method
Represents the goal as an attractive force and obstacles as repulsive forces.
Attractive potential:
    U_att(q) = ½k_att||q − q_goal||²
Repulsive potential, within an influence distance:
    U_rep(q) = ½k_rep(1/d(q) − 1/d₀)²
For d(q) ≤ d₀.
The resulting virtual force is:
    F(q) = −∇U(q)
Where:
U(q) = U_att(q) + U_rep(q)
Limitations:
- Can become trapped in local minima.
- May produce oscillatory movement.
- Requires suitable parameter selection.

 Vector Field Histogram (VFH)
Uses range-sensor data to identify free movement directions and select safe steering commands.
 Dynamic Window Approach (DWA)
Evaluates possible linear and angular velocity commands within the robot's dynamically reachable velocity window.
It selects a suitable command based on factors such as:
- Distance to obstacles.
- Progress toward the goal.
- Robot speed.
- Safety and stopping distance.

 Velocity Obstacles (VO)
Identifies velocities that would lead to future collisions with moving obstacles.
Used in multi-agent and dynamic environments.

 MOTION PLANNING
Motion planning determines a feasible movement sequence that a robot can physically execute.
 It considers:
- Robot geometry.
- Joint limits.
- Velocity limits.
- Acceleration limits.
- Obstacle locations.
- Mechanical constraints.
  Path vs. trajectory
Path: Geometric route through space without specifying timing.
Trajectory: Path with time information, including position, velocity, and acceleration.
A trajectory can be represented as:
    q(t), q̇(t), q̈(t)
  Joint-space planning
Plans motion using robot joint coordinates.
 Applications:
- Robotic arms.
- Industrial manipulators.
- Joint-controlled robots.
  Cartesian-space planning
Plans movement in the robot's task space, usually the end-effector coordinate system.
 Applications:
- Welding.
- Painting.
- Assembly.
- Surface following.
  Trajectory interpolation
Common methods include:
- Linear interpolation.
- Cubic polynomial interpolation.
- Quintic polynomial interpolation.
- Spline interpolation.
A cubic trajectory:
    q(t) = a₀ + a₁t + a₂t² + a₃t³
A quintic trajectory:
    q(t) = a₀ + a₁t + a₂t² + a₃t³ + a₄t⁴ + a₅t⁵
Quintic trajectories can satisfy boundary conditions on position, velocity, and acceleration.

 ROBOT NAVIGATION CONTROL
Navigation control ensures that the robot follows a planned route and reaches its destination.
It uses feedback from sensors to compare actual movement with desired movement.
  A. Position control
Controls the robot's position relative to a desired target.
Position error:
    e(t) = x_desired(t) − x_actual(t)
  B. Velocity control
Controls the speed and direction of robot movement.
  C. PID control
A Proportional-Integral-Derivative controller uses the current error, accumulated error, and rate of change of error.
Control equation:
    u(t) = Kp e(t) + Ki∫e(t)dt + Kd de(t)/dt
Where:
- Kp = proportional gain.
- Ki = integral gain.
- Kd = derivative gain.
- e(t) = control error.
- u(t) = control output.
Proportional action: Responds to current error.
Integral action: Reduces persistent steady-state error.
Derivative action: Responds to the rate of error change and can improve damping.
  D. Pure Pursuit
A path-tracking algorithm that selects a look-ahead point on a reference path and steers the robot toward it.
Used in:
- Autonomous mobile robots.
- Autonomous vehicles.
- Agricultural robots.
  E. Model Predictive Control (MPC)
Predicts future robot behaviour using a mathematical model and optimizes control actions over a finite prediction horizon.
It can account for:
- Velocity constraints.
- Acceleration constraints.
- Obstacle avoidance.
- Path-tracking errors.
The first control action is applied, and the optimization is repeated as new measurements arrive.

12. NAVIGATION OF DIFFERENT ROBOT TYPES
  A. Wheeled mobile robots
Common configurations:
- Differential drive.
- Ackermann steering.
- Omnidirectional drive.
- Tricycle drive.
Important considerations:
- Wheel odometry.
- Steering.
- Traction.
- Turning radius.
- Wheel slippage.
  B. Legged robots
Navigate using coordinated leg movements.
Important considerations:
- Balance.
- Foot placement.
- Centre of mass.
- Ground contact.
- Dynamic stability.
  C. Aerial robots and drones
Navigate in three-dimensional space.
Common sensors:
- IMU.
- GPS/GNSS.
- Cameras.
- LiDAR.
- Barometers.
Important considerations:
- Altitude control.
- Attitude estimation.
- Three-dimensional obstacle avoidance.
- Wind disturbances.
  D. Underwater robots
Navigate in underwater environments.
Common sensors:
- Sonar.
- Doppler velocity logs.
- Pressure sensors.
- IMUs.
- Acoustic positioning systems.
Important considerations:
- Limited visibility.
- Water currents.
- Communication constraints.
- Depth control.
  E. Robotic arms
Navigate through joint or Cartesian space to reach target positions while avoiding collisions with surrounding objects.
Important considerations:
- Inverse kinematics.
- Joint limits.
- Collision detection.
- Workspace constraints.

 GLOBAL AND LOCAL NAVIGATION ARCHITECTURE
Modern autonomous robots commonly use a hierarchical navigation architecture.
  Global planner
- Uses a map.
- Calculates an overall route.
- Selects a path toward the destination.
Examples: A*, Dijkstra, D* Lite.
  Local planner
- Examines nearby obstacles.
- Adjusts movement in response to local conditions.
- Produces feasible short-term motion commands.
Examples: DWA, TEB, MPC.
  Low-level controller
- Converts motion commands into motor or actuator commands.
- Controls wheel speeds, steering, or joint movements.
Typical architecture
Goal specification → Global path planner → Local motion planner → Motion controller → Actuators.
Sensor feedback → Localization and mapping → Updated environment information → Planner.
This architecture separates long-range route planning from immediate movement control.

 NAVIGATION PERFORMANCE METRICS
Robot navigation systems are evaluated using several performance measures.
1. Path length
Total distance travelled along a path.
    L = Σ||pᵢ₊₁ − pᵢ||
2. Navigation time
Time required to reach the destination.
3. Path efficiency
Compares the actual route length with a reference shortest-path length.
    Efficiency = (Reference path length / Actual path length) × 100%
4. Localization error
Difference between estimated and actual position.
    e_p = √[(x_est − x_true)² + (y_est − y_true)²]
5. Collision rate
Frequency of collisions during navigation.
6. Success rate
Percentage of navigation attempts that reach their goals successfully.
7. Energy consumption
Energy used during navigation.
8. Clearance
Distance maintained between the robot and nearby obstacles.

 PRACTICAL APPLICATIONS OF ROBOT NAVIGATION
Industrial robots
- Movement between production stations.
- Automated material handling.
- Warehouse transportation.
Autonomous vehicles
- Road navigation.
- Lane following.
- Obstacle avoidance.
- Route planning.
Agricultural robots
- Autonomous field movement.
- Crop-row navigation.
- Precision spraying and harvesting.
Drones
- Autonomous flight.
- Waypoint navigation.
- Aerial mapping.
- Search and rescue.
Service robots
- Indoor navigation.
- Delivery operations.
- Human-aware movement.
Exploration robots
- Navigation through unknown environments.
- Planetary exploration.
- Underground and underwater inspection.

 PRACTICAL IMPLEMENTATION TOOLS
Robot Operating System (ROS 2)
ROS 2 is a robotics software framework that provides communication, libraries, tools, and packages for developing robotic applications.
  Important navigation-related components include:
- Nav2: navigation framework for ROS 2 mobile robots.
- TF2: manages coordinate transformations between reference frames.
- RViz: visualizes robot models, maps, sensor data, and navigation paths.
- Gazebo: simulates robots and environments.
- SLAM Toolbox: provides 2D SLAM functionality.
- AMCL: Adaptive Monte Carlo Localization for localization on a known 2D map.
  Common programming tools
- Python.
- C++.
- OpenCV.
- PCL (Point Cloud Library).
- NumPy.
- MATLAB and Simulink.
  Simulation platforms
- Gazebo.
- Webots.
- CoppeliaSim.
- NVIDIA Isaac Sim.
- MATLAB Robotics System Toolbox.

 IMPORTANT ENGINEERING AND EXAM TIPS
1. Distinguish localization, mapping, path planning, and motion control.
2. Understand the difference between a path and a trajectory.
3. Know how differential-drive robots move and turn.
4. Remember that odometry errors accumulate over time.
5. Understand the role of SLAM in unknown environments.
6. Know the differences between global and local path planning.
7. Understand the evaluation function of A*: f(n) = g(n) + h(n).
8. Remember that Dijkstra's algorithm requires non-negative edge costs.
9. Understand that basic RRT is not guaranteed to find an optimal path.
10. Consider robot dimensions when checking whether a path is collision-free.
11. Account for dynamic obstacles, not only stationary objects.
12. Consider acceleration, braking distance, and turning constraints when planning motion.
13. Combine multiple sensors for improved localization.
14. Use feedback control to correct deviations from the planned path.
15. Test navigation algorithms in simulation before deploying them on physical robots.
16. Consider computational resources and real-time processing requirements.
17. Always account for uncertainty in sensor measurements and localization.

 KEY FORMULA SUMMARY
Robot pose
    ξ = [x, y, θ]ᵀ
Differential-drive robot
Linear velocity:
    v = r(ωᵣ + ωₗ)/2
Angular velocity:
    ω = r(ωᵣ − ωₗ)/L
Robot motion:
    ẋ = v cosθ
    ẏ = v sinθ
    θ̇ = ω
Localization error
    e_p = √[(x_est − x_true)² + (y_est − y_true)²]
A* algorithm
    f(n) = g(n) + h(n)
Manhattan distance:
    h(n) = |x₁ − x₂| + |y₁ − y₂|
Euclidean distance:
    h(n) = √[(x₁ − x₂)² + (y₁ − y₂)²]
Potential field method
    U_att(q) = ½k_att||q − q_goal||²
    U_rep(q) = ½k_rep(1/d(q) − 1/d₀)²
    F(q) = −∇U(q)
PID control
    u(t) = Kp e(t) + Ki∫e(t)dt + Kd de(t)/dt
Path length
    L = Σ||pᵢ₊₁ − pᵢ||
Path efficiency
    Efficiency = (Reference path length / Actual path length) × 100%
Position error
    e_p = √[(x_est − x_true)² + (y_est − y_true)²]

CORE IDEA
Robot navigation enables a robot to move intelligently from one location to another.
  Its central processes are:
1. Localization: Where am I?
2. Mapping: What does my environment look like?
3. Path planning: Which route should I take?
4. Obstacle avoidance: How do I avoid collisions?
5. Motion control: How do I execute the route?
6. Feedback: Am I moving as intended?
The combination of these processes enables robots to navigate structured, dynamic, and previously unknown environments autonomously.