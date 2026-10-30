                OPTIMIZATION
Optimization is the mathematical process of finding the best possible solution to a problem by maximizing or minimizing an objective function while satisfying given constraints.
Main objectives:
- Maximization: finding the largest possible value (e.g., maximum efficiency, output or profit).
- Minimization: finding the smallest possible value (e.g., minimum cost, energy consumption or material usage).
Applications:
- Engineering design and system performance.
- Production planning and resource allocation.
- Structural design and weight reduction.
- Robotics and trajectory planning.
- Machine learning and parameter estimation.
- Transportation and logistics.
- Energy management.

MATHEMATICAL FORMULATION OF AN OPTIMIZATION PROBLEM
A general optimization problem is expressed as:
Maximize or minimize:
        f(x)
Subject to:
    g_i(x) ≤ 0,  i = 1, 2, ..., m
    h_j(x) = 0,  j = 1, 2, ..., p
Where:
- f(x) = objective function.
- x = vector of decision variables.
- g_i(x) = inequality constraints.
- h_j(x) = equality constraints.
- m and p = number of inequality and equality constraints.
Decision variables: Unknown quantities whose values are to be determined.
Objective function: Mathematical expression representing what is to be maximized or minimized.
Constraints: Restrictions that a solution must satisfy.
Feasible solution: Any solution satisfying all constraints.
Feasible region: Set of all feasible solutions.
Optimal solution: Feasible solution giving the best objective-function value.

CLASSIFICATION OF OPTIMIZATION PROBLEMS
 Based on objective functions:
- Linear optimization: Objective and constraints are linear.
- Nonlinear optimization: At least one objective or constraint is nonlinear.
- Quadratic optimization: Objective function is quadratic, usually with linear constraints.
 Based on constraints:
- Unconstrained optimization: No explicit constraints.
- Constrained optimization: Subject to equality or inequality constraints.
 Based on decision variables:
- Continuous optimization: Variables can take any value within a range.
- Integer optimization: Variables must be integers.
- Binary optimization: Variables take only 0 or 1.
- Mixed-integer optimization: Contains both continuous and integer variables.
 Based on uncertainty:
- Deterministic optimization: All parameters are known.
- Stochastic optimization: Some parameters are uncertain or probabilistic.
- Robust optimization: Finds solutions that remain effective under uncertainty.

UNCONSTRAINED OPTIMIZATION
Unconstrained optimization involves finding the maximum or minimum of a function without explicit restrictions.
For a single-variable function:
    y = f(x)
First-order necessary condition for an interior optimum:
    f'(x) = 0
Second-order test:
    f''(x) > 0  → Local minimum.
    f''(x) < 0  → Local maximum.
    f''(x) = 0  → Test is inconclusive.
For multivariable functions:
    f(x₁, x₂, ..., xₙ)
The gradient is:
    ∇f(x) = [∂f/∂x₁, ∂f/∂x₂, ..., ∂f/∂xₙ]ᵀ
Stationary points satisfy:
    ∇f(x) = 0
The Hessian matrix is:
    H(x) = ∇²f(x)
It contains all second-order partial derivatives.
For a stationary point:
- Positive definite Hessian → Strict local minimum.
- Negative definite Hessian → Strict local maximum.
- Indefinite Hessian → Saddle point.
- Semidefinite Hessian → Test may be inconclusive.
For two variables:
    f(x,y)
Hessian determinant:
    D = fₓₓfᵧᵧ - (fₓᵧ)²
At a stationary point:
- D > 0 and fₓₓ > 0 → Local minimum.
- D > 0 and fₓₓ < 0 → Local maximum.
- D < 0 → Saddle point.
- D = 0 → Inconclusive.

CONSTRAINED OPTIMIZATION
Constrained optimization finds the best solution while satisfying specified restrictions.
 Equality constraints – LAGRANGE MULTIPLIERS
For optimizing:
    f(x,y)
Subject to:
    g(x,y) = 0
Construct the Lagrangian:
    L(x,y,λ) = f(x,y) + λg(x,y)
Set partial derivatives to zero:
    ∂L/∂x = 0
    ∂L/∂y = 0
    ∂L/∂λ = 0
Solve simultaneously to obtain candidate optimal points.
For n variables and multiple equality constraints:
    L(x,λ) = f(x) + Σ λᵢhᵢ(x)
 Inequality constraints – KKT CONDITIONS
Karush-Kuhn-Tucker (KKT) conditions are used in constrained nonlinear optimization.
For minimizing f(x), subject to:
    gᵢ(x) ≤ 0
    hⱼ(x) = 0
Using the Lagrangian:
    L = f(x) + Σ μᵢgᵢ(x) + Σ λⱼhⱼ(x)
The main KKT conditions are:
1. Stationarity:
   ∇f + Σ μᵢ∇gᵢ + Σ λⱼ∇hⱼ = 0
2. Primal feasibility:
   gᵢ(x) ≤ 0
   hⱼ(x) = 0
3. Dual feasibility:
   μᵢ ≥ 0
4. Complementary slackness:
   μᵢgᵢ(x) = 0
KKT conditions are necessary under suitable regularity conditions and are sufficient for global optimality in convex optimization.

LINEAR PROGRAMMING (LP)
Linear programming optimizes a linear objective function subject to linear constraints.
General form:
    Maximize or minimize:
            Z = c₁x₁ + c₂x₂ + ... + cₙxₙ
    Subject to:
        a₁₁x₁ + ... + a₁ₙxₙ ≤ b₁
        a₂₁x₁ + ... + a₂ₙxₙ ≤ b₂
        ...
        x₁, x₂, ..., xₙ ≥ 0
Important methods:
A. Graphical method:
- Formulate the objective function and constraints.
- Plot the constraint boundaries.
- Identify the feasible region.
- Determine its corner points.
- Evaluate the objective function at each corner.
- Select the point giving the best objective value.
Applicable mainly to two decision variables.
 Simplex method:
An iterative algorithm that moves between basic feasible solutions (corner points) to improve the objective function until optimality is reached.
Important terms:
- Basic variables: Variables included in the current basis.
- Non-basic variables: Variables set to zero in a basic solution.
- Slack variable: Added to a ≤ constraint to convert it into equality.
- Surplus variable: Subtracted from a ≥ constraint.
- Artificial variable: Introduced when necessary to obtain an initial basic feasible solution.
Common initialization methods:
- Big-M method.
- Two-phase simplex method.

NONLINEAR PROGRAMMING (NLP)
Nonlinear programming involves optimizing an objective function or constraints that contain nonlinear expressions.
General form:
    Minimize f(x)
    Subject to:
        gᵢ(x) ≤ 0
        hⱼ(x) = 0
Common methods:
 Gradient descent:
An iterative method for minimizing a differentiable function.
Update equation:
    xₖ₊₁ = xₖ - α∇f(xₖ)
Where:
- α = learning rate or step size.
- ∇f(xₖ) = gradient at the current point.
- k = iteration number.
 Newton's method:
    xₖ₊₁ = xₖ - [H(xₖ)]⁻¹∇f(xₖ)
Uses both gradient and Hessian information.
 Quasi-Newton methods:
Approximate the Hessian or its inverse to reduce computational cost.
Example: BFGS method.
 Conjugate gradient:
Uses conjugate search directions and is useful for large-scale problems.

CONVEX OPTIMIZATION
Convex optimization is a class of optimization problems in which the objective function is convex (for minimization) and the feasible region is convex.
A function f is convex if:
    f(λx + (1-λ)y) ≤ λf(x) + (1-λ)f(y)
For all x, y and 0 ≤ λ ≤ 1.
For twice-differentiable functions:
- Positive semidefinite Hessian → Convex function.
- Positive definite Hessian → Strictly convex function.
Important properties:
- Every local minimum of a convex function is a global minimum.
- A convex optimization problem has no inferior local minima.
- Convexity makes optimization more reliable and mathematically tractable.
Applications:
- Portfolio optimization.
- Machine learning.
- Power-system optimization.
- Signal processing.
- Engineering design.

INTEGER AND BINARY OPTIMIZATION
Integer programming requires some or all decision variables to be integers.
Binary optimization restricts variables to:
    xᵢ ∈ {0,1}
Applications:
- Selecting projects.
- Scheduling tasks.
- Facility location.
- Resource allocation.
- Equipment selection.
Common solution methods:
- Branch and bound.
- Cutting planes.
- Branch and cut.

MULTI-OBJECTIVE OPTIMIZATION
Involves optimizing two or more conflicting objectives simultaneously.
Example:
    Minimize cost: f₁(x)
    Minimize weight: f₂(x)
    Maximize efficiency: f₃(x)
A single solution may not optimize all objectives simultaneously.
Important concepts:
 Pareto optimality:
A solution is Pareto optimal if no objective can be improved without worsening at least one other objective.
 Pareto front:
Set of Pareto-optimal solutions representing trade-offs between objectives.
 Weighted-sum method:
    F(x) = w₁f₁(x) + w₂f₂(x) + ... + wₙfₙ(x)
Where:
- wᵢ = objective weights.
- Weights represent relative importance.

STOCHASTIC AND ROBUST OPTIMIZATION
 Stochastic optimization:
Deals with uncertain parameters represented by probability distributions or random variables.
Applications:
- Demand forecasting.
- Inventory management.
- Energy systems.
- Financial and risk analysis.
 Robust optimization:
Finds solutions that remain feasible and perform acceptably under a defined range of uncertainty.
Key distinction:
- Stochastic optimization models uncertainty probabilistically.
- Robust optimization protects against specified uncertain variations.

NUMERICAL OPTIMIZATION AND CONVERGENCE
Numerical optimization uses iterative computational algorithms to approximate optimal solutions.
Important concepts:
- Iteration: Repeated computational step toward a solution.
- Convergence: Process approaching a solution.
- Objective value: Value of the function being optimized.
- Gradient: Indicates direction of steepest increase.
- Search direction: Direction in which the algorithm moves.
- Step size: Distance moved during an iteration.
- Tolerance: Acceptable numerical error.
- Local optimum: Best solution within a neighbourhood.
- Global optimum: Best solution over the entire feasible region.
Common stopping criteria:
    ||∇f(xₖ)|| < ε
    ||xₖ₊₁ - xₖ|| < ε
    |f(xₖ₊₁) - f(xₖ)| < ε
Where ε is a small tolerance.

ENGINEERING APPLICATIONS OF OPTIMIZATION
- Mechanical engineering: Minimize component weight while maintaining strength.
- Electrical engineering: Minimize power losses and improve efficiency.
- Civil engineering: Optimize structural dimensions and material costs.
- Chemical engineering: Optimize temperature, pressure and production yield.
- Robotics: Find optimal trajectories and minimize energy consumption.
- Control engineering: Minimize tracking error and control effort.
- Computer engineering: Optimize processor performance and resource usage.
- Data science: Minimize prediction error during model training.
- Industrial engineering: Optimize production schedules and resource allocation.

IMPORTANT FORMULAS SUMMARY
First-order optimality:
    f'(x) = 0
Multivariable stationary condition:
    ∇f(x) = 0
Second derivative test:
    f''(x) > 0 → Minimum
    f''(x) < 0 → Maximum
Hessian:
    H(x) = ∇²f(x)
Lagrangian:
    L(x,λ) = f(x) + λg(x)
Gradient descent:
    xₖ₊₁ = xₖ - α∇f(xₖ)
Newton's method:
    xₖ₊₁ = xₖ - [H(xₖ)]⁻¹∇f(xₖ)
Linear objective:
    Z = cᵀx
Convexity:
    f(λx+(1-λ)y) ≤ λf(x)+(1-λ)f(y)

EXAMINATION AND PROBLEM-SOLVING TIPS
1. Identify whether the problem requires maximization or minimization.
2. Define all decision variables clearly.
3. Formulate the objective function correctly.
4. Identify and express all constraints mathematically.
5. Check whether the problem is linear, nonlinear, constrained or unconstrained.
6. For single-variable unconstrained problems, differentiate and solve f'(x)=0.
7. Apply the second derivative test to classify stationary points.
8. For equality constraints, construct the Lagrangian and solve the simultaneous equations.
9. For linear programming, identify the feasible region and evaluate the corner points.
10. For numerical methods, show the iteration formula, substitutions and convergence checks.
11. Check that the final solution satisfies every constraint.
12. Include appropriate units when variables represent physical quantities.
13. Distinguish between local and global optimality.
14. Do not assume that every stationary point is a maximum or minimum.

KEY TAKEAWAY:
Optimization provides mathematical methods for making the best engineering decisions under given objectives and constraints. 
Its central components are objective-function formulation, constraint modelling, optimality conditions, solution algorithms and interpretation of results.