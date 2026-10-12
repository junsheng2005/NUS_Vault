# MA1513 --- Important MCQ Concepts and Relationships

> \[!info\] Revision Focus This note consolidates the concepts and
> relationships that repeatedly matter across the MA1513 MCQ/FIB papers
> and their worked solutions. Use it as a **relationship map**: many
> exam questions give one property and ask you to infer several others.

------------------------------------------------------------------------

# Chapter 1 --- Systems of Linear Equations and Matrices

## 1. Systems of Linear Equations

### 1.1 REF/RREF, Pivot Columns and Free Variables

For a linear system

$$
A\mathbf{x}=\mathbf{b},
$$

the augmented matrix is

$$
[A\mid \mathbf{b}].
$$

Important relationships:

-   A **pivot column in a variable column** corresponds to a basic
    variable.
-   A **non-pivot variable column** corresponds to a free variable.
-   Free variables are what allow infinitely many solutions when the
    system is consistent.
-   The augmented column must be treated differently from the variable
    columns.

> \[!important\] Common MCQ trap A non-pivot column in the **augmented
> matrix** does **not** automatically mean infinitely many solutions.
> The only non-pivot column could be the augmented column.

### 1.2 Consistency

A system is inconsistent if REF/RREF contains a row of the form

$$
\begin{bmatrix}
0 & 0 & \cdots & 0 & \mid & c
\end{bmatrix},
\qquad c\neq 0.
$$

Therefore:

$$
\text{pivot in augmented column}
\Longrightarrow
\text{inconsistent}.
$$

Conversely,

$$
\text{no pivot in augmented column}
\Longrightarrow
\text{consistent}.
$$

For a consistent system:

-   no free variables $\Rightarrow$ exactly one solution;
-   at least one free variable $\Rightarrow$ infinitely many solutions.

### 1.3 Homogeneous vs Non-Homogeneous Systems

For

$$
A\mathbf{x}=\mathbf{0},
$$

the system is always consistent because $\mathbf{x}=\mathbf{0}$ is
always a solution.

If a homogeneous system has a non-trivial solution, then it has
infinitely many solutions.

For a non-homogeneous system

$$
A\mathbf{x}=\mathbf{b},
$$

if $\mathbf{x}_p$ is a particular solution and $\mathbf{x}_h$ is any
solution of $A\mathbf{x}=\mathbf{0}$, then

$$
\mathbf{x}=\mathbf{x}_p+\mathbf{x}_h
$$

is a solution of $A\mathbf{x}=\mathbf{b}$.

Hence the general solution can be viewed as

$$
\boxed{\text{general solution}
=
\text{homogeneous part}
+
\text{particular solution}.}
$$

> \[!important\] Common MCQ trap Solutions of a non-homogeneous system
> are generally **not** closed under scalar multiplication or addition.

------------------------------------------------------------------------

## 2. Rank

For an $m\times n$ matrix,

$$
\operatorname{rank}(A)\leq \min(m,n).
$$

A matrix is **full rank** when

$$
\operatorname{rank}(A)=\min(m,n).
$$

Important cases:

### If $m<n$

A full-rank matrix has

$$
\operatorname{rank}(A)=m.
$$

There is room for the rank to increase if a suitable **row** is added,
but adding another column cannot increase the rank beyond $m$.

### If $m>n$

A full-rank matrix has

$$
\operatorname{rank}(A)=n.
$$

There is room for the rank to increase if a suitable **column** is
added, but adding another row cannot increase the rank beyond $n$.

### If $m=n$

A full-rank matrix already has maximum possible rank $n$.

Adding only one row or one column cannot increase its rank beyond $n$.

------------------------------------------------------------------------

## 3. Singular and Non-Singular Matrices

For an $n\times n$ matrix $A$, the following relationships are central:

$$
A\text{ is non-singular}
\Longleftrightarrow
A^{-1}\text{ exists}
$$

$$
\Longleftrightarrow
\det(A)\neq 0
$$

$$
\Longleftrightarrow
\operatorname{rank}(A)=n
$$

$$
\Longleftrightarrow
A\text{ has }n\text{ pivot columns}
$$

$$
\Longleftrightarrow
\operatorname{RREF}(A)=I_n
$$

$$
\Longleftrightarrow
A\mathbf{x}=\mathbf{0}\text{ has only the trivial solution}
$$

$$
\Longleftrightarrow
\operatorname{Null}(A)=\{\mathbf{0}\}
$$

$$
\Longleftrightarrow
\operatorname{nullity}(A)=0
$$

$$
\Longleftrightarrow
\text{columns of }A\text{ are linearly independent}
$$

$$
\Longleftrightarrow
\text{rows of }A\text{ are linearly independent}
$$

$$
\Longleftrightarrow
\operatorname{Col}(A)=\mathbb{R}^n
$$

$$
\Longleftrightarrow
\operatorname{Row}(A)=\mathbb{R}^n.
$$

For a singular matrix, the corresponding statements reverse:

$$
\det(A)=0,
\qquad
\operatorname{rank}(A)<n,
\qquad
\operatorname{nullity}(A)>0.
$$

Thus

$$
A\mathbf{x}=\mathbf{0}
$$

has non-trivial solutions.

### 3.1 Consistency and Non-Singularity

If $A$ is $n\times n$ and non-singular, then for every
$\mathbf{b}\in\mathbb{R}^n$,

$$
A\mathbf{x}=\mathbf{b}
$$

has exactly one solution:

$$
\mathbf{x}=A^{-1}\mathbf{b}.
$$

If $A$ is singular, there can be choices of $\mathbf{b}$ for which the
system is inconsistent.

------------------------------------------------------------------------

## 4. Matrix Inverses and Products

If $A$ and $B$ are non-singular square matrices, then

$$
AB
$$

is non-singular and

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

The order reverses.

Also,

$$
(A^T)^{-1}=(A^{-1})^T.
$$

If $A$ is non-singular, then

$$
A^k
$$

is non-singular for positive integers $k$.

> \[!important\] Common MCQ traps - $A+B$ need not be non-singular even
> if both $A$ and $B$ are non-singular. - $cA$ is singular when $c=0$. -
> Do not reverse the inverse-product rule incorrectly.

------------------------------------------------------------------------

## 5. Determinants of Matrices

### 5.1 Determinant and Singularity

$$
\boxed{\det(A)=0
\Longleftrightarrow
A\text{ is singular}.}
$$

Hence

$$
\det(A)=0
\Longleftrightarrow
\text{rows/columns are linearly dependent}.
$$

This means a determinant can often be evaluated without expansion by
spotting dependence.

### 5.2 Row/Column Operations

Swapping two rows:

$$
\det(B)=-\det(A).
$$

Multiplying one row by $c$:

$$
\det(B)=c\det(A).
$$

Adding a multiple of one row to another:

$$
\det(B)=\det(A).
$$

The same relationships apply to column operations.

### 5.3 Scalar Multiplication of the Whole Matrix

For an $n\times n$ matrix,

$$
\det(cA)=c^n\det(A).
$$

Do not confuse scaling **one row** with scaling the **entire matrix**.

### 5.4 Products, Inverses and Transposes

$$
\det(AB)=\det(A)\det(B)
$$

$$
\det(A^{-1})=\frac{1}{\det(A)}
$$

$$
\det(A^T)=\det(A).
$$

### 5.5 Triangular Matrices

For a triangular matrix,

$$
\det(A)
$$

is the product of the diagonal entries.

### 5.6 Linear Dependence Shortcut

If:

-   two rows are equal;
-   two columns are equal;
-   one row/column is a linear combination of the others;

then

$$
\det(A)=0.
$$

------------------------------------------------------------------------

# Chapter 2 --- Vector Space

## 6. Linear Combination and Linear Span

A vector $\mathbf{v}$ belongs to

$$
\operatorname{span}\{\mathbf{u}_1,\ldots,\mathbf{u}_k\}
$$

exactly when there exist scalars $c_1,\ldots,c_k$ such that

$$
\mathbf{v}
=
c_1\mathbf{u}_1+\cdots+c_k\mathbf{u}_k.
$$

This is equivalent to asking whether the system

$$
\begin{bmatrix}
\mathbf{u}_1&\cdots&\mathbf{u}_k
\end{bmatrix}
\mathbf{c}
=
\mathbf{v}
$$

is consistent.

Therefore:

$$
\boxed{\mathbf{v}\in\operatorname{span}(S)
\Longleftrightarrow
\text{the corresponding linear system is consistent}.}
$$

### 6.1 Equality of Spans

To show

$$
\operatorname{span}(S)=\operatorname{span}(T),
$$

show that every vector in $S$ can be generated by $T$ and every vector
in $T$ can be generated by $S$.

A useful shortcut is:

-   establish that both spans are the same subspace;
-   establish that they have the same dimension.

------------------------------------------------------------------------

## 7. Subspaces

A subset $V$ of $\mathbb{R}^n$ is a subspace when it satisfies the
required closure properties and contains the zero vector.

Important examples from the course include:

-   row spaces;
-   column spaces;
-   nullspaces;
-   solution spaces of homogeneous systems;
-   spans of vectors.

A plane through the origin can be represented as:

-   the span of two linearly independent vectors lying in the plane;
-   the solution space/nullspace of a homogeneous linear equation.

> \[!important\] Common MCQ trap A plane that does **not** pass through
> the origin is not a subspace of $\mathbb{R}^3$.

------------------------------------------------------------------------

## 8. Linear Independence

Vectors $\mathbf{v}_1,\ldots,\mathbf{v}_k$ are linearly independent if

$$
c_1\mathbf{v}_1+\cdots+c_k\mathbf{v}_k=\mathbf{0}
$$

has only

$$
c_1=\cdots=c_k=0.
$$

They are linearly dependent if a non-trivial solution exists.

### Immediate Dependence Tests

A set is automatically linearly dependent if:

-   it contains the zero vector;
-   one vector is a scalar multiple of another;
-   one vector is a linear combination of the others;
-   there are more than $n$ vectors in $\mathbb{R}^n$.

### Matrix Test

Stack the vectors as columns:

$$
A=
\begin{bmatrix}
\mathbf{v}_1&\cdots&\mathbf{v}_k
\end{bmatrix}.
$$

Then

$$
\{\mathbf{v}_1,\ldots,\mathbf{v}_k\}
\text{ is linearly independent}
$$

if and only if every column is a pivot column.

For $n$ vectors in $\mathbb{R}^n$,

$$
\text{linearly independent}
\Longleftrightarrow
\det(A)\neq0.
$$

------------------------------------------------------------------------

## 9. Basis and Dimension

A basis for a vector space $V$ must satisfy **both**:

$$
\boxed{\text{linearly independent + spans }V.}
$$

If

$$
\dim(V)=k,
$$

then every basis of $V$ contains exactly $k$ vectors.

Useful shortcuts:

-   $k$ linearly independent vectors in a $k$-dimensional space
    automatically form a basis.
-   $k$ vectors spanning a $k$-dimensional space automatically form a
    basis.

For $\mathbb{R}^n$, every basis contains exactly $n$ vectors.

------------------------------------------------------------------------

## 10. Row Space, Column Space and Nullspace

For a matrix $A$:

$$
\dim(\operatorname{Row}(A))
=
\dim(\operatorname{Col}(A))
=
\operatorname{rank}(A).
$$

The nullity satisfies the rank-nullity relationship:

$$
\boxed{\operatorname{rank}(A)+\operatorname{nullity}(A)=n}
$$

for an $m\times n$ matrix.

### 10.1 What Row Reduction Preserves

If $R=\operatorname{RREF}(A)$:

$$
\operatorname{Row}(R)=\operatorname{Row}(A)
$$

and

$$
\operatorname{Null}(R)=\operatorname{Null}(A).
$$

However, generally

$$
\operatorname{Col}(R)\neq\operatorname{Col}(A).
$$

To find a basis for $\operatorname{Col}(A)$:

1.  row reduce $A$;
2.  locate the pivot columns in the reduced matrix;
3.  take the **corresponding original columns of $A$**.

> \[!important\] High-yield distinction Use non-zero rows of REF/RREF
> for a basis of the **row space**, but use pivot positions to select
> columns from the **original matrix** for a basis of the column space.

------------------------------------------------------------------------

## 11. Coordinate Vectors

Let

$$
S=\{\mathbf{u}_1,\ldots,\mathbf{u}_n\}
$$

be a basis.

If

$$
\mathbf{v}
=
c_1\mathbf{u}_1+\cdots+c_n\mathbf{u}_n,
$$

then the coordinate vector of $\mathbf{v}$ with respect to $S$ is

$$
[\mathbf{v}]_S
=
\begin{bmatrix}
c_1\\
\vdots\\
c_n
\end{bmatrix}.
$$

Define the basis matrix

$$
P_S=
\begin{bmatrix}
\mathbf{u}_1&\cdots&\mathbf{u}_n
\end{bmatrix}.
$$

Then

$$
\boxed{\mathbf{v}=P_S[\mathbf{v}]_S.}
$$

Therefore,

$$
\boxed{[\mathbf{v}]_S=P_S^{-1}\mathbf{v}.}
$$

### 11.1 Change of Basis

If $S$ and $T$ are two bases, then

$$
\mathbf{v}=P_S[\mathbf{v}]_S=P_T[\mathbf{v}]_T.
$$

Hence

$$
\boxed{
[\mathbf{v}]_T
=
P_T^{-1}P_S[\mathbf{v}]_S.
}
$$

This relationship is especially useful for coordinate-vector FIB
questions.

------------------------------------------------------------------------

## 12. Orthogonality and Projection

Vectors $\mathbf{u}$ and $\mathbf{v}$ are orthogonal when

$$
\mathbf{u}\cdot\mathbf{v}=0.
$$

For projection onto a non-zero vector $\mathbf{u}$,

$$
\operatorname{proj}_{\mathbf{u}}\mathbf{v}
=
\frac{\mathbf{v}\cdot\mathbf{u}}
{\mathbf{u}\cdot\mathbf{u}}
\mathbf{u}.
$$

### 12.1 Projection onto a Subspace

If the columns of $A$ span a subspace, the projection $\mathbf{p}$ of
$\mathbf{b}$ onto $\operatorname{Col}(A)$ can be found through the
least-squares solution

$$
A^TA\hat{\mathbf{x}}=A^T\mathbf{b},
$$

then

$$
\boxed{\mathbf{p}=A\hat{\mathbf{x}}.}
$$

The residual

$$
\mathbf{r}=\mathbf{b}-\mathbf{p}
$$

is orthogonal to the column space:

$$
A^T\mathbf{r}=\mathbf{0}.
$$

Thus

$$
\boxed{
\mathbf{b}
=
\mathbf{p}
+
\mathbf{r},
\qquad
\mathbf{p}\in\operatorname{Col}(A),
\qquad
\mathbf{r}\perp\operatorname{Col}(A).
}
$$

------------------------------------------------------------------------

# Chapter 3 --- Linear Transformations, Eigenvalues and Diagonalization

## 13. Linear Transformations

For a linear transformation $T$,

$$
T(c_1\mathbf{u}+c_2\mathbf{v})
=
c_1T(\mathbf{u})+c_2T(\mathbf{v}).
$$

Therefore,

$$
T(\mathbf{0})=\mathbf{0}.
$$

If

$$
T:\mathbb{R}^n\to\mathbb{R}^m,
$$

then there is a standard matrix $A$ such that

$$
\boxed{T(\mathbf{x})=A\mathbf{x}.}
$$

### 13.1 Standard Matrix

Using the standard basis vectors,

$$
A=
\begin{bmatrix}
T(\mathbf{e}_1)&
T(\mathbf{e}_2)&
\cdots&
T(\mathbf{e}_n)
\end{bmatrix}.
$$

### 13.2 Images of a Basis Determine the Transformation

If

$$
S=\{\mathbf{u}_1,\ldots,\mathbf{u}_n\}
$$

is a basis for $\mathbb{R}^n$, then knowing

$$
T(\mathbf{u}_1),\ldots,T(\mathbf{u}_n)
$$

is enough to determine $T$ completely.

The stacking relationship is

$$
A
\begin{bmatrix}
\mathbf{u}_1&\cdots&\mathbf{u}_n
\end{bmatrix}
=
\begin{bmatrix}
T(\mathbf{u}_1)&\cdots&T(\mathbf{u}_n)
\end{bmatrix}.
$$

If the input matrix is invertible,

$$
\boxed{
A=
\begin{bmatrix}
T(\mathbf{u}_1)&\cdots&T(\mathbf{u}_n)
\end{bmatrix}
\begin{bmatrix}
\mathbf{u}_1&\cdots&\mathbf{u}_n
\end{bmatrix}^{-1}.
}
$$

------------------------------------------------------------------------

## 14. Eigenvalues and Eigenvectors

A non-zero vector $\mathbf{x}$ is an eigenvector of $A$ if

$$
A\mathbf{x}=\lambda\mathbf{x}.
$$

Then $\lambda$ is the corresponding eigenvalue.

### 14.1 Finding Eigenvalues

Eigenvalues satisfy

$$
\boxed{\det(A-\lambda I)=0.}
$$

### 14.2 Finding Eigenvectors

For each eigenvalue $\lambda$,

$$
(A-\lambda I)\mathbf{x}=\mathbf{0}.
$$

Thus the eigenspace is

$$
E_\lambda
=
\operatorname{Null}(A-\lambda I).
$$

### 14.3 Eigenvalue $0$

$$
0\text{ is an eigenvalue}
\Longleftrightarrow
A\text{ is singular}.
$$

This gives the chain

$$
0\text{ eigenvalue}
\Longleftrightarrow
\det(A)=0
\Longleftrightarrow
\operatorname{Null}(A)\neq\{\mathbf{0}\}.
$$

------------------------------------------------------------------------

## 15. Diagonalization

A matrix $A$ is diagonalizable when there is an invertible matrix $P$
and diagonal matrix $D$ such that

$$
\boxed{A=PDP^{-1}.}
$$

The columns of $P$ are linearly independent eigenvectors of $A$.

The corresponding diagonal entries of $D$ are their eigenvalues.

If

$$
P=
\begin{bmatrix}
\mathbf{v}_1&\mathbf{v}_2&\cdots&\mathbf{v}_n
\end{bmatrix},
$$

then

$$
D=
\begin{bmatrix}
\lambda_1&&0\\
&\ddots&\\
0&&\lambda_n
\end{bmatrix}
$$

where

$$
A\mathbf{v}_i=\lambda_i\mathbf{v}_i.
$$

> \[!important\] Ordering relationship The order of the eigenvalues in
> $D$ must match the order of their eigenvectors in $P$.

### 15.1 Key Diagonalizability Test

$$
\boxed{
A\text{ diagonalizable}
\Longleftrightarrow
A\text{ has }n\text{ linearly independent eigenvectors}.
}
$$

Distinct eigenvalues give linearly independent eigenvectors.

Therefore, an $n\times n$ matrix with $n$ distinct eigenvalues is
diagonalizable.

The converse is not required: a matrix can be diagonalizable even with
repeated eigenvalues.

### 15.2 Eigenspace Dimension and Multiplicity

For an eigenvalue $\lambda$,

$$
1
\leq
\dim(E_\lambda)
\leq
\text{multiplicity of }\lambda.
$$

For diagonalizability, the eigenspaces together must provide $n$
linearly independent eigenvectors.

### 15.3 Powers of a Diagonalizable Matrix

If

$$
A=PDP^{-1},
$$

then

$$
\boxed{A^k=PD^kP^{-1}.}
$$

This is especially useful for population/transition models.

------------------------------------------------------------------------

## 16. Population Models

A discrete population model can often be written as

$$
\mathbf{x}_{n+1}=A\mathbf{x}_n.
$$

Hence

$$
\mathbf{x}_n=A^n\mathbf{x}_0.
$$

If

$$
A=PDP^{-1},
$$

then

$$
\mathbf{x}_n=PD^nP^{-1}\mathbf{x}_0.
$$

Long-run behaviour is governed by the eigenvalues of $A$:

-   terms involving $|\lambda|<1$ decay;
-   an eigenvalue $\lambda=1$ can determine a steady-state component;
-   the corresponding eigenvector determines the long-run population
    ratio when applicable.

------------------------------------------------------------------------

# Chapter 4 --- Systems of Differential Equations

## 17. Converting Higher-Order ODEs to SDEs

For a higher-order ODE, introduce state variables such as

$$
y_1=y,
\qquad
y_2=y',
\qquad
y_3=y''.
$$

Then

$$
y_1'=y_2,
\qquad
y_2'=y_3,
$$

and use the original ODE to obtain $y_3'$.

This produces

$$
\mathbf{y}'=A\mathbf{y}.
$$

------------------------------------------------------------------------

## 18. Solutions of $\mathbf{y}'=A\mathbf{y}$

If $A$ has a real eigenvalue $\lambda$ with eigenvector $\mathbf{v}$,
then

$$
\boxed{
\mathbf{y}(t)=e^{\lambda t}\mathbf{v}
}
$$

is a solution.

With linearly independent eigenvectors
$\mathbf{v}_1,\ldots,\mathbf{v}_n$,

$$
\mathbf{y}(t)
=
c_1e^{\lambda_1t}\mathbf{v}_1
+\cdots+
c_ne^{\lambda_nt}\mathbf{v}_n.
$$

Initial conditions determine the constants.

------------------------------------------------------------------------

## 19. Phase Plane and Direction Fields

For

$$
\mathbf{y}'=A\mathbf{y},
$$

a point $\mathbf{y}$ in the phase plane has tangent/direction vector

$$
\boxed{\mathbf{y}'=A\mathbf{y}.}
$$

Therefore, to test a direction field:

1.  choose an easy point;
2.  compute $A\mathbf{y}$;
3.  compare its direction with the arrow shown at that point.

Eigenvectors give special straight-line trajectories because

$$
A\mathbf{v}=\lambda\mathbf{v}.
$$

Along an eigenvector direction,

$$
\mathbf{y}(t)=ce^{\lambda t}\mathbf{v}.
$$

------------------------------------------------------------------------

## 20. Real Eigenvalues and Equilibrium Classification

### 20.1 Distinct Real Eigenvalues, Same Sign

Both negative:

$$
\lambda_1<0,
\qquad
\lambda_2<0
$$

$\Rightarrow$ trajectories approach the origin.

This gives an **asymptotically stable node**.

Both positive:

$$
\lambda_1>0,
\qquad
\lambda_2>0
$$

$\Rightarrow$ trajectories move away from the origin.

This gives an **unstable node**.

### 20.2 Opposite Signs

$$
\lambda_1\lambda_2<0
$$

gives a **saddle point**.

A saddle is unstable.

One eigenvector direction approaches the origin while the other moves
away.

------------------------------------------------------------------------

## 21. Repeated Eigenvalues

Suppose a $2\times2$ matrix has repeated eigenvalue $\lambda$.

### Two linearly independent eigenvectors

There are enough eigenvectors to diagonalize the matrix.

In the special scalar-matrix case,

$$
A=\lambda I,
$$

every non-zero vector is an eigenvector and the phase portrait is a
**star node**.

### Only one linearly independent eigenvector

The matrix is not diagonalizable and the equilibrium is a **degenerate
node**.

Thus:

$$
\boxed{
\text{repeated eigenvalue}
+
\text{eigenspace information}
\Longrightarrow
\text{phase portrait classification}.
}
$$

------------------------------------------------------------------------

## 22. Complex Eigenvalues

For eigenvalues

$$
\lambda=\alpha\pm\beta i,
$$

the real part $\alpha$ controls growth/decay.

### If $\alpha<0$

The exponential factor

$$
e^{\alpha t}
$$

decays, so trajectories spiral towards the origin.

The equilibrium is asymptotically stable.

### If $\alpha>0$

The exponential factor grows, so trajectories spiral away from the
origin.

The equilibrium is unstable.

### If $\alpha=0$

There is no exponential growth or decay.

The trajectories form a centre/closed-loop behaviour in the
corresponding case.

> \[!important\] Key distinction The eigenvalues tell you whether the
> spiral moves **towards or away from the origin**, but the
> **clockwise/anti-clockwise direction** must be determined from the
> solution or direction field.

### 22.1 Determining Rotation Direction

For a solution involving sine and cosine, evaluate at a convenient value
such as $t=0$ and inspect the direction of motion from

$$
\mathbf{y}'=A\mathbf{y}
$$

or from the derivative of the given solution.

Do not infer clockwise/anti-clockwise motion from the eigenvalues alone.

------------------------------------------------------------------------

## 23. Equilibrium Points and Stability

An equilibrium point satisfies

$$
A\mathbf{y}=\mathbf{0}.
$$

Therefore the set of equilibrium points is

$$
\operatorname{Null}(A).
$$

Hence:

$$
A\text{ non-singular}
\Longrightarrow
\text{origin is the only equilibrium point}.
$$

If $A$ is singular,

$$
\operatorname{Null}(A)
$$

contains non-zero vectors, so there can be infinitely many equilibrium
points.

This links Chapter 4 directly back to Chapter 1:

$$
\boxed{
0\text{ eigenvalue}
\Longleftrightarrow
A\text{ singular}
\Longleftrightarrow
\operatorname{Null}(A)\neq\{\mathbf{0}\}
\Longleftrightarrow
\text{non-zero equilibrium points exist}.
}
$$

------------------------------------------------------------------------

## 24. Mass-Spring Systems

A mass-spring model

$$
my''+cy'+ky=0
$$

can be converted using

$$
y_1=y,
\qquad
y_2=y'.
$$

Then

$$
\begin{bmatrix}
y_1'\\
y_2'
\end{bmatrix}
=
\begin{bmatrix}
0&1\\
-\frac{k}{m}&-\frac{c}{m}
\end{bmatrix}
\begin{bmatrix}
y_1\\
y_2
\end{bmatrix}.
$$

Therefore the eigenvalues of

$$
A=
\begin{bmatrix}
0&1\\
-\frac{k}{m}&-\frac{c}{m}
\end{bmatrix}
$$

determine the qualitative motion.

Important connections:

-   real negative eigenvalues $\Rightarrow$ return to equilibrium
    without sustained oscillation;
-   complex eigenvalues with negative real part $\Rightarrow$ decaying
    oscillation;
-   phase-plane stability corresponds to the physical behaviour of the
    mass.

------------------------------------------------------------------------

# High-Yield Cross-Chapter Relationships

## 25. The Singularity Chain

One of the most important relationship chains in the module is

$$
\boxed{
\det(A)=0
}
$$

$$
\Updownarrow
$$

$$
\boxed{
A\text{ singular}
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\operatorname{rank}(A)<n
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\operatorname{nullity}(A)>0
}
$$

$$
\Updownarrow
$$

$$
\boxed{
A\mathbf{x}=\mathbf{0}
\text{ has non-trivial solutions}
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\text{columns of }A\text{ are linearly dependent}
}
$$

$$
\Updownarrow
$$

$$
\boxed{
0\text{ is an eigenvalue of }A
}
$$

and, for an SDE $\mathbf{y}'=A\mathbf{y}$,

$$
\Downarrow
$$

$$
\boxed{
\text{non-zero equilibrium points may exist}.
}
$$

------------------------------------------------------------------------

## 26. The Basis Chain

For a set of $n$ vectors in $\mathbb{R}^n$,

$$
\boxed{
\text{basis}
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\text{linearly independent}
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\text{spans }\mathbb{R}^n
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\text{matrix formed by the vectors is non-singular}
}
$$

$$
\Updownarrow
$$

$$
\boxed{
\det(A)\neq0.
}
$$

This connects Chapter 1 determinant questions directly to Chapter 2
basis questions.

------------------------------------------------------------------------

## 27. The Pivot--Rank--Dimension Chain

For a matrix $A$,

$$
\boxed{
\#\text{ pivot columns}
=
\operatorname{rank}(A)
}
$$

and

$$
\boxed{
\operatorname{rank}(A)
=
\dim(\operatorname{Col}(A))
=
\dim(\operatorname{Row}(A)).
}
$$

Also,

$$
\boxed{
\operatorname{nullity}(A)
=
n-\operatorname{rank}(A).
}
$$

Therefore, once the pivot structure is known, many dimension questions
can be answered immediately.

------------------------------------------------------------------------

## 28. The Eigenvector--Diagonalization--SDE Chain

$$
A\mathbf{v}=\lambda\mathbf{v}
$$

means $\mathbf{v}$ is an eigenvector.

Enough linearly independent eigenvectors give

$$
A=PDP^{-1}.
$$

This gives

$$
A^n=PD^nP^{-1}
$$

for discrete models and

$$
\mathbf{y}(t)
=
\sum_i c_ie^{\lambda_i t}\mathbf{v}_i
$$

for SDEs.

Therefore:

$$
\boxed{
\text{Eigenvalues/eigenvectors}
\rightarrow
\text{Diagonalization}
\rightarrow
\text{Population models and SDE solutions}.
}
$$

------------------------------------------------------------------------

## 29. Eigenvalues and Phase Portraits

For

$$
\mathbf{y}'=A\mathbf{y},
$$

the eigenvalues determine much of the qualitative behaviour:

  Eigenvalues                     Typical behaviour
  ------------------------------- --------------------------------
  Real, distinct, both negative   Stable node
  Real, distinct, both positive   Unstable node
  Real, opposite signs            Saddle
  Complex, negative real part     Stable spiral
  Complex, positive real part     Unstable spiral
  Pure imaginary                  Centre / closed-loop behaviour
  Repeated real                   Check eigenspace/eigenvectors

The eigenvectors determine important trajectory directions.

------------------------------------------------------------------------

# Fast MCQ Checklist

When you see a question about **REF/RREF**, immediately ask:

-   Where are the pivots?
-   Is the augmented column a pivot?
-   How many free variables?
-   What is the rank?
-   Is the system consistent?

When you see **$\det(A)=0$**, immediately think:

-   singular;
-   rank deficient;
-   linearly dependent rows/columns;
-   non-trivial nullspace;
-   eigenvalue $0$.

When you see **basis**, immediately check:

-   correct space;
-   correct number of vectors;
-   linearly independent;
-   spans the required space.

When you see **RREF and column space**, remember:

> Pivot positions come from RREF, but basis vectors for
> $\operatorname{Col}(A)$ come from the **original matrix**.

When you see **coordinate vector**, write

$$
\mathbf{v}=P_S[\mathbf{v}]_S.
$$

When you see **linear transformation**, use

$$
T(c_1\mathbf{u}_1+\cdots+c_k\mathbf{u}_k)
=
c_1T(\mathbf{u}_1)+\cdots+c_kT(\mathbf{u}_k).
$$

When you see **diagonalizable**, ask:

> Are there enough linearly independent eigenvectors?

When you see an **SDE phase portrait**, first inspect the eigenvalues:

-   signs of real eigenvalues;
-   sign of the real part of complex eigenvalues;
-   repeated eigenvalue and eigenspace dimension;
-   whether $0$ is an eigenvalue.

Then use the eigenvectors/direction field to determine trajectory
directions.

------------------------------------------------------------------------

# Highest-Priority Revision Relationships

If revision time is limited, make sure you can use these without
hesitation:

1.  $A$ non-singular
    $\Longleftrightarrow \det(A)\neq0 \Longleftrightarrow \operatorname{rank}(A)=n$.
2.  $A$ singular $\Longleftrightarrow A\mathbf{x}=0$ has non-trivial
    solutions.
3.  $\operatorname{rank}(A)+\operatorname{nullity}(A)=n$.
4.  Basis $=$ linearly independent $+$ spanning.
5.  Pivot positions in RREF identify which **original columns** form a
    basis for $\operatorname{Col}(A)$.
6.  $\mathbf{v}=P_S[\mathbf{v}]_S$ for coordinate vectors.
7.  Projection residual is orthogonal to the projection subspace.
8.  $T$ is completely determined by the images of a basis.
9.  $A\mathbf{v}=\lambda\mathbf{v}$ links eigenvalues/eigenvectors to
    transformations.
10. Diagonalizable $\Longleftrightarrow$ enough linearly independent
    eigenvectors.
11. $A=PDP^{-1}\Rightarrow A^n=PD^nP^{-1}$.
12. For SDEs, $\mathbf{y}=e^{\lambda t}\mathbf{v}$ comes from an
    eigenpair.
13. Signs/real parts of eigenvalues determine phase-plane stability.
14. $0$ eigenvalue $\Longleftrightarrow$ singular matrix
    $\Longleftrightarrow$ non-trivial nullspace.
15. Direction fields satisfy $\mathbf{y}'=A\mathbf{y}$ at every point.
