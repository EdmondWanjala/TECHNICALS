                SERIES AND TRANSFORMS

    SEQUENCES
A sequence is an ordered list of numbers arranged according to a specific mathematical rule.
Example:
    2, 4, 6, 8, 10, ...
Types:
- Finite sequence: has a fixed number of terms.
- Infinite sequence: continues indefinitely.
- Arithmetic sequence: has a constant difference between consecutive terms.
- Geometric sequence: has a constant ratio between consecutive terms.
  Arithmetic sequence:
    an = a + (n-1)d
Sum of n terms:
    Sn = n/2 [2a + (n-1)d]
Where:
a = first term
d = common difference
n = number of terms
  Geometric sequence:
    an = ar^(n-1)
Sum of n terms:
    Sn = a(1-r^n)/(1-r), r ≠ 1
Infinite geometric series (|r| < 1):
    S∞ = a/(1-r)

    INFINITE SERIES
A series is the sum of the terms of a sequence.
    Σan = a1 + a2 + a3 + ...
An infinite series converges if its partial sums approach a finite limit.
It diverges if its partial sums do not approach a finite limit.
Convergence is important in engineering because infinite series are used to approximate functions, solve differential equations and represent signals.
Necessary condition for convergence:
    lim(n→∞) an = 0
If the limit is not zero, the series diverges.
Important: A zero limit alone does not guarantee convergence.

    CONVERGENCE TESTS
  Geometric series test
    Σ ar^(n-1)
Converges when |r| < 1.
Diverges when |r| ≥ 1.
  Comparison test
Compare a positive-term series with another series whose convergence behaviour is known.
  Ratio test
    L = lim(n→∞) |a(n+1)/an|
- L < 1: absolutely convergent.
- L > 1: divergent.
- L = 1: inconclusive.
  Root test
    L = lim(n→∞) ⁿ√|an|
- L < 1: absolutely convergent.
- L > 1: divergent.
- L = 1: inconclusive.
  Integral test
If f(x) is positive, continuous and decreasing, then the corresponding series and improper integral have the same convergence behaviour.
  Alternating series test
For a series with alternating signs:
    Σ(-1)^(n-1)bn
It converges if:
- bn decreases monotonically.
- lim(n→∞) bn = 0.

    POWER SERIES
A power series is an infinite series involving powers of a variable.
    Σ an(x-c)^n
Expanded form:
    a0 + a1(x-c) + a2(x-c)² + ...
Where:
an = coefficients
x = variable
c = centre of the series.
-Radius of convergence (R):
Determines the range within which the power series converges.
Interval of convergence:
-The set of x-values for which the series converges.
For a power series:
    |x-c| < R
The endpoints must be tested separately.
Applications:
- Approximating mathematical functions.
- Solving differential equations.
- Numerical engineering calculations.
- Modelling physical systems.

    TAYLOR AND MACLAURIN SERIES
Taylor series represent a sufficiently differentiable function as an infinite polynomial expansion around a point.
Taylor series about x = a:
    f(x) = Σ[n=0 to ∞] [f⁽ⁿ⁾(a)/n!](x-a)^n
Expanded:
    f(x) = f(a) + f'(a)(x-a)+ f''(a)(x-a)²/2!+ f'''(a)(x-a)³/3! + ...
Maclaurin series:
A Taylor series centred at x = 0.
    f(x) = Σ[n=0 to ∞] [f⁽ⁿ⁾(0)/n!]x^n
Important standard expansions:
    e^x = 1 + x + x²/2! + x³/3! + ...
    sin x = x - x³/3! + x⁵/5! - ...
    cos x = 1 - x²/2! + x⁴/4! - ...
    ln(1+x) = x - x²/2 + x³/3 - x⁴/4 + ...
    1/(1-x) = 1 + x + x² + x³ + ...
These expansions are useful for approximating functions when exact calculations are difficult.

    FOURIER SERIES
Fourier series express a periodic function as a combination of sine and cosine functions.
A periodic function can be represented as:
    f(x) = a0/2 + Σ[n=1 to ∞][an cos(nx) + bn sin(nx)]
For a function with period 2π:
    an = (1/π) ∫[-π to π] f(x)cos(nx) dx
    bn = (1/π) ∫[-π to π] f(x)sin(nx) dx
    a0 = (1/π) ∫[-π to π] f(x) dx
  Types of symmetry:
Even function:
    f(-x) = f(x)
For even functions:
    bn = 0
Odd function:
    f(-x) = -f(x)
For odd functions:
    an = 0 and a0 = 0.
Important concepts:
- Fundamental frequency: lowest frequency of a periodic signal.
- Harmonics: integer multiples of the fundamental frequency.
- Amplitude: magnitude of a frequency component.
- Period: time or distance required for one complete cycle.
  Applications:
- Electrical signal analysis.
- AC circuit analysis.
- Vibration analysis.
- Heat transfer.
- Communication systems.
- Signal decomposition.

    FOURIER TRANSFORM
The Fourier transform converts a signal from the time or spatial domain into the frequency domain.
Continuous Fourier transform:
    X(ω) = ∫[-∞ to ∞] x(t)e^(-jωt)dt
Inverse Fourier transform:
    x(t) = (1/2π) ∫[-∞ to ∞] X(ω)e^(jωt)dω
Where:
x(t) = original signal.
X(ω) = frequency-domain representation.
ω = angular frequency in rad/s.
j = √(-1).
  Important properties:
Linearity:
    F{ax(t)+by(t)} = aX(ω)+bY(ω)
Time shifting:
    F{x(t-t0)} = e^(-jωt0)X(ω)
Time differentiation:
    F{dx(t)/dt} = jωX(ω)
Convolution:
    F{x(t)*h(t)} = X(ω)H(ω)
  Applications:
- Frequency analysis.
- Digital signal processing.
- Image processing.
- Communication engineering.
- Noise and filter analysis.

    LAPLACE TRANSFORM
The Laplace transform converts a function of time into a function of a complex variable s.
Definition (unilateral Laplace transform):
    F(s) = L{f(t)}
        = ∫[0 to ∞] f(t)e^(-st)dt
Where:
s = σ + jω
t = time.
F(s) = transformed function.
Common Laplace transforms:
    L{1} = 1/s
    L{t} = 1/s²
    L{t^n} = n!/s^(n+1)
    L{e^(at)} = 1/(s-a)
    L{sin(at)} = a/(s²+a²)
    L{cos(at)} = s/(s²+a²)
    L{sinh(at)} = a/(s²-a²)
    L{cosh(at)} = s/(s²-a²)
  Important properties:
Linearity:
    L{af(t)+bg(t)} = aF(s)+bG(s)
First derivative:
    L{f'(t)} = sF(s)-f(0)
Second derivative:
    L{f''(t)} = s²F(s)-sf(0)-f'(0)
Integration:
    L{∫[0 to t] f(τ)dτ} = F(s)/s
Time shifting:
    L{u(t-a)f(t-a)} = e^(-as)F(s)
Frequency shifting:
    L{e^(at)f(t)} = F(s-a)
Convolution:
    L{f*g} = F(s)G(s)
  Applications:
- Solving ordinary differential equations.
- Electrical circuit transient analysis.
- Control system modelling.
- Mechanical vibration analysis.
- System stability analysis.

    INVERSE LAPLACE TRANSFORM
The inverse Laplace transform converts a function in the s-domain back into the time domain.
    f(t) = L⁻¹{F(s)}
Common methods:
- Partial fraction decomposition.
- Direct use of standard transform tables.
- Completing the square.
- Using shifting properties.
- Convolution theorem.
  Partial fraction decomposition:
Example structure:
    F(s) = A/(s-a) + B/(s-b)
Determine A and B, then apply inverse transforms.
  Procedure for solving differential equations:
1. Take the Laplace transform of both sides.
2. Substitute initial conditions.
3. Rearrange to make the transformed unknown the subject.
4. Simplify using algebra and partial fractions.
5. Apply the inverse Laplace transform.
6. Obtain the time-domain solution.

    Z-TRANSFORM
The Z-transform is a mathematical tool used to analyse discrete-time signals and systems.
Bilateral Z-transform:
    X(z) = Σ[n=-∞ to ∞] x[n]z^(-n)
Unilateral Z-transform:
    X(z) = Σ[n=0 to ∞] x[n]z^(-n)
Where:
x[n] = discrete-time sequence.
z = complex variable.
X(z) = transformed sequence.
Common Z-transforms:
    Z{δ[n]} = 1
    Z{u[n]} = z/(z-1)
    Z{a^n u[n]} = z/(z-a)
For the last two expressions, the region of convergence is |z| > 1 and |z| > |a|, respectively.
  Important properties:
Linearity:
    Z{ax[n]+by[n]} = aX(z)+bY(z)
Time shifting:
    Z{x[n-k]} = z^(-k)X(z)
(for bilateral Z-transform)
First difference:
    Z{x[n]-x[n-1]} = (1-z^(-1))X(z)
Applications:
- Digital signal processing.
- Digital control systems.
- Discrete-time system analysis.
- Digital filters.
- Embedded systems.

    CONVOLUTION
Convolution is a mathematical operation used to determine the output of a linear time-invariant (LTI) system from its input and impulse response.
Continuous-time convolution:
    y(t) = x(t)*h(t)
    y(t) = ∫[-∞ to ∞] x(τ)h(t-τ)dτ
Discrete-time convolution:
    y[n] = Σ[k=-∞ to ∞] x[k]h[n-k]
Where:
x = input signal.
h = impulse response.
y = output signal.
  Important relationship:
Fourier transform:
    F{x*h} = X(ω)H(ω)
Laplace transform:
    L{x*h} = X(s)H(s)
Z-transform:
    Z{x*h} = X(z)H(z)
Applications:
- Digital filters.
- Signal processing.
- Image processing.
- Communication systems.
- System response calculations.

RELATIONSHIP BETWEEN FOURIER, LAPLACE AND Z-TRANSFORMS
FOURIER TRANSFORM:
- Mainly analyses frequency components of continuous-time signals.
- Useful for periodic and non-periodic signal analysis.
- Frequency-domain variable: jω.
LAPLACE TRANSFORM:
- Analyses continuous-time systems.
- Handles transient behaviour and initial conditions.
- Variable: s = σ+jω.
- Widely used in control and circuit analysis.
Z-TRANSFORM:
- Analyses discrete-time signals and systems.
- Used in digital signal processing and digital control.
- Variable: z.
Relationship:
Laplace transform:
    s = σ+jω
Fourier transform:
Obtained from the bilateral Laplace transform along the imaginary axis (s=jω), when the region of convergence includes that axis.
Z-transform:
A discrete-time counterpart of the Laplace transform.
Fourier analysis:
A special frequency-domain representation of signals.

    ENGINEERING APPLICATIONS OF SERIES AND TRANSFORMS
ELECTRICAL ENGINEERING:
- Fourier analysis of AC waveforms.
- Laplace analysis of RLC circuits.
- Transient and steady-state response.
- Harmonic analysis.
MECHANICAL ENGINEERING:
- Vibration analysis.
- Oscillatory motion.
- Mechanical system response.
- Heat transfer and differential equations.
CONTROL ENGINEERING:
- Transfer functions.
- Stability analysis.
- Feedback system analysis.
- System response and pole-zero analysis.
ELECTRONICS AND EMBEDDED SYSTEMS:
- Digital filtering.
- Signal sampling and reconstruction.
- Discrete-time signal processing.
- Noise reduction.
COMMUNICATION ENGINEERING:
- Modulation and demodulation.
- Frequency spectrum analysis.
- Bandwidth analysis.
- Signal transmission.
ROBOTICS:
- Dynamic system modelling.
- Sensor signal filtering.
- Motion and vibration analysis.
- Control system design.
AI AND COMPUTATIONAL ENGINEERING:
- Signal feature extraction.
- Frequency-domain data analysis.
- Numerical approximation.
- Time-series analysis.

    IMPORTANT PROBLEM-SOLVING TIPS
1. Identify whether the problem involves a sequence, finite series or infinite series.
2. For convergence questions, select the appropriate test instead of assuming every infinite series converges.
3. Memorise standard Taylor and Maclaurin expansions.
4. Check whether a function is even or odd before calculating Fourier coefficients. This can significantly reduce integration work.
5. In Fourier series, identify the fundamental period correctly.
6. For Laplace transforms, carefully apply initial conditions when transforming derivatives.
7. Master partial fraction decomposition because it is essential for inverse Laplace transforms.
8. Distinguish between continuous-time and discrete-time signals before selecting Laplace, Fourier or Z-transform methods.
9. For transform problems, always state the transform and inverse transform where required.
10. Pay attention to units:
   - Frequency: Hz.
   - Angular frequency: rad/s.
   - Period: seconds.
   - Time: seconds.
11. Remember that the Laplace transform is particularly useful for solving differential equations, while Fourier transforms are particularly useful for frequency analysis.
12. Practise both analytical calculations and computational implementations using MATLAB, Python (NumPy/SciPy) and appropriate signal-processing tools.