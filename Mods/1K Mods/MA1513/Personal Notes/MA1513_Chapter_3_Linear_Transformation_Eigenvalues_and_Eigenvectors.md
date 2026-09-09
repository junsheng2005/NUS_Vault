# MA1513 — Chapter 3: Linear Transformation, Eigenvalues and Eigenvectors

> [!summary] Chapter overview
> This chapter treats matrices as transformations and develops **linear transformations, eigenvalues and eigenvectors, eigenspaces, diagonalizable matrices, diagonalization, and powers of matrices**. It ends by applying powers of matrices to an iterative population model.

---

## 3.1 Linear Transformation

### 3.1.1 Matrix as a Mapping

A matrix can be viewed as a mapping that transforms an input vector into an output vector through matrix multiplication.

For the $2 \times 2$ case in the notes,

$$
T : R^2 \to R^2
$$

defined by

$$
T(u)=Au \text{ for all } u \text{ in } R^2.
$$

The resulting vector $Au$ is the **output vector**, or the **image** of $u$.

### 3.1.2 Linear Transformation

For the example in the notes, the geometrical effect of the transformation is a **90° counterclockwise rotation about the origin**. The diagram of the letter F makes this effect visible.

![[Attachments/Linear Transformation Geometry.png]]

### 3.1.3 $m \times n$ Linear Transformation

For a general $m \times n$ matrix $A$:

- the input vector must be an $n$-vector;
- the output vector $Au$ is an $m$-vector;
- the domain is $R^n$;
- the codomain is $R^m$.

The transformation is written as

$$
T : R^n \to R^m
$$

defined by

$$
T(u)=Au \text{ for all } u \in R^n.
$$

$A$ is called the **standard matrix** of the linear transformation.

### 3.1.4 Linear Transformation by Formula

The notes consider

$$
T : R^2 \to R^3
$$

with

$$
T\left(\begin{bmatrix}x\\y\end{bmatrix}\right)
=
\begin{bmatrix}x+y\\2x\\-3y\end{bmatrix}.
$$

Rewrite the output as

$$
x\begin{bmatrix}1\\2\\0\end{bmatrix}
+y\begin{bmatrix}1\\0\\-3\end{bmatrix}.
$$

The two vectors form the columns of the standard matrix

$$
A=
\begin{bmatrix}
1&1\\
2&0\\
0&-3
\end{bmatrix}.
$$

### 3.1.5 Images of Standard Basis

Let $T : R^n \to R^m$ have standard matrix $A$.

If the standard basis vectors are used as inputs, the image of each basis vector gives the corresponding column of $A$.

> [!important]
> The image $T(e_k)$ is the $k$th column of $A$ and
>
> $$
> A=(T(e_1)\ T(e_2)\ \cdots\ T(e_n)).
> $$

### 3.1.6 Properties of Linear Transformation

If $T : R^n \to R^m$ is a linear transformation, then

$$
T(0)=0
$$

$$
T(u+v)=T(u)+T(v)
$$

$$
T(cu)=cT(u)
$$

and

$$
T(c_1u_1+c_2u_2+\cdots+c_ku_k)
=c_1T(u_1)+c_2T(u_2)+\cdots+c_kT(u_k).
$$

These are the **linearity properties** of a linear transformation.

The worked example in the notes shows that if the images of two vectors forming a basis for $R^2$ are known, the standard basis vectors can be written as linear combinations of that basis. The linearity property then gives $T(e_1)$ and $T(e_2)$, from which the standard matrix can be recovered.

### 3.1.7 Stacking Method

The **stacking method** gives a shortcut when the images of a basis are known.

In the worked example,

$$
A\begin{bmatrix}1\\1\end{bmatrix}
=\begin{bmatrix}4\\2\end{bmatrix}
$$

and

$$
A\begin{bmatrix}1\\-1\end{bmatrix}
=\begin{bmatrix}0\\6\end{bmatrix}.
$$

Stack the two input vectors and the two output vectors as columns:

$$
A
\begin{bmatrix}
1&1\\
1&-1
\end{bmatrix}
=
\begin{bmatrix}
4&0\\
2&6
\end{bmatrix}.
$$

Since the two input column vectors are linearly independent, the matrix is non-singular. Hence

$$
A=
\begin{bmatrix}
4&0\\
2&6
\end{bmatrix}
\begin{bmatrix}
1&1\\
1&-1
\end{bmatrix}^{-1}
=
\begin{bmatrix}
2&2\\
4&-2
\end{bmatrix}.
$$

![[Attachments/Stacking Method.jpg]]

### 3.1.8 Images of a Basis

Given a linear transformation $T : R^n \to R^m$ and a basis $\{u_1,u_2,\ldots,u_n\}$ for $R^n$, any $v$ in $R^n$ can be written as

$$
v=c_1u_1+c_2u_2+\cdots+c_nu_n.
$$

Therefore

$$
T(v)=c_1T(u_1)+c_2T(u_2)+\cdots+c_nT(u_n).
$$

Knowing $T(u_1),T(u_2),\ldots,T(u_n)$ is enough to determine:

- the image $T(v)$ of any vector $v$ in $R^n$;
- the standard matrix of $T$;
- the formula of $T$.

> [!important]
> The linear transformation $T$ is completely determined by the images of a basis for $R^n$.

---

## 3.2 Eigenvalues and Eigenvectors

### 3.2.1 Eigenvalues and Eigenvectors

Let $A$ be an $n \times n$ square matrix and let $x$ be a nonzero vector in $R^n$.

If $Ax$ is a scalar multiple of $x$, then $x$ is an **eigenvector** of $A$.

The lecturer emphasizes that this is a **special situation**: for a general input vector, the input and output need not be scalar multiples of each other. Whether a vector is an eigenvector also depends on the particular square matrix $A$.

$$
Ax=\lambda x
$$

![[Attachments/Eigenvector_Visualization.jpg]]

The scalar $\lambda$ is the corresponding **eigenvalue**.

Geometrically, in 2- or 3-spaces, the arrows representing $x$ and $Ax$ are parallel and point either in the same or opposite directions.

If $x$ is an eigenvector associated with eigenvalue $\lambda$, then for any non-zero scalar $k$, $kx$ is also an eigenvector associated with the same eigenvalue:

$$
A(kx)=kAx=k\lambda x=\lambda(kx).
$$

> [!important]
> 1. $0$ can be an eigenvalue, but the zero vector $0$ cannot be an eigenvector.
> 2. Two eigenvectors that are not scalar multiples of each other may have the same eigenvalue.

### 3.2.2 Finding Eigenvalues without Eigenvectors

Eigenvalues can be found without first knowing the eigenvectors by solving

$$
\det(\lambda I-A)=0.
$$

For the matrix used in the notes,

$$
\det(\lambda I-A)=\lambda^2-1.95\lambda+0.95.
$$

The solutions are

$$
\lambda=1 \text{ and } 0.95.
$$

> [!important] Lecturer summary: ways to find eigenvalues
> - If an eigenvector is given, multiply it by the matrix and identify the scalar in $Au=\lambda u$.
> - If the eigenvector is not given, solve the characteristic equation $\det(\lambda I-A)=0$.
> - For a triangular matrix, the eigenvalues are the diagonal entries.
> - The lecture also states that if $\lambda$ is an eigenvalue of $A$, then $\lambda$ is an eigenvalue of $A^T$, $\lambda^k$ is an eigenvalue of $A^k$, and $\lambda^{-1}$ is an eigenvalue of $A^{-1}$ when $A$ is non-singular.

### 3.2.3 Characteristic Polynomial

For an $n \times n$ square matrix $A$,

$$
\det(\lambda I-A)
$$

is a polynomial of degree $n$, called the **characteristic polynomial** of $A$.

The relationship used in the notes is

$$
\lambda \text{ is an eigenvalue of } A
\Leftrightarrow \det(\lambda I-A)=0
\Leftrightarrow \lambda \text{ is a root of the characteristic polynomial}.
$$

The reasoning begins with

$$
Ax=\lambda x
$$

for some nonzero column vector $x$, which gives

$$
(\lambda I-A)x=0.
$$

For a non-trivial solution to exist, the coefficient matrix $\lambda I-A$ must be singular, so

$$
\det(\lambda I-A)=0.
$$

### 3.2.4 Triangular Matrices

> [!important]
> If $A$ is a triangular matrix, the eigenvalues of $A$ are all the diagonal entries of $A$.
>
> In particular, the eigenvalues of a diagonal matrix are its diagonal entries.

### 3.2.5 Eigenvalue and Singularity

The notes establish

$$
0 \text{ is an eigenvalue of } A
\Leftrightarrow A \text{ is singular}.
$$

This follows through

$$
0 \text{ is an eigenvalue of } A
\Leftrightarrow \det(0I-A)=0
\Leftrightarrow \det(-A)=0
\Leftrightarrow \det(A)=0
\Leftrightarrow A \text{ is singular}.
$$

### 3.2.6 Matrix with Complex Eigenvalues

A characteristic polynomial may have complex roots.

For the example in the notes,

$$
\det(\lambda I-A)=\lambda^2+1,
$$

with roots

$$
\lambda=\pm i.
$$

The corresponding eigenvectors have complex components.

---

## 3.3 Eigenspaces

### 3.3.1 Eigenspace

The lecture connects this directly back to Chapter 2: an eigenspace is a **solution space of a homogeneous system**, so the same approach used previously to find a basis for a solution space is used here.

![[Attachments/Eigenvalue_Eigenvector_Workflow.jpg]]

Suppose $\lambda$ is an eigenvalue of an $n \times n$ square matrix $A$. Then

$$
(\lambda I-A)x=0
$$

has non-trivial solutions.

All non-trivial solutions are eigenvectors of $A$ associated with $\lambda$.

The solution space of this homogeneous system is the **eigenspace** of $A$ associated with $\lambda$, denoted by $E_\lambda$.

![[Attachments/Eigenvalue Workflow.jpg]]

For the matrix $A$ used in the notes, the eigenvalues are $1$ and $0.95$.

For $\lambda=1$, solving

$$
(I-A)x=0
$$

gives

$$
\begin{bmatrix}x\\y\end{bmatrix}
=
\begin{bmatrix}0.25t\\t\end{bmatrix}
=t\begin{bmatrix}0.25\\1\end{bmatrix}.
$$

Hence

$$
E_1=\operatorname{span}\left\{\begin{bmatrix}0.25\\1\end{bmatrix}\right\}.
$$

For $\lambda=0.95$,

$$
E_{0.95}=\operatorname{span}\left\{\begin{bmatrix}-1\\1\end{bmatrix}\right\}.
$$

The notes also show an example where an eigenspace has two basis vectors. For the matrix $B$ and eigenvalue $0$,

$$
E_0=\operatorname{span}\left\{
\begin{bmatrix}-1\\1\\0\end{bmatrix},
\begin{bmatrix}-1\\0\\1\end{bmatrix}
\right\}.
$$

### 3.3.2 Eigenspace of Identity Matrix

For the $3 \times 3$ identity matrix $I_3$:

1. the only eigenvalue is $1$;
2. there is only one eigenspace $E_1$;
3. the eigenspace is $R^3$.

For any vector $v$ in $R^3$,

$$
I_3v=v.
$$

Thus any non-zero 3-vector in $R^3$ is an eigenvector associated with eigenvalue $1$.

### 3.3.3 Multiplicity of Eigenvalues

The **multiplicity** of an eigenvalue is the power of its corresponding factor in the characteristic polynomial.

Examples from the notes include

$$
\det(\lambda I-A)=(\lambda-1)(\lambda-0.95),
$$

$$
\det(\lambda I-B)=(\lambda-3)\lambda^2,
$$

and

$$
\det(\lambda I-I)=(\lambda-1)^3.
$$

### 3.3.4 Dimension of Eigenspace

The lecturer highlights that **multiplicity** and **dimension of the eigenspace** are different quantities. They can be equal, but the dimension cannot be greater than the multiplicity.

![[Attachments/Multiplicity_and_Eigenspace_Dimension.jpg]]

Suppose

$$
\det(\lambda I-A)
=(\lambda-\lambda_1)^{r_1}(\lambda-\lambda_2)^{r_2}\cdots(\lambda-\lambda_k)^{r_k}.
$$

Then $\lambda_1$ to $\lambda_k$ are the eigenvalues and $r_1$ to $r_k$ are their respective multiplicities.

For an $n \times n$ matrix,

$$
r_1+r_2+\cdots+r_k=n
$$

and

$$
\dim E_{\lambda_i}\le r_i \text{ for all } i.
$$

> [!warning]
> The dimension of an eigenspace can equal the multiplicity of the corresponding eigenvalue, but this is **not true in general**.

---

## 3.4 Diagonalizable Matrices

### 3.4.1 Power of Matrix

The notes motivate diagonalization by considering powers of a square matrix.

If

$$
A=PDP^{-1},
$$

then

$$
A^n=(PDP^{-1})^n.
$$

Using the associative law and cancelling the intermediate products $P^{-1}P$ gives

$$
A^n=PD^nP^{-1}.
$$

> [!warning]
> The notes specifically point out that
>
> $$
> (PDP^{-1})^n\ne P^nD^nP^{-n}.
> $$

For a diagonal matrix, raising the matrix to power $n$ means raising its diagonal entries to power $n$.

### 3.4.2 Diagonalizable Matrix

A square matrix $A$ is called **diagonalizable** if a non-singular matrix $P$ can be found such that

$$
P^{-1}AP
$$

is a diagonal matrix.

Writing the diagonal matrix as $D$,

$$
P^{-1}AP=D.
$$

Equivalently,

$$
A=PDP^{-1}.
$$

The matrix $P$ is said to **diagonalize** $A$.

### 3.4.3 Non-diagonalizable Matrix

Not every square matrix is diagonalizable. The notes give an example of a matrix $M$ for which no non-singular matrix $P$ can make $P^{-1}MP$ diagonal.

The example is presented as an ad hoc argument; the following sections develop a systematic method for deciding diagonalizability.

### 3.4.4 Diagonalizability

The examples compare matrices that are diagonalizable with one that is not. The deciding issue is not simply the number of eigenvalues, but whether there are enough **linearly independent eigenvectors**.

### 3.4.5 Diagonalizability and Eigenvectors

> [!important]
> Let $A$ be an $n \times n$ square matrix.
>
> If $A$ has $n$ linearly independent eigenvectors, then $A$ is diagonalizable.

If $n$ linearly independent eigenvectors cannot be found, then $A$ is not diagonalizable.

![[Attachments/Diagonalizability Example.jpg]]

### 3.4.6 Two Useful Observations

**Observation 1**

If the columns of $B$ are $b_1,b_2,\ldots,b_n$, then

$$
AB=A(b_1\ b_2\ \cdots\ b_n)
=(Ab_1\ Ab_2\ \cdots\ Ab_n).
$$

**Observation 2**

If $D$ is diagonal with diagonal entries $d_1,d_2,\ldots,d_n$, then

$$
BD=(b_1\ b_2\ \cdots\ b_n)D
=(d_1b_1\ d_2b_2\ \cdots\ d_nb_n).
$$

### 3.4.7 Diagonalizability and Eigenvectors — Optional Reading

Let $u_1,u_2,\ldots,u_n$ be $n$ linearly independent eigenvectors with corresponding eigenvalues $\lambda_1,\lambda_2,\ldots,\lambda_n$.

Form

$$
P=(u_1\ u_2\ \cdots\ u_n).
$$

Since the columns are linearly independent, $P$ is non-singular.

Then

$$
AP=(Au_1\ Au_2\ \cdots\ Au_n)
=(\lambda_1u_1\ \lambda_2u_2\ \cdots\ \lambda_nu_n).
$$

Using the second observation, the right-hand side is $PD$. Hence

$$
AP=PD
$$

and therefore

$$
P^{-1}AP=D.
$$

This shows why $n$ linearly independent eigenvectors make $A$ diagonalizable.

---

## 3.5 Diagonalization

### 3.5.1 Algorithm for Diagonalization

For an $n \times n$ square matrix $A$:

1. Solve the characteristic polynomial
   $$
   \det(\lambda I-A)
   $$
   to find all distinct eigenvalues $\lambda_1,\lambda_2,\ldots,\lambda_k$.
2. For each $\lambda_i$, find a basis $S_{\lambda_i}$ for the eigenspace $E_{\lambda_i}$ by solving
   $$
   (\lambda_iI-A)x=0.
   $$
3. Let
   $$
   S=S_{\lambda_1}\cup S_{\lambda_2}\cup\cdots\cup S_{\lambda_k}.
   $$
4. Compare $|S|$ with $n$:
   - if $|S|<n$, then $A$ is not diagonalizable;
   - if $|S|=n$, then $A$ is diagonalizable.
5. If
   $$
   S=\{u_1,u_2,\ldots,u_n\},
   $$
   form
   $$
   P=(u_1\ u_2\ \cdots\ u_n).
   $$
   Then $P$ diagonalizes $A$.

![[Attachments/Diagonalization Example.jpg]]

The diagonal matrix contains the eigenvalues corresponding to the eigenvectors used as the columns of $P$.

> [!important]
> Matrix $P$ is not unique. Scalar multiples of the eigenvectors may be used as long as the chosen columns remain linearly independent. The columns may also be reordered, with the diagonal entries reordered accordingly.

### 3.5.2 Dimension of Eigenspace

Recall

$$
\det(\lambda I-A)
=(\lambda-\lambda_1)^{r_1}(\lambda-\lambda_2)^{r_2}\cdots(\lambda-\lambda_k)^{r_k},
$$

with

$$
r_1+r_2+\cdots+r_k=n
$$

and

$$
\dim E_{\lambda_i}\le r_i \text{ for all } i.
$$

The notes separate two cases:

- If
  $$
  \dim E_{\lambda_i}=r_i \text{ for all } i,
  $$
  then $A$ is diagonalizable.
- If
  $$
  \dim E_{\lambda_i}<r_i
  $$
  for at least one $i$, then $A$ is not diagonalizable.

### 3.5.3 Matrix with Maximum Distinct Eigenvalues

> [!important]
> Let $A$ be an $n \times n$ square matrix. If $A$ has $n$ distinct eigenvalues, then $A$ is diagonalizable.

When the $n$ eigenvalues are distinct, their corresponding eigenvectors are linearly independent, giving the required $n$ linearly independent eigenvectors.

The notes also emphasize that the converse need not hold: a diagonalizable matrix need not have $n$ distinct eigenvalues. A diagonal matrix is already diagonalizable even when some diagonal entries repeat.

---

## 3.6 Powers of Matrices

### 3.6.1 Iterative Systems

An iterative system has stages represented by

$$
x_0,x_1,x_2,\ldots
$$

with consecutive stages related by a fixed matrix $A$:

$$
x_k=Ax_{k-1}.
$$

Therefore

$$
x_1=Ax_0,
$$

$$
x_2=A^2x_0,
$$

and in general

$$
x_n=A^nx_0.
$$

### 3.6.2 Power of Diagonalizable Matrices

For a diagonalizable matrix $A$, if

$$
P^{-1}AP=D,
$$

then powers of $A$ can be analysed using the corresponding powers of the diagonal matrix.

The notes use this to obtain a simple way to compute large powers of a diagonalizable matrix by matrix multiplication involving $P$, the powered diagonal matrix, and $P^{-1}$.

### 3.6.3 Population Modeling

The population is divided into rural and urban populations. Every year:

- $4\%$ of the rural population moves to the urban area;
- $1\%$ of the urban population moves to the rural area.

The current populations are $40,000$ rural and $60,000$ urban.

Let

- $a_n$ = rural population after $n$ years;
- $b_n$ = urban population after $n$ years.

Then

$$
A=
\begin{bmatrix}
0.96&0.01\\
0.04&0.99
\end{bmatrix}
$$

and

$$
x_n=
\begin{bmatrix}
a_n\\b_n
\end{bmatrix}.
$$

The iterative relation is

$$
x_n=Ax_{n-1}=A^nx_0,
$$

where

$$
x_0=
\begin{bmatrix}
40,000\\60,000
\end{bmatrix}.
$$

Using diagonalization, the notes obtain

$$
A^n=
\begin{bmatrix}
1&1\\
4&-1
\end{bmatrix}
\begin{bmatrix}
1^n&0\\
0&0.95^n
\end{bmatrix}
\begin{bmatrix}
1&1\\
4&-1
\end{bmatrix}^{-1}.
$$

Hence

$$
x_n=
\begin{bmatrix}
a_n\\b_n
\end{bmatrix}
=
\begin{bmatrix}
20,000(1+0.95^n)\\
20,000(4-0.95^n)
\end{bmatrix}.
$$

![[Attachments/Population Model.png]]

For large $n$, $0.95^n$ is close to $0$. The notes therefore obtain the long-term approximation

$$
A^{(big\ n)}\approx
\begin{bmatrix}
0.2&0.2\\
0.8&0.8
\end{bmatrix}.
$$

Thus

$$
x_{(big\ n)}=
\begin{bmatrix}
a_{(big\ n)}\\b_{(big\ n)}
\end{bmatrix}
=
\begin{bmatrix}
0.2(100,000)\\
0.8(100,000)
\end{bmatrix}.
$$

The long-term population is therefore **20% rural and 80% urban**.

> [!important]
> The notes point out that this is a simple population model and does not take factors such as migration, birth and death into account.

---

## Chapter Summary / Key Connections

- A matrix can be interpreted as a **linear transformation** through matrix multiplication.
- The images of a basis determine the linear transformation completely.
- An eigenvector satisfies $Ax=\lambda x$ for an eigenvalue $\lambda$.
- Eigenvalues are found from the roots of the characteristic polynomial $\det(\lambda I-A)$.
- The eigenspace $E_\lambda$ is obtained from the solution space of $(\lambda I-A)x=0$.
- The dimension of an eigenspace cannot exceed the multiplicity of its corresponding eigenvalue.
- An $n \times n$ matrix is diagonalizable when it has $n$ linearly independent eigenvectors.
- Diagonalization produces $P^{-1}AP=D$ and allows powers of a matrix to be handled through powers of a diagonal matrix.
- Powers of matrices describe iterative systems such as the rural–urban population model in the notes.

## Exam / Revision Checklist

- [ ] Explain how a matrix acts as a mapping from $R^n$ to $R^m$.
- [ ] Find the standard matrix from a formula for a linear transformation.
- [ ] Use images of standard basis vectors to construct the standard matrix.
- [ ] Apply the linearity properties of a linear transformation.
- [ ] Use the stacking method when images of a basis are given.
- [ ] Identify eigenvalues and eigenvectors from $Ax=\lambda x$.
- [ ] Find eigenvalues using $\det(\lambda I-A)=0$.
- [ ] Read eigenvalues directly from a triangular matrix.
- [ ] Relate eigenvalue $0$ to singularity.
- [ ] Find an eigenspace by solving $(\lambda I-A)x=0$.
- [ ] Compare eigenspace dimension with eigenvalue multiplicity.
- [ ] Determine whether a matrix has enough linearly independent eigenvectors to be diagonalizable.
- [ ] Carry out the diagonalization algorithm and form $P$.
- [ ] Use diagonalization to work with powers of matrices.
- [ ] Set up and interpret an iterative system of the form $x_n=A^nx_0$.

## Key Equations / Relationships

$$
T(u)=Au
$$

$$
A=(T(e_1)\ T(e_2)\ \cdots\ T(e_n))
$$

$$
T(c_1u_1+c_2u_2+\cdots+c_ku_k)
=c_1T(u_1)+c_2T(u_2)+\cdots+c_kT(u_k)
$$

$$
Ax=\lambda x
$$

$$
\det(\lambda I-A)=0
$$

$$
(\lambda I-A)x=0
$$

$$
\dim E_{\lambda_i}\le r_i
$$

$$
P^{-1}AP=D
$$

$$
A=PDP^{-1}
$$

$$
A^n=PD^nP^{-1}
$$

$$
x_n=A^nx_0
$$
