                LIMITS AND CONTINUITY
Limits describe the value a function approaches as its input approaches a particular point. Continuity determines whether a function behaves without a break at that point.
Engineering applications: 
-Analyzing sensor response 
-signal behavior 
-control systems 
-physical models
-transitions between operating conditions.

LIMITS:
The notation
    lim(x→a) f(x) = L
means that f(x) approaches L as x approaches a.
The value of f(a) does not necessarily equal L, and f(a) may not even be defined.
  Types of Limits;
- Left-hand limit: lim(x→a⁻) f(x)
- Right-hand limit: lim(x→a⁺) f(x)
- Finite limit: The function approaches a finite number.
- Infinite limit: The function grows without bound positively or negatively.
- Limit at infinity: Describes behavior as x→∞ or x→−∞.
A two-sided limit exists if and only if the left-hand and right-hand limits exist and are equal.
    lim(x→a⁻) f(x) = lim(x→a⁺) f(x) = L
  Laws of Limits;
If lim(x→a) f(x) = L and lim(x→a) g(x) = M:
- Sum: lim(f + g) = L + M
- Difference: lim(f − g) = L − M
- Product: lim(fg) = LM
- Quotient: lim(f/g) = L/M, provided M ≠ 0
- Constant multiple: lim(cf) = cL
- Power: lim[f(x)]ⁿ = Lⁿ for integer n, subject to the expression being defined.
- Composition: lim h(f(x)) = h(L) when h is continuous at L.
For polynomials, substitute x = a directly.
For rational functions, direct substitution works if the denominator is nonzero.
  Indeterminate Forms;
Common indeterminate forms include:
    0/0, ∞/∞, 0 × ∞, ∞ − ∞, 0⁰, 1^∞, ∞⁰.
An indeterminate form does not determine the limit. Further analysis is required.
Methods for evaluating limits:
1. Direct substitution.
2. Factorization and cancellation.
3. Rationalization using conjugates.
4. Finding a common denominator.
5. Standard trigonometric limits.
6. L'Hôpital's rule when applicable.
7. Series expansions for sufficiently advanced problems.
  Important Standard Limits;
lim(x→0) sin(x)/x = 1
lim(x→0) tan(x)/x = 1
lim(x→0) [1 − cos(x)]/x² = 1/2
lim(x→0) (eˣ − 1)/x = 1
lim(x→0) ln(1 + x)/x = 1
lim(x→0) [(1 + x)^(1/x)] = e
Important: Trigonometric limits assume angles are measured in radians.
  L'Hôpital's Rule;
If a limit produces 0/0 or ∞/∞, and the required differentiability and other rule conditions hold:
    lim(x→a) f(x)/g(x) = lim(x→a) f′(x)/g′(x)
provided the derivative ratio limit exists or satisfies the rule's applicable extended-limit conditions.
Differentiate the numerator and denominator separately; do not apply the quotient rule to the ratio.
Other indeterminate forms must first be rewritten into an appropriate quotient if L'Hôpital's rule is to be used.
  Limits at Infinity;
For a rational function:
    f(x) = P(x)/Q(x)
Compare the degrees of the numerator and denominator.
- Degree of numerator < degree of denominator: limit is 0.
- Equal degrees: limit is the ratio of leading coefficients.
- Degree of numerator > degree of denominator: the function generally has no finite limit; determine the behavior using leading terms.
For example:
    lim(x→∞) (3x² + 1)/(2x² − 5) = 3/2
  Continuity;
A function f(x) is continuous at x = a if all three conditions hold:
1. f(a) is defined.
2. lim(x→a) f(x) exists.
3. lim(x→a) f(x) = f(a).
A function is continuous on an interval if it is continuous at every point in that interval, with one-sided continuity used at included endpoints.
  Types of Discontinuity;
- Removable: A hole in the graph; the finite limit exists, but the function value is missing or different.
- Jump: Left-hand and right-hand limits are finite but unequal.
- Infinite: The function becomes unbounded near a point, often producing a vertical asymptote.
- Oscillatory: The function does not approach a single value because it oscillates near the point.
Polynomials are continuous everywhere. Rational functions are continuous wherever their denominators are nonzero. Exponential and trigonometric functions are continuous throughout their domains.
  Worked Examples;
Example 1: Factorization
Evaluate:
    lim(x→2) (x² − 4)/(x − 2)
Factor:
    = lim(x→2) [(x − 2)(x + 2)]/(x − 2)
    = lim(x→2) (x + 2)
    = 4
The original expression is undefined at x = 2, but its limit exists.
Example 2: Continuity
Determine k such that
    f(x) = (x² − 1)/(x − 1), x ≠ 1
    f(1) = k
is continuous at x = 1.
For x ≠ 1:
    f(x) = x + 1
Therefore:
    lim(x→1) f(x) = 2
Continuity requires k = 2.
    Answer: k = 2
  Problem-Solving Tips;
1. Try direct substitution first.
2. If you obtain 0/0, factor or simplify before applying advanced methods.
3. Never cancel terms across addition; factor first.
4. Compare one-sided limits for piecewise functions.
5. Check all three continuity conditions.
6. For rational functions, identify excluded denominator values.
7. Use radians for standard trigonometric limits.
8. Distinguish a function's value at a point from the limit approaching that point.