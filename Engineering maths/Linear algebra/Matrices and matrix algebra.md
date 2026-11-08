            MATRICES AND MATRIX ALGEBRA
A matrix is a rectangular arrangement of numbers in rows and columns.
    A = [aᵢⱼ]
Where:
i = row index
j = column index
Matrix order:
    m × n, where m is the number of rows and n is the number of columns.
Types of matrices:
• Row matrix: One row.
• Column matrix: One column.
• Square matrix: Equal number of rows and columns.
• Zero matrix: All elements are zero.
• Diagonal matrix: All off-diagonal elements are zero.
• Scalar matrix: Diagonal matrix with equal diagonal elements.
• Identity matrix: Diagonal elements are 1 and all others are 0.
• Symmetric matrix: Aᵀ = A.
• Skew-symmetric matrix: Aᵀ = -A.
• Triangular matrix: All entries above or below the main diagonal are zero.

 MATRIX OPERATIONS;
Addition and subtraction:
Matrices must have equal dimensions.
    A ± B = [aᵢⱼ ± bᵢⱼ]
Scalar multiplication:
    kA = [kaᵢⱼ]
Matrix multiplication:
If A is m × n and B is n × p, then AB is m × p.
    (AB)ᵢⱼ = Σ aᵢₖbₖⱼ
Important:
Matrix multiplication is generally not commutative.
    AB ≠ BA
However, it is associative:
    A(BC) = (AB)C
And distributive:
    A(B+C) = AB + AC

TRANSPOSE OF A MATRIX;
The transpose is obtained by interchanging rows and columns.
    (Aᵀ)ᵢⱼ = Aⱼᵢ
Properties:
(Aᵀ)ᵀ = A
(A+B)ᵀ = Aᵀ+Bᵀ
(AB)ᵀ = BᵀAᵀ

 DETERMINANTS;
A determinant is a scalar value associated with a square matrix.
For a 2 × 2 matrix:
    A = [a b; c d]
    det(A) = |A| = ad - bc
For a 3 × 3 matrix:
    |A| = a(ei-fh) - b(di-fg) + c(dh-eg)
Properties:
• det(Aᵀ) = det(A).
• det(AB) = det(A)det(B).
• det(I) = 1.
• Swapping two rows changes the determinant's sign.
• Multiplying a row by k multiplies the determinant by k.
• Equal or linearly dependent rows give determinant zero.
If det(A) ≠ 0, the matrix is non-singular.
If det(A) = 0, the matrix is singular.

 MATRIX INVERSE;
The inverse of a square matrix A is A⁻¹, satisfying:    
    AA⁻¹ = A⁻¹A = I
For a 2 × 2 matrix:
    A = [a b; c d]
    A⁻¹ = 1/(ad-bc) [d -b; -c a]
Provided det(A) ≠ 0.
General formula:
    A⁻¹ = adj(A)/det(A)
Where adj(A) is the adjugate (transpose of the cofactor matrix).
Properties:
(AB)⁻¹ = B⁻¹A⁻¹
(Aᵀ)⁻¹ = (A⁻¹)ᵀ
( A⁻¹ )⁻¹ = A

 TRACE AND RANK;
Trace:
Sum of the main diagonal elements of a square matrix.
    tr(A) = Σ aᵢᵢ
Rank:
The maximum number of linearly independent rows or columns.
Rank can be determined using row reduction or non-zero pivots.
Important:
    rank(A) ≤ min(m,n).

ENGINEERING APPLICATIONS:
Matrices are used in structural analysis, circuit equations, coordinate transformations, robotics, numerical methods, computer graphics, control systems and data modelling.