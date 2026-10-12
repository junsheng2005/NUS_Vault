# MA1513 MCQ & FIB Revision Compilation

> [!info] Formatting
> All mathematical notation has been reconstructed into Obsidian-compatible MathJax. Inline mathematics uses `$...$`; displayed equations, vectors and matrices use `$$...$$`. Exam instructions and answer-booklet boilerplate are excluded.

> [!info] Organisation
> Questions are grouped by Chapter 1-4. FIB questions are included with MCQ. If a question uses concepts from multiple chapters, the later chapter takes precedence.

# Chapter 1

## AY2024/2025 Semester 1 / Question 1 / Chapter 1 / Ranks of Matrices

### Question

Given $Ax=b$ is a non-homogeneous linear system where $A$ is a $3\times5$ matrix. Suppose the general solution is

$$
\begin{cases}
x_1=s+2t\\
x_2=t-s-1\\
x_3=s\\
x_4=t+2\\
x_5=t
\end{cases}
$$

Which statements are correct?

1. The RREF of $(A\mid b)$ has exactly 2 non-pivot columns.
2. Any REF of $A$ does not have a zero row.
3. $$\begin{bmatrix}2\\1\\0\\1\\1\end{bmatrix}$$ is a solution of $Ax=0$.
4. $$\begin{bmatrix}0\\1\\0\\-2\\0\end{bmatrix}$$ is a solution of $Ax=b$.
5. For any $3\times1$ column matrix $c$, $Ax=c$ is consistent.

> [!success]- Worked Solution
> The two parameters $s,t$ give two free-variable columns in $A$. In the augmented matrix, the augmented column is also non-pivot, so statement 1 is false.
>
> The coefficient matrix has rank $3$, so an REF of $A$ has three non-zero rows: statement 2 is true.
>
> For $Ax=0$, remove the constant part:
> $$\begin{cases}x_1=s+2t\\x_2=t-s\\x_3=s\\x_4=t\\x_5=t\end{cases}$$
> Taking $s=0,t=1$ gives $(\begin{bmatrix}2\\1\\0\\1\\1\end{bmatrix})$, so statement 3 is true.
>
> The vector in statement 4 is the negative of a particular solution of the non-homogeneous system; solutions of a non-homogeneous system are not closed under scalar multiplication, so it is false.
>
> Since $\operatorname{rank}(A)=3$ equals the number of rows, every $Ax=c$ is consistent. Statement 5 is true.
>
> **Answer: 2, 3 and 5.**

---

## AY2024/2025 Semester 1 / Question 3 / Chapter 1 / Determinants of Matrices

### Question

Suppose $A$ is a $2\times2$ matrix with $\det(A)=2$. Find

1. $a=\det(-A)$
2. $b=\det(2A^TA)$
3. $c=\det(4A^{-1})$.

> [!success]- Worked Solution
> For a $2\times2$ matrix, $\det(cA)=c^2\det(A)$.
>
> $$\det(-A)=(-1)^2\det(A)=2.$$
>
> $$\det(2A^TA)=2^2\det(A^T)\det(A)=4(2)(2)=16.$$
>
> $$\det(4A^{-1})=4^2\det(A^{-1})=16\cdot\frac1{2}=8.$$
>
> **Answer: $a=2,\ b=16,\ c=8$.**

---

## AY2024/2025 Semester 2 / Question 1 / Chapter 1 / Solving System of Linear Equations

### Question

Let $Ax=b$ be non-homogeneous and let $R$ be the RREF of the augmented matrix $(A\mid b)$. Which statements must be true?

1. If every column of $R$ is a pivot column, then $Ax=b$ is inconsistent.
2. If $R$ has a non-pivot column, then $Ax=b$ has infinitely many solutions.
3. If $R$ has a zero row, then $Ax=b$ is consistent.
4. If every row of $R$ has a leading entry, then $Ax=b$ has exactly one solution.
5. If the last column of $R$ has no leading entry, then $Ax=b$ is consistent.

> [!success]- Worked Solution
> A pivot in the augmented column makes the system inconsistent, so 1 is true. A non-pivot column might be only the augmented column, so 2 is false. A zero row does not prevent an inconsistent row above it, so 3 is false. A leading entry in every row could include the augmented column, so 4 is false. If the augmented column is non-pivot, there is no inconsistent row, so 5 is true.
>
> **Answer: 1 and 5.**

---

## AY2024/2025 Semester 2 / Question 2 / Chapter 1 / Matrix Inverses

### Question

Which are equivalent conditions for an $n\times n$ matrix $A$ to be non-singular?

1. The $n$ rows of $A$ are linearly independent.
2. Any REF of $A$ has $n$ pivot columns.
3. The column space of $A$ is $\mathbb R^n$.
4. $\det(A)=1$.
5. The non-homogeneous system $Ax=b$ has only the trivial solution.

> [!success]- Worked Solution
> Statements 1, 2 and 3 are standard equivalent conditions for non-singularity. A non-singular matrix need only have non-zero determinant, not determinant 1. “Trivial solution” applies to a homogeneous system, not a non-homogeneous one.
>
> **Answer: 1, 2 and 3.**

---

## AY2024/2025 Semester 2 / Question 3 / Chapter 1 / Determinants of Matrices

### Question

Given
$$A=\begin{bmatrix}a & b & c\\i & j & k\\x & y & z\end{bmatrix},\qquad \det(A)=n\ne0,$$
which statements are correct?

1. $\det\begin{bmatrix}a & b & c\\2i & 2j & 2k\\x & y & z\end{bmatrix}=2^3n$
2. $\det\begin{bmatrix}x & y & z\\a & b & c\\i & j & k\end{bmatrix}=-n$
3. $\det\begin{bmatrix}z & y & x\\k & j & i\\c & b & a\end{bmatrix}=n$
4. $\det\begin{bmatrix}a & 3i & 5x\\b & 3j & 5y\\c & 3k & 5z\end{bmatrix}=15n$
5. $\det\begin{bmatrix}a-i & b-j & c-k\\i-x & j-y & k-z\\x-a & y-b & z-c\end{bmatrix}=n$.

> [!success]- Worked Solution
> 1: scaling one row by 2 multiplies the determinant by 2, not $2^3$. 2: the row order is a 3-cycle, equivalent to two swaps, so determinant remains $n$. 3: one row swap and one column swap give two sign changes, so determinant remains $n$. 4: factors 3 and 5 can be taken from columns 2 and 3, giving $15n$. 5: the three rows are linearly dependent because their sum is zero, so determinant is 0.
>
> **Answer: 3 and 4.**

---

## AY2024/2025 Semester 2 / Question 4 / Chapter 1 / Ranks of Matrices

### Question

$A$ is an $m\times n$ full-rank matrix. Which statements are correct?

1. If $m<n$, an additional row can always be added to increase rank.
2. If $m<n$, an additional column can always be added to increase rank.
3. If $m>n$, an additional row can always be added to increase rank.
4. If $m>n$, an additional column can always be added to increase rank.
5. If $m=n$, adding a row or column always increases rank.

> [!success]- Worked Solution
> If $m<n$, full rank means rank $m$; a suitable new row can increase rank to $m+1$, but a new column cannot exceed $m$. If $m>n$, full rank means rank $n$; a suitable new column can increase rank to $n+1$, but a new row cannot exceed $n$. For $m=n$, rank is already $n$, so adding only one row or column does not increase the maximum rank.
>
> **Answer: 1 and 4.**

---

## AY2025/2026 Semester 1 / Question 1 / Chapter 1 / Solving System of Linear Equations

### Question

Given the general solution of the non-homogeneous system $Ax=b$:
$$\begin{cases}x=s-t+1\\y=s\\z=t\end{cases}$$
Which of the proposed systems are general solutions of $Ax=0$ or $Ax=b$ as stated?

> [!success]- Worked Solution
> Split the solution into its parameter part and constant part:
> $$\begin{bmatrix}x\y\z\end{bmatrix}=s\begin{bmatrix}1\1\0\end{bmatrix}+t\begin{bmatrix}-1\0\1\end{bmatrix}+\begin{bmatrix}1\0\0\end{bmatrix}.$$
> The parameter part is the general solution of $Ax=0$. Reparameterizing $s,t$ does not change the solution set. Adding any particular solution of $Ax=b$ to the homogeneous general solution gives another general solution of $Ax=b$. Applying these checks to the options gives A, B and C.
>
> **Answer: A, B and C.**

---

## AY2025/2026 Semester 1 / Question 2 / Chapter 1 / Determinants of Matrices

### Question

Given
$$A=\begin{bmatrix}1 & 1 & *\\a & b & *\\b & a & *\end{bmatrix},$$
where $a,b$ are non-zero and $a\ne\pm b$, which can be the third column if $\det(A)=0$?

**A.** $$\begin{bmatrix}0\\1\\-1\end{bmatrix}$$

**B.** $$\begin{bmatrix}1\\a+b\\a+b\end{bmatrix}$$

**C.** $$\begin{bmatrix}1\\a\\b\end{bmatrix}$$

**D.** $$\begin{bmatrix}0\\b\\a\end{bmatrix}$$

**E.** $$\begin{bmatrix}1\\2a-b\\2b-a\end{bmatrix}$$

> [!success]- Worked Solution
> A determinant is zero exactly when the columns are linearly dependent.
>
> - **A:** direct expansion gives determinant $0$.
> - **B:** determinant is $b^2-a^2\ne0$.
> - **C:** this is identical to the first column, so determinant $0$.
> - **D:** determinant is $b^2-a^2\ne0$.
> - **E:** the column equals $2C_1-C_2$, so the columns are dependent.
>
> **Answer: A, C and E.**

---

# Chapter 2

## AY2024/2025 Semester 1 / Question 4 / Chapter 2 / Linear Combination and Linear Span

### Question

Which vectors are coplanar with $(1,2,3)$ and $(3,2,1)$?

1. $(1,3,2)$
2. Any linear combination of $(1,2,3)$ and $(2,1,3)$
3. $(2,1,0)$
4. $(2,0,2)$
5. Any linear combination of $(1,0,-1)$ and $(0,1,2)$.

> [!success]- Worked Solution
> A vector is coplanar with the two given vectors exactly when it lies in their span. Testing the candidates shows that $(2,1,0)$ lies in the span, and both spanning vectors in option 5 lie in the same plane. The other options do not.
>
> **Answer: 3 and 5.**

---

## AY2024/2025 Semester 1 / Question 5 / Chapter 2 / Basis and Dimension

### Question

Which sets are bases for
$$\operatorname{span}\{(1,0,1,1),(1,2,0,1),(1,4,-1,1),(1,-2,2,1),(2,2,1,1)\}?$$

1. $\{(1,0,1,1),(1,2,0,1),(1,4,-1,1)\}$
2. $\{(1,4,-1,1),(1,-2,2,1),(2,2,1,1)\}$
3. $\{(1,0,0,0),(0,1,0,0),(0,0,1,0)\}$
4. $\{(1,2,0,1),(1,4,-1,1),(1,-2,2,1)\}$
5. $\{(1,0,1,1),(1,4,-1,1),(2,2,1,1)\}$.

> [!success]- Worked Solution
> Stack the five vectors as columns and row-reduce:
> $$R=\begin{bmatrix}1 & 0 & -1 & 2 & 0\\0 & 1 & 2 & -1 & 0\\0 & 0 & 0 & 0 & 1\\0 & 0 & 0 & 0 & 0\end{bmatrix}.$$
> A basis must contain three linearly independent vectors spanning the same column space. Options 2 and 5 satisfy this.
>
> **Answer: 2 and 5.**

---

## AY2024/2025 Semester 1 / Question 6 / Chapter 2 / Coordinate Vectors

### Question

With respect to
$$S=\{(1,0,1),(0,1,1),(1,1,0)\},$$
the coordinate vector is $[v]_S=(3,6,9)$. For
$$T=\{(2,1,0),(0,2,1),(1,0,2)\},$$
find $[v]_T=(a,b,c)$.

> [!success]- Worked Solution
> First reconstruct $v$:
> $$v=3(1,0,1)+6(0,1,1)+9(1,1,0)=(12,15,9).$$
> Now solve
> $$(12,15,9)=a(2,1,0)+b(0,2,1)+c(1,0,2).$$
> This gives $a=5,b=5,c=2$.
>
> **Answer: $[v]_T=(5,5,2)$.**

---

## AY2024/2025 Semester 1 / Question 7 / Chapter 2 / Linear Independence

### Question

Which sets are linearly independent?

1. $\{(10,20,30,40),(11,22,33,44)\}$
2. $\{(1,5,1,3),(2,0,2,4),(0,0,0,0)\}$
3. $\{(1,1,0,0),(0,0,1,1),(1,0,1,0),(0,1,0,1)\}$
4. $\{(1,2,3,0),(2,3,1,0),(3,1,2,0)\}$
5. $\{(1,1,1,1),(2,2,0,2),(3,0,3,0),(0,0,0,4)\}$.

> [!success]- Worked Solution
> 1 is dependent because the two vectors are scalar multiples. 2 contains the zero vector. 3 satisfies $v_1+v_2=v_3+v_4$. For 4, the homogeneous vector equation has only the trivial solution. For 5, stacking the four vectors gives a non-zero determinant.
>
> **Answer: 4 and 5.**

---

## AY2024/2025 Semester 1 / Question 8 / Chapter 2 / Subspaces

### Question

Three of the following subspaces of $\mathbb R^3$ are the same. Select the two that are not the same as those three.

1. $\operatorname{span}\{(1,-1,0),(1,0,-1)\}$
2. Nullspace of $$\begin{bmatrix}1 & 1 & 1\\2 & 2 & 2\\3 & 3 & 3\end{bmatrix}$$
3. Row space of $$\begin{bmatrix}1 & -1 & 0\\1 & 0 & -1\\1 & 1 & 1\end{bmatrix}$$
4. Column space of $$\begin{bmatrix}2 & 0 & 0\\-1 & 1 & 0\\-1 & -1 & 0\end{bmatrix}$$
5. Solution space of $x+2y+3z=0$.

> [!success]- Worked Solution
> The nullspace in option 2 has dimension 2. The two vectors in option 1 lie in that nullspace and are independent, so 1 and 2 are the same. The columns in option 4 also lie in that nullspace and span a 2-dimensional space, so 4 is the same space. Options 3 and 5 are different.
>
> **Answer: 3 and 5.**

---

## AY2024/2025 Semester 2 / Question 5 / Chapter 2 / Linear Combination and Linear Span

### Question

Which represent the plane $x-y+2z=0$?

1. $\operatorname{span}\{(1,-1,2),(0,0,0)\}$
2. $\operatorname{span}\{(1,1,0),(0,2,1),(2,0,-1)\}$
3. $\operatorname{span}\{(1,3,1),(3,9,3)\}$
4. $\operatorname{span}\{(3,1,-1),(3,-1,-2)\}$
5. $\operatorname{span}\{(1,0,0),(0,-1,0),(0,0,2)\}$.

> [!success]- Worked Solution
> Every spanning vector must lie in the plane, and the span must have dimension 2. Option 2 contains vectors in the plane and has two independent directions. Option 4 also contains two independent vectors in the plane. Options 1 and 5 contain vectors outside the plane; option 3 has only one independent direction.
>
> **Answer: 2 and 4.**

---

## AY2024/2025 Semester 2 / Question 6 / Chapter 2 / Linear Independence

### Question

Which sets are linearly independent?

1. $\{(10,11,12),(100,121,144)\}$
2. $\{(1,5,1,3),(1,3,1,5),(5,1,3,1),(3,1,5,1)\}$
3. $\{(3,6,9),(13,16,19),(23,26,29)\}$
4. $\{(0,1,2,3),(0,0,1,2),(0,0,0,3)\}$
5. $\{(1,0,1,0),(0,2,0,2),(3,3,3,3)\}$.

> [!success]- Worked Solution
> 1 consists of two non-scalar-multiple vectors, so it is independent. 2 forms a $4\times4$ matrix with non-zero determinant. 3 satisfies $v_3-v_1=2(v_2-v_1)$, so it is dependent. 4 is independent by back-substitution from the last non-zero components. 5 satisfies $3v_1+\frac12v_2=v_3$.
>
> **Answer: 1, 2 and 4.**

---

## AY2024/2025 Semester 2 / Question 7 / Chapter 2 / Basis and Dimension

### Question

A $3\times5$ matrix $C=[c_1\ c_2\ c_3\ c_4\ c_5]$ has
$$\operatorname{RREF}(C)=\begin{bmatrix}1 & 1 & 0 & 1 & 0\\0 & 0 & 1 & 1 & 0\\0 & 0 & 0 & 0 & 1\end{bmatrix}.$$
Which sets are bases for $\operatorname{Col}(C)$?

1. $\{c_1,c_3,c_5\}$
2. $\{c_1,c_2,c_5\}$
3. $\{c_1,c_3,c_4\}$
4. $\{c_3,c_4,c_5\}$
5. Any set of 3 linearly independent vectors in $\mathbb R^3$.

> [!success]- Worked Solution
> The rank is 3, so $\operatorname{Col}(C)=\mathbb R^3$. Pivot columns 1,3,5 give a basis, so 1 is true. Columns 1 and 2 are dependent, so 2 is false. Column 4 equals column 1 plus column 3 in the RREF, so 3 is dependent. Columns 3,4,5 are independent, so 4 is true. Since the column space is all of $\mathbb R^3$, any three independent vectors in $\mathbb R^3$ form a basis, so 5 is true.
>
> **Answer: 1, 4 and 5.**

---

## AY2024/2025 Semester 2 / Question 8 / Chapter 2 / Coordinate Vectors

### Question

Given $S=\{u_1,u_2\}$ is a basis for $\mathbb R^2$,
$$v=\begin{bmatrix}-3\\6\end{bmatrix},\quad [v]_S=\begin{bmatrix}2\\-1\end{bmatrix},\quad w=\begin{bmatrix}6\\3\end{bmatrix},\quad [w]_S=\begin{bmatrix}-1\\2\end{bmatrix}.$$
If
$$u_1=\begin{bmatrix}a\\b\end{bmatrix},\qquad u_2=\begin{bmatrix}c\\d\end{bmatrix},$$
find $a,b,c,d$.

> [!success]- Worked Solution
> From the coordinate vectors,
> $$2u_1-u_2=\begin{bmatrix}-3\\6\end{bmatrix},\qquad -u_1+2u_2=\begin{bmatrix}6\\3\end{bmatrix}.$$
> Writing components gives
> $$2a-c=-3,\quad 2b-d=6,$$
> $$-a+2c=6,\quad -b+2d=3.$$
> Solving gives
> $$\boxed{a=0,\ b=5,\ c=3,\ d=4}.$$

---

## AY2024/2025 Semester 2 / Question 12 / Chapter 2 / Projection and Linear Approximation

### Question

Given
$$V=\operatorname{span}\{(1,1,0,0),(0,0,1,1)\},\qquad u=(3,-1,2,-4),$$
find the vector $v=(a,b,c,d)\in V$ closest to $u$.

> [!success]- Worked Solution
> Let
> $$A=\begin{bmatrix}1 & 0\\1 & 0\\0 & 1\\0 & 1\end{bmatrix}.$$
> The closest vector is the projection $v=Ax_0$, where $x_0$ is a least-squares solution of $Ax=u$. Solving gives
> $$x_0=\begin{bmatrix}1\\-1\end{bmatrix},\qquad v=Ax_0=\begin{bmatrix}1\\1\\-1\\-1\end{bmatrix}.$$
>
> **Answer: $a=1,b=1,c=-1,d=-1$.**

---

## AY2025/2026 Semester 1 / Question 4 / Chapter 2 / Basis and Dimension

### Question

Given
$$A=\begin{bmatrix}2 & 3 & 1\\0 & 1 & -1\\1 & 1 & 1\end{bmatrix},$$
which proposed sets form a basis for $\operatorname{Col}(A)$?

> [!success]- Worked Solution
> The RREF has two pivot columns, so the column space has dimension 2. A basis must therefore contain exactly two independent vectors in the column space. Checking the proposed sets gives options B and D.
>
> **Answer: B and D.**

---

## AY2025/2026 Semester 1 / Question 5 / Chapter 2 / Linear Independence

### Question

Which proposed sets are linearly independent?

> [!success]- Worked Solution
> Stack each set as rows (or columns) of a matrix and row-reduce. A set is independent exactly when there is a pivot for every vector. Applying this to the five sets gives options B, C and D.
>
> **Answer: B, C and D.**

---

## AY2025/2026 Semester 1 / Question 6 / Chapter 2 / Linear Combination and Linear Span

### Question

Which spans are equal to
$$\operatorname{span}\{(1,0,1),(0,1,0)\}?$$

A. $\operatorname{span}\{(1,1,1)\}$
B. $\operatorname{span}\{(1,1,0),(0,0,1)\}$
C. $\operatorname{span}\{(1,0,1),(0,1,0),(1,1,1)\}$
D. $\operatorname{span}\{(1,0,0),(0,1,0),(0,0,1)\}$
E. $\operatorname{span}\{(2,1,2),(1,2,1)\}$.

> [!success]- Worked Solution
> The target span has dimension 2. A has dimension 1 and D has dimension 3. In C, the third vector is the sum of the first two, so C is the same span. The vectors in B do not both lie in the target span. Both vectors in E are linear combinations of the target generators and are independent, so E gives the same span.
>
> **Answer: C and E.**

---

## AY2025/2026 Semester 1 / Question 7 / Chapter 2 / Coordinate Vectors

### Question

Let
$$v_1=\begin{bmatrix}1\\0\\1\\1\end{bmatrix},\ v_2=\begin{bmatrix}1\\1\\0\\1\end{bmatrix},\ v_3=\begin{bmatrix}1\\1\\1\\0\end{bmatrix},\ v_4=\begin{bmatrix}0\\1\\1\\1\end{bmatrix},\ w=\begin{bmatrix}3\\4\\5\\6\end{bmatrix}.$$
If $S=\{v_1,v_2,v_3,v_4\}$ and
$$[w]_S=\begin{bmatrix}a\\b\\c\\d\end{bmatrix},$$
find $a,b,c,d$.

> [!success]- Worked Solution
> Solve
> $$a v_1+b v_2+c v_3+d v_4=w.$$
> Equivalently, solve $Ax=w$ with $A=[v_1\ v_2\ v_3\ v_4]$. Row reduction gives
> $$[w]_S={vec(2,1,0,3)}.$$
>
> **Answer: $a=2,b=1,c=0,d=3$.**

---

## AY2025/2026 Semester 1 / Question 8 / Chapter 2 / Orthogonal Vectors

### Question

Given
$$u_1=(1,1,0,2),\quad u_2=(2,0,1,1),\quad u_3=(1,0,2,1),$$
and $v=(a,b,c,-3)$ is orthogonal to all three, find $a,b,c$.

> [!success]- Worked Solution
> Set each dot product to zero:
> $$v\cdot u_1=a+b-6=0,$$
> $$v\cdot u_2=2a+c-3=0,$$
> $$v\cdot u_3=a+2c-3=0.$$
> Solving gives $a=1,b=5,c=1$.
>
> **Answer: $(a,b,c)=(1,5,1)$.**

---

# Chapter 3

## AY2024/2025 Semester 1 / Question 2 / Chapter 3 / Diagonalizable Matrices

### Question

Suppose $A$ is a non-singular $n\times n$ matrix. Which statements are true?

1. Any REF of $A^T$ is non-singular.
2. $A$ has $n$ linearly independent eigenvectors.
3. The row space of $A$ is $\mathbb{R}^n$.
4. $\operatorname{rank}(A^k)=n$ for any integer $k>1$.
5. Any column of $A$ can be expressed as a linear combination of the remaining columns.

> [!success]- Worked Solution
> Because $A$ is non-singular, $A^T$ and every REF of $A^T$ are non-singular, so 1 is true. Non-singularity does not imply diagonalizability, so 2 is false. A non-singular $n\times n$ matrix has RREF $I_n$, hence row space $\mathbb R^n$: 3 is true. Powers of a non-singular matrix remain non-singular, so 4 is true. Its columns are linearly independent, so 5 is false.
>
> **Answer: 1, 3 and 4.**

---

## AY2024/2025 Semester 1 / Question 9 / Chapter 3 / Linear Transformation

### Question

Let $T:\mathbb R^3\to\mathbb R^3$ be linear with
$$T\left(\begin{bmatrix}1\\1\\0\end{bmatrix}\right)=\begin{bmatrix}0\\1\\1\end{bmatrix},\qquad T\left(\begin{bmatrix}0\\1\\1\end{bmatrix}\right)=\begin{bmatrix}1\\1\\0\end{bmatrix}.$$
Find
$$T\left(\begin{bmatrix}2\\5\\3\end{bmatrix}\right)=\begin{bmatrix}a\\b\\c\end{bmatrix}.$$

> [!success]- Worked Solution
> Since
> $$\begin{bmatrix}2\\5\\3\end{bmatrix}=2\begin{bmatrix}1\\1\\0\end{bmatrix}+3\begin{bmatrix}0\\1\\1\end{bmatrix},$$
> linearity gives
> $$T\left(\begin{bmatrix}2\\5\\3\end{bmatrix}
> ight)=2\begin{bmatrix}0\\1\\1\end{bmatrix}+3\begin{bmatrix}1\\1\\0\end{bmatrix}=\begin{bmatrix}3\\5\\2\end{bmatrix}.$$
>
> **Answer: $a=3,b=5,c=2$.**

---

## AY2024/2025 Semester 1 / Question 10 / Chapter 3 / Diagonalization

### Question

$A$ is a diagonalizable $3\times3$ matrix with eigenvalues $1$ and $3$ and eigenspaces
$$E_1=\operatorname{span}\left\{\begin{bmatrix}1\\1\\1\end{bmatrix}\right\},\qquad E_3=\operatorname{span}\left\{\begin{bmatrix}1\\0\\1\end{bmatrix},\begin{bmatrix}0\\0\\1\end{bmatrix}\right\}.$$
Which matrices diagonalize $A$?

1. $$\begin{bmatrix}0 & 1 & 1\\0 & 1 & 0\\1 & 1 & 0\end{bmatrix}$$
2. $$\begin{bmatrix}2 & 4 & 0\\0 & 4 & 0\\2 & 4 & 6\end{bmatrix}$$
3. $$\begin{bmatrix}1 & 1 & 2\\1 & 0 & 2\\1 & 1 & 2\end{bmatrix}$$
4. $$\begin{bmatrix}2 & 1 & 0\\1 & 0 & 0\\2 & 1 & 1\end{bmatrix}$$
5. $$\begin{bmatrix}1 & 0 & 0\\0 & 0 & 0\\1 & 1 & 0\end{bmatrix}$$

> [!success]- Worked Solution
> A diagonalizing matrix must have three linearly independent eigenvectors as columns: one from $E_1$ and two from $E_3$. Checking the columns gives options 1 and 2. Option 3 has dependent columns, option 4 contains a column that mixes eigenspaces, and option 5 contains the zero vector.
>
> **Answer: 1 and 2.**

---

## AY2024/2025 Semester 1 / Question 11 / Chapter 3 / Eigenspaces

### Question

A $4\times4$ matrix $A$ has characteristic polynomial
$$x(x-1)^a(x+1)^b,$$
where $a,b$ are positive integers. Which statements are true?

1. Nullity of $A$ is 1.
2. The dimension of one eigenspace is 2.
3. Exactly one eigenvalue has multiplicity 2.
4. $A$ cannot be diagonalizable.
5. $\det(A)=0$.

> [!success]- Worked Solution
> The eigenvalue $0$ has algebraic multiplicity 1, so its eigenspace has dimension 1; hence nullity is 1. Since the total degree is 4, $a+b=3$, so one of $a,b$ is 2 and the other is 1. An eigenspace of algebraic multiplicity 2 need not have dimension 2, so 2 is not guaranteed. The matrix can be diagonalizable if each eigenspace has full dimension. Since 0 is an eigenvalue, $\det(A)=0$.
>
> **Answer: 1, 3 and 5.**

---

## AY2024/2025 Semester 2 / Question 9 / Chapter 3 / Linear Transformation

### Question

$T:\mathbb R^2\to\mathbb R^2$ scales vectors on $y=2x$ by $2$ and vectors on $y=-2x$ by $-2$. Find the standard matrix
$$A=\begin{bmatrix}a & b\\c & d\end{bmatrix}.$$

> [!success]- Worked Solution
> Use basis vectors $u=\begin{bmatrix}1\\2\end{bmatrix}$ and $v=\begin{bmatrix}1\\-2\end{bmatrix}$. Then
> $$T(u)=2u=\begin{bmatrix}2\\4\end{bmatrix},\qquad T(v)=-2v=\begin{bmatrix}-2\\4\end{bmatrix}.$$
> By stacking,
> $$A\begin{bmatrix}1 & 1\\2 & -2\end{bmatrix}=\begin{bmatrix}2 & -2\\4 & 4\end{bmatrix}.$$
> Hence
> $$A=\begin{bmatrix}0 & 1\\4 & 0\end{bmatrix}.$$
>
> **Answer: $a=0,b=1,c=4,d=0$.**

---

## AY2024/2025 Semester 2 / Question 10 / Chapter 3 / Eigenspaces

### Question

$A$ is a $4\times4$ matrix with eigenvalues $3$ and $0$ and eigenspaces
$$E_3=\operatorname{span}\left\{\begin{bmatrix}1\\0\\0\\1\end{bmatrix},\begin{bmatrix}0\\1\\1\\0\end{bmatrix},\begin{bmatrix}1\\2\\2\\1\end{bmatrix}\right\},$$
$$E_0=\operatorname{span}\left\{\begin{bmatrix}0\\0\\0\\1\end{bmatrix}\right\}.$$
Which statements must be true?

1. $A$ has exactly 2 eigenvalues.
2. Multiplicity of eigenvalue 0 is 1.
3. $A$ may be non-diagonalizable.
4. $\dim(E_3)=3$.
5. $\lambda=3$ is a repeated root of the characteristic polynomial.

> [!success]- Worked Solution
> The third spanning vector of $E_3$ is a linear combination of the first two, so $\dim(E_3)=2$. Thus the algebraic multiplicity of 3 is at least 2, so 5 is true. A third eigenvalue may exist, so 1 is not forced. The algebraic multiplicity of 0 may exceed 1, so 2 is not forced. If 3 and 0 are the only eigenvalues, there may be only three independent eigenvectors, so $A$ may be non-diagonalizable: 3 is true. Statement 4 is false.
>
> **Answer: 3 and 5.**

---

## AY2024/2025 Semester 2 / Question 11 / Chapter 3 / Diagonalization

### Question

Suppose
$$P^{-1}AP=D,\quad P=\begin{bmatrix}1 & 0 & 2\\1 & 0 & 1\\0 & 1 & 0\end{bmatrix},\quad D=\begin{bmatrix}a & 0 & 0\\0 & a & 0\\0 & 0 & b\end{bmatrix},$$
where $a\ne b$. Which proposed diagonalizations are true?

> [!success]- Worked Solution
> The columns of $P$ show that the eigenspace for $a$ is spanned by $(1,1,0)^T$ and $(0,0,1)^T$, while the eigenspace for $b$ is spanned by $(2,1,0)^T$. A valid diagonalizing matrix must have independent columns chosen from these eigenspaces, and the diagonal entries must match their eigenvalues. Checking the five proposed matrices gives options 1 and 5.
>
> **Answer: 1 and 5.**

---

## AY2025/2026 Semester 1 / Question 3 / Chapter 3 / Eigenspaces

### Question

$A$ is an $n\times n$ matrix such that $Ax=0$ has a non-trivial solution. Which statements are true?

A. Nullity of $A$ is not 0.
B. The last column of the RREF of $A$ must be non-pivot.
C. The $n$ rows of $A$ are linearly dependent.
D. The eigenspace for eigenvalue 0 has dimension 1.
E. There exists $b$ such that $Ax=b$ is inconsistent.

> [!success]- Worked Solution
> A non-trivial solution means $A$ is singular. Hence nullity is positive and the rows are linearly dependent. Zero is an eigenvalue, but its eigenspace may have dimension greater than 1. A singular square matrix has a zero row in RREF, so an appropriate augmented column can create an inconsistent row; thus some $Ax=b$ is inconsistent. The non-pivot column need not be the last coefficient column.
>
> **Answer: A, C and E.**

---

## AY2025/2026 Semester 1 / Question 9 / Chapter 3 / Linear Transformation

### Question

Given a linear transformation $T:\mathbb R^4\to\mathbb R^3$ with
$$T\left(\begin{bmatrix}3\\5\\2\\2\end{bmatrix}\right)=\begin{bmatrix}3\\2\\1\end{bmatrix},\qquad T\left(\begin{bmatrix}4\\4\\2\\3\end{bmatrix}\right)=\begin{bmatrix}1\\1\\1\end{bmatrix},$$
find
$$T\left(\begin{bmatrix}1\\7\\2\\0\end{bmatrix}\right).$$

> [!success]- Worked Solution
> First express the input as
> $$\begin{bmatrix}1\\7\\2\\0\end{bmatrix}=3\begin{bmatrix}3\\5\\2\\2\end{bmatrix}-2\begin{bmatrix}4\\4\\2\\3\end{bmatrix}.$$
> By linearity,
> $$T\left(\begin{bmatrix}1\\7\\2\\0\end{bmatrix}
> ight)=3\begin{bmatrix}3\\2\\1\end{bmatrix}-2\begin{bmatrix}1\\1\\1\end{bmatrix}=\begin{bmatrix}7\\4\\1\end{bmatrix}.$$
>
> **Answer: $(a,b,c)=(7,4,1)$.**

---

## AY2025/2026 Semester 1 / Question 10 / Chapter 3 / Eigenspaces

### Question

$A$ is a $4\times4$ matrix with exactly two distinct eigenvalues and three linearly independent eigenvectors. Which statements are true?

A. At least one eigenvalue has multiplicity 2.
B. One eigenspace has dimension 3.
C. One eigenspace has dimension 1.
D. A $4\times3$ matrix can diagonalize $A$.
E. At most one eigenvalue has multiplicity 1.

> [!success]- Worked Solution
> The three independent eigenvectors must split between the two eigenspaces as dimensions 2 and 1. Hence C is true and B is false. Algebraic multiplicities can be $(2,2)$ or $(3,1)$, so A is not guaranteed, while E is always true. A diagonalizing matrix for a $4\times4$ matrix must be an invertible $4\times4$ matrix, so D is false.
>
> **Answer: C and E.**

---

## AY2025/2026 Semester 1 / Question 11 / Chapter 3 / Diagonalization

### Question

A diagonalizable $3\times3$ matrix has eigenspaces
$$E_1=\operatorname{span}\{(1,2,0),(1,0,2)\},\qquad E_2=\operatorname{span}\{(0,1,1)\}.$$
Which proposed matrices diagonalize $A$?

> [!success]- Worked Solution
> A diagonalizing matrix must have two independent columns from $E_1$ and one non-zero column from $E_2$. Checking the five proposed matrices gives options A and D.
>
> **Answer: A and D.**

---

# Chapter 4

## AY2024/2025 Semester 1 / Question 12 / Chapter 4 / Initial Value Problem

### Question

A $3\times3$ SDE $y'=Ay$ has fundamental solutions
$$x_1=e^t\begin{bmatrix}0\\1\\-1\end{bmatrix},\quad x_2=e^{-t}\begin{bmatrix}0\\1\\1\end{bmatrix},\quad x_3=\begin{bmatrix}1\\1\\1\end{bmatrix}.$$
Given $y(0)=\begin{bmatrix}3\\6\\4\end{bmatrix}$ and
$$y=ax_1+bx_2+cx_3,$$
find $a,b,c$.

> [!success]- Worked Solution
> At $t=0$,
> $$\begin{bmatrix}3\\6\\4\end{bmatrix}=a\begin{bmatrix}0\\1\\-1\end{bmatrix}+b\begin{bmatrix}0\\1\\1\end{bmatrix}+c\begin{bmatrix}1\\1\\1\end{bmatrix}.$$
> Solving gives $a=1,b=2,c=3$.
>
> **Answer: $a=1,b=2,c=3$.**

---

## AY2024/2025 Semester 1 / Question 13 / Chapter 4 / Repeated Eigenvalues

### Question

For the SDE
$$y'=\begin{bmatrix}0 & 2\\-2 & -4\end{bmatrix}y,$$
which of the following are solutions?

1. $y=e^{-2t}\begin{bmatrix}1/2\\-1/2\end{bmatrix}$
2. $y=e^{-2t}\begin{bmatrix}-1/2\\0\end{bmatrix}$
3. $y=e^{-2t}\begin{bmatrix}-t-1\\t\end{bmatrix}$
4. $y=e^{-2t}\begin{bmatrix}-t\\t-1/2\end{bmatrix}$
5. $y=e^{-2t}\begin{bmatrix}t-1/2\\-t\end{bmatrix}$.

> [!success]- Worked Solution
> The matrix has repeated eigenvalue $-2$ with eigenvector $v=(-1,1)^T$. A generalized eigenvector $u$ satisfies $(A+2I)u=v$, giving $u=(-1/2-s,s)^T$.
>
> Option 1 is a scalar multiple of $ve^{-2t}$ and is a solution. Option 4 has the form $(tv+u)e^{-2t}$ with $u=(0,-1/2)^T$, so it is also a solution. The others do not have the required eigenvector/generalized-eigenvector form.
>
> **Answer: 1 and 4.**

---

## AY2024/2025 Semester 1 / Question 14 / Chapter 4 / Direction Field

### Question

Which direction fields are possible for
$$y'=\begin{bmatrix}0 & a\\-1 & b\end{bmatrix}y$$
for some $a,b$? (The original question provides five direction-field diagrams.)

> [!success]- Worked Solution
> Use the test point $(1,0)^T$:
> $$\begin{bmatrix}0 & a\\-1 & b\end{bmatrix}\begin{bmatrix}1\\0\end{bmatrix}=\begin{bmatrix}0\\-1\end{bmatrix}.$$
> Therefore the tangent arrow at $(1,0)$ must point vertically downward. In the source diagrams, only options 1 and 2 have this behaviour.
>
> **Answer: 1 and 2.**

---

## AY2024/2025 Semester 1 / Question 15 / Chapter 4 / Mixing Problem Involving Two Tanks

### Question

Two tanks contain 100 L and 200 L of salt water. The SDE is
$$y'=\frac1{100}\begin{bmatrix}-6 & 2\\6 & -3\end{bmatrix}y.$$
From the flow diagram, determine the flow rates $a,b,c$.

> [!success]- Worked Solution
> For tank 1, inflow is $(a/200)y_2$ and outflow is $(b/100)y_1$. Comparing coefficients gives $b=6$ and $a/200=2/100$, hence $a=4$. For tank 2, total outflow coefficient is $(a+c)/200=3/100$, so $a+c=6$ and $c=2$.
>
> **Answer: $a=4,b=6,c=2$.**

---

## AY2024/2025 Semester 2 / Question 13 / Chapter 4 / Repeated Eigenvalues

### Question

A $2\times2$ matrix $A$ has only eigenvalue $\lambda=-1$ and one independent eigenvector $v=\begin{bmatrix}1\\-1\end{bmatrix}$. Suppose
$$(A+I)u=v$$
has general solution $u=\begin{bmatrix}1+s\\s\end{bmatrix}$. Which proposed vector functions are solutions of $y'=Ay$?

> [!success]- Worked Solution
> An eigenvector gives the solution $ve^{-t}$, and a generalized eigenvector $u$ gives $(tv+u)e^{-t}$. Option 1 is $-ve^{-t}$, so it is a solution. Option 3 uses $u=(0,-1)^T$ and has the correct generalized-eigenvector form. Option 5 is the sum of $ve^{-t}$ and $(tv+u)e^{-t}$ with $u=(1,0)^T$, so it is also a solution.
>
> **Answer: 1, 3 and 5.**

---

## AY2024/2025 Semester 2 / Question 14 / Chapter 4 / Complex Eigenvalues

### Question

For
$$y'=\begin{bmatrix}0 & 1\\-2 & 2\end{bmatrix}y,$$
which of the five proposed real vector functions are solutions?

> [!success]- Worked Solution
> The eigenvalues are $1\pm i$. Using the corresponding complex eigenvectors, the standard real fundamental solutions are obtained from the real and imaginary parts of $ve^{(1+i)t}$. Matching the proposed expressions with these forms gives options 1 and 3.
>
> **Answer: 1 and 3.**

---

## AY2024/2025 Semester 2 / Question 15 / Chapter 4 / Mixing Problem Involving Two Tanks

### Question

Suppose $A$ is a non-zero, singular, diagonalizable $2\times2$ matrix. Which statements about $y'=Ay$ are correct?

1. The equilibrium point can be a centre.
2. The equilibrium point cannot be a degenerate node.
3. The equilibrium point can be a star node.
4. There are straight-line trajectories.
5. There are trajectories that are not straight lines.

> [!success]- Worked Solution
> Since $A$ is singular, 0 is an eigenvalue. Because $A$ is non-zero and diagonalizable, the other eigenvalue is non-zero and there are two independent eigenvectors. Thus the equilibrium is the exceptional case, not a centre, star node, or degenerate node. Its phase portrait consists of straight-line trajectories.
>
> **Answer: 2 and 4.**

---

## AY2025/2026 Semester 1 / Question 12 / Chapter 4 / Complex Eigenvalues

### Question

An SDE has a solution
$$y=e^{2t}\left(\begin{bmatrix}-2\\1\end{bmatrix}\sin t+\begin{bmatrix}1\\0\end{bmatrix}\cos t\right).$$
Which description is correct?

A. Clockwise, towards the origin
B. Clockwise, away from the origin
C. Anti-clockwise, towards the origin
D. Anti-clockwise, away from the origin
E. Closed loops, clockwise.

> [!success]- Worked Solution
> The real part of the eigenvalue is $2>0$, so the equilibrium is an unstable spiral and trajectories move away from the origin. Reconstructing the matrix gives
> $$A={mat([[0,-5],[1,4]])}.$$
> At $(1,0)$, the tangent vector is $(0,1)^T$, which points upward, so the rotation is anti-clockwise.
>
> **Answer: D.**

---

## AY2025/2026 Semester 1 / Question 13 / Chapter 4 / Repeated Eigenvalues

### Question

A phase portrait of a $2\times2$ SDE shows a degenerate node. Which statements are true?

A. The SDE has only one linearly independent solution.
B. $A$ has a repeated eigenvalue.
C. $A$ has complex eigenvalues.
D. Both ends of every trajectory are parallel to the same vector.
E. There is no straight-line trajectory.

> [!success]- Worked Solution
> A degenerate node occurs with a repeated real eigenvalue and only one independent eigenvector. A generalized eigenvector still provides a second independent SDE solution, so A is false. The guiding axis is the single eigenvector direction, so both ends of trajectories become parallel to it. There is also a straight-line trajectory along that axis.
>
> **Answer: B and D.**

---

## AY2025/2026 Semester 1 / Question 14 / Chapter 4 / Solutions of System of Differential Equations

### Question

Suppose $y'=Ay$ has eigenvalues $r_1=0$ and $r_2\ne0$ with eigenvectors $\begin{bmatrix}a\\b\end{bmatrix}$ and $\begin{bmatrix}c\\d\end{bmatrix}$ respectively. Which proposed functions are solutions?

> [!success]- Worked Solution
> A fundamental set is
> $$Y_1=\begin{bmatrix}a\\b\end{bmatrix},\qquad Y_2=e^{r_2t}\begin{bmatrix}c\\d\end{bmatrix}.$$
> Every constant linear combination $c_1Y_1+c_2Y_2$ is a solution. Matching the options gives C and E. Option A would require $(k,k)$ to be parallel to $(a,b)$ for every $k$, which is not guaranteed.
>
> **Answer: C and E.**

---

## AY2025/2026 Semester 1 / Question 15 / Chapter 4 / Mixing Problem Involving Two Tanks

### Question

Three tanks are described by
$$y'=\frac1{100}\begin{bmatrix}-6 & 4 & 2\\3 & -8 & 5\\3 & 4 & -7\end{bmatrix}y.$$
Initially the amounts of salt are $10,20,30$ kg. Find the long-run amounts $(a,b,c)$.

> [!success]- Worked Solution
> The eigenvalues are $0,-3/25,-9/100$. The negative-eigenvalue terms decay to zero, leaving only the eigenvector for eigenvalue 0, $(1,1,1)^T$. Thus all three tanks have equal salt amounts in the long run. Total salt is conserved:
> $$10+20+30=60.$$
> Hence each tank tends to $60/3=20$ kg.
>
> **Answer: $a=b=c=20$.**

---

