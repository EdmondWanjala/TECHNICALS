            PARTIAL DIFFERENTIAL EQUATIONS (PDEs)
A PDE relates an unknown function of two or more independent variables to its partial derivatives.
Example:
    ∂u/∂t = α ∂²u/∂x²
Here, u = u(x,t) may represent temperature, displacement, pressure, or concentration.
Notation:
-u_x = ∂u/∂x
-u_t = ∂u/∂t
-u_xx = ∂²u/∂x²
-u_xy = ∂²u/(∂x∂y)
The order is the highest order of partial derivative present.

CLASSIFICATION OF SECOND-ORDER PDEs:
General two-variable second-order PDE:
    A u_xx + B u_xy + C u_yy + lower-order terms = f
Use the discriminant:
    D = B² - 4AC
-D < 0: Elliptic
-D = 0: Parabolic
-D > 0: Hyperbolic
Examples:
-Elliptic: Laplace equation.
-Parabolic: Heat equation.
-Hyperbolic: Wave equation.
Note: This classification assumes the coefficients and principal part are evaluated at the point of interest.

IMPORTANT ENGINEERING PDEs:
  Heat/diffusion equation:
    ∂u/∂t = α∂²u/∂x²
α = k/(ρc_p) for a homogeneous material under standard assumptions.
Applications: Heat conduction, diffusion, smoothing processes.
  Wave equation:
∂   ²u/∂t² = c²∂²u/∂x²
Applications: Vibrating strings, acoustic waves, elastic waves.
  Laplace equation:
    ∇²u = 0
In Cartesian coordinates:
    u_xx + u_yy = 0  (2D)
Applications: Steady-state heat conduction without internal heat generation, electrostatic potential in charge-free regions, incompressible potential flow.
  Poisson equation:
    ∇²u = f(x,y,z)
Applications: Electrostatic potential with charge sources and steady heat conduction with internal generation. The sign and scaling of f depend on the physical convention.

SEPARATION OF VARIABLES:
For a linear PDE, assume:
    u(x,t) = X(x)T(t)
Example: Heat equation
    u_t = αu_xx
Substitution gives:
    XT' = αX''T
Divide by αXT:
    T'/(αT) = X''/X = -λ
Hence:
    X'' + λX = 0
    T' + αλT = 0
Solutions:
    X'' + λX = 0
    T(t) = C e^(-αλt)
Boundary conditions determine allowed eigenvalues λ and eigenfunctions X.
For a fixed-end rod/string on 0 < x < L, common spatial eigenfunctions are:
    X_n(x) = sin(nπx/L)
Eigenvalues:
    λ_n = (nπ/L)²
The final solution is generally a series of modes:
    u(x,t) = Σ b_n sin(nπx/L)e^[-α(nπ/L)²t]
For heat conduction, coefficients b_n are obtained from the initial temperature distribution using a Fourier sine series.

FOURIER SERIES:
For a function on (-L,L):
    f(x) = a₀/2 + Σ[a_n cos(nπx/L) + b_n sin(nπx/L)]
Coefficients:
-a₀ = (1/L)∫₋Lᴸ f(x)dx
-a_n = (1/L)∫₋Lᴸ f(x)cos(nπx/L)dx
-b_n = (1/L)∫₋Lᴸ f(x)sin(nπx/L)dx
Use Fourier series to represent initial or boundary data as a sum of spatial modes.

METHOD OF CHARACTERISTICS:
For a first-order PDE:
    a(x,t,u)u_x + b(x,t,u)u_t = c(x,t,u)
Solve characteristic equations:
-dx/ds = a
-dt/ds = b
-du/ds = c
The PDE becomes a system of ODEs along characteristic curves.
For the transport equation:
    u_t + c u_x = 0
Solution:
    u(x,t) = f(x - ct)
The initial profile travels at speed c without changing shape.

INITIAL AND BOUNDARY CONDITIONS:
Initial condition:
    u(x,0) = f(x)
Dirichlet boundary condition:
    u specified on the boundary.
Neumann boundary condition:
    Normal derivative ∂u/∂n specified on the boundary.
Robin (mixed) boundary condition:
    a u + b ∂u/∂n = g
A PDE solution must satisfy the governing equation and the appropriate initial and boundary conditions.

NUMERICAL METHODS:
Finite difference method (FDM):
    Approximate derivatives using grid values.
Forward time difference:
    u_t ≈ (u_i^(n+1) - u_i^n)/Δt
Central spatial difference:
    u_xx ≈ (u_(i+1)^n - 2u_i^n + u_(i-1)^n)/(Δx)²
For the 1D heat equation, the explicit FTCS scheme is:
u_i^(n+1) = u_i^n + r(u_(i+1)^n - 2u_i^n + u_(i-1)^n)
where:
r = αΔt/(Δx)²
For the standard explicit 1D heat scheme, stability requires r ≤ 1/2.
Other methods:
- Finite element method (FEM): Especially useful for complex geometries and material properties.
- Finite volume method (FVM): Enforces conservation over control volumes.
- Crank-Nicolson: Implicit time-stepping method, second-order accurate in time for smooth solutions.

SOLUTION TIPS
- Classify the PDE before selecting a solution method.
- Identify whether the problem is steady-state or time-dependent.
- Apply boundary conditions to determine eigenvalues and eigenfunctions.
- Match the initial condition to determine Fourier coefficients.
- Check dimensional consistency.
- For numerical solutions, consider stability, convergence, grid resolution, and boundary implementation.