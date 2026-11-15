                CONTROL SYSTEMS
A control system is an arrangement of components designed to regulate, manage or control the behaviour of a system or process to achieve a desired output.
It works by manipulating input variables and monitoring system behaviour to maintain the required performance.
  Examples:
- Temperature regulation in air conditioners.
- Speed control in electric motors.
- Automatic voltage regulation.
- Cruise control in vehicles.
- Robotic arm positioning.
- Industrial process control.
- Aircraft autopilot systems.
- Automatic water-level control.
  Main objectives:
- Maintain system stability.
- Improve accuracy.
- Minimize errors.
- Improve response speed.
- Reject disturbances.
- Maintain desired system performance.

 BASIC COMPONENTS OF A CONTROL SYSTEM
A typical control system consists of:
- Reference input (setpoint): Desired value of the system output.
- Controller: Determines the control action required.
- Actuator: Converts the control signal into physical action.
- Plant/process: The system being controlled.
- Sensor: Measures the actual output.
- Feedback path: Returns measured information to the controller.
- Disturbance: An unwanted external influence affecting the system.
  Example: Automatic temperature control
1. The user sets a desired temperature.
2. A temperature sensor measures the actual room temperature.
3. The controller compares the measured temperature with the setpoint.
4. It determines whether heating or cooling is required.
5. The actuator operates the heating or cooling equipment.
6. The process continues until the required temperature is achieved.

 TYPES OF CONTROL SYSTEMS
A. OPEN-LOOP CONTROL SYSTEM
An open-loop system operates without measuring its output and feeding it back to correct the control action.
The control action does not automatically depend on the actual output.
Examples:
- Timer-based washing machine.
- Basic electric toaster.
- Timer-controlled irrigation.
- A fixed-time traffic light system.
Advantages:
- Simple construction.
- Low cost.
- Easy to design and maintain.
- Generally stable if properly designed.
Disadvantages:
- Cannot automatically correct errors.
- Sensitive to disturbances and parameter changes.
- Requires accurate calibration.
- May produce inaccurate outputs.
B. CLOSED-LOOP CONTROL SYSTEM
A closed-loop system uses feedback to compare the actual output with the desired output and correct any difference.
Error signal:
    e(t) = r(t) - y(t)
Where:
r(t) = reference input
y(t) = actual output
e(t) = error signal
Examples:
- Thermostat-controlled heating.
- Automatic motor speed control.
- Cruise control.
- Automatic voltage regulation.
- Robot position control.
Advantages:
- Automatically corrects errors.
- Better accuracy.
- Can reject disturbances.
- Less sensitive to certain parameter variations.
Disadvantages:
- More complex.
- Higher cost.
- Requires sensors and feedback components.
- Poorly designed feedback can cause instability.

 CONTROL SYSTEM CLASSIFICATION
Control systems may also be classified as:
a) Linear systems
- Satisfy the principles of superposition and homogeneity.
- Mathematical models are often represented using linear differential equations.
b) Nonlinear systems
- Do not satisfy the superposition principle.
- Examples include systems with saturation, friction, backlash and nonlinear actuators.
c) Continuous-time systems
- Signals and system variables are defined continuously in time.
- Often described using differential equations.
d) Discrete-time systems
- Signals are represented at discrete time intervals.
- Often implemented using digital controllers and described using difference equations.
e) Time-invariant systems
- System parameters do not change with time.
f) Time-varying systems
- System characteristics change with time.
g) SISO systems
- Single Input, Single Output.
h) MIMO systems
- Multiple Input, Multiple Output.

 MATHEMATICAL MODELLING OF CONTROL SYSTEMS
Mathematical modelling represents the physical behaviour of a system using equations.
  Common modelling methods:
- Differential equations.
- Transfer functions.
- Block diagrams.
- Signal-flow graphs.
- State-space equations.
  Examples of physical systems:
A. Mechanical translational system
Newton's second law:
    ΣF = ma
For a mass-spring-damper system:
    m(d²x/dt²) + c(dx/dt) + kx = F(t)
Where:
m = mass (kg)
c = damping coefficient (N·s/m)
k = spring stiffness (N/m)
x = displacement (m)
F(t) = applied force (N)
B. Electrical system
For a series RLC circuit:
    L(d²q/dt²) + R(dq/dt) + q/C = V(t)
Where:
L = inductance (H)
R = resistance (Ω)
C = capacitance (F)
q = electric charge (C)
V(t) = applied voltage (V)
C. Rotational mechanical system
    J(d²θ/dt²) + b(dθ/dt) + kθ = T(t)
Where:
J = moment of inertia
b = rotational damping coefficient
k = torsional stiffness
θ = angular displacement
T(t) = applied torque

 TRANSFER FUNCTIONS
A transfer function describes the relationship between the output and input of a linear time-invariant system in the Laplace domain, assuming zero initial conditions.
General expression:
    G(s) = Y(s)/X(s)
Where:
G(s) = transfer function
Y(s) = output Laplace transform
X(s) = input Laplace transform
s = complex frequency variable
A transfer function can be expressed as:
    G(s) = (b_ms^m + ... + b_1s + b_0) /(a_ns^n + ... + a_1s + a_0)
Important concepts:
- Numerator: Determines the system zeros.
- Denominator: Determines the system poles.
- Poles: Values of s that make the denominator zero.
- Zeros: Values of s that make the numerator zero.
Example:
For a mass-spring-damper system:
    m(d²x/dt²) + c(dx/dt) + kx = F(t)
Taking the Laplace transform with zero initial conditions:
    (ms² + cs + k)X(s) = F(s)
Therefore:
    G(s) = X(s)/F(s) = 1/(ms² + cs + k)
Transfer functions are useful for analysing stability, transient response and frequency response.

 BLOCK DIAGRAMS AND BLOCK DIAGRAM REDUCTION
A block diagram represents the functional relationships between components of a control system.
Main elements:
- Blocks: Represent system components or transfer functions.
- Arrows: Show signal direction.
- Summing points: Add or subtract signals.
- Take-off points: Allow signals to branch.
  Important reduction rules:
a) Series connection
    G_eq(s) = G₁(s)G₂(s)
b) Parallel connection
    G_eq(s) = G₁(s) ± G₂(s)
c) Negative feedback system
    T(s) = G(s)/[1 + G(s)H(s)]
d) Positive feedback system
    T(s) = G(s)/[1 - G(s)H(s)]
Where:
G(s) = forward-path transfer function
H(s) = feedback-path transfer function
T(s) = closed-loop transfer function
The product G(s)H(s) is called the loop transfer function.

 FEEDBACK CONTROL
Feedback is the process of using information about the actual system output to influence its future control action.
A. Negative feedback
- The feedback signal is subtracted from the reference input.
- Reduces error under suitable conditions.
- Often improves disturbance rejection and robustness.
- Can reduce overall system gain.
- May affect stability and bandwidth.
B. Positive feedback
- The feedback signal is added to the reference input.
- Can increase effective gain.
- May lead to instability if not carefully controlled.
- Used in applications such as oscillators and regenerative circuits.
Important:
Negative feedback does not automatically guarantee stability. Stability depends on the complete system dynamics.

 TIME-DOMAIN RESPONSE
Time-domain response describes how a system behaves as time progresses after an input is applied.
  It consists of:
A. Transient response
- Temporary behaviour immediately after an input change.
- Includes rise, overshoot and settling behaviour.
B. Steady-state response
- Behaviour after transient effects have sufficiently decayed.
- Describes the final or long-term response.
  Important performance parameters:
1. Rise time (Tr)
- Time taken for the response to rise from a specified lower percentage to a specified upper percentage of its final value.
- Commonly measured from 10% to 90% for many systems.
2. Peak time (Tp)
- Time taken to reach the first maximum peak.
3. Maximum overshoot (Mp)
- Amount by which the response exceeds its final value.
- Usually expressed as a percentage.
4. Settling time (Ts)
- Time required for the response to enter and remain within a specified tolerance band around the final value.
- Common bands are ±2% or ±5%.
5. Steady-state error (ess)
- Difference between the desired and actual output after transient effects have decayed.

 FIRST-ORDER SYSTEMS
A standard first-order transfer function is:
    G(s) = K/(τs + 1)
Where:
K = system gain
τ = time constant
For a unit-step input, the response is:
    y(t) = K(1 - e^(-t/τ))
  Important characteristics:
- Response is generally exponential.
- At t = τ, the output reaches approximately 63.2% of its final value.
- At about 4τ, it reaches approximately 98.2% of its final value.
- A smaller time constant generally means a faster response.
Applications:
- Thermal systems.
- RC circuits.
- Liquid-level systems.
- Simple sensor dynamics.

 SECOND-ORDER SYSTEMS
A standard second-order transfer function is:
    G(s) = ω_n²/(s² + 2ζω_ns + ω_n²)
Where:
ω_n = natural frequency (rad/s)
ζ = damping ratio
  Types of damping:
a) Underdamped system (0 < ζ < 1)
- Oscillatory response.
- Has overshoot.
- Oscillations gradually decay.
b) Critically damped system (ζ = 1)
- Fast response without oscillation or overshoot for a standard second-order step response.
c) Overdamped system (ζ > 1)
- Non-oscillatory response.
- Usually slower than a critically damped response.
d) Undamped system (ζ = 0)
- Sustained oscillations in the ideal model.
Damped natural frequency:
    ω_d = ω_n√(1 - ζ²)
For an underdamped second-order system:
Peak time:
    T_p = π/ω_d
Percentage overshoot:
    %OS = e^[-ζπ/√(1-ζ²)] × 100
Approximate 2% settling time:
    T_s ≈ 4/(ζω_n)
These standard formulas assume a conventional second-order system with an underdamped response and no additional dynamics that significantly change the result.

 STEADY-STATE ERROR
Steady-state error is the difference between the reference input and the output after transient behaviour has settled.
    e_ss = lim(t→∞) e(t)
Using the final value theorem, where applicable:
    e_ss = lim(s→0) sE(s)
For a unity-feedback system:
    E(s) = R(s)/[1 + G(s)]
  Important standard inputs:
- Step input: Constant reference.
- Ramp input: Linearly increasing reference.
- Parabolic input: Quadratically increasing reference.
System type is determined by the number of pure integrators (poles at the origin) in the open-loop transfer function G(s)H(s).
Static error constants for unity feedback:
Position constant:
    K_p = lim(s→0) G(s)
Velocity constant:
    K_v = lim(s→0) sG(s)
Acceleration constant:
    K_a = lim(s→0) s²G(s)
Standard steady-state errors:
For a unit step:
    e_ss = 1/(1 + K_p)
For a unit ramp:   
    e_ss = 1/K_v
For a unit parabolic input:
    e_ss = 1/K_a
These formulas assume the relevant limits produce the applicable finite or infinite constants and the closed-loop system is stable.

 STABILITY OF CONTROL SYSTEMS
Stability describes whether a system produces a bounded response to a bounded input and whether its natural response decays appropriately.
For a continuous-time linear time-invariant system, asymptotic stability requires all closed-loop poles to lie in the left half of the complex s-plane.
  Types:
a) Stable system
- Natural response decays with time.
b) Unstable system
- Response may grow without bound or fail to settle.
c) Marginally stable system
- Sustained oscillations may occur under ideal conditions.
  Methods of stability analysis:
- Pole-zero analysis.
- Routh-Hurwitz criterion.
- Root locus.
- Nyquist stability criterion.
- Bode plots.

 ROUTH-HURWITZ STABILITY CRITERION
The Routh-Hurwitz criterion determines the stability of a continuous-time system without explicitly calculating all polynomial roots.
For a characteristic equation:
    a_ns^n + a_(n-1)s^(n-1) + ... + a_1s + a_0 = 0
The coefficients are arranged in a Routh array.
  Important rules:
- Construct the Routh array using the characteristic polynomial coefficients.
- Examine the signs of the first-column elements.
- The number of sign changes equals the number of roots in the right half-plane, subject to handling special cases correctly.
- A stable system requires no sign changes and all necessary first-column entries strictly positive, with no unresolved special cases.
  Special cases:
- A zero first-column element may require an epsilon substitution.
- An entire row of zeros requires formation of an auxiliary polynomial and differentiation.

 ROOT LOCUS
Root locus is a graphical method used to study how closed-loop poles move as a system gain changes.
For a negative-feedback system:
    1 + K G(s)H(s) = 0
Root locus helps determine:
- Closed-loop stability.
- Damping ratio.
- Natural frequency.
- Transient response.
- Suitable controller gain.
Important rules:
- Branches begin at open-loop poles.
- Branches terminate at open-loop zeros or infinity.
- The number of branches equals the number of open-loop poles.
- The locus is symmetric about the real axis for real-coefficient systems.

 FREQUENCY-DOMAIN ANALYSIS
Frequency-domain analysis studies how a system responds to sinusoidal inputs at different frequencies.
  Important concepts:
a) Frequency response
- Describes the steady-state response to sinusoidal inputs.
- Shows how gain and phase vary with frequency.
b) Magnitude response
- Describes the ratio of output amplitude to input amplitude.
c) Phase response
- Describes the phase difference between output and input.
d) Bandwidth
- Frequency range over which a system maintains an acceptable response.
e) Resonance
- A condition where a system exhibits a pronounced response near a particular frequency.
Frequency response is especially useful in amplifier design, motor control, filters and feedback-system analysis.

BODE PLOTS
A Bode plot consists of two graphs:
1. Magnitude plot:
   Shows gain against logarithmic frequency.
2. Phase plot:
   Shows phase angle against logarithmic frequency.
Magnitude is commonly expressed in decibels:
    Magnitude(dB) = 20log₁₀|G(jω)|
  Important terms:
Gain crossover frequency (ω_gc):
- Frequency at which the open-loop magnitude equals 1 (0 dB).
Phase crossover frequency (ω_pc):
- Frequency at which the open-loop phase reaches -180°.
Gain margin (GM):
- Factor by which the loop gain can increase before reaching the critical stability condition, evaluated at phase crossover.
Phase margin (PM):
- Additional phase lag required to reach -180° at the gain crossover frequency.
For a conventional negative-feedback system:
    PM = 180° + ∠G(jω_gc)H(jω_gc)
Positive gain and phase margins generally indicate useful relative stability margins, but they do not replace a complete stability analysis in every system.

 CONTROLLERS
A controller determines the action required to make a system output follow a desired reference.
A. Proportional controller (P)
The control signal is proportional to the error.
    u(t) = K_p e(t)
Advantages:
- Simple.
- Improves response speed.
- Reduces steady-state error in many systems.
Limitations:
- May not eliminate steady-state error.
- Excessive gain can cause overshoot or instability.
B. Integral controller (I)
The control signal depends on the accumulated error.
    u(t) = K_i ∫e(t)dt
Advantages:
- Can eliminate steady-state error for suitable systems.
Limitations:
- Can increase overshoot.
- May slow settling.
- Can cause integral windup when actuators saturate.
C. Derivative controller (D)
The control signal depends on the rate of change of error.
    u(t) = K_d de(t)/dt
Advantages:
- Can improve damping.
- Helps anticipate rapid error changes.
Limitations:
- Sensitive to measurement noise.
- Usually implemented with filtering.
D. PID CONTROLLER
Combines proportional, integral and derivative actions.
    u(t) = K_p e(t) + K_i∫e(t)dt + K_d de(t)/dt
Where:
K_p = proportional gain
K_i = integral gain
K_d = derivative gain
Functions:
- P: Responds to present error.
- I: Responds to accumulated past error.
- D: Responds to the rate of error change.
Applications:
- Motor speed control.
- Temperature control.
- Pressure regulation.
- Robotics.
- Industrial process automation.

 PID TUNING
PID tuning is the process of selecting controller gains to achieve the desired system response.
  Common tuning methods:
a) Trial and error
- Adjust gains experimentally while monitoring system performance.
b) Ziegler-Nichols method
- Uses process-response or sustained-oscillation characteristics to estimate controller settings.
c) Cohen-Coon method
- Uses process reaction-curve information for certain process models.
d) Model-based tuning
- Uses a mathematical model of the plant to select controller parameters.
  Important considerations:
- Rise time.
- Overshoot.
- Settling time.
- Steady-state error.
- Disturbance rejection.
- Actuator limits.
- Measurement noise.
- Stability and robustness.

 STATE-SPACE REPRESENTATION
State-space modelling represents a dynamic system using a set of first-order differential equations.
General continuous-time form:
    dx/dt = Ax + Bu
    y = Cx + Du
Where:
x = state vector
u = input vector
y = output vector
A = system matrix
B = input matrix
C = output matrix
D = feedthrough matrix
  Advantages:
- Handles multiple-input, multiple-output systems.
- Suitable for modern control design.
- Supports time-varying and nonlinear extensions.
- Useful for computer simulation and digital control.
  Important concepts:
Controllability:
- Determines whether suitable inputs can move the system between states.
Observability:
- Determines whether internal states can be reconstructed from available outputs.

 CONTROLLABILITY AND OBSERVABILITY
A. Controllability
A system is completely controllable if its states can be driven from any initial state to any desired final state within a finite time using suitable inputs.
For an n-state linear system, the controllability matrix is:
    𝒞 = [B AB A²B ... A^(n-1)B]
The system is completely controllable if:
    rank(𝒞) = n
B. Observability
A system is completely observable if its internal states can be determined from its outputs over a finite time interval.
The observability matrix is:
    𝒪 = [C; CA; CA²; ...; CA^(n-1)]
The system is completely observable if:
    rank(𝒪) = n

 DIGITAL CONTROL SYSTEMS
Digital control systems use computers, microcontrollers, DSPs or other digital processors to control physical processes.
  Basic structure:
Reference → Digital Controller → DAC/PWM → Actuator → Plant → Sensor → ADC → Digital Controller
  Main operations:
1. Sensor measures the physical output.
2. Signal conditioning prepares the sensor signal.
3. ADC converts the analog measurement into digital data.
4. Digital controller calculates the control action.
5. DAC or PWM produces a suitable actuator command.
6. The actuator influences the plant.
7. The process repeats at the sampling frequency.
  Important concepts:
Sampling period:
    T_s = 1/f_s
Where:
T_s = sampling period
f_s = sampling frequency
Difference equation:
- Discrete-time equivalent of a differential equation.
- Used to implement digital controllers.
Quantization:
- Finite numerical resolution of digital measurements and control outputs.
Control-loop delay:
- Time consumed by sampling, computation and actuation.
- Excessive delay can reduce stability and performance.
 Applications:
- Embedded motor controllers.
- Robotics.
- Automotive electronics.
- Industrial automation.
- Smart appliances.

 INDUSTRIAL CONTROL SYSTEMS
Industrial control systems regulate and automate manufacturing and process operations.
  Important components:
PLC (Programmable Logic Controller):
- Industrial computer designed for automation.
- Controls machinery using programmed logic.
SCADA (Supervisory Control and Data Acquisition):
- Monitors and supervises geographically distributed processes.
- Collects data from sensors and remote equipment.
DCS (Distributed Control System):
- Controls complex industrial processes using distributed controllers.
HMI (Human-Machine Interface):
- Allows operators to monitor and interact with industrial processes.
Sensors:
- Measure temperature, pressure, flow, level, position and other physical variables.
Actuators:
- Convert control signals into physical actions.
- Examples: motors, valves, relays and hydraulic cylinders.

 SENSORS AND ACTUATORS IN CONTROL SYSTEMS
Sensors provide feedback by measuring physical quantities.
  Common sensors:
- Temperature sensors: thermistors, RTDs and thermocouples.
- Position sensors: potentiometers, encoders and LVDTs.
- Speed sensors: tachometers and rotary encoders.
- Pressure sensors.
- Flow sensors.
- Level sensors.
- Light sensors.
- Accelerometers and gyroscopes.
Actuators produce physical movement or changes.
  Common actuators:
- DC motors.
- Servo motors.
- Stepper motors.
- Solenoid valves.
- Pneumatic cylinders.
- Hydraulic actuators.
- Heating elements.
  Important selection factors:
- Accuracy.
- Range.
- Resolution.
- Response time.
- Sensitivity.
- Power consumption.
- Operating environment.
- Compatibility with the controller.

 APPLICATIONS OF CONTROL SYSTEMS
Electrical engineering:
- Voltage regulation.
- Power converters.
- Generator excitation control.
- Motor drives.
Mechanical engineering:
- Vehicle cruise control.
- Speed regulation.
- Position control.
- Vibration control.
Electronics:
- Automatic gain control.
- Power supply regulation.
- Signal tracking.
Robotics:
- Joint position control.
- Motor speed control.
- Trajectory tracking.
- Autonomous navigation.
Industrial engineering:
- Temperature regulation.
- Pressure and flow control.
- Manufacturing automation.
- Process monitoring.
Aerospace:
- Aircraft autopilot.
- Flight stabilization.
- Attitude and altitude control.

 IMPORTANT FORMULAS SUMMARY
1. Error:
   e(t) = r(t) - y(t)
2. Transfer function:
   G(s) = Y(s)/X(s)
3. Negative-feedback closed-loop transfer function:
   T(s) = G(s)/[1 + G(s)H(s)]
4. Positive-feedback closed-loop transfer function:
   T(s) = G(s)/[1 - G(s)H(s)]
5. Mass-spring-damper model:
   m(d²x/dt²) + c(dx/dt) + kx = F(t)
6. Series RLC equation:
   L(d²q/dt²) + R(dq/dt) + q/C = V(t)
7. First-order transfer function:
   G(s) = K/(τs + 1)
8. First-order unit-step response:
   y(t) = K(1 - e^(-t/τ))
9. Standard second-order transfer function:
   G(s) = ω_n²/(s² + 2ζω_ns + ω_n²)
10. Damped natural frequency:
    ω_d = ω_n√(1 - ζ²)
11. Peak time:
    T_p = π/ω_d
12. Percentage overshoot:
    %OS = e^[-ζπ/√(1-ζ²)] × 100
13. Approximate 2% settling time:
    T_s ≈ 4/(ζω_n)
14. Proportional control:
    u(t) = K_p e(t)
15. Integral control:
    u(t) = K_i∫e(t)dt
16. Derivative control:
    u(t) = K_d de(t)/dt
17. PID control:
    u(t) = K_p e(t) + K_i∫e(t)dt + K_d de(t)/dt
18. State-space model:
    dx/dt = Ax + Bu
    y = Cx + Du
19. Sampling frequency:
    f_s = 1/T_s

 PRACTICAL ENGINEERING PROJECTS
1. DC motor speed control:
   Use an encoder, motor driver and microcontroller to maintain a desired motor speed using PID control.
2. Automatic temperature control:
   Use a temperature sensor, heating element and controller to maintain a set temperature.
3. Water-level control:
   Use a level sensor and pump to maintain a desired water level.
4. Line-following robot:
   Use infrared sensors and motor control to follow a defined path.
5. Servo position control:
   Control the angular position of a servo motor using a reference command and feedback.
6. Self-balancing robot:
   Use an IMU, microcontroller and PID controller to maintain balance.
7. Automatic voltage regulation:
   Simulate or implement a system that maintains output voltage despite input or load variations.
8. MATLAB/Python control simulation:
   Model first- and second-order systems, plot step responses and investigate the effect of changing PID gains.

 STUDY AND EXAMINATION TIPS
- Understand the difference between open-loop and closed-loop control.
- Know the functions of all components in a feedback system.
- Practise deriving transfer functions from differential equations.
- Understand block diagram reduction and feedback equations.
- Learn first-order and second-order system responses.
- Understand damping ratio, natural frequency, overshoot and settling time.
- Practise steady-state error calculations.
- Study stability using pole locations and the Routh-Hurwitz criterion.
- Understand root locus and Bode plots.
- Know the operation and limitations of P, PI, PD and PID controllers.
- Understand state-space modelling, controllability and observability.
- Relate digital control theory to microcontrollers, sensors, actuators and embedded systems.
- Always include correct units and clearly state assumptions when solving numerical problems.