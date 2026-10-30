                    NUMERICAL METHODS
Numerical methods are mathematical techniques used to obtain approximate solutions to mathematical problems when exact analytical solutions are difficult, impractical or impossible to obtain.
They involve numerical calculations and algorithms implemented manually or using computers
IMPORTANCE:
- Solving complex mathematical equations.
- Approximating roots of nonlinear equations.
- Evaluating definite integrals.
- Solving differential equations.
- Performing engineering simulations.
- Analysing physical and dynamic systems.
- Optimising engineering designs.

    KEY CONCEPTS:
 Exact solution:
The mathematically precise solution to a problem.
 Approximate solution:
A numerical estimate sufficiently close to the exact solution.
 Iteration:
Repeated application of a numerical procedure to improve an approximation.
 Convergence:
The process by which successive approximations approach the true solution.
 Numerical stability:
The ability of a numerical method to control the propagation of computational errors.
 Accuracy:
How close a computed result is to the true value.
 Precision:
The level of detail or number of significant digits represented in a result.

    ERRORS AND ERROR ANALYSIS
Numerical calculations introduce errors because of approximations, finite precision and computational limitations.
Understanding errors is essential for determining the reliability of numerical results.
 Absolute Error;
Absolute error is the magnitude of the difference between the exact value and approximate value.
Absolute Error = |Exact value - Approximate value|
 Relative Error;
Relative Error = Absolute Error / |Exact value|
 Percentage Error;
Percentage Error = Relative Error × 100%
 Approximate Relative Error;
Used when the exact value is unknown.
Approximate Relative Error =|(Current approximation - Previous approximation)/Current approximation| × 100%
 Types of Numerical Errors;
-Round-off error:
Occurs when numbers are rounded or stored using limited computer precision.
-Truncation error:
Occurs when an infinite mathematical process is approximated using a finite number of terms or steps.
-Inherent error:
Error already present in the original measured or supplied data.
-Propagation error:
Occurs when errors in intermediate calculations affect subsequent results.
-Significant Figures:
Significant figures represent meaningful digits in a numerical value.
Engineering calculations should maintain sufficient precision during intermediate steps and round only the final result.
-Error Tolerance:
Tolerance is the maximum acceptable error.
A numerical method may stop when:
    Approximate Relative Error < Tolerance
For example:
Tolerance = 0.001
The method stops when the specified accuracy requirement is satisfied.

    ROOT-FINDING METHODS: NONLINEAR EQUATIONS
Root-finding methods are numerical techniques used to determine the values of x that satisfy:
    f(x) = 0
A root is a value of x for which the function becomes zero.
 BISECTION METHOD;
The bisection method repeatedly divides an interval into two equal halves to locate a root.
Condition:
    f(a)f(b) < 0
This indicates a sign change and, for a continuous function, guarantees at least one root in the interval.
Formula:
    c = (a+b)/2
Where:
a = lower bound
b = upper bound
c = midpoint.
PROCEDURE:
1. Select an interval [a,b].
2. Check that f(a)f(b) < 0.
3. Calculate the midpoint c.
4. Evaluate f(c).
5. Determine which half contains the sign change.
6. Replace the interval with that half.
7. Repeat until the required tolerance is achieved.
Advantages:
- Simple and reliable.
- Guaranteed convergence for a continuous function with a sign change.
Limitations:
- Relatively slow convergence.
- Requires an initial interval containing a sign change.
 NEWTON-RAPHSON METHOD;
An iterative method that uses the derivative of a function to estimate its root.
Formula:
    x(n+1) = xn - f(xn)/f'(xn)
PROCEDURE:
1. Choose an initial approximation x0.
2. Calculate f(x0) and f'(x0).
3. Substitute into the Newton-Raphson formula.
4. Calculate the next approximation.
5. Repeat until convergence.
Advantages:
- Very fast near a simple root when the initial estimate is suitable.
- Quadratic convergence under appropriate conditions.
Limitations:
- Requires differentiation.
- May fail if f'(x) = 0 or is very small.
- Sensitive to the initial approximation.
 SECANT METHOD;
An approximation of Newton-Raphson that does not require explicit differentiation.
Formula:
    x(n+1) = xn -[f(xn)(xn-x(n-1))]/[f(xn)-f(x(n-1))]
PROCEDURE:
1. Choose two initial approximations.
2. Evaluate the function at both points.
3. Apply the secant formula.
4. Replace the older approximation.
5. Repeat until the required accuracy is achieved.
Advantages:
- Does not require derivatives.
- Often faster than bisection.
Limitations:
- Not guaranteed to converge.
- Requires two initial approximations.
 FIXED-POINT ITERATION;
A method that rearranges an equation into:
    x = g(x)
Iteration formula:
    x(n+1) = g(xn)
PROCEDURE:
1. Rearrange f(x) = 0 into x = g(x).
2. Select an initial value x0.
3. Calculate x1 = g(x0).
4. Continue iterating.
5. Check convergence.
Convergence condition:
A sufficient local condition is:
    |g'(x)| < 1
near the fixed point.
Applications:
- Nonlinear equation solving.
- Engineering mathematical modelling.
- Iterative computational algorithms.

    SOLUTION OF SIMULTANEOUS LINEAR EQUATIONS
Numerical methods solve systems of linear equations of the form:
    AX = B
Where:
A = coefficient matrix.
X = unknown vector.
B = constant vector.
 GAUSSIAN ELIMINATION;
A direct method that transforms a system into upper triangular form.
PROCEDURE:
1. Write the augmented matrix [A|B].
2. Apply elementary row operations.
3. Eliminate variables below the pivots.
4. Obtain upper triangular form.
5. Use back-substitution.
 GAUSS-JORDAN ELIMINATION;
Reduces the augmented matrix to reduced row-echelon form.
The objective is to obtain the identity matrix on the coefficient side, where possible.
 LU DECOMPOSITION;
Expresses a matrix as:
    A = LU
Where:
L = lower triangular matrix.
U = upper triangular matrix.
To solve AX = B:
1. Solve LY = B using forward substitution.
2. Solve UX = Y using back-substitution.
Useful when solving several systems with the same coefficient matrix.
 JACOBI ITERATIVE METHOD;
An iterative method for solving systems of linear equations.
For a system:
    a11x1 + a12x2 + ... = b1
Rearrange each equation to make one variable the subject.
General formula:
    x_i^(k+1) =[bi - Σ(j≠i) aij x_j^(k)]/aii
All new values are calculated using values from the previous iteration.
 GAUSS-SEIDEL METHOD;
Similar to Jacobi, but uses newly calculated values immediately.
General formula:
    x_i^(k+1) =[bi - Σ(j<i) aij x_j^(k+1)- Σ(j>i) aij x_j^(k)]/aii
Advantages:
- Often converges faster than Jacobi.
- Useful for large systems.
CONVERGENCE:
Strict diagonal dominance is a sufficient condition for convergence of both Jacobi and Gauss-Seidel methods.
Applications:
- Electrical circuit analysis.
- Structural engineering.
- Fluid mechanics.
- Heat transfer.
- Computational modelling.

    INTERPOLATION METHODS
Interpolation estimates unknown values within the range of known data points.
It is used when measurements are available at specific points but values between those points are required.
 LINEAR INTERPOLATION;
Uses a straight line between two known data points.
Formula:
    y = y1 + [(x-x1)/(x2-x1)](y2-y1)
Where:
(x1,y1) and (x2,y2) are known data points.
 LAGRANGE INTERPOLATION;
Constructs a polynomial passing through a set of known data points.
Formula:
    P(x) = Σ(i=0 to n) yi Li(x)
Where:
    Li(x) = Π(j≠i) [(x-xj)/(xi-xj)]
The polynomial passes through all supplied data points, assuming distinct x-values.
 NEWTON DIVIDED DIFFERENCE INTERPOLATION;
Uses divided differences to construct an interpolation polynomial.
Formula:
    P(x) = f[x0]+ f[x0,x1](x-x0)+ f[x0,x1,x2](x-x0)(x-x1)+ ...
First divided difference:
    f[x0,x1] = [f(x1)-f(x0)]/(x1-x0)
Higher divided differences are calculated recursively.
 NEWTON FORWARD INTERPOLATION;
Used for equally spaced data, particularly when the required value is near the beginning of the table.
Formula:
    y = y0 + uΔy0+ [u(u-1)/2!]Δ²y0+ [u(u-1)(u-2)/3!]Δ³y0 + ...
Where:
    u = (x-x0)/h
h = equal interval spacing.
 NEWTON BACKWARD INTERPOLATION;
Used for equally spaced data when the required value is near the end of the table.
Formula:
    y = yn + u∇yn+ [u(u+1)/2!]∇²yn+ [u(u+1)(u+2)/3!]∇³yn + ...
Where:
    u = (x-xn)/h
APPLICATIONS:
- Engineering measurement estimation.
- Experimental data analysis.
- Sensor calibration.
- Temperature and pressure estimation.
- Engineering lookup tables.

    NUMERICAL DIFFERENTIATION
Numerical differentiation estimates derivatives using discrete data points.
It is particularly useful when a function is known only through measurements or tabulated values.
FORWARD DIFFERENCE;
    f'(x) ≈ [f(x+h)-f(x)]/h
BACKWARD DIFFERENCE
    f'(x) ≈ [f(x)-f(x-h)]/h
CENTRAL DIFFERENCE
    f'(x) ≈ [f(x+h)-f(x-h)]/(2h)
SECOND DERIVATIVE
    f''(x) ≈ [f(x+h)-2f(x)+f(x-h)]/h²
ERROR CHARACTERISTICS:
    Forward difference: O(h)
    Backward difference: O(h)
    Central difference: O(h²)
The central difference generally provides better accuracy for smooth functions with equal step sizes.
APPLICATIONS:
- Calculating velocity from position measurements.
- Calculating acceleration from velocity data.
- Analysing experimental measurements.
- Determining gradients.
- Engineering optimisation.

    NUMERICAL INTEGRATION
Numerical integration approximates definite integrals when analytical integration is difficult or when data is available only in tabular form.
RECTANGULAR RULE;
Approximates the area under a curve using rectangles.
Left rectangle:
    I ≈ hΣ(i=0 to n-1) f(xi)
Right rectangle:
    I ≈ hΣ(i=1 to n) f(xi)
Midpoint rule:
    I ≈ hΣ(i=0 to n-1) f(xi+h/2)
Where:
    h = (b-a)/n
TRAPEZOIDAL RULE;
Approximates the area under a curve using trapezoids.
Single interval:
    I ≈ (h/2)[f(a)+f(b)]
Composite trapezoidal rule:
    I ≈ h/2 [f(x0)+f(xn)+ 2Σ(i=1 to n-1)f(xi)]
SIMPSON'S 1/3 RULE;
Approximates the integral using quadratic polynomials.
Formula:
    I ≈ h/3 [f(x0)+f(xn)+ 4Σ(odd i)f(xi)+ 2Σ(even i)f(xi)]
Requirements:
- Equal spacing.
- Number of subintervals must be even.
SIMPSON'S 3/8 RULE;
Formula for three equal subintervals:
    I ≈ (3h/8)[f(x0)+3f(x1)+3f(x2)+f(x3)]
Composite Simpson's 3/8 rule can be used when the number of subintervals is a multiple of three.
APPLICATIONS:
- Calculating areas and volumes.
- Work and energy calculations.
- Fluid flow analysis.
- Heat transfer.
- Structural engineering.
- Estimating accumulated quantities from measured data.

NUMERICAL SOLUTION OF ORDINARY DIFFERENTIAL EQUATIONS
Numerical methods solve differential equations when exact analytical solutions are difficult or unavailable.
General initial-value problem:
    dy/dx = f(x,y)
    y(x0) = y0
Where:
x0 = initial independent variable.
y0 = initial condition.
 EULER'S METHOD;
The simplest numerical method for solving first-order differential equations.
Formula:
    y(n+1) = yn + h f(xn,yn)
    xn+1 = xn + h
Where h is the step size.
PROCEDURE:
1. Identify the differential equation.
2. Identify initial conditions.
3. Select a step size.
4. Evaluate the derivative at the current point.
5. Calculate the next value.
6. Repeat.
 MODIFIED EULER METHOD (HEUN'S METHOD);
Improves Euler's method using a predictor-corrector approach.
Predictor:
    y* = yn + h f(xn,yn)
Corrector:
    y(n+1) = yn + (h/2)[f(xn,yn)+f(xn+h,y*)]
 RUNGE-KUTTA FOURTH-ORDER METHOD (RK4);
A widely used method for accurately solving initial-value problems.
For:
    dy/dx = f(x,y)
Calculate:
    k1 = h f(xn,yn)
    k2 = h f(xn+h/2, yn+k1/2)
    k3 = h f(xn+h/2, yn+k2/2)
    k4 = h f(xn+h, yn+k3)
Then:
    y(n+1) = yn + (k1+2k2+2k3+k4)/6
Advantages:
- High accuracy for many smooth problems.
- Does not require higher derivatives.
- Widely used in engineering simulations.
 SYSTEMS OF DIFFERENTIAL EQUATIONS;
A system can be expressed as:
    dx/dt = f(t,x,y,...)
    dy/dt = g(t,x,y,...)
Numerical methods are applied to each equation simultaneously.
APPLICATIONS:
- Mechanical vibrations.
- Electrical circuit dynamics.
- Population and process modelling.
- Heat transfer.
- Fluid dynamics.
- Robotics and control systems.

    NUMERICAL OPTIMISATION
Numerical optimisation involves finding the maximum or minimum value of an objective function.
General form:
Minimise or maximise:
    f(x)
Subject to:
    g_i(x) ≤ 0
    h_j(x) = 0
 GOLDEN SECTION SEARCH;
A derivative-free method for finding a minimum or maximum of a unimodal function within an interval.
It repeatedly reduces the search interval using the golden ratio.
Golden ratio:
    φ = (1+√5)/2 ≈ 1.618
 GRADIENT DESCENT;
An iterative method for minimising a differentiable function.
Update formula:
    x(n+1) = xn - α∇f(xn)
Where:
α = learning rate or step size.
∇f = gradient of the objective function.
For one variable:
    x(n+1) = xn - αf'(xn)
 NEWTON'S OPTIMISATION METHOD;
For a single variable:
    x(n+1) = xn - f'(xn)/f''(xn)
For multiple variables:
    x(n+1) = xn - H⁻¹∇f(xn)
Where H is the Hessian matrix.
 CONSTRAINED OPTIMISATION;
Optimisation problems may include restrictions on available resources, dimensions, forces, costs or operating conditions.
Lagrange multiplier method:
    ∇f(x) = λ∇g(x)
For a single equality constraint g(x)=0.
APPLICATIONS:
- Engineering design.
- Minimising material and energy costs.
- Machine learning.
- Structural optimisation.
- Resource allocation.
- Process efficiency.

    NUMERICAL SOLUTION OF PARTIAL DIFFERENTIAL EQUATIONS
Partial differential equations (PDEs) involve unknown functions of two or more independent variables and their partial derivatives.
Numerical methods approximate their solutions over a computational domain.
 FINITE DIFFERENCE METHOD (FDM);
Approximates derivatives using differences between neighbouring grid points.
First derivative:
    ∂u/∂x ≈ [u(i+1)-u(i)]/Δx
Second derivative:
    ∂²u/∂x² ≈[u(i+1)-2u(i)+u(i-1)]/(Δx)²
Applications:
- Heat transfer.
- Fluid flow.
- Wave propagation.
- Electromagnetic field calculations.
 FINITE ELEMENT METHOD (FEM);
Divides a physical domain into smaller elements connected at nodes.
General procedure:
1. Discretise the domain into elements.
2. Select suitable interpolation or shape functions.
3. Formulate element equations.
4. Assemble the global system.
5. Apply boundary conditions.
6. Solve the resulting equations.
Applications:
- Structural stress analysis.
- Mechanical design.
- Thermal analysis.
- Electromagnetic modelling.
 FINITE VOLUME METHOD (FVM);
Divides a domain into control volumes and applies conservation laws to each volume.
It is particularly useful for conservation of:
- Mass.
- Momentum.
- Energy.
Applications:
- Computational fluid dynamics.
- Heat transfer.
- Fluid flow simulation.
 BOUNDARY CONDITIONS;
Common types:
-Dirichlet condition:
Specifies the value of the unknown function at the boundary.
-Neumann condition:
Specifies the derivative or flux at the boundary.
-Robin condition:
Specifies a combination of the function and its derivative.

    INTERPOLATION, REGRESSION AND CURVE FITTING
These methods are used to establish mathematical relationships between observed data.
 INTERPOLATION;
Estimates values within the range of available data points.
 EXTRAPOLATION;
Estimates values outside the range of available data points.
Extrapolation is generally less reliable because it extends beyond the known data.
 LEAST SQUARES REGRESSION;
Determines the mathematical model that minimises the sum of squared residuals.
For a linear model:
    y = mx + c
The least squares objective is:
    S = Σ[yi-(mxi+c)]²
Slope:
    m = [nΣxiyi-(Σxi)(Σyi)]/[nΣxi²-(Σxi)²]
Intercept:
    c = (Σyi-mΣxi)/n
 POLYNOMIAL REGRESSION;
Fits a polynomial to observed data.
    y = a0+a1x+a2x²+...+anx^n
 RESIDUAL;
Residual = Observed value - Predicted value
Residual analysis helps evaluate how well a model represents the data.
APPLICATIONS:
- Experimental engineering.
- Sensor calibration.
- Predictive modelling.
- Data analysis.
- Performance estimation.

    STABILITY, CONVERGENCE AND CONDITIONING
These concepts determine whether numerical results are dependable.
 CONVERGENCE;
A numerical method converges if its approximations approach the correct solution as the iteration count increases or the step size decreases, under the relevant assumptions.
 STABILITY;
A method is stable if small computational disturbances do not grow uncontrollably.
 CONDITIONING;
Conditioning describes the sensitivity of the mathematical problem itself to small changes in input data.
Condition number:
    κ(A) = ||A|| ||A⁻¹||
A large condition number indicates that a linear system may be sensitive to small perturbations.
 CONSISTENCY;
A numerical approximation is consistent if its local approximation error tends to zero as the discretisation step tends to zero.
 STEP SIZE;
The step size controls the spacing between numerical calculations.
A smaller step size often improves accuracy but increases computational cost.
Important:
Smaller step sizes do not automatically guarantee stability or better results for every numerical method.

    COMPUTATIONAL TOOLS FOR NUMERICAL METHODS
 MATLAB;
Used for:
- Matrix calculations.
- Numerical integration.
- Root finding.
- Differential equation solving.
- Engineering simulations.
 PYTHON;
Important libraries:
NumPy:
Numerical arrays, matrices and mathematical operations.
SciPy:
Scientific computing, optimisation, integration, interpolation and differential equations.
SymPy:
Symbolic mathematics, differentiation, integration and equation manipulation.
Matplotlib:
Plotting numerical results and analysing errors.
 EXCEL;
Used for:
- Numerical tables.
- Iterative calculations.
- Data interpolation.
- Regression.
- Basic numerical integration.
 APPLICATION-SPECIFIC SOFTWARE;
- ANSYS: engineering simulation and finite element analysis.
- COMSOL Multiphysics: multiphysics numerical modelling.
- OpenFOAM: computational fluid dynamics.

    IMPORTANT ENGINEERING APPLICATIONS
ELECTRICAL AND ELECTRONICS ENGINEERING:
- Circuit equation solving.
- Transient response calculations.
- Semiconductor modelling.
- Signal processing.
- Numerical circuit simulation.
MECHANICAL ENGINEERING:
- Vibration analysis.
- Heat transfer.
- Fluid mechanics.
- Structural analysis.
- Mechanical system simulation.
CIVIL ENGINEERING:
- Structural calculations.
- Finite element analysis.
- Soil and foundation modelling.
- Hydrological modelling.
ROBOTICS AND CONTROL:
- Robot motion simulation.
- Trajectory optimisation.
- Dynamic system modelling.
- Numerical integration of equations of motion.
- Sensor data processing.
AI AND MACHINE LEARNING:
- Gradient descent.
- Numerical optimisation.
- Regression.
- Approximation.
- Matrix computation.
EMBEDDED SYSTEMS:
- Sensor calibration.
- Digital filtering.
- Real-time numerical computation.
- Numerical integration in control algorithms.

    IMPORTANT PROBLEM-SOLVING AND EXAM TIPS
1. Identify the type of mathematical problem before selecting a numerical method.
2. For root finding:
   - Bisection: reliable but relatively slow.
   - Newton-Raphson: fast but requires derivatives.
   - Secant: does not require derivatives.
   - Fixed-point iteration: depends on the choice of rearrangement.
3. For simultaneous equations:
   - Gaussian elimination and LU decomposition are direct methods.
   - Jacobi and Gauss-Seidel are iterative methods.
4. For interpolation, determine whether data points are equally spaced before choosing Newton forward or backward interpolation.
5. For numerical differentiation, remember that central differences generally provide better accuracy than basic forward and backward differences.
6. For numerical integration:
   - Trapezoidal rule uses straight-line approximations.
   - Simpson's 1/3 rule uses quadratic approximations.
   - Simpson's 3/8 rule uses cubic approximations.
7. For differential equations:
   - Euler's method is simple but relatively less accurate.
   - Heun's method improves Euler's method.
   - RK4 is generally more accurate for smooth initial-value problems.
8. Always show iterations clearly in examination questions.
9. Maintain sufficient decimal places during calculations and round only the final answer.
10. Check convergence and stopping criteria before accepting an iterative solution.
11. Always include units in engineering calculations.
12. Verify numerical results by substitution, comparison with known solutions or independent computational methods whenever possible.