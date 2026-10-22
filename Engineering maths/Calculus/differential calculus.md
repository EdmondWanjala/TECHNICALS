                DIFFERENTIAL CALCULUS
Differential calculus studies derivatives, which measure how a function changes with respect to its independent variable.
The derivative represents the instantaneous rate of change or the slope of a tangent to a curve.
Engineering applications: Velocity, acceleration, optimization, sensitivity analysis, electrical signals, thermodynamics, and control-system modeling.

THE DERIVATIVE:
For y = f(x), the derivative is defined by:
    f′(x) = dy/dx = lim(h→0) [f(x + h) − f(x)]/h
The derivative exists when this limit exists as a finite number.
At a particular point x = a:
    f′(a) = lim(h→0) [f(a + h) − f(a)]/h
Higher derivatives:
    First derivative: dy/dx
    Second derivative: d²y/dx²
    Third derivative: d³y/dx³
    Nth derivative: dⁿy/dxⁿ

BASIC DIFFERENTIATION RULES:
Constant and Power Rules;
    d(c)/dx = 0
    d(xⁿ)/dx = nxⁿ⁻¹
    d[cf(x)]/dx = cf′(x)
    d/dx [f(x) ± g(x)] = f′(x) ± g′(x)
Product Rule;
    If y = uv:
    dy/dx = u(dv/dx) + v(du/dx)
Quotient Rule
    If y = u/v:
    dy/dx = [v(du/dx) − u(dv/dx)]/v²
    where v ≠ 0.
Chain Rule
    For y = f(g(x)):
    dy/dx = f′(g(x))g′(x)
Differentiate the outer function, keep the inner function unchanged, then multiply by the derivative of the inner function.
Example:
    y = (3x² + 1)⁵
    dy/dx = 5(3x² + 1)⁴(6x)
    = 30x(3x² + 1)⁴

STANDARD DERIVATIVES:
Algebraic and Exponential Functions;
    d(xⁿ)/dx = nxⁿ⁻¹
    d(eˣ)/dx = eˣ
    d(aˣ)/dx = aˣ ln(a), for a > 0
    d(ln x)/dx = 1/x, for x > 0
    d(logₐ x)/dx = 1/[x ln(a)]
More generally:
    d(ln|x|)/dx = 1/x, for x ≠ 0 
Trigonometric Functions
    d(sin x)/dx = cos x
    d(cos x)/dx = −sin x
    d(tan x)/dx = sec²x
    d(cot x)/dx = −csc²x
    d(sec x)/dx = sec x tan x   
    d(csc x)/dx = −csc x cot x
Angles must be in radians when using these derivative formulas.
Inverse Trigonometric Functions
    d(arcsin x)/dx = 1/√(1 − x²)
    d(arccos x)/dx = −1/√(1 − x²)
    d(arctan x)/dx = 1/(1 + x²)
These formulas apply within their appropriate domains.
Hyperbolic Functions
    d(sinh x)/dx = cosh x
    d(cosh x)/dx = sinh x
    d(tanh x)/dx = sech²x

IMPLICIT DIFFERENTIATION:
Used when x and y are related by an equation that is not conveniently expressed as y = f(x).
Differentiate both sides with respect to x, treating y as a function of x.
Example:
    x² + y² = 25
    2x + 2y(dy/dx) = 0
    dy/dx = −x/y
    For x = 3 and y = 4:
    dy/dx = −3/4

LOGARITHMIC DIFFERENTIATION
Useful for functions involving variable powers or complicated products.
Example:
    y = xˣ, x > 0
Take natural logarithms:
    ln y = x ln x
Differentiate:
    (1/y)(dy/dx) = ln x + 1
Therefore:  
    dy/dx = xˣ(ln x + 1)

PARAMETRIC DIFFERENTIATION
If x = x(t) and y = y(t):
    dy/dx = (dy/dt)/(dx/dt)
provided dx/dt ≠ 0.
Second derivative:
    d²y/dx² = [d/dt(dy/dx)]/(dx/dt)
Useful in motion analysis and curves defined by a time parameter.

HIGHER DERIVATIVES
The second derivative describes the rate of change of the first derivative.
    For displacement s(t):
    Velocity: v = ds/dt
    Acceleration: a = dv/dt = d²s/dt²
For a function y = f(x):
- f′(x) > 0: Increasing on the interval.
- f′(x) < 0: Decreasing on the interval.
- f″(x) > 0: Concave upward.
- f″(x) < 0: Concave downward.
A change in concavity may indicate an inflection point, but the sign change must be verified.

STATIONARY POINTS AND OPTIMIZATION
A stationary point occurs where f′(x) = 0.
Critical points can occur where f′(x) = 0 or where the derivative does not exist, provided the function itself is defined there.
 First-Derivative Test;
- Positive to negative derivative: Local maximum.
- Negative to positive derivative: Local minimum.
- No sign change: Neither a local maximum nor a local minimum.
 Second-Derivative Test;
At a stationary point x = a:
-If f′(a) = 0 and f″(a) > 0, there is a local minimum.
-If f′(a) = 0 and f″(a) < 0, there is a local maximum.
-If f″(a) = 0, the test is inconclusive.
For absolute maxima and minima on a closed interval, evaluate the function at all relevant critical points and endpoints.
 Engineering Applications;
Optimization can be used to:
- Minimize material cost.
- Maximize mechanical efficiency.
- Minimize energy consumption.
- Optimize dimensions and operating conditions.
- Find the maximum or minimum response of a system.

RELATED RATES
Related-rates problems involve quantities changing with time.
Differentiate the governing relationship with respect to time using the chain rule.
Example:
A circle has area A = πr².
    dA/dt = 2πr(dr/dt)
If r = 3 m and dr/dt = 0.2 m/s:
    dA/dt = 2π(3)(0.2)
    = 1.2π m²/s

TAYLOR AND MACLAURIN SERIES
Taylor series approximates a sufficiently smooth function near x = a:
    f(x) = f(a) + f′(a)(x − a) + [f″(a)/2!](x − a)² + ...
Maclaurin series is the special case a = 0.
Important expansions:
    eˣ = 1 + x + x²/2! + x³/3! + ...
    sin x = x − x³/3! + x⁵/5! − ...
    cos x = 1 − x²/2! + x⁴/4! − ...
    ln(1 + x) = x − x²/2 + x³/3 − ... for −1 < x ≤ 1, with endpoint convergence interpreted appropriately.
These expansions are useful for numerical approximation, error estimation, and modeling nonlinear systems near an operating point.

WORKED EXAMPLES
Example 1: Differentiate a polynomial
    y = 4x³ − 5x² + 2x − 7
    dy/dx = 12x² − 10x + 2
Example 2: Product rule
    y = x² sin x
    dy/dx = 2x sin x + x² cos x
Example 3: Optimization 
Find the stationary points of:
    f(x) = x² − 6x + 5
    f′(x) = 2x − 6
    Set f′(x) = 0:
    x = 3
    f″(x) = 2 > 0
Therefore, x = 3 is a minimum.
    f(3) = 9 − 18 + 5 = −4
    Minimum point: (3, −4)

PROBLEM-SOLVING TIPS
1. Identify the appropriate rule before differentiating.
2. Use the chain rule whenever one function is inside another.
3. Apply product and quotient rules carefully; they are not interchangeable.
4. Remember that d/dx of a constant is zero.
5. Use implicit differentiation when x and y are mixed in one equation.
6. Check whether stationary points are maxima, minima, or neither.
7. Include units when derivatives represent physical rates.
8. Use radians for trigonometric differentiation.
9. For optimization on a bounded interval, check endpoints as well as critical points.
10. Simplify the final expression where possible.