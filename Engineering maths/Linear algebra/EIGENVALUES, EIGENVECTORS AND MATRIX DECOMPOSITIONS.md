                EIGENVALUES, EIGENVECTORS AND MATRIX DECOMPOSITIONS
 EIGENVALUES AND EIGENVECTORS:
For a square matrix A, an eigenvector is a non-zero vector v whose direction remains unchanged after multiplication by A.
    Av = λv
Where:
A = square matrix
v = eigenvector
λ = eigenvalue
Rearranging:
    (A - λI)v = 0
For a non-trivial solution:
    det(A - λI) = 0
This is the characteristic equation.
Its roots are the eigenvalues.
 To find eigenvectors:
1. Determine eigenvalues from det(A - λI) = 0.
2. Substitute each eigenvalue into (A - λI)v = 0.
3. Solve for the corresponding eigenvector.
  PROPERTIES OF EIGENVALUES;
For an n × n matrix:
    Sum of eigenvalues = tr(A).
    Product of eigenvalues = det(A).
Eigenvalues of a triangular matrix are its diagonal elements.
If A is invertible:
    Eigenvalues of A⁻¹ are 1/λ.
    Eigenvalues of Aᵏ are λᵏ.
If A is symmetric and real:
• All eigenvalues are real.
• Eigenvectors corresponding to distinct eigenvalues are orthogonal.
  DIAGONALISATION;
Diagonalisation expresses a matrix in terms of a diagonal matrix.
    A = PDP⁻¹
Where:
P = matrix of linearly independent eigenvectors.
D = diagonal matrix of corresponding eigenvalues.
This is possible when A has enough linearly independent eigenvectors.
 Applications:
• Computing matrix powers.
• Solving systems of differential equations.
• Dynamic system analysis.
• Stability analysis.
  SINGULAR VALUE DECOMPOSITION (SVD);
Any real matrix A can be decomposed as:
    A = UΣVᵀ
Where:
U = orthogonal matrix of left singular vectors.
Σ = diagonal matrix of singular values.
V = orthogonal matrix of right singular vectors.
 Applications:
• Data compression.
• Noise reduction.
• Image processing.
• Principal component analysis.
• Solving ill-conditioned problems.
  ORTHOGONAL MATRICES;
A square matrix Q is orthogonal if:
    QᵀQ = QQᵀ = I
Therefore:
    Q⁻¹ = Qᵀ
Orthogonal matrices preserve vector lengths and angles.
 Applications:
Coordinate transformations, robotics, computer graphics and rotations.
  POSITIVE DEFINITE MATRICES;
A symmetric matrix A is positive definite if:
    xᵀAx > 0
For every non-zero vector x.
Positive semidefinite:
    xᵀAx ≥ 0
For every vector x.
 Applications:
Optimisation, energy functions, stability analysis and engineering system modelling.
  QUADRATIC FORMS;
A quadratic form is an expression of the form:
    Q(x) = xᵀAx
For example, for a symmetric 2 × 2 matrix:
    A = [a b; b c]
    Q(x) = ax₁² + 2bx₁x₂ + cx₂²
Quadratic forms are important in optimisation, mechanical energy, structural analysis and control systems.

ENGINEERING TIP:
Understand how eigenvalues describe system behaviour. In dynamic systems, eigenvalues are especially important for determining stability, natural frequencies and modes of vibration.