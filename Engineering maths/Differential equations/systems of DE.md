            SYSTEMS OF DIFFERENTIAL EQUATIONS
A system of differential equations describes multiple interacting dependent variables.
General first-order system:
    dx₁/dt = f₁(t,x₁,...,xₙ)
    dx₂/dt = f₂(t,x₁,...,xₙ)
    dxₙ/dt = fₙ(t,x₁,...,xₙ)
Vector form:
    x' = f(t,x)
For a linear system:
    x' = A(t)x + g(t)
For a constant-coefficient homogeneous system:
    x' = Ax

MATRIX FORMULATION
Let:
    x = [x₁, x₂, ..., xₙ]ᵀ
A is an n×n coefficient matrix.
For x' = Ax, assume:
    x = ve^(λt)
Substitution gives:
    Av = λv
Therefore:
    (A - λI)v = 0
Characteristic equation:
    det(A - λI) = 0
The eigenvalues λ determine the modes of the system, while the eigenvectors v determine their directions.

SOLUTION FOR DISTINCT EIGENVALUES:
If A has n linearly independent eigenvectors v_i with eigenvalues λ_i:
    x(t) = Σ C_i v_i e^(λ_i t)
Determine constants C_i from the initial condition x(0) = x₀.
For complex eigenvalues, combine complex-conjugate solutions to obtain real-valued solutions when the system is real.

REPEATED EIGENVALUES:
If A does not have enough independent eigenvectors, generalized eigenvectors may be required.
For a Jordan block with eigenvalue λ, solutions can contain terms such as:
    e^(λt), te^(λt), t²e^(λt), ...
The powers of t depend on the Jordan block size.

NONHOMOGENEOUS SYSTEMS:
For:
    x' = Ax + g(t)
The general solution is:
    x(t) = e^(At)x₀ + ∫₀ᵗ e^[A(t-s)]g(s)ds
where e^(At) is the matrix exponential.
If g(t) = 0:
    x(t) = e^(At)x₀
The matrix exponential can be calculated using eigenvalue decomposition, Jordan form, or numerical algorithms.

STABILITY OF LINEAR SYSTEMS:
For the continuous-time system x' = Ax:
- All eigenvalues have negative real parts: asymptotically stable.
- At least one eigenvalue has positive real part: unstable.
- Eigenvalues with zero real parts require further analysis; their presence alone does not establish stability.
For a stable system, free-response modes decay with time.
For a mechanical system, eigenvalues often describe oscillation frequencies and damping.

CONVERTING A HIGHER-ORDER ODE TO A FIRST-ORDER SYSTEM:
Consider:
    y'' + a y' + b y = f(t)
Define:
    x₁ = y
    x₂ = y'
Then:
    x₁' = x₂
    x₂' = -b x₁ - a x₂ + f(t)
Matrix form:
    x' = Ax + g(t)
    A = [[0, 1], [-b, -a]]
    g(t) = [0, f(t)]ᵀ
This form is convenient for numerical integration and state-space modelling.

ENGINEERING APPLICATIONS:
  Coupled mechanical systems;
    M q'' + C q' + Kq = F(t)
M = mass matrix
C = damping matrix
K = stiffness matrix
q = displacement vector
Convert to first-order state-space form for simulation and control.
  Electrical networks;
Use Kirchhoff's laws to form coupled equations for capacitor voltages and inductor currents.
  Chemical and thermal systems;
Coupled reaction rates, species concentrations, and temperatures form nonlinear systems.
  Population and interacting processes;
dx/dt = ax - bxy
dy/dt = -cy + dxy
Such models describe interacting populations or other coupled processes, depending on parameter interpretation.

STATE-SPACE MODEL:
Control systems often use;
    x' = Ax + Bu
    y = Cx + Du
x = state vector
u = input vector
y = output vector
A = system matrix
B = input matrix
C = output matrix
D = direct-feedthrough matrix
The state-space model supports simulation, stability analysis, feedback control, and observer design.

SOLUTION TIPS:
- Convert higher-order equations to first-order form when using state-space or numerical methods.
- Check matrix dimensions before multiplication.
- Compute eigenvalues and eigenvectors carefully.
- Apply the initial vector to determine constants.
- Examine eigenvalue real parts for stability.
- Verify the final solution by substituting into x' = Ax + g(t).