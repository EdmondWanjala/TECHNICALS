            SYSTEMS OF LINEAR EQUATIONS
A system of linear equations consists of two or more linear equations involving common unknown variables.
General form:
    a₁₁x₁ + a₁₂x₂ + ... + a₁ₙxₙ = b₁
    a₂₁x₁ + a₂₂x₂ + ... + a₂ₙxₙ = b₂
    ...
    aₘ₁x₁ + aₘ₂x₂ + ... + aₘₙxₙ = bₘ
Matrix representation:
    AX = B
Where:
A = coefficient matrix
X = vector of unknowns
B = constant vector

 METHODS OF SOLVING LINEAR SYSTEMS;
-SUBSTITUTION METHOD
Solve one equation for a variable and substitute into the remaining equations.
-ELIMINATION METHO
Multiply and add/subtract equations to eliminate variables systematically.
-GAUSSIAN ELIMINATION
Convert the augmented matrix [A|B] into row echelon form using elementary row operations.
 Allowed operations:
• Interchange two rows.
• Multiply a row by a non-zero scalar.
• Add a multiple of one row to another row.
Then use back-substitution to obtain unknowns.
-GAUSS-JORDAN ELIMINATION
Continue row reduction until the coefficient matrix becomes reduced row echelon form (RREF).
For a system with a unique solution:
    [A|B] → [I|X]
-MATRIX INVERSE METHOD
From:
    AX = B
Multiply both sides by A⁻¹:
    X = A⁻¹B
This method requires A to be square and non-singular.
-CRAMER'S RULE
For a square system with det(A) ≠ 0:       
    xᵢ = det(Aᵢ)/det(A)
Where Aᵢ is obtained by replacing the ith column of A with B.

 CONSISTENCY AND NUMBER OF SOLUTIONS;
For AX = B:
• Unique solution:
    rank(A) = rank([A|B]) = number of unknowns.
• Infinitely many solutions:
    rank(A) = rank([A|B]) < number of unknowns.
• No solution:
    rank(A) ≠ rank([A|B]).

 HOMOGENEOUS SYSTEMS;
A homogeneous system has the form:
    AX = 0
It always has the trivial solution:
    X = 0
Non-trivial solutions exist if:
    rank(A) < number of unknowns.
For a square matrix, this is equivalent to:
    det(A) = 0.

 LEAST-SQUARES METHOD;
Used when a system has more equations than unknowns or when exact solutions do not exist.
The objective is to minimise the sum of squared residuals:
    ||AX - B||²
For full column rank A, the least-squares solution is:
    X = (AᵀA)⁻¹AᵀB
Applications include data fitting, regression, measurement estimation and experimental analysis.

 NUMERICAL STABILITY;
Numerical methods can introduce rounding errors and computational inaccuracies.
Important concepts:
• Pivoting: Rearranging rows to improve numerical stability.
• Condition number: Measures sensitivity of a solution to small input changes.
• Ill-conditioned matrix: Small changes in input can produce large changes in output.
• Residual: Difference between the calculated and actual right-hand side.
Residual:
    r = B - AX
    
ENGINEERING TIP:
For hand calculations, Gaussian elimination and Gauss-Jordan elimination are especially important. For large computational systems, numerical algorithms are generally preferred over explicitly calculating matrix inverses.