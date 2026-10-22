            ORDINARY DIFFERENTIAL EQUATIONS (ODEs)
An ordinary differential equation (ODE) relates an unknown function of one independent variable to its derivatives.
Example: 
    d²y/dx² + 3dy/dx + 2y = 0
Order: Highest derivative present.
Degree: Power of the highest-order derivative, provided the equation is polynomial in derivatives.
Linear ODE: The dependent variable and its derivatives appear only to the first power and are not multiplied together.
Nonlinear ODE: Contains nonlinear terms such as y², yy', sin(y), etc.
Homogeneous linear ODE: Has zero forcing term.
Nonhomogeneous linear ODE: Has a nonzero forcing term.
General nth-order linear ODE:
    a_n(x)y⁽ⁿ⁾ + ... + a_1(x)y' + a_0(x)y = f(x)
A general solution usually contains n arbitrary constants for an nth-order ODE.

FIRST-ORDER ODEs:
  Separable equations;
    dy/dx = g(x)h(y)
Separate variables
    dy/h(y) = g(x)dx
Integrate both sides
    ∫dy/h(y) = ∫g(x)dx + C
  Linear first-order equations;
    dy/dx + P(x)y = Q(x)
Integrating factor
    μ(x) = e^[∫P(x)dx]
Solution
    yμ = ∫μQ(x)dx + C
Hence
    y = [∫μQ dx + C]/μ
  Exact equations;
    M(x,y)dx + N(x,y)dy = 0
Exactness condition
    ∂M/∂y = ∂N/∂x
Find a potential function F(x,y) such that:
    ∂F/∂x = M and ∂F/∂y = N
Then:
    F(x,y) = C
  Homogeneous first-order equations;
    dy/dx = F(y/x)
Substitute:
    y = vx; dy/dx = v + x(dv/dx)
The equation becomes separable in x and v.
  Bernoulli equation;
    dy/dx + P(x)y = Q(x)yⁿ
For n ≠ 0,1, use:
    v = y^(1-n)
Then:
    dv/dx + (1-n)P(x)v = (1-n)Q(x)
This transforms the equation into a linear ODE.

SECOND-ORDER LINEAR ODEs:
Standard constant-coefficient form:
    ay'' + by' + cy = f(x)
First solve the homogeneous equation:
    ay'' + by' + cy = 0
Assume y = e^(rx). The characteristic equation is:
    ar² + br + c = 0
Case 1: Distinct real roots r₁, r₂;
    y_h = C₁e^(r₁x) + C₂e^(r₂x)
Case 2: Repeated real root r;
    y_h = (C₁ + C₂x)e^(rx)
Case 3: Complex roots α ± iβ;
    y_h = e^(αx)[C₁cos(βx) + C₂sin(βx)]
For a nonhomogeneous equation:
    y = y_h + y_p
where y_h is the complementary (homogeneous) solution and y_p is a particular solution.

METHODS FOR NONHOMOGENEOUS ODEs:
  Undetermined coefficients;
Use when f(x) consists of polynomials, exponentials, sines, cosines, or their finite sums.
Choose a trial y_p with the same general form as the forcing function.
If the trial overlaps with y_h, multiply it by x repeatedly until it is linearly independent.
  Variation of parameters
For y'' + P(x)y' + Q(x)y = R(x), let y₁ and y₂ be independent homogeneous solutions.
Wronskian:
    W = y₁y₂' - y₁'y₂
Particular solution:
    y_p = -y₁∫(y₂R/W)dx + y₂∫(y₁R/W)dx
  Reduction of order;
If one homogeneous solution y₁ is known, set:
    y = v(x)y₁(x)
Substitute into the ODE to obtain an equation for v.

CAUCHY-EULER EQUATION:
Standard form:
    ax²y'' + bxy' + cy = 0
Try:
    y = x^m
Characteristic equation:
    am(m-1) + bm + c = 0
Alternatively, use t = ln(x), for x > 0, to transform it into a constant-coefficient equation.

INITIAL AND BOUNDARY CONDITIONS:
  Initial-value problem (IVP);
Conditions specified at one point, e.g. y(x₀), y'(x₀).
  Boundary-value problem (BVP);
Conditions specified at different points, e.g. y(0), y(L).
For an nth-order ODE, n independent conditions are generally required to determine the constants uniquely.

LAPLACE TRANSFORM METHOD:
Definition;
    L{f(t)} = ∫₀∞ e^(-st)f(t)dt
Key formulas:
L{f'} = sF(s) - f(0)
L{f''} = s²F(s) - sf(0) - f'(0)
L{1} = 1/s
L{e^(at)} = 1/(s-a)
L{sin(at)} = a/(s²+a²)
L{cos(at)} = s/(s²+a²)
Procedure:
1. Transform the ODE.
2. Insert initial conditions.
3. Solve algebraically for Y(s).
4. Use partial fractions where appropriate.
5. Apply the inverse Laplace transform.

ENGINEERING APPLICATIONS:
Mass-spring-damper system:
    m x'' + c x' + kx = F(t)
Natural frequency:
    ω_n = √(k/m)
Damping ratio:
    ζ = c/(2√(mk))
    ζ < 1: Underdamped.
    ζ = 1: Critically damped.
    ζ > 1: Overdamped.
Electrical circuits:
 Series RLC circuit
    Lq'' + Rq' + q/C = V(t)
where q is charge and current i = q'.
Newton's law of cooling:
    dT/dt = -k(T - T_s)
Solution:
    T(t) = T_s + (T₀ - T_s)e^(-kt)

SOLUTION TIPS:
- Identify the order and linearity before choosing a method.
- For first-order equations, check separability, linearity, exactness, and Bernoulli form.
- For constant-coefficient linear ODEs, start with the characteristic equation.
- Apply initial or boundary conditions only after obtaining the general solution, unless they simplify the method.
- Verify by substituting the result into the original equation.
- Check units and physical meaning when interpreting engineering solutions.