                ENGINEERING MODELLING
Engineering modelling is the process of representing real-world engineering systems, physical processes and phenomena using mathematical equations, logical relationships, computational algorithms or simulations.
It simplifies complex real-world systems into manageable representations that can be analysed, predicted, optimised and controlled.
PURPOSES:
- Understand how engineering systems behave.
- Predict system performance under different conditions.
- Analyse physical processes without conducting expensive experiments.
- Design and optimise engineering systems.
- Identify system limitations and failure conditions.
- Simulate real-world engineering scenarios.
- Support decision-making and engineering design.

KEY CONCEPTS:
 Physical system:
The actual engineering object or process being studied.
 Mathematical model:
A mathematical representation of the physical system using equations, functions and relationships.
 Variables:
Quantities that can change within a model.
 Parameters:
Fixed or specified quantities that characterise a model.
 Inputs:
External signals or quantities applied to a system.
 Outputs:
The resulting responses of a system.
 Assumptions:
Simplifications introduced to make a problem mathematically manageable.
 Constraints:
Conditions or limitations that a model must satisfy.
 Initial conditions:
Values of system variables at the starting time.
 Boundary conditions:
Conditions imposed at the boundaries of a physical domain.

TYPES OF ENGINEERING MODELS
 PHYSICAL MODELS;
Physical representations of actual systems, often constructed at a different scale.
Examples:
- Scale models of bridges.
- Wind tunnel aircraft models.
- Prototype machines.
- Hydraulic system models.
 MATHEMATICAL MODELS;
Represent systems using mathematical relationships.
Examples:
- Differential equations describing motion.
- Equations describing electrical circuits.
- Mathematical models of heat transfer.
- Structural stress equations.
 COMPUTATIONAL MODELS;
Use computer algorithms to represent and analyse engineering systems.
Examples:
- Finite element simulations.
- Computational fluid dynamics.
- Numerical circuit simulations.
- Robot motion simulations.
 EMPIRICAL MODELS;
Developed using experimental observations and measured data rather than entirely from theoretical physical laws.
Examples:
- Predicting material strength from test data.
- Estimating motor efficiency from measurements.
- Modelling temperature variation using experimental data.
 CONCEPTUAL MODELS;
Describe system components, relationships and operations without necessarily using detailed mathematical equations.
Examples:
- Block diagrams.
- Flowcharts.
- System architecture diagrams.
- Process flow diagrams.

MODELLING PROCESS AND METHODOLOGY
Engineering modelling follows a systematic process.
 PROBLEM DEFINITION;
Clearly identify:
- The engineering problem.
- The system to be studied.
- The objectives of modelling.
- The required outputs.
 SYSTEM IDENTIFICATION;
Identify:
- System components.
- Inputs and outputs.
- Internal variables.
- System boundaries.
- Interactions between components.
 ASSUMPTIONS AND SIMPLIFICATION;
Introduce reasonable assumptions to simplify the physical problem.
Examples:
- Neglecting air resistance.
- Assuming constant temperature.
- Treating a body as a rigid object.
- Assuming ideal electrical components.
- Assuming uniform material properties.
 MATHEMATICAL FORMULATION;
Translate physical relationships into mathematical equations.
Common governing principles:
- Newton's laws of motion.
- Conservation of mass.
- Conservation of energy.
- Conservation of momentum.
- Kirchhoff's circuit laws.
- Thermodynamic laws.
- Constitutive material relationships.
 SOLUTION;
Solve the resulting mathematical model using:
- Analytical methods.
- Numerical methods.
- Computational algorithms.
 SIMULATION;
Use computational tools to investigate system behaviour under different conditions.
 VERIFICATION
Check whether the mathematical equations and computational implementation are correct.
 VALIDATION;
Compare model predictions with actual experimental measurements or trusted real-world observations.
 REFINEMENT;
Improve the model by correcting assumptions, equations, parameters or computational methods.
 INTERPRETATION;
Analyse the results and determine their engineering significance.

FUNDAMENTAL MATHEMATICAL REPRESENTATIONS
Engineering systems can be represented using different mathematical structures.
 ALGEBRAIC EQUATIONS;
Represent relationships between variables without derivatives.
Example:
    F = ma
    V = IR
    P = VI
Applications:
- Static force calculations.
- Electrical circuit analysis.
- Basic engineering design.
 DIFFERENTIAL EQUATIONS;
Represent systems involving rates of change.
Ordinary differential equation (ODE):
    dy/dt = f(t,y)
Second-order example:
    m(d²x/dt²) + c(dx/dt) + kx = F(t)
Applications:
- Mechanical vibrations.
- Electrical circuit dynamics.
- Thermal systems.
- Motion modelling.
 PARTIAL DIFFERENTIAL EQUATIONS;
Describe systems involving multiple independent variables.
Examples:
Heat equation:
    ∂T/∂t = α∇²T
Wave equation:
    ∂²u/∂t² = c²∇²u
Applications:
- Heat conduction.
- Fluid flow.
- Electromagnetic fields.
- Structural deformation.
 MATRIX EQUATIONS;
Represent interconnected systems and multiple equations.
    AX = B
Applications:
- Structural analysis.
- Electrical networks.
- Robotics.
- Control systems.
 INTEGRAL EQUATIONS;
Represent relationships involving accumulated quantities or distributed effects.
General form:
    f(x) = g(x) + λ∫a^b K(x,t)f(t)dt
Applications:
- Potential theory.
- Heat transfer.
- Electromagnetic modelling.
- Boundary value problems.

DIMENSIONAL ANALYSIS AND SIMILARITY
Dimensional analysis examines the physical dimensions of variables and equations.
It helps verify equations, simplify models and establish relationships between physical quantities.
 FUNDAMENTAL SI DIMENSIONS:
Length = L
Mass = M
Time = T
Electric current = I
Temperature = Θ
Amount of substance = N
Luminous intensity = J
  EXAMPLES:
Velocity:
[v] = LT⁻¹
Acceleration:
[a] = LT⁻²
Force:
[F] = MLT⁻²
Energy:
[E] = ML²T⁻²
Pressure:
[P] = ML⁻¹T⁻²
POWER:
[P] = ML²T⁻³
 DIMENSIONAL HOMOGENEITY;
Every term in a physically meaningful equation must have compatible dimensions.
Example:
    s = ut + ½at²
Dimensions:
    [s] = L
    [ut] = (LT⁻¹)(T) = L
    [at²] = (LT⁻²)(T²) = L
Therefore, the equation is dimensionally consistent.
BUCKINGHAM PI THEOREM;
A dimensional relationship involving n variables and k independent fundamental dimensions can be expressed using:
    n-k
independent dimensionless groups (π terms), assuming the required dimensional independence conditions are satisfied.
IMPORTANT DIMENSIONLESS NUMBERS;
Reynolds number:
    Re = ρvL/μ
Froude number:
    Fr = v/√(gL)
Mach number:
    Ma = v/c
Prandtl number:
    Pr = μcp/k
Where:
ρ = density
v = velocity
L = characteristic length
μ = dynamic viscosity
g = gravitational acceleration
c = speed of sound
cp = specific heat capacity
k = thermal conductivity
APPLICATIONS:
- Fluid mechanics.
- Aerodynamics.
- Heat transfer.
- Hydraulic engineering.
- Scale-model testing.

MECHANICAL SYSTEM MODELLING
Mechanical modelling describes the motion, forces, energy and dynamic behaviour of mechanical systems.
 NEWTON'S SECOND LAW;
    ΣF = ma
Where:
F = resultant force
m = mass
a = acceleration
 ROTATIONAL MOTION;
    Στ = Iα
Where:
τ = torque
I = moment of inertia
α = angular acceleration
 MASS-SPRING-DAMPER MODEL;
A common mechanical dynamic model is:
    m(d²x/dt²) + c(dx/dt) + kx = F(t)
Where:
m = mass
c = damping coefficient
k = spring stiffness
x = displacement
F(t) = external force.
Natural angular frequency (undamped):
    ωn = √(k/m)
Natural frequency:
    fn = ωn/(2π)
Damping ratio:
    ζ = c/(2√(mk))
System classification:
Underdamped:
    0 < ζ < 1
Critically damped:
    ζ = 1
Overdamped: 
    ζ > 1
Undamped:
    ζ = 0
APPLICATIONS:
- Vehicle suspension systems.
- Building vibration analysis.
- Machine dynamics.
- Robotic joints.
- Mechanical shock absorbers.

ELECTRICAL AND ELECTRONIC SYSTEM MODELLING
Electrical modelling represents voltage, current, resistance, capacitance, inductance and their dynamic relationships.
 OHM'S LAW
    V = IR
 KIRCHHOFF'S LAWS
Kirchhoff's Current Law (KCL):
    ΣIin = ΣIout
Kirchhoff's Voltage Law (KVL):
    ΣV = 0
 RC CIRCUIT MODEL
For a series RC circuit:
    RC(dV_C/dt) + V_C = V_in
Time constant:
    τ = RC
 RL CIRCUIT MODEL
For a series RL circuit:
    L(di/dt) + Ri = V_in
Time constant:
    τ = L/R
 RLC CIRCUIT MODEL
For a series RLC circuit:
    L(d²q/dt²) + R(dq/dt) + q/C = V(t)
Where:
L = inductance
R = resistance
C = capacitance
q = electrical charge.
APPLICATIONS:
- Electronic circuit design.
- Filter modelling.
- Power systems.
- Motor control.
- Semiconductor circuit analysis.
- Embedded electronics.

THERMAL SYSTEM MODELLING
Thermal modelling describes heat transfer, temperature distribution and energy exchange.
THREE MODES OF HEAT TRANSFER:
 CONDUCTION;
Fourier's law:
    Q̇ = -kA(dT/dx)
Where:
Q̇ = heat transfer rate
k = thermal conductivity
A = cross-sectional area.
 CONVECTION;
Newton's law of cooling:
    Q̇ = hA(Ts-T∞)
Where:
h = convection heat transfer coefficient
Ts = surface temperature
T∞ = surrounding fluid temperature.
 RADIATION;
Stefan-Boltzmann law:
    Q̇ = εσA(Ts⁴-Tsur⁴)
Where:
ε = emissivity
σ = Stefan-Boltzmann constant.
 THERMAL ENERGY BALANCE;
Rate of energy accumulation:
    Heat input - Heat output = Rate of energy storage
For a lumped thermal system:
    ρVc_p(dT/dt) = Q̇in - Q̇out
Applications:
- Engine cooling.
- Refrigeration systems.
- Electronic device thermal management.
- Industrial furnaces.
- Building temperature control.

 FLUID SYSTEM MODELLING
Fluid modelling describes the behaviour of liquids and gases in motion or at rest.
 CONTINUITY EQUATION;
Conservation of mass:
    ρ1A1v1 = ρ2A2v2
For incompressible steady flow:
    A1v1 = A2v2
 BERNOULLI'S EQUATION;
    P + ½ρv² + ρgh = constant
For ideal steady incompressible flow along a streamline.
 NAVIER-STOKES EQUATION;
A general momentum equation for fluid motion:
    ρ(∂v/∂t + v·∇v)= -∇p + μ∇²v + ρg
For an incompressible Newtonian fluid with constant viscosity.
 PRESSURE AND FLOW RELATIONSHIPS;
Hydrostatic pressure:
    P = ρgh
Volumetric flow rate:
    Q = Av
APPLICATIONS:
- Hydraulic systems.
- Pipe networks.
- Pumps and turbines.
- Aerodynamics.
- Computational fluid dynamics.
- Water distribution systems.

STATE-SPACE MODELLING
State-space modelling represents dynamic systems using a set of first-order differential equations.
It is widely used in control engineering, robotics and electrical and mechanical system analysis.
GENERAL FORM:
    ẋ = Ax + Bu
    y = Cx + Du
Where:
x = state vector
u = input vector
y = output vector
A = system matrix
B = input matrix
C = output matrix
D = direct transmission matrix
 STATE VARIABLES;
Variables that describe the internal condition of a dynamic system.
Examples:
- Position.
- Velocity.
- Current.
- Capacitor voltage.
- Temperature.
 INPUT VARIABLES;
External signals that influence system behaviour.
Examples:
- Applied force.
- Input voltage.
- Motor torque.
- Heat supplied.
 OUTPUT VARIABLES;
Measured or observed system responses.
Examples:
- Displacement.
- Temperature.
- Output voltage.
- Angular velocity.
APPLICATIONS:
- Feedback control.
- Robot motion.
- Aircraft control.
- Motor control.
- Process automation.

TRANSFER FUNCTION MODELLING
A transfer function represents the input-output relationship of a linear time-invariant system in the Laplace domain, assuming zero initial conditions.
GENERAL FORM:
    G(s) = Y(s)/U(s)
Where:
Y(s) = output transform.
U(s) = input transform.
 FIRST-ORDER SYSTEM;
    G(s) = K/(τs+1)
Where:
K = system gain
τ = time constant.
 SECOND-ORDER SYSTEM
    G(s) = ωn²/(s²+2ζωns+ωn²)
Where:
ωn = natural frequency
ζ = damping ratio.
 POLES AND ZEROS
Poles:
Values of s that make the denominator zero.
Zeros:
Values of s that make the numerator zero.
 SYSTEM STABILITY
For a continuous-time linear system, asymptotic stability requires all poles to have strictly negative real parts.
APPLICATIONS:
- Control system design.
- Feedback systems.
- Motor speed control.
- Industrial automation.
- Dynamic response analysis.

OPTIMISATION AND ENGINEERING DESIGN MODELLING
Engineering optimisation involves selecting the best design or operating conditions while satisfying specified constraints.
GENERAL FORM:
Minimise or maximise:
    f(x)
Subject to:
    g_i(x) ≤ 0
    h_j(x) = 0
Where:
f(x) = objective function.
g_i(x) = inequality constraints.
h_j(x) = equality constraints.
 COMMON OBJECTIVES:
- Minimise cost.
- Minimise weight.
- Maximise efficiency.
- Minimise energy consumption.
- Maximise strength.
- Minimise material usage.
 LINEAR PROGRAMMING
Optimises a linear objective function subject to linear constraints.
 NONLINEAR PROGRAMMING
Deals with objective functions or constraints that are nonlinear.
 MULTI-OBJECTIVE OPTIMISATION
Optimises several objectives simultaneously.
Example:
Minimise weight while maximising strength and minimising cost.
 DESIGN VARIABLES
Quantities that can be changed during the design process.
Examples:
- Beam dimensions.
- Material thickness.
- Motor power.
- Spring stiffness.
APPLICATIONS:
- Structural design.
- Machine design.
- Manufacturing.
- Energy systems.
- Engineering resource allocation.

MODEL VERIFICATION, VALIDATION AND CALIBRATION
These processes establish the reliability and usefulness of an engineering model.
 VERIFICATION
Determines whether the model has been implemented correctly.
Question:
Are we solving the equations correctly?
Methods:
- Checking mathematical derivations.
- Checking computer code.
- Testing numerical algorithms.
- Comparing with analytical solutions.
- Checking conservation laws.
 VALIDATION
Determines whether the model accurately represents the real physical system for its intended application.
Question:
Are we solving the correct problem?
Methods:
- Comparing predictions with experimental data.
- Comparing with field measurements.
- Evaluating prediction errors.
- Conducting independent experiments.
 CALIBRATION
Adjusts model parameters so that model predictions agree with observed data.
Example:
Adjusting a motor model's friction coefficient using experimental measurements.
 SENSITIVITY ANALYSIS
Determines how changes in input parameters affect model outputs.
For output y depending on parameter p:
    Sensitivity = ∂y/∂p
It helps identify the parameters that have the greatest influence on system performance.
 UNCERTAINTY ANALYSIS
Examines how uncertainty in input data and parameters affects model predictions.
Sources:
- Measurement uncertainty.
- Material property variations.
- Environmental changes.
- Simplifying assumptions.
- Numerical approximations.

ENGINEERING SIMULATION AND COMPUTATIONAL MODELLING
Simulation uses mathematical and computational models to reproduce the behaviour of engineering systems under specified conditions.
COMMON SIMULATION TYPES:
 STATIC SIMULATION
Studies systems under steady or static loading conditions.
Example:
Structural deformation under a constant load.
 DYNAMIC SIMULATION
Studies system behaviour as it changes with time.
Example:
Vehicle suspension response.
 STEADY-STATE SIMULATION
Studies system behaviour after transient effects have disappeared.
 TRANSIENT SIMULATION
Studies how a system responds over time following a change in input or operating conditions.
 MONTE CARLO SIMULATION
Uses repeated random sampling to analyse systems involving uncertainty.
 DISCRETE-EVENT SIMULATION
Models systems in which changes occur at distinct events.
Examples:
Manufacturing lines, queues and production systems.
IMPORTANT COMPUTATIONAL TOOLS:
MATLAB:
- Mathematical modelling.
- Control system simulation.
- Numerical analysis.
- Signal processing.
SIMULINK:
- Block-based dynamic system modelling.
- Control system design.
- Physical system simulation.
PYTHON:
- NumPy: numerical calculations.
- SciPy: scientific computation.
- SymPy: symbolic mathematics.
- Matplotlib: plotting and visualisation.
- Pandas: data analysis.
ANSYS:
- Structural analysis.
- Thermal simulation.
- Fluid simulation.
COMSOL:
- Multiphysics modelling.
- Electromagnetic and thermal simulation.
SOLIDWORKS:
- Mechanical design.
- CAD modelling.
- Engineering simulation.
APPLICATIONS:
- Virtual prototyping.
- Product development.
- Predictive engineering.
- System testing.
- Design optimisation.

MODEL LIMITATIONS AND GOOD MODELLING PRACTICES
A mathematical model is a simplified representation of reality, not reality itself.
IMPORTANT LIMITATIONS:
1. Assumptions may not accurately represent actual conditions.
2. Input data may contain measurement errors.
3. Mathematical models may exclude important physical effects.
4. Numerical methods may introduce computational errors.
5. Model predictions may only be reliable within a specified operating range.
6. Complex systems may require multiple interacting models.
GOOD PRACTICES:
- Clearly define the modelling objectives.
- Use physically justified assumptions.
- Apply correct governing equations.
- Maintain dimensional consistency.
- Use realistic material and system parameters.
- Apply suitable initial and boundary conditions.
- Select appropriate numerical methods.
- Verify computational implementation.
- Validate against experimental data.
- Document assumptions and limitations.
- Perform sensitivity and uncertainty analysis.
- Update models when new experimental information becomes available.

ENGINEERING APPLICATIONS OF MATHEMATICAL MODELLING
MECHANICAL ENGINEERING:
- Machine dynamics.
- Vehicle suspension.
- Mechanical vibrations.
- Heat engines.
- Structural mechanics.
ELECTRICAL AND ELECTRONICS:
- Electrical circuit models.
- Semiconductor behaviour.
- Power systems.
- Signal processing.
- Electronic thermal management.
CIVIL ENGINEERING:
- Bridge and building structures.
- Soil mechanics.
- Fluid and water systems.
- Structural stability.
- Construction optimisation.
ROBOTICS:
- Robot kinematics.
- Robot dynamics.
- Joint and actuator modelling.
- Motion planning.
- Robot control.
EMBEDDED SYSTEMS:
- Sensor modelling.
- Microcontroller-based control.
- Real-time system modelling.
- Digital filtering.
- Hardware-in-the-loop simulation.
AI AND MACHINE LEARNING:
- Predictive models.
- System identification.
- Data-driven modelling.
- Optimisation.
- Digital twins.
INDUSTRIAL ENGINEERING:
- Production systems.
- Manufacturing processes.
- Resource optimisation.
- Process control.
- Reliability modelling.

ESSENTIAL ENGINEERING MODELLING FORMULAS
NEWTON'S SECOND LAW:
    F = ma
ROTATIONAL DYNAMICS:
    τ = Iα
OHM'S LAW:
    V = IR
ELECTRICAL POWER:
    P = VI
MASS-SPRING-DAMPER:
    mẍ + cẋ + kx = F(t)
NATURAL FREQUENCY:
    ωn = √(k/m)
DAMPING RATIO:
    ζ = c/(2√mk)
HEAT CONDUCTION:
    Q̇ = -kA(dT/dx)
CONVECTION:
    Q̇ = hA(Ts-T∞)
BERNOULLI'S EQUATION:
    P + ½ρv² + ρgh = constant
CONTINUITY EQUATION:
    ρAv = constant (for steady one-dimensional flow)
STATE-SPACE MODEL:  
    ẋ = Ax + Bu
    y = Cx + Du
TRANSFER FUNCTION:
    G(s) = Y(s)/U(s)
REYNOLDS NUMBER:
    Re = ρvL/μ
DIMENSIONLESS MODEL GROUPS:
    Number of π terms = n-k
OPTIMISATION:
Minimise or maximise f(x), subject to specified constraints.