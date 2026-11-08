            VECTORS AND VECTOR SPACES
VECTORS:
A vector is a mathematical quantity having both magnitude and direction.
A scalar has magnitude only, while a vector has magnitude and direction.
Examples:
Scalars: Mass, temperature, time, energy.
Vectors: Force, velocity, acceleration, displacement.
A vector in three-dimensional space:
    A = a₁i + a₂j + a₃k
Or:
    A = [a₁, a₂, a₃]ᵀ
Magnitude:
    |A| = √(a₁² + a₂² + a₃²)
Unit vector:
    Â = A/|A|
  VECTOR OPERATIONS;
Addition:
    A + B = [a₁+b₁, a₂+b₂, a₃+b₃]
Subtraction:
    A - B = [a₁-b₁, a₂-b₂, a₃-b₃]
Scalar multiplication:
    kA = [ka₁, ka₂, ka₃]
Dot product (scalar product):
    A · B = a₁b₁ + a₂b₂ + a₃b₃
Also:
    A · B = |A||B|cos θ
Applications: Work, projections and determining angles between vectors.
Cross product (vector product):
    A × B = |A||B|sin θ n̂
For 3D vectors:
A × B =(a₂b₃-a₃b₂)i+ (a₃b₁-a₁b₃)j+ (a₁b₂-a₂b₁)k
Applications: Torque, angular momentum and magnetic force.

VECTOR SPACES:
A vector space is a set of vectors that satisfies the rules of vector addition and scalar multiplication.
  Important properties:
• Closure under addition and scalar multiplication.
• Existence of a zero vector.
• Existence of additive inverses.
• Associativity and commutativity of addition.
• Distributive properties of scalar multiplication.
  LINEAR COMBINATIONS AND SPAN;
A linear combination of vectors is:
    v = c₁v₁ + c₂v₂ + ... + cₙvₙ
The span of a set of vectors is the collection of all possible linear combinations of those vectors.
If the span covers the entire vector space, the vectors span that space.
  LINEAR INDEPENDENCE AND DEPENDENCE;
Vectors are linearly independent if:
    c₁v₁ + c₂v₂ + ... + cₙvₙ = 0
has only the trivial solution:
    c₁ = c₂ = ... = cₙ = 0.
Otherwise, they are linearly dependent.
  BASIS AND DIMENSION;
Basis:
A set of linearly independent vectors that spans a vector space.
Dimension:
The number of vectors in a basis.
Example:
The standard basis of R³ is:
e₁ = [1,0,0]ᵀ
e₂ = [0,1,0]ᵀ
e₃ = [0,0,1]ᵀ
Dimension = 3.
  SUBSPACES;
A subspace is a subset of a vector space that is itself a vector space under the same operations.
A non-empty subset is a subspace if:
• It contains the zero vector.
• It is closed under addition.
• It is closed under scalar multiplication.
  INNER PRODUCTS AND ORTHOGONALITY;
An inner product generalises the dot product.
For real vectors:
    ⟨u,v⟩ = uᵀv
Orthogonal vectors:
    uᵀv = 0
Orthogonal vectors meet at 90° when both are non-zero.
Orthonormal vectors are mutually orthogonal and each has unit magnitude.

ENGINEERING APPLICATIONS:
Vectors are essential in mechanics, robotics, computer graphics, electromagnetism, structural analysis, navigation and machine learning.