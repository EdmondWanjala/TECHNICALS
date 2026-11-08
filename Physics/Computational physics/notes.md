                COMPUTATIONAL PHYSICS
Computational physics is the branch of physics that uses numerical methods, mathematical algorithms and computer simulations to solve physical problems that are difficult or impossible to solve analytically.
It combines:
- Classical and modern physics.
- Mathematics and numerical analysis.
- Programming and algorithms.
- Data analysis and visualization.
- Computer modelling and simulation.
Main objectives:
- Solve complex physical equations.
- Simulate physical systems.
- Predict the behaviour of physical phenomena.
- Analyse experimental data.
- Model systems under different conditions.
- Verify theoretical predictions.
Applications:
- Fluid dynamics and heat transfer.
- Electromagnetic field simulation.
- Quantum mechanics.
- Astrophysics and particle physics.
- Robotics and control systems.
- Material science.
- Computational engineering.
- Weather and climate modelling.

MATHEMATICAL FOUNDATIONS
Computational physics relies on mathematical models that describe physical systems.
Important mathematical concepts:
 Algebra:
Used to manipulate equations and solve mathematical relationships.
 Calculus:
- Differentiation: Determines rates of change.
- Integration: Determines accumulated quantities.
- Partial differentiation: Used for functions of several variables.
 Linear algebra:
Deals with vectors, matrices and systems of linear equations.
 Differential equations:
Describe how physical quantities change with time or space.
 Probability and statistics:
Used in uncertainty analysis, random processes and statistical mechanics.
 Complex numbers:
Used in wave mechanics, electrical engineering and quantum physics.

PHYSICAL MODELLING
A physical model is a mathematical representation of a real-world physical system.
General modelling procedure:
1. Identify the physical problem.
2. Define the system and its boundaries.
3. Identify relevant physical laws.
4. Make reasonable assumptions.
5. Define variables and parameters.
6. Formulate mathematical equations.
7. Select a numerical method.
8. Implement the model computationally.
9. Analyse and visualize results.
10. Validate the model against theory or experimental data.
Important modelling concepts:
 Independent variables:
Variables that determine the input or position in a model.
Examples: Time (t), position (x).
 Dependent variables:
Quantities whose values depend on independent variables.
Examples: Velocity, temperature, pressure.
 Parameters:
Fixed quantities that characterize the system.
Examples: Mass, density, gravitational acceleration.
 Initial conditions:
Values specifying the state of a system at the beginning of a simulation.
 Boundary conditions:
Conditions imposed at the physical boundaries of a system.

NUMERICAL REPRESENTATION AND DISCRETIZATION
Discretization converts continuous physical quantities or mathematical equations into finite computational representations.
 Spatial discretization:
Divides a physical domain into discrete points, cells or elements.
 Temporal discretization:
Divides time into discrete intervals.
Time step:
    Δt = tₙ₊₁ - tₙ
Spatial step:
    Δx = xᵢ₊₁ - xᵢ
A smaller step size generally improves resolution but increases computational cost.
Common discretization methods:
- Finite Difference Method (FDM).
- Finite Element Method (FEM).
- Finite Volume Method (FVM).
- Spectral Methods.

NUMERICAL ERRORS
Numerical calculations introduce errors because computers use finite precision and numerical approximations.
 Round-off error:
Occurs when numbers are represented with limited precision.
 Truncation error:
Occurs when an infinite mathematical process is approximated by a finite number of terms or steps.
 Absolute error:
Eₐ = |x_true - x_approx|
 Relative error:
Eᵣ = |x_true - x_approx|/|x_true|
 Percentage error:
E% = Eᵣ × 100%
 Numerical stability:
Describes whether numerical errors remain bounded or grow during computation.
 Convergence:
A numerical method converges if its approximate solution approaches the exact solution as the discretization is refined.
Important:
A numerical result can be precise but inaccurate if the mathematical model or input data are incorrect.

ROOT-FINDING METHODS
Root-finding methods determine the values of x satisfying:
    f(x) = 0
 BISECTION METHOD
Requires an interval [a,b] where:
    f(a)f(b) < 0
The root is approximated by repeatedly dividing the interval into two halves.
Midpoint:
    c = (a+b)/2
Procedure:
1. Select an interval containing a sign change.
2. Calculate the midpoint.
3. Evaluate the function at the midpoint.
4. Select the half-interval containing the sign change.
5. Repeat until the required accuracy is achieved.
Advantages:
- Simple.
- Reliable for continuous functions with a sign-changing interval.
Limitation:
- Relatively slow convergence.
 NEWTON-RAPHSON METHOD
Uses the function and its derivative to estimate a root.
Formula:
    xₙ₊₁ = xₙ - f(xₙ)/f'(xₙ)
Advantages:
- Fast convergence near a suitable root.
- Requires relatively few iterations.
Limitations:
- Requires a derivative.
- Can fail if the derivative is zero or very small.
- Sensitive to the initial guess.
 SECANT METHOD
Approximates the derivative using two previous estimates.
    xₙ₊₁ = xₙ - f(xₙ)(xₙ - xₙ₋₁)/[f(xₙ) - f(xₙ₋₁)]
It does not require an explicit derivative.
Applications:
- Finding equilibrium points.
- Solving nonlinear physical equations.
- Determining critical parameters.

NUMERICAL SOLUTION OF LINEAR EQUATIONS
Many physical models produce systems of simultaneous linear equations.
General form:
    Ax = b
Where:
A = Coefficient matrix.
x = Unknown vector.
b = Constant vector.
Methods:
 Gaussian elimination:
Uses elementary row operations to transform a system into upper triangular form, followed by back substitution.
 Gauss-Jordan elimination:
Reduces the coefficient matrix to reduced row-echelon form.
 LU decomposition:
Factorizes a matrix into:
    A = LU
Where:
L = Lower triangular matrix.
U = Upper triangular matrix.
 Jacobi iterative method:
Uses previous iteration values to calculate new unknowns.
 Gauss-Seidel method:
Uses newly calculated values immediately within the same iteration.
Applications:
- Electrical circuit analysis.
- Structural mechanics.
- Electromagnetic field calculations.
- Heat transfer.
- Fluid dynamics.

NUMERICAL DIFFERENTIATION
Numerical differentiation approximates derivatives using discrete data points.
First derivative using forward difference:
    f'(x) ≈ [f(x+h)-f(x)]/h
Backward difference:
    f'(x) ≈ [f(x)-f(x-h)]/h
Central difference:
    f'(x) ≈ [f(x+h)-f(x-h)]/(2h)
Second derivative:
    f''(x) ≈ [f(x+h)-2f(x)+f(x-h)]/h²
Applications:
- Calculating velocity from position data.
- Calculating acceleration from velocity data.
- Determining temperature gradients.
- Estimating rates of change in experimental measurements.
Central differences generally provide better accuracy than forward or backward differences for smooth functions using the same step size.

NUMERICAL INTEGRATION
Numerical integration approximates definite integrals when analytical integration is difficult or impossible.
 RECTANGULAR RULE
Approximates the area using rectangular strips.
 TRAPEZOIDAL RULE
Approximates the area under a curve using trapezoids.
For equally spaced data:
    I ≈ h[(y₀+yₙ)/2 + y₁+y₂+...+yₙ₋₁]
Where:
h = Step size.
 SIMPSON'S 1/3 RULE
Uses parabolic approximations.
I ≈ (h/3)[y₀+yₙ+ 4(y₁+y₃+...)+ 2(y₂+y₄+...)]
Requirements:
- Number of subintervals must be even.
- Data points must be equally spaced for the standard formula.
Applications:
- Calculating work from force-displacement data.
- Determining energy.
- Computing areas and volumes.
- Calculating total heat transfer.
- Analysing experimental measurements.

NUMERICAL SOLUTION OF ORDINARY DIFFERENTIAL EQUATIONS
Ordinary differential equations (ODEs) describe physical quantities that change with one independent variable, commonly time.
General form:
    dy/dt = f(t,y)
With initial condition:
    y(t₀) = y₀
 EULER'S METHOD
Uses the slope at the beginning of each time step.
    yₙ₊₁ = yₙ + h f(tₙ,yₙ)
Where:
    h = Time step.
Advantages:
- Simple to implement.
- Useful for introductory simulations.
Limitation:
- Relatively low accuracy.
 IMPROVED EULER METHOD (HEUN'S METHOD)
Predictor:
    y* = yₙ + h f(tₙ,yₙ)
Corrector:
    yₙ₊₁ = yₙ + (h/2)[f(tₙ,yₙ)+f(tₙ₊₁,y*)]
 RUNGE-KUTTA FOURTH-ORDER METHOD (RK4)
A widely used numerical method for solving initial-value problems.
    k₁ = f(tₙ,yₙ)
    k₂ = f(tₙ+h/2, yₙ+hk₁/2)
    k₃ = f(tₙ+h/2, yₙ+hk₂/2)
    k₄ = f(tₙ+h, yₙ+hk₃)
Update:
    yₙ₊₁ = yₙ + (h/6)(k₁+2k₂+2k₃+k₄)
Applications:
- Projectile motion.
- Oscillations.
- Electrical circuit simulations.
- Population dynamics.
- Orbital motion.
- Control systems.

PARTIAL DIFFERENTIAL EQUATIONS (PDEs)
PDEs describe physical systems involving multiple independent variables, such as space and time.
 HEAT EQUATION
Describes heat diffusion through a material.
    ∂T/∂t = α∇²T
Where:
T = Temperature.
α = Thermal diffusivity.
For one-dimensional heat conduction:
    ∂T/∂t = α ∂²T/∂x²
 WAVE EQUATION
Describes wave propagation.
    ∂²u/∂t² = c²∇²u
For one-dimensional propagation:
    ∂²u/∂t² = c²∂²u/∂x²
 LAPLACE'S EQUATION
Describes steady-state potential fields.
    ∇²φ = 0
Applications:
- Electrostatics.
- Steady-state heat conduction.
- Gravitational potential problems.
 POISSON'S EQUATION
Describes potential fields with a source distribution.
    ∇²φ = -ρ/ε₀
For electrostatic potential in a vacuum.
Numerical PDE methods include:
- Finite differences.
- Finite elements.
- Finite volumes.

MONTE CARLO METHODS
Monte Carlo methods use random sampling to estimate numerical quantities and simulate systems with probabilistic behaviour.
General procedure:
1. Define the problem.
2. Specify probability distributions.
3. Generate random samples.
4. Evaluate the model for each sample.
5. Aggregate results.
6. Estimate uncertainty.
For estimating an expectation:
    E[f(X)] ≈ (1/N)Σf(Xᵢ)
Where:
    N = Number of random samples.
Applications:
- Statistical mechanics.
- Particle transport.
- Radiation physics.
- Quantum physics.
- Risk and uncertainty analysis.
- Multidimensional integration.
Accuracy generally improves as the number of independent samples increases.

FOURIER ANALYSIS
Fourier analysis represents complex periodic signals as combinations of sinusoidal components.
A periodic function can be represented using a Fourier series:
    f(x) = a₀/2 + Σ[aₙcos(nωx)+bₙsin(nωx)]
Where:
a₀, aₙ, bₙ = Fourier coefficients.
ω = Fundamental angular frequency.
Fourier transform:
    F(ω) = ∫f(t)e⁻ⁱωᵗdt
The inverse Fourier transform reconstructs the original signal from its frequency components.
Discrete Fourier Transform (DFT):
    Xₖ = Σₙ₌₀ᴺ⁻¹ xₙe⁻ⁱ²πkn/N
Fast Fourier Transform (FFT):
An efficient algorithm for computing the DFT.
Applications:
- Signal processing.
- Sound analysis.
- Vibration analysis.
- Image processing.
- Spectroscopy.
- Communication systems.

COMPUTATIONAL MODELLING OF PHYSICAL SYSTEMS
 PROJECTILE MOTION
For ideal projectile motion without air resistance:
Horizontal position:
    x(t) = x₀ + v₀cosθ × t
Vertical position:
    y(t) = y₀ + v₀sinθ × t - (1/2)gt²
Velocity components:
    vₓ = v₀cosθ
    vᵧ = v₀sinθ - gt
A computational model can calculate the position and velocity at successive time steps.
 SIMPLE HARMONIC MOTION
Differential equation:
    d²x/dt² + ω²x = 0
Solution:
    x(t) = A cos(ωt + φ)
Velocity:
    v(t) = -Aω sin(ωt + φ)
Acceleration:
    a(t) = -ω²x
 SIMPLE PENDULUM
For small angular displacements:
    d²θ/dt² + (g/L)θ = 0
Natural angular frequency:
    ω = √(g/L)
Period:
    T = 2π√(L/g)
 NEWTON'S SECOND LAW
    F = ma
For variable forces:
    m d²x/dt² = F(x,v,t)
Numerical integration can determine position and velocity over time.

COMPUTATIONAL FLUID DYNAMICS (CFD)
CFD is the use of numerical methods and computer simulations to analyse fluid flow, heat transfer and related physical phenomena.
It is based primarily on:
- Conservation of mass.
- Conservation of momentum.
- Conservation of energy.
Important equations:
Continuity equation:
    ∂ρ/∂t + ∇·(ρv) = 0
Navier-Stokes momentum equation for a Newtonian fluid:
    ρ[Dv/Dt] = -∇p + ρg + μ∇²v
For incompressible flow with constant viscosity.
Where:
ρ = Fluid density.
v = Velocity vector.
p = Pressure.
μ = Dynamic viscosity.
Applications:
- Aircraft aerodynamic design.
- Turbine analysis.
- Pipeline systems.
- Heat exchangers.
- Vehicle aerodynamics.
- Weather modelling.

COMPUTATIONAL ELECTROMAGNETICS
Computational electromagnetics uses numerical methods to solve electromagnetic field problems.
Maxwell's equations:
Gauss's law for electricity:
    ∇·E = ρ/ε₀
Gauss's law for magnetism:
    ∇·B = 0
Faraday's law:
    ∇×E = -∂B/∂t
Ampere-Maxwell law: 
    ∇×B = μ₀J + μ₀ε₀∂E/∂t
Common numerical methods:
- Finite Difference Time Domain (FDTD).
- Finite Element Method (FEM).
- Method of Moments (MoM).
Applications:
- Antenna design.
- Microwave engineering.
- Electromagnetic compatibility.
- Wireless communication.
- Radar systems.
- Electrical machine design.

COMPUTATIONAL QUANTUM PHYSICS
Computational quantum physics uses numerical methods to approximate quantum mechanical systems.
Important equation:
    Ĥψ = Eψ
Where:
Ĥ = Hamiltonian operator.
ψ = Wave function.
E = Energy eigenvalue.
Computational approaches:
- Matrix diagonalization.
- Finite difference methods.
- Variational methods.
- Monte Carlo methods.
- Numerical solution of Schrödinger's equation.
Applications:
- Atomic structure calculations.
- Molecular modelling.
- Quantum materials.
- Nanotechnology.
- Quantum computing research.

DATA ANALYSIS AND CURVE FITTING
Computational physics frequently involves analysing experimental data and comparing it with theoretical models.
-Linear regression:
    y = mx + c
Where:
m = Slope.
c = Intercept.
-Least squares method:
Minimizes the sum of squared residuals:
    S = Σ(yᵢ - ŷᵢ)²
-Polynomial fitting:
    y = a₀ + a₁x + a₂x² + ... + aₙxⁿ
-Residual analysis:
Examines differences between measured and predicted values.
Applications:
- Experimental physics.
- Calibration.
- Parameter estimation.
- Scientific prediction.
- Model validation.

NUMERICAL OPTIMIZATION
Optimization identifies the best solution to a problem by minimizing or maximizing an objective function.
General form:
Minimize or maximize:
    f(x)
Subject to:
    gᵢ(x) ≤ 0
    hⱼ(x) = 0
Common methods:
- Gradient descent.
- Newton's optimization method.
- Genetic algorithms.
- Simulated annealing.
- Linear programming.
Gradient descent update:
    xₙ₊₁ = xₙ - η∇f(xₙ)
Where:
η = Learning rate or step size.
∇f = Gradient of the objective function.
Applications:
- Minimizing energy.
- Engineering design.
- Parameter estimation.
- Material optimization.
- Machine learning.

PROGRAMMING IN COMPUTATIONAL PHYSICS
Programming languages and tools:
 Python:
Commonly used for scientific computation, modelling, data analysis and visualization.
Important libraries:
- NumPy: Numerical arrays and mathematical operations.
- SciPy: Scientific and numerical algorithms.
- Matplotlib: Graphs and visualization.
- SymPy: Symbolic mathematics.
- Pandas: Data manipulation.
- Jupyter: Interactive computational notebooks.
 MATLAB:
Used for numerical computation, matrix operations, simulations and engineering analysis.
 C and C++:
Used for high-performance scientific simulations and computationally intensive applications.
 Fortran:
Widely used in established scientific computing and numerical simulation codes.
 Julia:
Designed for high-performance numerical and scientific computing.
Important programming concepts:
- Variables and data types.
- Loops and conditional statements.
- Functions.
- Arrays and matrices.
- Numerical algorithms.
- File input and output.
- Plotting and visualization.
- Error handling.
- Code testing and validation.

SCIENTIFIC VISUALIZATION
Scientific visualization converts numerical results into graphical representations for easier interpretation.
Common techniques:
- Line graphs.
- Scatter plots.
- Contour plots.
- Heat maps.
- Vector field plots.
- 3D surface plots.
- Animation.
- Streamlines.
Applications:
- Visualizing wave propagation.
- Temperature distributions.
- Fluid flow patterns.
- Electric and magnetic fields.
- Particle trajectories.
- Stress and strain distributions.

VERIFICATION AND VALIDATION
Verification:
Checks whether the computational model has been implemented correctly.
Question:
Are we solving the equations correctly?
Methods:
- Code testing.
- Comparing with analytical solutions.
- Checking numerical convergence.
- Checking conservation laws.
Validation:
Checks whether the model accurately represents the real physical system.
Question:
Are we solving the correct physical problem?
Methods:
- Comparing with experimental data.
- Comparing with established physical measurements.
- Checking whether predictions agree with observed behaviour.
Sensitivity analysis:
Examines how changes in input parameters affect model outputs.
Uncertainty analysis:
Quantifies uncertainty in inputs, numerical results and predictions.

HIGH-PERFORMANCE COMPUTING (HPC)
High-performance computing uses powerful computing systems to solve computationally demanding scientific problems.
Important concepts:
 Parallel computing:
Divides a problem into tasks that execute simultaneously.
 Distributed computing:
Uses multiple connected computers to solve a problem.
 GPU computing:
Uses graphics processing units to accelerate highly parallel numerical calculations.
 Multithreading:
Allows multiple execution threads within a program.
 Cluster computing:
Combines multiple computers to operate as a coordinated computational resource.
Applications:
- Climate simulations.
- Molecular dynamics.
- Astrophysics.
- Nuclear simulations.
- Large-scale fluid dynamics.
- Machine learning.

IMPORTANT COMPUTATIONAL PHYSICS APPLICATIONS
- Numerical simulation of mechanical systems.
- Modelling heat transfer and temperature distributions.
- Solving electromagnetic field equations.
- Predicting fluid flow and aerodynamic performance.
- Simulating atomic and molecular behaviour.
- Analysing experimental data.
- Predicting orbital and planetary motion.
- Designing optical and photonic systems.
- Modelling nuclear reactions.
- Simulating electrical circuits.
- Optimizing engineering systems.
- Scientific research and technological development.

IMPORTANT EXAMINATION TIPS
1. Understand the physical problem before selecting a numerical method.
2. Distinguish analytical solutions from numerical approximations.
3. Know the difference between accuracy, precision, stability and convergence.
4. Understand round-off and truncation errors.
5. Practise bisection and Newton-Raphson root-finding calculations.
6. Understand Gaussian elimination and iterative linear-system methods.
7. Memorize forward, backward and central difference formulas.
8. Practise trapezoidal and Simpson's numerical integration.
9. Understand Euler's method and RK4 for differential equations.
10. Identify whether a physical problem is governed by an ODE or PDE.
11. Know the basic applications of FDM, FEM and FVM.
12. Understand Monte Carlo simulation and random sampling.
13. Know the difference between Fourier series, Fourier transforms and FFT.
14. Understand initial conditions and boundary conditions.
15. Distinguish model verification from model validation.
16. Always check dimensional consistency and SI units.
17. Smaller time steps do not automatically guarantee stability.
18. Compare numerical results with analytical or experimental results whenever possible.
19. Use suitable visualizations to interpret simulation results.
20. Remember that computational results depend on the assumptions, equations, input data and numerical methods used.