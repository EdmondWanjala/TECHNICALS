                INTEGRAL CALCULUS
Integral calculus studies accumulation, areas, volumes, and quantities obtained by summing infinitesimal contributions.
Integration is closely related to differentiation and is widely used to determine displacement, work, energy, mass, charge, fluid quantities, and total system response.
Engineering applications: Calculating areas, volumes, work, energy, electrical charge, fluid flow, and accumulated quantities.

INDEFINITE INTEGRATION
An indefinite integral represents a family of antiderivatives.
    ∫f(x) dx = F(x) + C
where:
    F′(x) = f(x)
C is the constant of integration.
  Basic Integration Rules;
Power rule:
    ∫xⁿ dx = xⁿ⁺¹/(n + 1) + C, for n ≠ −1
Constant rule:
    ∫k dx = kx + C
Sum and difference:
    ∫[f(x) ± g(x)]dx = ∫f(x)dx ± ∫g(x)dx
Constant multiple:
    ∫kf(x)dx = k∫f(x)dx
Special case:
    ∫(1/x)dx = ln|x| + C
  Standard Integrals;
Algebraic and exponential:
    ∫eˣ dx = eˣ + C
    ∫aˣ dx = aˣ/ln(a) + C, for a > 0 and a ≠ 1
    ∫ln x dx = x ln x − x + C, for x > 0
Trigonometric:
    ∫sin x dx = −cos x + C
    ∫cos x dx = sin x + C
    ∫sec²x dx = tan x + C
    ∫csc²x dx = −cot x + C
    ∫sec x tan x dx = sec x + C
    ∫csc x cot x dx = −csc x + C
Inverse-trigonometric forms:
    ∫dx/√(1 − x²) = arcsin x + C
    ∫dx/(1 + x²) = arctan x + C
These formulas assume appropriate domains and radians for trigonometric functions.

METHODS OF INTEGRATION:
  Substitution Method;
Used when an integral contains a function and its derivative.
    Let u = g(x).
    Then du = g′(x) dx.
Rewrite the integral in terms of u, integrate, and substitute back.
Example:
    ∫2x(x² + 1)³ dx
    Let u = x² + 1, so du = 2x dx.
    ∫u³ du = u⁴/4 + C
Answer:
    (x² + 1)⁴/4 + C
  Integration by Parts;
Derived from the product rule.
    ∫u dv = uv − ∫v du
Choose u and dv so the remaining integral is simpler.
Example:
    ∫x eˣ dx
    Choose u = x and dv = eˣ dx.
    Then du = dx and v = eˣ.
Answer:
    xeˣ − eˣ + C
  Partial Fractions;
Used to integrate suitable rational functions after factoring the denominator.
Example:
    1/[x(x + 1)] = 1/x − 1/(x + 1)
Therefore:
    ∫dx/[x(x + 1)] = ln|x| − ln|x + 1| + C
For rational functions, perform polynomial division first if the numerator degree is at least the denominator degree.
  Trigonometric Identities
Useful identities include:
    sin²x + cos²x = 1
    1 + tan²x = sec²x
    sin²x = [1 − cos(2x)]/2
    cos²x = [1 + cos(2x)]/2
Use identities to simplify powers or products before integrating.

  DEFINITE INTEGRATION
A definite integral measures signed accumulation over an interval.
    ∫ₐᵇ f(x) dx
    If F′(x) = f(x), the Fundamental Theorem of Calculus gives:
    ∫ₐᵇ f(x) dx = F(b) − F(a)
This is evaluated using an antiderivative and the upper and lower limits.
Properties:
    ∫ₐᵇ f(x)dx = −∫ᵦₐ f(x)dx
    ∫ₐᵃ f(x)dx = 0
    ∫ₐᵇ [f(x) + g(x)]dx = ∫ₐᵇ f(x)dx + ∫ₐᵇ g(x)dx
    ∫ₐᵇ f(x)dx = ∫ₐᶜ f(x)dx + ∫ᶜᵇ f(x)dx
For a continuous nonnegative function, the definite integral equals the area under its curve. For functions that change sign, it represents signed area.

AREA BETWEEN CURVES:
If f(x) lies above g(x) on [a, b]:
    A = ∫ₐᵇ [f(x) − g(x)]dx
If the curves cross, split the interval at the intersection points or integrate the absolute difference:
    A = ∫ₐᵇ |f(x) − g(x)|dx
For integration with respect to y:
    A = ∫₍c₎ᵈ [x_right(y) − x_left(y)]dy

VOLUMES OF SOLIDS:
  Disk Method;
For a solid formed by rotating a region about the x-axis:
    V = π∫ₐᵇ [f(x)]² dx
  Washer Method;
For an outer radius R(x) and inner radius r(x):
    V = π∫ₐᵇ [R(x)² − r(x)²]dx
  Cylindrical Shell Method;
For rotation about the y-axis, using vertical shells:
    V = 2π∫ₐᵇ x f(x) dx
when f(x) represents the shell height and the region is appropriately defined.
More generally:
    V = 2π∫ (radius)(height)(integration variable)
Always identify the radius, height, and axis of rotation before choosing a formula.

IMPROPER INTEGRALS:
An improper integral involves an infinite interval or an integrand that becomes unbounded in the integration interval.
Example:
    ∫₁^∞ 1/x² dx
    = lim(b→∞) ∫₁ᵇ x⁻² dx
    = lim(b→∞) [−1/x]₁ᵇ
    = 1
The integral converges because the limit is finite.
If the required limit does not exist or is infinite, the integral diverges.
An integral with an interior singularity must be split at the singular point and evaluated using the appropriate one-sided limits.

NUMERICAL INTEGRATION:
Used when an antiderivative is difficult to find or data are available only at discrete points.
  Trapezoidal Rule;
For n equal subintervals of width h = (b − a)/n:   
    ∫ₐᵇ f(x)dx ≈ (h/2)[y₀ + yₙ + 2Σyᵢ]
where the summation covers i = 1 to n − 1.
  Simpson's 1/3 Rule;
For an even number n of equal subintervals:
    ∫ₐᵇ f(x)dx ≈ (h/3)[y₀ + yₙ + 4Σyᵢ(odd i) + 2Σyᵢ(even i)]
The odd-indexed terms are weighted by 4, and the interior even-indexed terms by 2.
Simpson's rule is exact for polynomials of degree at most three under the standard composite-rule setup.

ENGINEERING APPLICATIONS:
  Displacement from Velocity;
If velocity v(t) is known:
    s(t) − s(t₀) = ∫ₜ₀ᵗ v(τ)dτ
  Distance from Speed;
Total distance traveled:
    D = ∫ₜ₀ᵗ |v(τ)|dτ
Unlike displacement, total distance does not cancel motion in opposite directions.
  Work;
For a variable force F(x) acting along a line:
    W = ∫ₐᵇ F(x)dx
For a spring obeying Hooke's law, F = kx in magnitude:
    W = ∫₀ˣ kx dx = ½kx²
  Charge from Current
If current varies with time:
    Q = ∫ₜ₁ᵗ₂ i(t)dt
  Mass from Density
For a one-dimensional object with linear density ρ(x):
    m = ∫ₐᵇ ρ(x)dx
For a three-dimensional object:
    m = ∫∫∫ᵥ ρ(x,y,z)dV

WORKED EXAMPLES:
Example 1: Indefinite integral
    ∫(3x² + 4x − 2)dx
    = x³ + 2x² − 2x + C
Example 2: Definite integral
    ∫₀² 3x² dx
    = [x³]₀²
    = 8 − 0
    = 8
Example 3: Area under a curve
Find the area under y = 2x from x = 0 to x = 3.
    A = ∫₀³ 2x dx   
    = [x²]₀³
    = 9 square units

PROBLEM-SOLVING TIPS:
1. Add + C to every indefinite integral.
2. Do not add + C to the final evaluation of a definite integral.
3. Verify an antiderivative by differentiating it.
4. Use substitution for composite functions.
5. Use integration by parts for suitable products.
6. Use partial fractions for suitable rational functions.
7. For area, ensure the integrand represents upper minus lower, or use an absolute difference.
8. For volume, identify the axis of rotation and the relevant radii.
9. For improper integrals, evaluate limits rather than substituting infinity directly.
10. Check units: integrating velocity over time gives displacement, while integrating force over distance gives work.