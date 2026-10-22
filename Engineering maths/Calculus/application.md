        APPLICATIONS OF CALCULUS AND DIFFERENTIAL EQUATIONS
Calculus applications use derivatives and integrals to model physical systems. Differential equations describe relationships involving unknown functions and their derivatives.
Engineering applications: 
-Mechanical motion
-electrical circuits 
-heat transfer 
-fluid systems
-control systems
-population or process models.

LINEAR APPROXIMATION AND ERROR ESTIMATION:
For a small change dx:
    dy ≈ f′(x)dx
If y = f(x), the differential dy estimates the change in y.
The first-order Taylor approximation near x = a is:
    f(x) ≈ f(a) + f′(a)(x − a)
This is useful when a system operates close to a known operating point.
For a measured quantity y = f(x), a small input uncertainty δx gives approximately:
    δy ≈ f′(x)δx
Relative error, when the quantities are nonzero:
    Relative error ≈ δy/y
    Percentage error ≈ |δy/y| × 100%
For multiple independent input uncertainties, uncertainty propagation may require combining their contributions using a suitable statistical model.

OPTIMIZATION IN ENGINEERING:
Optimization seeks the maximum or minimum value of a function subject to the problem's constraints.
General procedure:
1. Define the objective function.
2. Express constraints mathematically.
3. Reduce the problem to one or more independent variables.
4. Find critical points using derivatives.
5. Test critical points and boundary values.
6. Interpret the result using physical constraints and units.
Examples include minimum-cost designs, maximum power transfer, optimal dimensions, and minimum material usage.

DIFFERENTIAL EQUATIONS
A differential equation contains an unknown function and one or more of its derivatives.
Order: The highest derivative present.  
Degree: The power of the highest-order derivative, provided the equation is polynomial in its derivatives.
Ordinary differential equation (ODE): Involves derivatives with respect to one independent variable.
Partial differential equation (PDE): Involves partial derivatives with respect to multiple independent variables.
A solution must satisfy the equation and any specified initial or boundary conditions.

FIRST-ORDER DIFFERENTIAL EQUATIONS:
  Separable Equations;
General form
    dy/dx = g(x)h(y)
Separate variables:
    dy/h(y) = g(x)dx    
Integrate both sides and apply initial conditions if supplied.
Example:
    dy/dx = ky
Separate and integrate:
    dy/y = k dx
    ln|y| = kx + C
Therefore:
    y = Aeᵏˣ
where A is determined by the initial condition.
  First-Order Linear Equations;
Standard form
    dy/dx + P(x)y = Q(x)
Integrating factor:
    IF = e^(∫P(x)dx)
Multiply the equation by the integrating factor:
    d/dx [y(IF)] = Q(x)(IF)
Integrate:
    y(IF) = ∫Q(x)(IF)dx + C
Hence:
    y = [∫Q(x)(IF)dx + C]/IF
  Exponential Growth and Decay;
General model
    dy/dt = ky
Solution:
    y(t) = y₀eᵏᵗ
- k > 0: Exponential growth.
- k < 0: Exponential decay.
For radioactive decay or a suitable discharge model, k is negative.
Half-life for exponential decay:
    t₁/₂ = ln(2)/|k|

SECOND-ORDER LINEAR DIFFERENTIAL EQUATIONS:
A constant-coefficient equation may have the form:
    ay″ + by′ + cy = 0
Assume a solution y = eʳˣ to obtain the characteristic equation:
    ar² + br + c = 0
Case 1: Distinct real roots
    If r₁ ≠ r₂:
    y = C₁eʳ¹ˣ + C₂eʳ²ˣ
Case 2: Repeated real root
    If r₁ = r₂ = r:
    y = (C₁ + C₂x)eʳˣ
Case 3: Complex roots
    If r = α ± iβ:
    y = eᵅˣ(C₁ cos βx + C₂ sin βx)
The constants are determined by initial or boundary conditions.

SIMPLE HARMONIC MOTION:
For an ideal undamped oscillator:
    m d²x/dt² + kx = 0
Natural angular frequency:
    ωₙ = √(k/m)
General solution:
    x(t) = A cos(ωₙt) + B sin(ωₙt)
Period:
    T = 2π/ωₙ
Frequency:
    f = 1/T = ωₙ/(2π)
Here m is mass and k is spring stiffness.

DAMPED AND FORCED SYSTEMS:
A common mechanical vibration model is:
    m x″ + c x′ + kx = F(t)
where:
- m = mass.
- c = damping coefficient.
- k = stiffness.
- F(t) = applied force.
The response depends on mass, damping, stiffness, and the applied force.
For the unforced system, the damping ratio is:
    ζ = c/(2√(mk))
- ζ < 1: Underdamped.
- ζ = 1: Critically damped.
- ζ > 1: Overdamped.
This classification assumes m > 0, c ≥ 0, and k > 0.

NUMERICAL SOLUTION: EULER'S METHOD:
When an analytical solution is unavailable or inconvenient, numerical methods approximate the solution.
For:
    dy/dx = f(x,y)
with initial condition y(x₀) = y₀:
    yₙ₊₁ = yₙ + h f(xₙ,yₙ)
    xₙ₊₁ = xₙ + h
where h is the step size.
Euler's method is simple but generally less accurate than higher-order methods for the same step size. Smaller steps often improve accuracy, but the effect depends on the equation and numerical stability.

WORKED EXAMPLE: EXPONENTIAL MODEL
A quantity obeys
    dy/dt = −0.5y
    with y(0) = 10.
The solution is:
    y(t) = Ae⁻⁰·⁵ᵗ
Using y(0) = 10 gives A = 10.
Therefore:
    y(t) = 10e⁻⁰·⁵ᵗ
    At t = 2:
    y(2) = 10e⁻¹ ≈ 3.68

PROBLEM-SOLVING TIPS:
1. Identify the order and type of differential equation.
2. Check whether the equation is separable or first-order linear before choosing a method.
3. Apply initial conditions after obtaining the general solution.
4. Verify analytical solutions by substitution into the original equation.
5. Check units and signs in physical models.
6. Distinguish natural frequency from ordinary frequency.
7. For numerical methods, state the step size and recognize approximation error.
8. Ensure mathematical solutions satisfy physical constraints, such as nonnegative mass or temperature in the intended model.