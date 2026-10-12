# MA1513 MCQ & FIB Revision

# Chapter 1

### AY2022/2023 Semester 1 / Question 1 / Chapter 1 / Solving System of Linear Equations

#### Question

Given the augmented matrix

$$
\left[\begin{array}{ccccc|c}1&2&1&0&2&a\\0&0&1&0&1&b\\0&0&2&0&2&c\end{array}\right]
$$

which statements are true? (Select all correct options.)

**A.** The system is consistent only when $c=2b$.

**B.** If consistent, the general solution has two parameters.

**C.** For some $a,b,c$, the system has exactly one solution.

**D.** The augmented column can be a pivot column in a row echelon form.

**E.** If $c=0$, the system has infinitely many solutions.

> [!success]- Worked Solution
> Subtract twice row 2 from row 3:
>
> $$R_3\leftarrow R_3-2R_2\implies [0\ 0\ 0\ 0\ 0\mid c-2b].$$
>
> **A — True.** Consistency requires $c-2b=0$.
>
> **B — False.** When consistent, the two pivot variables are $x_1,x_3$; $x_2,x_4,x_5$ are free, giving three parameters.
>
> **C — False.** The coefficient matrix has rank $2<5$, so a unique solution is impossible.
>
> **D — True.** If $c\ne 2b$, the augmented column becomes a pivot column.
>
> **E — False.** $c=0$ with $b\ne0$ gives inconsistency.
>
> **Answer: A and D.**


### AY2022/2023 Semester 2 / Question 1 / Chapter 1 / Solving System of Linear Equations

#### Question

Given the row echelon form of an augmented matrix
$$\left[\begin{array}{ccc|c}a&1&1&1\\0&b&1&1\\0&0&c&1\end{array}\right]$$
where $a,b,c$ are real. Which statements are true? (Pick all correct options)

**A.** The system is consistent for any $a,b,c$.

**B.** If consistent, the system has exactly one solution.

**C.** The system can have infinitely many solutions.

**D.** The first column can be a non-pivot column.

**E.** The augmented matrix is full rank for any $a,b,c$.

> [!success]- Worked Solution
> **A — False.** $c=0$ produces $0=1$ in the last row.
>
> **B — True.** Consistency requires $c\ne0$, and row-echelon constraints then imply $b\ne0$ and $a\ne0$. All three coefficient columns pivot.
>
> **C — False.** Every consistent instance has three pivots and a unique solution.
>
> **D — True.** With $a=b=c=0$, the first column is non-pivot.
>
> **E — True.** Each of the three rows has a nonzero entry (possibly in the augmented column), so augmented rank is 3.
>
> **Answer: B, D and E.**


### AY2023/2024 Semester 1 / Question 1 / Chapter 1 / Solving System of Linear Equations

#### Question

A $3\times4$ homogeneous linear system has general solution 

$$
\begin{cases}x_1=s-2t\\x_2=t-2s\\x_3=s\\x_4=t\end{cases}
$$

 Its augmented matrix has row echelon form 

$$
\left[\begin{array}{cccc|c}1&0&a&b&0\\0&1&c&d&0\\0&0&0&0&0\end{array}\right].
$$

 Find $a,b,c,d$.

> [!success]- Worked Solution
> From $x_3=s,x_4=t$, substitute $x_1=s-2t$, $x_2=-2s+t$. Hence $x_1-x_3+2x_4=0$ and $x_2+2x_3-x_4=0$. **Answer:** $a=-1,b=2,c=2,d=-1$.


### AY2023/2024 Semester 2 / Question 1 / Chapter 1 / Solving System of Linear Equations

#### Question

Given a linear system $Ax=b$ with general solution 

$$
\begin{cases}x_1=s+t\\x_2=3t-4s\\x_3=s+1\\x_4=t-2\end{cases}.
$$

 Which vectors are particular solutions of $Ax=0$?

**A.** $\begin{bmatrix}0\\0\\1\\-2\end{bmatrix}$

**B.** $\begin{bmatrix}1\\-4\\1\\-2\end{bmatrix}$

**C.** $\begin{bmatrix}1\\3\\0\\1\end{bmatrix}$

**D.** $\begin{bmatrix}1\\10\\0\\0\end{bmatrix}$

**E.** $\begin{bmatrix}2\\-1\\1\\1\end{bmatrix}$

> [!success]- Worked Solution
> Remove the particular part $(0,0,1,-2)$ to obtain the homogeneous solution $s(1,-4,1,0)+t(1,3,0,1)$. **Answer: C and E.**


### AY2024/2025 Semester 1 / Question 1 / Chapter 1 / Solving System of Linear Equations

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
3. $\begin{bmatrix}2\\1\\0\\1\\1\end{bmatrix}$ is a solution of $Ax=0$.
4. $\begin{bmatrix}0\\1\\0\\-2\\0\end{bmatrix}$ is a solution of $Ax=b$.
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


### AY2024/2025 Semester 2 / Question 1 / Chapter 1 / Solving System of Linear Equations

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



### AY2022/2023 Semester 1 / Question 2 / Chapter 1 / Singular Matrices

#### Question

Given $A$ is a singular $n\times n$ matrix, which statements are true?

**A.** $\operatorname{rank}(A)=n$.

**B.** $\det(A)=0$.

**C.** The homogeneous system $Ax=0$ has no trivial solution.

**D.** The $n$ columns of $A$ are linearly dependent.

**E.** There is a nonzero vector in the nullspace of $A$.

> [!success]- Worked Solution
> **A — False.** A singular square matrix has rank less than $n$.
>
> **B — True.** Singularity means its determinant vanishes.
>
> **C — False.** Every homogeneous system has the zero solution.
>
> **D — True.** Fewer than $n$ pivot columns means the columns are dependent.
>
> **E — True.** A free variable yields a nontrivial nullspace vector.
>
> **Answer: B, D and E.**



### AY2022/2023 Semester 1 / Question 3 / Chapter 1 / Determinants of Matrices

#### Question

Given

$$
\det\begin{bmatrix}a&b&c\\a&0&c\\ *&*&*\end{bmatrix}=0,
$$

where $a,b,c$ are non-zero distinct numbers. Which of the following could be the third row **for every such choice of** $a,b,c$? (Select all correct options.)

**A.** $(a,b,c)$

**B.** $(0,p,0)$, where $p\ne0$

**C.** $(a,n,c)$, where $n\ne0,b$

**D.** $(a,a,a)$

**E.** $(c,b,a)$

> [!success]- Worked Solution
> **A — Correct.** Row 3 equals row 1, so the determinant is zero.
>
> **B — Correct.** Columns 1 and 3 are proportional, since their first two entries are $(a,a)$ and $(c,c)$, and the third entries are both zero.
>
> **C — Correct.** Columns 1 and 3 are again proportional: $(a,a,a)$ and $(c,c,c)$.
>
> **D — Incorrect.** The determinant need not be zero; choosing suitable distinct $a,b,c$ gives a nonzero determinant.
>
> **E — Incorrect.** It likewise does not force a zero determinant for arbitrary $a,b,c$.
>
> **Answer: A, B and C.**


### AY2022/2023 Semester 2 / Question 3 / Chapter 1 / Determinants of Matrices

#### Question

Which determinants equal $\det\begin{bmatrix}a&b&c\\0&b&c\\0&0&c\end{bmatrix}$ for every $a,b,c$?

**A.** $\det\begin{bmatrix}a&0&0\\a&b&0\\a&b&c\end{bmatrix}$

**B.** $\det\begin{bmatrix}0&0&c\\0&b&c\\a&b&c\end{bmatrix}$

**C.** $\det\begin{bmatrix}0&c&0\\b&c&0\\b&c&a\end{bmatrix}$

**D.** $\det\begin{bmatrix}b&a&c\\0&0&c\\b&0&c\end{bmatrix}$

**E.** $\det\begin{bmatrix}a&0&0\\b&b&0\\c&c&c\end{bmatrix}$

> [!success]- Worked Solution
> The given upper triangular determinant is $abc$. Direct expansion gives $abc,-abc,-abc,abc,abc$ for options A–E respectively.
>
> **Answer: A, D and E.**


### AY2023/2024 Semester 1 / Question 3 / Chapter 1 / Determinants of Matrices

#### Question

For 

$$
\det\begin{bmatrix}1&1&1\\a&b&c\\d&e&f\end{bmatrix},
$$

 which expressions always have the same value?

**A.** $\begin{vmatrix}b&c\\e&f\end{vmatrix}+\begin{vmatrix}a&c\\d&f\end{vmatrix}+\begin{vmatrix}a&b\\d&e\end{vmatrix}$

**B.** $a\begin{vmatrix}1&1\\e&f\end{vmatrix}-b\begin{vmatrix}1&1\\d&f\end{vmatrix}+c\begin{vmatrix}1&1\\d&e\end{vmatrix}$

**C.** $d\begin{vmatrix}1&1\\b&c\end{vmatrix}-e\begin{vmatrix}1&1\\a&c\end{vmatrix}+f\begin{vmatrix}1&1\\a&b\end{vmatrix}$

**D.** $\begin{vmatrix}a&b\\d&e\end{vmatrix}+\begin{vmatrix}b&c\\e&f\end{vmatrix}+\begin{vmatrix}c&a\\f&d\end{vmatrix}$

**E.** $\begin{vmatrix}b&c\\e&f\end{vmatrix}-a\begin{vmatrix}1&1\\e&f\end{vmatrix}+d\begin{vmatrix}1&1\\b&c\end{vmatrix}$

> [!success]- Worked Solution
> Expand along the first row or first column and compare each expression, including the alternating signs. The official key identifies **C, D and E**.


### AY2023/2024 Semester 2 / Question 3 / Chapter 1 / Determinants of Matrices

#### Question

Which determinants equal $\begin{vmatrix}a&b&c\\d&e&0\\f&0&0\end{vmatrix}$ for all $a,b,c,d,e,f$?

**A.** $\begin{vmatrix}f&0&0\\d&e&0\\a&b&c\end{vmatrix}$

**B.** $\begin{vmatrix}0&0&f\\0&e&d\\c&b&a\end{vmatrix}$

**C.** $\begin{vmatrix}-c&-b&-a\\0&-e&-d\\0&0&-f\end{vmatrix}$

**D.** $\begin{vmatrix}e&d&0\\b&a&c\\0&f&0\end{vmatrix}$

**E.** $\begin{vmatrix}0&0&f\\c&b&a\\0&e&d\end{vmatrix}$

> [!success]- Worked Solution
> The original determinant is $-cef$. Evaluate each candidate by expansion or row operations. **Answer: B, C and D.**


### AY2024/2025 Semester 1 / Question 3 / Chapter 1 / Determinants of Matrices

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


### AY2024/2025 Semester 2 / Question 3 / Chapter 1 / Determinants of Matrices

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


### AY2025/2026 Semester 1 / Question 2 / Chapter 1 / Determinants of Matrices

### Question

Given
$$A=\begin{bmatrix}1 & 1 & *\\a & b & *\\b & a & *\end{bmatrix},$$
where $a,b$ are non-zero and $a\ne\pm b$, which can be the third column if $\det(A)=0$?

**A.** $\begin{bmatrix}0\\1\\-1\end{bmatrix}$

**B.** $\begin{bmatrix}1\\a+b\\a+b\end{bmatrix}$

**C.** $\begin{bmatrix}1\\a\\b\end{bmatrix}$

**D.** $\begin{bmatrix}0\\b\\a\end{bmatrix}$

**E.** $\begin{bmatrix}1\\2a-b\\2b-a\end{bmatrix}$

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



### AY2022/2023 Semester 2 / Question 2 / Chapter 1 / Non-Singular Matrices

#### Question

Let $A,B$ be non-singular $n\times n$ matrices. Which statements are always true?

**A.** $AB$ is non-singular.

**B.** $A+B$ is non-singular.

**C.** $A^{-1}B^{-1}=(AB)^{-1}$.

**D.** $A^T$ is non-singular.

**E.** $cB$ is non-singular for any scalar $c$.

> [!success]- Worked Solution
> **A — True.** $(AB)^{-1}=B^{-1}A^{-1}$.
>
> **B — False.** Take $B=-A$.
>
> **C — False.** The correct order is $(AB)^{-1}=B^{-1}A^{-1}$.
>
> **D — True.** $\det(A^T)=\det(A)\ne0$.
>
> **E — False.** $c=0$ gives the zero matrix.
>
> **Answer: A and D.**


### AY2023/2024 Semester 1 / Question 2 / Chapter 1 / Non-Singular Matrices

#### Question

Suppose $A=(c_1\ c_2\ c_3)$ is a singular $3\times3$ matrix. Which statements are always true?

**A.** $c_1$ is a linear combination of $c_2,c_3$.

**B.** $\{c_1,c_2,c_3\}$ is a basis for $\mathbb R^3$.

**C.** Any row echelon form of $A$ has a non-pivot column.

**D.** $\operatorname{nullity}(A)\ne0$.

**E.** $Ax=b$ has infinitely many solutions for every $b\in\mathbb R^3$.

> [!success]- Worked Solution
> **C — True:** rank is less than 3, so at least one non-pivot column exists. **D — True:** rank-nullity gives positive nullity. **A, B, E — False:** singularity does not force $c_1$ to depend on the other two; columns cannot be a basis; some right-hand sides yield inconsistent systems. **Answer: C, D.**


### AY2023/2024 Semester 2 / Question 2 / Chapter 1 / Non-Singular Matrices

#### Question

Let $A=(c_1\ c_2\ c_3)$ be a non-singular $3\times3$ matrix. Which statements hold?

**A.** $c_1,c_2,c_3$ are coplanar.

**B.** Any REF of $A$ has three pivot columns.

**C.** The rows of $A$ form a basis for $\mathbb R^3$.

**D.** $\det A\ne0$.

**E.** The system $[c_1\ c_2]x=c_3$ is consistent.

> [!success]- Worked Solution
> Non-singularity means rows and columns are independent, rank is 3 and determinant is nonzero. The third column cannot be a combination of the first two. **Answer: B, C and D.**



### AY2024/2025 Semester 1 / Question 2 / Chapter 1 / Matrices

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



### AY2024/2025 Semester 2 / Question 2 / Chapter 1 / Matrix Inverses II

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



### AY2024/2025 Semester 2 / Question 4 / Chapter 1 / Ranks of Matrices

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



### AY2025/2026 Semester 1 / Question 1 / Chapter 1 / Systems of Linear Equations

### Question

Given the general solution of the non-homogeneous system $Ax=b$:

$$
\begin{cases}
x=s-t+1\\
y=s\\
z=t
\end{cases}
$$

Which of the following are true?

**A.** $\begin{cases}x=t-s\\y=t\\z=s\end{cases}$
is a general solution of $Ax=0$.

**B.** $\begin{cases}x=s-t+1\\y=s+1\\z=t+1\end{cases}$
is a general solution of $Ax=b$.

**C.** $\begin{cases}x=s-t\\y=s+1\\z=t+1\end{cases}$
is a general solution of $Ax=0$.

**D.** $\begin{cases}x=1\\y=t\\z=t\end{cases}$
is a general solution of $Ax=b$.

**E.** $\begin{cases}x=1-s+t\\y=s\\z=t\end{cases}$
is a general solution of $Ax=b$.

> [!success]- Worked Solution
> Split the given solution into the homogeneous parameter part and a particular solution:
>
> $$
> \begin{bmatrix}x\\y\\z\end{bmatrix}
> =s\begin{bmatrix}1\\1\\0\end{bmatrix}
> +t\begin{bmatrix}-1\\0\\1\end{bmatrix}
> +\begin{bmatrix}1\\0\\0\end{bmatrix}.
> $$
>
> **A - True.** This is the homogeneous solution with the parameter names interchanged.
>
> **B - True.** The parameter part is unchanged and $\begin{bmatrix}1&1&1\end{bmatrix}^T$ is another particular solution of $Ax=b$.
>
> **C - True.** The added vector $\begin{bmatrix}0&1&1\end{bmatrix}^T$ is itself a homogeneous solution.
>
> **D - False.** It contains only one parameter, so it is not the general solution.
>
> **E - False.** The signs in the parameter part do not give the same homogeneous solution set.
>
> **Answer: A, B and C.**



# Chapter 2

### AY2022/2023 Semester 1 / Question 4 / Chapter 2 / Linear Combination and Linear Span

#### Question

Which spans **do not** contain $(1,2,3,4)$? Select all correct answers.

**A.** $\operatorname{span}\{(4,3,2,1)\}$

**B.** $\operatorname{span}\{(1,2),(3,4)\}$

**C.** $\operatorname{span}\{(1,0,3,0),(0,2,0,4)\}$

**D.** $\operatorname{span}\{(2,3,4,1),(3,4,1,2),(4,1,2,3)\}$

**E.** $\operatorname{span}\{(4,0,0,0),(0,3,0,0),(0,0,2,0),(0,0,0,1)\}$

> [!success]- Worked Solution
> **A — Does not contain it.** $(1,2,3,4)$ is not a scalar multiple of $(4,3,2,1)$.
>
> **B — Does not contain it.** The spanning vectors lie in $\mathbb R^2$, whereas the target lies in $\mathbb R^4$.
>
> **C — Contains it.** $(1,2,3,4)=(1,0,3,0)+(0,2,0,4)$.
>
> **D — Does not contain it.** The linear combination equations for the three generators are inconsistent.
>
> **E — Contains it.** The four generators are nonzero multiples of the standard basis of $\mathbb R^4$.
>
> **Answer: A and D.**


### AY2022/2023 Semester 2 / Question 4 / Chapter 2 / Linear Combination and Linear Span

#### Question

Which spans contain $(3,6,9)$? (Pick all correct options)

**A.** $\operatorname{span}\{(9,0,0),(0,6,0),(0,0,3)\}$

**B.** $\operatorname{span}\{(9,6,3)\}$

**C.** $\operatorname{span}\{(10,20,30)\}$

**D.** $\operatorname{span}\{(3,0,9),(0,6,0)\}$

**E.** $\operatorname{span}\{(1,1,0),(0,1,1),(1,2,1),(1,0,-1)\}$

> [!success]- Worked Solution
> **A — True.** $(3,6,9)=\frac13(9,0,0)+(0,6,0)+3(0,0,3)$.
>
> **B — False.** The target is not a multiple of $(9,6,3)$.
>
> **C — True.** $(3,6,9)=\frac3{10}(10,20,30)$.
>
> **D — True.** $(3,6,9)=(3,0,9)+(0,6,0)$.
>
> **E — False.** Every spanning vector satisfies $x-y+z=0$, but the target gives $3-6+9=6$.
>
> **Answer: A, C and D.**


### AY2024/2025 Semester 1 / Question 4 / Chapter 2 / Linear Combination and Linear Span

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


### AY2024/2025 Semester 2 / Question 5 / Chapter 2 / Linear Combination and Linear Span

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


### AY2025/2026 Semester 1 / Question 6 / Chapter 2 / Linear Combination and Linear Span

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



### AY2022/2023 Semester 1 / Question 5 / Chapter 2 / Linear Dependence

#### Question

Which sets of vectors in $\mathbb R^3$ all lie in the same plane?

**A.** $(0,0,0),(1,2,0),(2,0,1)$

**B.** $(1,2,1),(2,1,1),(1,1,2)$

**C.** $(1,2,3),(4,5,6),(7,8,9)$

**D.** $(2,2,0),(0,0,3),(1,1,1),(3,3,2)$

**E.** $(1,0,1),(0,1,1),(0,0,1)$

> [!success]- Worked Solution
> Vectors lie in a common plane through the origin when their span has dimension at most two.
>
> **A — True.** The zero vector and two other vectors span at most a plane.
>
> **B — False.** The three vectors are linearly independent.
>
> **C — True.** $(7,8,9)=2(4,5,6)-(1,2,3)$.
>
> **D — True.** Every vector has its first two coordinates equal; all lie in the plane $x=y$.
>
> **E — False.** The three vectors are linearly independent.
>
> **Answer: A, C and D.**



### AY2022/2023 Semester 1 / Question 6 / Chapter 2 / Orthogonal Projection

#### Question

The projection of $(1,2,3,0)$ onto $V=\operatorname{span}\{(1,0,1,0),(0,1,0,1)\}$ is $p=(a,b,c,d)$. Find $a,b,c,d$.

> [!success]- Worked Solution
> The spanning vectors $u_1=(1,0,1,0)$ and $u_2=(0,1,0,1)$ are orthogonal, with $u_1\cdot u_1=u_2\cdot u_2=2$.
>
> $$p=\frac{(1,2,3,0)\cdot u_1}{u_1\cdot u_1}u_1+\frac{(1,2,3,0)\cdot u_2}{u_2\cdot u_2}u_2=2u_1+u_2.$$
>
> Thus $p=(2,1,2,1)$.
>
> **Answer: $a=2,b=1,c=2,d=1$.**



### AY2022/2023 Semester 1 / Question 7 / Chapter 2 / Coordinate Vectors

#### Question

Let $S=\{(1,1,0),(1,0,1),(0,1,1)\}$ and $T=\{(3,0,0),(0,4,0),(0,0,5)\}$ be bases for $\mathbb R^3$. If $[v]_S=(1,2,3)$, find $[v]_T=(a,b,c)$.

> [!success]- Worked Solution
> First recover $v$ from the $S$-coordinates:
>
> $$v=(1,1,0)+2(1,0,1)+3(0,1,1)=(3,4,5).$$
>
> Express $v=a(3,0,0)+b(0,4,0)+c(0,0,5)$, giving $a=b=c=1$.
>
> **Answer: $a=1,b=1,c=1$.**


### AY2022/2023 Semester 2 / Question 7 / Chapter 2 / Coordinate Vectors

#### Question

Let $M$ be a non-singular $3\times3$ matrix with columns $\mathbf c_1,\mathbf c_2,\mathbf c_3$. Suppose

$$M\begin{bmatrix}1\\2\\3\end{bmatrix}=\begin{bmatrix}3\\2\\1\end{bmatrix}.$$

Which statements are true?

**A.** $3\mathbf c_1+2\mathbf c_2+\mathbf c_3$ is the coordinate vector of $\begin{bmatrix}1\\2\\3\end{bmatrix}$ relative to the basis $\{\mathbf c_1,\mathbf c_2,\mathbf c_3\}$.

**B.** $\begin{bmatrix}3\\2\\1\end{bmatrix}$ is the coordinate vector of $\begin{bmatrix}1\\2\\3\end{bmatrix}$ relative to that basis.

**C.** $\begin{bmatrix}1\\2\\3\end{bmatrix}$ is the coordinate vector of $\begin{bmatrix}3\\2\\1\end{bmatrix}$ relative to that basis.

**D.** $\begin{bmatrix}1\\1\\1\end{bmatrix}$ is the coordinate vector of $\mathbf c_1+\mathbf c_2+\mathbf c_3$ relative to that basis.

**E.** $\mathbf c_1+\mathbf c_2+\mathbf c_3$ is the coordinate vector of $\begin{bmatrix}1\\1\\1\end{bmatrix}$ relative to that basis.

> [!success]- Worked Solution
> The defining equation means $\mathbf c_1+2\mathbf c_2+3\mathbf c_3=\begin{bmatrix}3\\2\\1\end{bmatrix}$. Thus the coordinate vector of the right-hand vector is $\begin{bmatrix}1\\2\\3\end{bmatrix}$ (**C**). By definition the coordinate vector of $\mathbf c_1+\mathbf c_2+\mathbf c_3$ is $\begin{bmatrix}1\\1\\1\end{bmatrix}$ (**D**).
>
> **Answer: C and D.**


### AY2023/2024 Semester 1 / Question 7 / Chapter 2 / Coordinate Vectors

#### Question

The coordinate axes are rotated $45^\circ$ clockwise about the $z$-axis, viewed from above. Find the coordinates $(a,b,c)$ of $(3\sqrt2,\sqrt2,3)$ in the new axes.

**A.** Fill in $a,b,c$.

> [!success]- Worked Solution
> Using the clockwise-rotated basis $e_1=(1,-1,0)/\sqrt2$ and $e_2=(1,1,0)/\sqrt2$, take dot products with the given vector. **Answer:** $(a,b,c)=(2,4,3)$.


### AY2023/2024 Semester 2 / Question 7 / Chapter 2 / Coordinate Vectors

#### Question

For $S=\{(1,0,0),(0,1,1),(0,-1,1)\}$ and $[v]_S=(2,3,5)$, find $[v]_T=(a,b,c)$ where $T=\{(1,-1,0),(1,1,0),(0,0,1)\}$.

> [!success]- Worked Solution
> First calculate $v=2(1,0,0)+3(0,1,1)+5(0,-1,1)=(2,-2,8)$. Then solve $a(1,-1,0)+b(1,1,0)+c(0,0,1)=v$. **Answer:** $(a,b,c)=(2,0,8)$.


### AY2024/2025 Semester 1 / Question 6 / Chapter 2 / Coordinate Vectors

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


### AY2024/2025 Semester 2 / Question 8 / Chapter 2 / Coordinate Vectors

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


### AY2025/2026 Semester 1 / Question 7 / Chapter 2 / Coordinate Vectors

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
> $$[w]_S=\begin{bmatrix}2\\1\\0\\3\end{bmatrix}.$$
>
> **Answer: $a=2,b=1,c=0,d=3$.**



### AY2022/2023 Semester 1 / Question 8 / Chapter 2 / Row Space, Column Space and Nullspace

#### Question

Let $A$ be a $3\times5$ matrix. Which statements are true?

**A.** The row space of $A$ is a subspace of $\mathbb R^3$.

**B.** The sum of two columns of $A$ is again a column of $A$.

**C.** $A$ cannot be full rank.

**D.** The nullity of $A$ is at least $2$.

**E.** The nullspace of $A$ is a subspace of $\mathbb R^5$.

> [!success]- Worked Solution
> **A — False.** Each row has five entries, so the row space is a subspace of $\mathbb R^5$.
>
> **B — False.** A column space is closed under addition, but the resulting vector need not be one of the actual columns of $A$.
>
> **C — False.** A $3\times5$ matrix can have full rank $3$.
>
> **D — True.** Rank-nullity gives $\operatorname{nullity}(A)=5-\operatorname{rank}(A)\ge2$.
>
> **E — True.** Solutions to $Ax=0$ are vectors in $\mathbb R^5$.
>
> **Answer: D and E.**



### AY2022/2023 Semester 2 / Question 5 / Chapter 2 / Basis and Dimension

#### Question

Which sets form bases for $\mathbb R^4$?

**A.** $\{(1,0,0,0),(0,1,0,0),(0,0,1,0),(1,1,1,1)\}$

**B.** $\{(1,1,1,1),(1,0,1,0),(0,1,0,1),(0,1,1,0)\}$

**C.** $\{(1,2,1,1),(1,1,2,1),(1,1,1,2)\}$

**D.** $\{(1,2,3,1),(1,4,5,1),(1,6,7,1),(1,8,9,1)\}$

**E.** $\{(1,1,1,0),(1,1,0,1),(1,0,1,1),(0,1,1,1)\}$

> [!success]- Worked Solution
> A basis of $\mathbb R^4$ requires four independent vectors. **A** is independent since the fourth vector has a nonzero fourth component. **B** is dependent since its first vector equals the sum of its second and third. **C** has only three vectors. **D** is dependent because successive columns have equal differences. **E** is independent (its determinant is nonzero).
>
> **Answer: A and E.**


### AY2023/2024 Semester 1 / Question 5 / Chapter 2 / Basis and Dimension

#### Question

Which sets form bases for $\operatorname{span}\{(1,2,1,1),(1,0,2,-1),(1,4,0,3),(-1,0,-2,1)\}\subseteq\mathbb R^4$?

**A.** $\{(1,0,0,0),(0,1,0,0),(0,0,1,0),(0,0,0,1)\}$

**B.** $\{(1,2,1,1),(1,0,2,-1),(1,4,0,3)\}$

**C.** $\{(1,0,2,-1),(1,4,0,3)\}$

**D.** $\{(1,2,1,1),(-1,0,-2,1)\}$

**E.** $\{(1,0,2,0),(0,1,-1,-1)\}$

> [!success]- Worked Solution
> The given span has dimension 2. Test each candidate for independence and whether its span equals the original span. The official solution identifies **C, D and E**.


### AY2024/2025 Semester 1 / Question 5 / Chapter 2 / Basis and Dimension

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


### AY2024/2025 Semester 2 / Question 7 / Chapter 2 / Basis and Dimension

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


### AY2025/2026 Semester 1 / Question 4 / Chapter 2 / Basis and Dimension

### Question

Given
$$A=\begin{bmatrix}2&3&1\\0&1&-1\\1&1&1\end{bmatrix},$$
which of the following sets form a basis for the column space of $A$?

**A.** $\left\{\begin{bmatrix}2\\0\\1\end{bmatrix},\begin{bmatrix}3\\1\\1\end{bmatrix},\begin{bmatrix}1\\-1\\1\end{bmatrix}\right\}$

**B.** $\left\{\begin{bmatrix}1\\-1\\1\end{bmatrix},\begin{bmatrix}3\\1\\1\end{bmatrix}\right\}$

**C.** $\left\{\begin{bmatrix}1\\0\\0\end{bmatrix},\begin{bmatrix}0\\1\\0\end{bmatrix}\right\}$

**D.** $\left\{\begin{bmatrix}1\\1\\0\end{bmatrix},\begin{bmatrix}1\\-1\\1\end{bmatrix}\right\}$

**E.** $\left\{\begin{bmatrix}2\\0\\-1\end{bmatrix},\begin{bmatrix}3\\-1\\-1\end{bmatrix}\right\}$

> [!success]- Worked Solution
> The RREF of $A$ has two pivot columns, so $\dim(\operatorname{Col}(A))=2$. A basis therefore needs two linearly independent vectors in the column space.
>
> **B** uses columns of $A$. **D** also lies in the column space, with its first vector obtained from the first two columns and its second vector equal to the third column. The other sets fail the span/dimension test.
>
> **Answer: B and D.**



### AY2022/2023 Semester 2 / Question 6 / Chapter 2 / Projection

#### Question

Find the projection $\mathbf p=(a,b,c)$ of $(3,3,3)$ onto the plane $x-y+2z=0$. (FIB)

> [!success]- Worked Solution
> A normal vector is $\mathbf n=(1,-1,2)$, so
>
> $$\mathbf p=(3,3,3)-\frac{(3,3,3)\cdot(1,-1,2)}{(1,-1,2)\cdot(1,-1,2)}(1,-1,2).$$
>
> Since the dot products are $6$ and $6$, $\mathbf p=(3,3,3)-(1,-1,2)=(2,4,1)$.
>
> **Answer: $a=2,\ b=4,\ c=1$.**


### AY2023/2024 Semester 1 / Question 6 / Chapter 2 / Projection

#### Question

Which vectors project orthogonally onto $p=(-1,1,3)$ on the plane $x-2y+z=0$?

**A.** $(1,-2,1)$

**B.** $(3,0,1)$

**C.** $(0,-1,4)$

**D.** $(-2,3,2)$

**E.** $(1,0,-1)$

> [!success]- Worked Solution
> The normal is $n=(1,-2,1)$. Every original vector must be $p+tn$. Check differences against this form. **Answer: C and D.**


### AY2023/2024 Semester 2 / Question 6 / Chapter 2 / Projection

#### Question

Project $\begin{bmatrix}6\\0\\12\end{bmatrix}$ onto the column space of $\begin{bmatrix}1&2\\2&1\\1&2\end{bmatrix}$. Find $p=(a,b,c)$.

> [!success]- Worked Solution
> Solve the normal equations $A^TAx=A^Tb$, then $p=Ax$. **Answer:** $(a,b,c)=(9,0,9)$.



### AY2022/2023 Semester 2 / Question 8 / Chapter 2 / Subspaces

#### Question

An unknown matrix $A$ is singular, and its RREF $R$ is known. Which statements are true?

**A.** We can determine the row space of $A$.

**B.** We can determine the column space of $A$.

**C.** We can determine the nullspace of $A$.

**D.** We can determine $A$.

**E.** We can find a basis for the solution space of $Ax=0$.

> [!success]- Worked Solution
> **A — True.** The nonzero rows of $R$ span the row space.
>
> **B — False.** Row reduction does not generally preserve column space.
>
> **C — True.** $Ax=0$ and $Rx=0$ have identical solution sets.
>
> **D — False.** Different matrices may have the same RREF.
>
> **E — True.** Solve $Rx=0$ and obtain a nullspace basis.
>
> **Answer: A, C and E.**


### AY2023/2024 Semester 2 / Question 8 / Chapter 2 / Subspaces

#### Question

Which subspaces equal the plane $3x+y-2z=0$?

**A.** $\operatorname{span}\\{(3,1,-2)\\}$

**B.** $\operatorname{Row}\begin{bmatrix}1&-1&1\\0&2&1\\3&1&-2\end{bmatrix}$

**C.** $\operatorname{Null}\begin{bmatrix}3&1&-2\\0&0&0\end{bmatrix}$

**D.** $\operatorname{Col}\begin{bmatrix}2&1&0\\0&-3&2\\3&0&1\end{bmatrix}$

**E.** $\operatorname{Null}\begin{bmatrix}3&0&0\\0&1&0\\0&0&-2\end{bmatrix}$

> [!success]- Worked Solution
> The plane is the nullspace of the row $(3,1,-2)$. The other proposed spaces must be tested for containment and dimension. **Answer: C.**


### AY2024/2025 Semester 1 / Question 8 / Chapter 2 / Subspaces

### Question

Three of the following subspaces of $\mathbb R^3$ are the same. Select the two that are not the same as those three.

1. $\operatorname{span}\{(1,-1,0),(1,0,-1)\}$
2. Nullspace of $\begin{bmatrix}1 & 1 & 1\\2 & 2 & 2\\3 & 3 & 3\end{bmatrix}$
3. Row space of $\begin{bmatrix}1 & -1 & 0\\1 & 0 & -1\\1 & 1 & 1\end{bmatrix}$
4. Column space of $\begin{bmatrix}2 & 0 & 0\\-1 & 1 & 0\\-1 & -1 & 0\end{bmatrix}$
5. Solution space of $x+2y+3z=0$.

> [!success]- Worked Solution
> The nullspace in option 2 has dimension 2. The two vectors in option 1 lie in that nullspace and are independent, so 1 and 2 are the same. The columns in option 4 also lie in that nullspace and span a 2-dimensional space, so 4 is the same space. Options 3 and 5 are different.
>
> **Answer: 3 and 5.**



### AY2023/2024 Semester 1 / Question 4 / Chapter 2 / Row Space

#### Question

Which matrices have $(3,6,9)$ in their row space?

**A.** $\begin{bmatrix}0&0&3\\0&6&0\\9&0&0\end{bmatrix}$

**B.** $\begin{bmatrix}3&3&3\\6&6&6\\9&9&9\end{bmatrix}$

**C.** $\begin{bmatrix}3&6&0\\0&6&9\end{bmatrix}$

**D.** $\begin{bmatrix}1&2&3\\1&1&1\\0&0&0\end{bmatrix}$

**E.** $\begin{bmatrix}3&3&3\\0&3&3\\0&0&3\\6&3&0\end{bmatrix}$

> [!success]- Worked Solution
> **A:** row space is all of $\mathbb R^3$. **B:** only multiples of $(1,1,1)$. **C:** no row combination gives the target. **D:** $(3,6,9)=3(1,2,3)$. **E:** the first three rows span $\mathbb R^3$. **Answer: A, D, E.**


### AY2023/2024 Semester 2 / Question 4 / Chapter 2 / Row Space

#### Question

Which vectors lie in the row space of $\begin{bmatrix}1&2&3&4\\1&1&1&1\\3&5&7&9\end{bmatrix}$?

**A.** $(3,6,9,12)$

**B.** $(4,3,2,1)$

**C.** $(1,2,4,8)$

**D.** $(3,7,5,9)$

**E.** $(19,29,39,49)$

> [!success]- Worked Solution
> Row 3 is a combination of rows 1 and 2. **A:** $3r_1$. **B:** $5r_2-r_1$. **E:** $10r_1+9r_2$. **Answer: A, B, E.**



### AY2023/2024 Semester 1 / Question 8 / Chapter 2 / Column Space

#### Question

Given the RREF $R$ of an unknown matrix $A$, which conditions allow the column space of $A$ to be determined?

**A.** $R$ is full rank.

**B.** $R$ has no zero row.

**C.** $R$ has no non-pivot columns.

**D.** $R$ is square.

**E.** It is impossible without knowing $A$.

> [!success]- Worked Solution
> The RREF generally preserves row space, not column space. If every column pivots, $A$ has full column rank and the column space is the full ambient space only when the number of rows equals rank; check the precise condition in the source. **Answer: C** (as given in the official key).


### AY2023/2024 Semester 2 / Question 5 / Chapter 2 / Column Space

#### Question

Which matrices have column space $\operatorname{span}\{(1,1,0),(0,0,1)\}$?

**A.** $\begin{bmatrix}2&0&0\\2&0&0\\0&3&0\end{bmatrix}$

**B.** $\begin{bmatrix}1&1&1\\1&1&1\\1&2&3\end{bmatrix}$

**C.** $\begin{bmatrix}1&0&1\\1&0&2\\0&1&3\end{bmatrix}$

**D.** $\begin{bmatrix}1&0&1&-1\\0&1&1&1\\0&1&1&1\end{bmatrix}$

**E.** $\begin{bmatrix}1&-1&1&-1\\1&-1&1&-1\\0&0&1&-1\end{bmatrix}$

> [!success]- Worked Solution
> The target plane consists of $(x,x,z)$. Test each column and ensure rank 2. **Answer: A, B and E.**



### AY2024/2025 Semester 1 / Question 7 / Chapter 2 / Linear Independence

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


### AY2024/2025 Semester 2 / Question 6 / Chapter 2 / Linear Independence

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


### AY2025/2026 Semester 1 / Question 5 / Chapter 2 / Linear Independence

### Question

Which of the following sets are linearly independent?

**A.** $\{(10,11,12),(20,21,22),(30,31,32)\}$

**B.** $\{(1,3,2,4),(4,2,3,1),(1,1,1,1)\}$

**C.** $\{(0,1,2,3),(0,2,3,1),(0,3,1,2)\}$

**D.** $\{(0,0,0,1),(0,0,1,5),(0,1,5,1),(1,5,1,3)\}$

**E.** $\{(2,3,5),(7,11,13),(17,19,23),(29,31,37)\}$

> [!success]- Worked Solution
> Stack the vectors in each option as rows or columns and row-reduce. A set is linearly independent exactly when every vector corresponds to a pivot.
>
> Applying this test gives **B, C and D** as the linearly independent sets.
>
> **Answer: B, C and D.**



### AY2024/2025 Semester 2 / Question 12 / Chapter 2 / Projection and Linear Approximation

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


### AY2025/2026 Semester 1 / Question 8 / Chapter 2 / Vectors in n-Space

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

# Chapter 3



# Chapter 3

### AY2022/2023 Semester 1 / Question 9 / Chapter 3 / Linear Transformation

#### Question

A linear transformation $T:\mathbb R^2\to\mathbb R^2$ satisfies

$$
T\left(\begin{bmatrix}2\\3\end{bmatrix}\right)=\begin{bmatrix}1\\-2\end{bmatrix},\qquad
T\left(\begin{bmatrix}3\\4\end{bmatrix}\right)=\begin{bmatrix}2\\1\end{bmatrix}.
$$

Find $a,b,c,d$ in its standard matrix $A=\begin{bmatrix}a&b\\c&d\end{bmatrix}$.

> [!success]- Worked Solution
> Place the given input vectors and their images into columns:
>
> $$
> A\begin{bmatrix}2&3\\3&4\end{bmatrix}=\begin{bmatrix}1&2\\-2&1\end{bmatrix}.
> $$
>
> The input matrix has determinant $8-9=-1$, hence
>
> $$
> A=\begin{bmatrix}1&2\\-2&1\end{bmatrix}\begin{bmatrix}-4&3\\3&-2\end{bmatrix}
> =\begin{bmatrix}2&-1\\11&-8\end{bmatrix}.
> $$
>
> **Answer: $a=2,\ b=-1,\ c=11,\ d=-8$.**


### AY2022/2023 Semester 2 / Question 9 / Chapter 3 / Linear Transformation

#### Question

Let $T:\mathbb R^3\to\mathbb R^3$ have standard matrix

$$A=\begin{bmatrix}1&2&a\\2&0&b\\1&-1&c\end{bmatrix}.$$

If $T\left(\begin{bmatrix}1\\2\\1\end{bmatrix}\right)=\begin{bmatrix}2\\0\\-1\end{bmatrix}$, find $a,b,c$. (FIB)

> [!success]- Worked Solution
> Multiply the matrix by the given vector:
>
> $$\begin{bmatrix}5+a\\2+b\\-1+c\end{bmatrix}=\begin{bmatrix}2\\0\\-1\end{bmatrix}.$$
>
> Equating components gives **$a=-3,\ b=-2,\ c=0$.**


### AY2023/2024 Semester 1 / Question 9 / Chapter 3 / Linear Transformation

#### Question

Let $T:\mathbb R^3\to\mathbb R^3$ have standard matrix $A$ with first two columns $\begin{bmatrix}1\\1\\0\end{bmatrix}$ and $\begin{bmatrix}0\\1\\1\end{bmatrix}$. Knowing $T(v)$ for which $v$ determines $T$ completely?

**A.** $\begin{bmatrix}1\\1\\0\end{bmatrix}$

**B.** $\begin{bmatrix}0\\1\\1\end{bmatrix}$

**C.** $\begin{bmatrix}1\\2\\1\end{bmatrix}$

**D.** $\begin{bmatrix}1\\0\\0\end{bmatrix}$

**E.** Any vector outside the span of the first two columns of $A$.

> [!success]- Worked Solution
> To determine the third column of $A$, one needs a vector with nonzero third coordinate in the standard basis. **Answer: B and C** according to the source-key classification; check the role of option E carefully when revising.


### AY2023/2024 Semester 2 / Question 9 / Chapter 3 / Linear Transformation

#### Question

Given $T(\begin{bmatrix}1\\2\\0\end{bmatrix})=\begin{bmatrix}1\\2\\1\end{bmatrix}$ and $T(\begin{bmatrix}1\\1\\1\end{bmatrix})=\begin{bmatrix}2\\1\\0\end{bmatrix}$, find $T(\begin{bmatrix}7\\10\\4\end{bmatrix})$.

> [!success]- Worked Solution
> Since $(7,10,4)=3(1,2,0)+4(1,1,1)$, linearity gives $3(0,2,1)+4(2,1,0)=(11,10,3)$. **Answer:** $(8,10,3)$.


### AY2024/2025 Semester 1 / Question 9 / Chapter 3 / Linear Transformation

### Question

Let $T:\mathbb R^3\to\mathbb R^3$ be linear with
$$T\left(\begin{bmatrix}1\\1\\0\end{bmatrix}\r\right)=\begin{bmatrix}0\\1\\1\end{bmatrix},\qquad T\left(\begin{bmatrix}0\\1\\1\end{bmatrix}\r\right)=\begin{bmatrix}1\\1\\0\end{bmatrix}.$$
Find
$$T\left(\begin{bmatrix}2\\5\\3\end{bmatrix}\r\right)=\begin{bmatrix}a\\b\\c\end{bmatrix}.$$

> [!success]- Worked Solution
> Since
> $$\begin{bmatrix}2\\5\\3\end{bmatrix}=2\begin{bmatrix}1\\1\\0\end{bmatrix}+3\begin{bmatrix}0\\1\\1\end{bmatrix},$$
> linearity gives
> $$T\left(\begin{bmatrix}2\\5\\3\end{bmatrix}
> \r\right)=2\begin{bmatrix}0\\1\\1\end{bmatrix}+3\begin{bmatrix}1\\1\\0\end{bmatrix}=\begin{bmatrix}3\\5\\2\end{bmatrix}.$$
>
> **Answer: $a=3,b=5,c=2$.**


### AY2024/2025 Semester 2 / Question 9 / Chapter 3 / Linear Transformation

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


### AY2025/2026 Semester 1 / Question 9 / Chapter 3 / Linear Transformation

### Question

Given a linear transformation $T:\mathbb R^4\to\mathbb R^3$ with
$$T\left(\begin{bmatrix}3\\5\\2\\2\end{bmatrix}\r\right)=\begin{bmatrix}3\\2\\1\end{bmatrix},\qquad T\left(\begin{bmatrix}4\\4\\2\\3\end{bmatrix}\r\right)=\begin{bmatrix}1\\1\\1\end{bmatrix},$$
find
$$T\left(\begin{bmatrix}1\\7\\2\\0\end{bmatrix}\r\right).$$

> [!success]- Worked Solution
> First express the input as
> $$\begin{bmatrix}1\\7\\2\\0\end{bmatrix}=3\begin{bmatrix}3\\5\\2\\2\end{bmatrix}-2\begin{bmatrix}4\\4\\2\\3\end{bmatrix}.$$
> By linearity,
> $$T\left(\begin{bmatrix}1\\7\\2\\0\end{bmatrix}
> \r\right)=3\begin{bmatrix}3\\2\\1\end{bmatrix}-2\begin{bmatrix}1\\1\\1\end{bmatrix}=\begin{bmatrix}7\\4\\1\end{bmatrix}.$$
>
> **Answer: $(a,b,c)=(7,4,1)$.**



### AY2022/2023 Semester 1 / Question 10 / Chapter 3 / Diagonalizable Matrices

#### Question

Let $A,B,C$ be upper-triangular matrices in which each $*$ is arbitrary:

$$
A=\begin{bmatrix}2&*&*\\0&3&*\\0&0&4\end{bmatrix},\quad
B=\begin{bmatrix}2&*&*\\0&2&*\\0&0&3\end{bmatrix},\quad
C=\begin{bmatrix}2&*&*\\0&2&*\\0&0&2\end{bmatrix}.
$$

Which statements are true?

**A.** $A$ may or may not be diagonalizable.

**B.** $B$ may or may not be diagonalizable.

**C.** $C$ must be non-diagonalizable.

**D.** All eigenspaces of $A$ must have dimension $1$.

**E.** $B$ must have an eigenspace of dimension $2$.

> [!success]- Worked Solution
> **A — False.** The three distinct diagonal entries of $A$ are distinct eigenvalues; $A$ is always diagonalizable.
>
> **B — True.** The repeated eigenvalue $2$ may have eigenspace dimension $1$ or $2$, depending on the starred entries.
>
> **C — False.** Setting all starred entries to zero gives $C=2I$, which is diagonalizable.
>
> **D — True.** Every eigenvalue of $A$ has algebraic multiplicity $1$, so each eigenspace has dimension $1$.
>
> **E — False.** For some choices of starred entries the eigenspace for eigenvalue $2$ has dimension $1$.
>
> **Answer: B and D.**


### AY2022/2023 Semester 2 / Question 10 / Chapter 3 / Diagonalizable Matrices

#### Question

Each $*$ may be any number. Which matrices must be diagonalizable?

**A.** $A=\begin{bmatrix}1&0&0\\ *&3&0\\ *&*&5\end{bmatrix}$

**B.** $B=\begin{bmatrix}6&*&*\\0&0&*\\0&0&6\end{bmatrix}$

**C.** $C=\begin{bmatrix}*&1&2\\1&*&3\\2&3&*\end{bmatrix}$

**D.** Matrix $D$ has one eigenvalue and its eigenspace is $\mathbb R^3$.

**E.** Matrix $E$ can be row-reduced to a diagonal matrix.

> [!success]- Worked Solution
> **A — True.** Three distinct diagonal eigenvalues imply diagonalizability.
>
> **B — False.** Repeated eigenvalue $6$ need not have two independent eigenvectors.
>
> **C — True.** Every real symmetric matrix is diagonalizable.
>
> **D — True.** Its eigenspace has dimension three.
>
> **E — False.** Row reduction is not a similarity transformation.
>
> **Answer: A, C and D.**


### AY2023/2024 Semester 2 / Question 10 / Chapter 3 / Diagonalizable Matrices

#### Question

A diagonalizable $4\times4$ lower-triangular matrix has diagonal entries $2,2,3,3$. Which statements are true?

**A.** Characteristic polynomial is $(x+2)^2(x+3)^2$.

**B.** An eigenspace may have dimension 1.

**C.** $\begin{bmatrix}0\\0\\0\\3\end{bmatrix}$ is an eigenvector.

**D.** There is an invertible $P$ with $PAP^{-1}=\operatorname{diag}(3,3,2,2)$.

**E.** $A^n$ is diagonalizable for every positive integer $n$.

> [!success]- Worked Solution
> The eigenvalues are 2 and 3, each of algebraic multiplicity 2. Since $A$ is diagonalizable, both eigenspaces have dimension 2. Similarity gives the specified diagonal ordering and powers remain diagonalizable. **Answer: D and E.**



### AY2022/2023 Semester 1 / Question 11 / Chapter 3 / Diagonalization

#### Question

Let $P$ be an invertible $3\times3$ matrix with columns $C_1,C_2,C_3$, and suppose

$$P^{-1}AP=\begin{bmatrix}1&0&0\\0&0&0\\0&0&1\end{bmatrix}.$$

Which statements are true?

**A.** The nullspace of $A$ is $\operatorname{span}\{C_2\}$.

**B.** $C_1+C_2$ is an eigenvector of $A$.

**C.** $A^2=A$.

**D.** The matrix with columns $3C_1,-C_2,2C_3+C_1$ diagonalizes $A$.

**E.** $A$ is nonsingular.

> [!success]- Worked Solution
> Since $AP=P\operatorname{diag}(1,0,1)$, we have $AC_1=C_1$, $AC_2=0$, and $AC_3=C_3$.
>
> **A — True.** The only zero-eigenvalue basis direction is $C_2$.
>
> **B — False.** $A(C_1+C_2)=C_1$, which is not a scalar multiple of $C_1+C_2$.
>
> **C — True.** The diagonal matrix $D$ satisfies $D^2=D$, so $A^2=PD^2P^{-1}=A$.
>
> **D — True.** The three proposed columns are independent eigenvectors with eigenvalues $1,0,1$.
>
> **E — False.** $A$ has eigenvalue $0$, hence $\det(A)=0$.
>
> **Answer: A, C and D.**


### AY2022/2023 Semester 2 / Question 11 / Chapter 3 / Diagonalization

#### Question

Suppose $A=PDP^{-1}$, where

$$P=\begin{bmatrix}1&1&0\\1&0&0\\1&1&1\end{bmatrix},\qquad D=\begin{bmatrix}a&0&0\\0&a&0\\0&0&b\end{bmatrix}.$$

Which of the following identities are valid? (Pick all correct options.)

**A.** $A=Q\operatorname{diag}(a,b,a)Q^{-1}$, $Q=\begin{bmatrix}7&0&-1\\7&0&0\\7&3&-1\end{bmatrix}$.

**B.** $2A=Q\operatorname{diag}(2a,2a,2b)Q^{-1}$, $Q=\begin{bmatrix}2&2&0\\2&0&0\\2&2&2\end{bmatrix}$.

**C.** $A^3=P^3\operatorname{diag}(a^3,a^3,b^3)(P^{-1})^3$.

**D.** $A^{-1}=P^{-1}\operatorname{diag}(1/a,1/a,1/b)P$.

**E.** $A=Q\operatorname{diag}(b,a,a)Q^{-1}$, $Q=\begin{bmatrix}0&1&1\\0&0&1\\1&1&2\end{bmatrix}$.

> [!success]- Worked Solution
> **A — True.** $Q$ contains rescaled and reordered eigenvectors, with matching reordered eigenvalues.
>
> **B — True.** Scaling eigenvectors does not change eigenvalues; scaling $A$ by 2 doubles them.
>
> **C — False.** The correct power formula is $A^3=P\operatorname{diag}(a^3,a^3,b^3)P^{-1}$.
>
> **D — False.** The inverse, when defined, has the order $P\operatorname{diag}(1/a,1/a,1/b)P^{-1}$, not the reversed order shown.
>
> **E — False.** The proposed first column is not an eigenvector for $b$.
>
> **Answer according to the official solution: A and B.**


### AY2024/2025 Semester 1 / Question 10 / Chapter 3 / Diagonalization

### Question

$A$ is a diagonalizable $3\times3$ matrix with eigenvalues $1$ and $3$ and eigenspaces
$$E_1=\operatorname{span}\left\{\begin{bmatrix}1\\1\\1\end{bmatrix}\right\},\qquad E_3=\operatorname{span}\left\{\begin{bmatrix}1\\0\\1\end{bmatrix},\begin{bmatrix}0\\0\\1\end{bmatrix}\right\}.$$
Which matrices diagonalize $A$?

1. $\begin{bmatrix}0 & 1 & 1\\0 & 1 & 0\\1 & 1 & 0\end{bmatrix}$
2. $\begin{bmatrix}2 & 4 & 0\\0 & 4 & 0\\2 & 4 & 6\end{bmatrix}$
3. $\begin{bmatrix}1 & 1 & 2\\1 & 0 & 2\\1 & 1 & 2\end{bmatrix}$
4. $\begin{bmatrix}2 & 1 & 0\\1 & 0 & 0\\2 & 1 & 1\end{bmatrix}$
5. $\begin{bmatrix}1 & 0 & 0\\0 & 0 & 0\\1 & 1 & 0\end{bmatrix}$

> [!success]- Worked Solution
> A diagonalizing matrix must have three linearly independent eigenvectors as columns: one from $E_1$ and two from $E_3$. Checking the columns gives options 1 and 2. Option 3 has dependent columns, option 4 contains a column that mixes eigenspaces, and option 5 contains the zero vector.
>
> **Answer: 1 and 2.**


### AY2024/2025 Semester 2 / Question 11 / Chapter 3 / Diagonalization

### Question

Suppose
$$P^{-1}AP=D,$$
where
$$P=\begin{bmatrix}1&0&2\\1&0&1\\0&1&0\end{bmatrix},\qquad D=\begin{bmatrix}a&0&0\\0&a&0\\0&0&b\end{bmatrix},\qquad a\ne b.$$
Which of the following are true?

**A.** $\begin{bmatrix}2&1&0\\1&1&0\\0&0&1\end{bmatrix}^{-1}A\begin{bmatrix}2&1&0\\1&1&0\\0&0&1\end{bmatrix}=\begin{bmatrix}b&0&0\\0&a&0\\0&0&a\end{bmatrix}$

**B.** $\begin{bmatrix}1&0&4\\1&0&2\\1&2&0\end{bmatrix}^{-1}A\begin{bmatrix}1&0&4\\1&0&2\\1&2&0\end{bmatrix}=\begin{bmatrix}a&0&0\\0&a&0\\0&0&2b\end{bmatrix}$

**C.** $\begin{bmatrix}1&0&2\\1&0&1\\0&1&1\end{bmatrix}^{-1}A\begin{bmatrix}1&0&2\\1&0&1\\0&1&1\end{bmatrix}=\begin{bmatrix}a&0&0\\0&a&0\\0&0&b\end{bmatrix}$

**D.** $\begin{bmatrix}1&2&4\\1&1&2\\1&0&0\end{bmatrix}^{-1}A\begin{bmatrix}1&2&4\\1&1&2\\1&0&0\end{bmatrix}=\begin{bmatrix}a&0&0\\0&b&0\\0&0&b\end{bmatrix}$

**E.** $\begin{bmatrix}2&2&1\\2&1&1\\1&0&2\end{bmatrix}^{-1}A\begin{bmatrix}2&2&1\\2&1&1\\1&0&2\end{bmatrix}=\begin{bmatrix}a&0&0\\0&b&0\\0&0&a\end{bmatrix}$

> [!success]- Worked Solution
> The columns of $P$ show that $E_a=\operatorname{span}\{(1,1,0)^T,(0,0,1)^T\}$ and $E_b=\operatorname{span}\{(2,1,0)^T\}$.
>
> A valid diagonalizing matrix must have independent eigenvectors as columns, and the diagonal entries must match the eigenvalues of those columns. Checking the options gives **A and E**.
>
> **Answer: A and E.**


### AY2025/2026 Semester 1 / Question 11 / Chapter 3 / Diagonalization

### Question

Suppose $A$ is a diagonalizable $3\times3$ matrix with eigenspaces
$$E_1=\operatorname{span}\left\{\begin{bmatrix}1\\2\\0\end{bmatrix},\begin{bmatrix}1\\0\\2\end{bmatrix}\right\},\qquad E_2=\operatorname{span}\left\{\begin{bmatrix}0\\1\\1\end{bmatrix}\right\}.$$
Which matrices diagonalize $A$?

**A.** $\begin{bmatrix}1&0&2\\0&1&4\\2&1&0\end{bmatrix}$

**B.** $\begin{bmatrix}2&2&0\\1&0&1\\0&1&1\end{bmatrix}$

**C.** $\begin{bmatrix}1&1/2&0\\1&0&2\\1&1&2\end{bmatrix}$

**D.** $\begin{bmatrix}1&1&0\\2&0&1\\0&2&-1\end{bmatrix}$

**E.** $\begin{bmatrix}1&1&0\\3&0&1\\1&2&1\end{bmatrix}$

> [!success]- Worked Solution
> A diagonalizing matrix needs two independent columns from $E_1$ and one non-zero column from $E_2$.
>
> Checking the columns of each candidate gives **A and D**.
>
> **Answer: A and D.**



### AY2023/2024 Semester 1 / Question 11 / Chapter 3 / Population Model

#### Question

Each year 25% of married men become single and 20% of single men become married. Initially there are 6000 married and 3000 single men. Find the long-run numbers $M,S$.

> [!success]- Worked Solution
> At equilibrium, $0.25M=0.20S$ and $M+S=9000$. Solve $5M=4S$. **Answer:** $M=4000$, $S=5000$.


### AY2023/2024 Semester 1 / Question 10 / Chapter 3 / Eigenvalues and Eigenvectors

#### Question

Let $u,v,w,x$ be linearly independent in $\mathbb R^4$ with $Au=v$, $Av=u$, $Aw=0$, $Ax=x$. Which statements hold?

**A.** $A$ has three distinct eigenvalues.

**B.** $A$ has only two linearly independent eigenvectors.

**C.** $A$ has an eigenspace of dimension 2.

**D.** $A$ is not diagonalizable.

**E.** $A$ is singular.

> [!success]- Worked Solution
> $u+v$ has eigenvalue $1$, $u-v$ eigenvalue $-1$, $w$ eigenvalue $0$, and $x$ eigenvalue $1$. Thus eigenvalues are $-1,0,1$ and the eigenspace for $1$ has dimension 2. Four independent eigenvectors exist. **Answer: A, C, E.**


### AY2023/2024 Semester 2 / Question 11 / Chapter 3 / Eigenvalues and Eigenvectors

#### Question

Given $\operatorname{Null}(A)=\operatorname{span}\{(1,1)\}$ and $A^3(1,2)=(8,16)$, find $A=\begin{bmatrix}a&b\\c&d\end{bmatrix}$.

> [!success]- Worked Solution
> Eigenvectors $(1,1)$ and $(1,2)$ have eigenvalues $0$ and $2$ respectively. Set $P=\begin{bmatrix}1&1\\1&2\end{bmatrix}$, $D=\operatorname{diag}(0,2)$. Then $A=PDP^{-1}=\begin{bmatrix}-2&2\\-4&4\end{bmatrix}$. **Answer:** $a=-2,b=2,c=-4,d=4$.


### AY2025/2026 Semester 1 / Question 3 / Chapter 3 / Eigenvalues and Eigenvectors

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



### AY2024/2025 Semester 1 / Question 11 / Chapter 3 / Eigenspaces

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


### AY2024/2025 Semester 2 / Question 10 / Chapter 3 / Eigenspaces

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


### AY2025/2026 Semester 1 / Question 10 / Chapter 3 / Eigenspaces

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



# Chapter 4

### AY2022/2023 Semester 1 / Question 12 / Chapter 4 / System of Differential Equations

#### Question

The third-order ODE $y'''+ay''+by'+cy=0$ is converted to the SDE

$$\mathbf y'=\begin{bmatrix}0&1&0\\0&0&1\\2&-1&3\end{bmatrix}\mathbf y.$$

Find $a,b,c$.

> [!success]- Worked Solution
> Take $y_1=y$, $y_2=y'$ and $y_3=y''$. The last equation of the SDE gives
>
> $$y'''=2y-y'+3y''.$$
>
> Move all terms to the left:
>
> $$y'''-3y''+y'-2y=0.$$
>
> **Answer: $a=-3,\ b=1,\ c=-2$.**


### AY2022/2023 Semester 2 / Question 12 / Chapter 4 / System of Differential Equations

#### Question

A system $\mathbf y'=A\mathbf y$ has general solution

$$\mathbf y=c_1e^{-3t}\begin{bmatrix}2\\1\end{bmatrix}+c_2e^{3t}\begin{bmatrix}1\\2\end{bmatrix}.$$

Find $a,b,c,d$ in $A=\begin{bmatrix}a&b\\c&d\end{bmatrix}$. (FIB)

> [!success]- Worked Solution
> The two solution vectors are eigenvectors with eigenvalues $-3$ and $3$. Thus
>
> $$P=\begin{bmatrix}2&1\\1&2\end{bmatrix},\quad D=\begin{bmatrix}-3&0\\0&3\end{bmatrix},\quad A=PDP^{-1}=\begin{bmatrix}-5&4\\-4&5\end{bmatrix}.$$
>
> **Answer: $a=-5,b=4,c=-4,d=5$.**


### AY2023/2024 Semester 2 / Question 15 / Chapter 4 / System of Differential Equations

#### Question

Two tanks hold 100 L and 50 L of salt water. From the indicated flow diagram, find the entries $a,b,c,d$ in $y^\prime=\frac1{100}\begin{bmatrix}a&b\\c&d\end{bmatrix}y$.

![[Attachments/S2_Q15_Tank_Diagram.png]]

> [!success]- Worked Solution
> Tank 1 outflow is $12/100$ times its salt amount; tank 2 inflow contributes $2/50=4/100$ to tank 1. Tank 2 receives $12/100$ from tank 1 and loses $12/50=24/100$. **Answer:** $a=-12,b=4,c=12,d=-24$.


### AY2024/2025 Semester 1 / Question 12 / Chapter 4 / System of Differential Equations

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


### AY2024/2025 Semester 1 / Question 15 / Chapter 4 / System of Differential Equations

### Question

Two tanks contain 100 L and 200 L of salt water.

![[Attachments/MA1513_AY2425_S1_Q15_Tank_Diagram.png]] The SDE is
$$y'=\frac1{100}\begin{bmatrix}-6 & 2\\6 & -3\end{bmatrix}y.$$
From the flow diagram, determine the flow rates $a,b,c$.

> [!success]- Worked Solution
> For tank 1, inflow is $(a/200)y_2$ and outflow is $(b/100)y_1$. Comparing coefficients gives $b=6$ and $a/200=2/100$, hence $a=4$. For tank 2, total outflow coefficient is $(a+c)/200=3/100$, so $a+c=6$ and $c=2$.
>
> **Answer: $a=4,b=6,c=2$.**


### AY2025/2026 Semester 1 / Question 15 / Chapter 4 / System of Differential Equations

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



### AY2022/2023 Semester 1 / Question 13 / Chapter 4 / Repeated Eigenvalues

#### Question

The SDE $\mathbf y'=A\mathbf y$ has a degenerate node. Matrix $A$ has eigenvalue $3$ with eigenvector $\begin{bmatrix}0\\1\end{bmatrix}$ and generalized eigenvectors $\begin{bmatrix}1/3\\s\end{bmatrix}$ for any $s$. Which are solutions?

**A.** $e^{3t}\begin{bmatrix}0\\3\end{bmatrix}$

**B.** $e^{3t}\begin{bmatrix}1\\t\end{bmatrix}$

**C.** $e^{3t}\begin{bmatrix}1/3\\0\end{bmatrix}$

**D.** $e^{3t}\begin{bmatrix}1/3\\t+1\end{bmatrix}$

**E.** $e^{3t}\begin{bmatrix}1/3\\1\end{bmatrix}$

> [!success]- Worked Solution
> The eigenvector gives solutions $c e^{3t}\begin{bmatrix}0\\1\end{bmatrix}$, so **A is correct**.
>
> A generalized eigenvector $w=\begin{bmatrix}1/3\\s\end{bmatrix}$ satisfies $(A-3I)w=v$, giving a second solution
>
> $$e^{3t}\left(t\begin{bmatrix}0\\1\end{bmatrix}+\begin{bmatrix}1/3\\s\end{bmatrix}\right).$$
>
> Taking $s=1$ gives **D**. Scaling the generalized solution by $3$ gives $e^{3t}\begin{bmatrix}1\\3t\end{bmatrix}$, not option B. C and E are not eigenvector solutions.
>
> **Answer: A and D.**


### AY2024/2025 Semester 1 / Question 13 / Chapter 4 / Repeated Eigenvalues

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


### AY2024/2025 Semester 2 / Question 13 / Chapter 4 / Repeated Eigenvalues

### Question

A $2\times2$ matrix $A$ has only one eigenvalue $\lambda=-1$ and only one linearly independent eigenvector
$$v=\begin{bmatrix}1\\-1\end{bmatrix}.$$
Suppose $(A+I)u=v$ has general solution
$$u=\begin{bmatrix}1+s\\s\end{bmatrix}.$$
Which of the following are solutions of $y'=Ay$?

**A.** $y=e^{-t}\begin{bmatrix}-1\\1\end{bmatrix}$

**B.** $y=e^{-t}\begin{bmatrix}1\\0\end{bmatrix}$

**C.** $y=e^{-t}\begin{bmatrix}t\\-t-1\end{bmatrix}$

**D.** $y=e^{-t}\begin{bmatrix}1+t\\t\end{bmatrix}$

**E.** $y=e^{-t}\begin{bmatrix}t+2\\-t-1\end{bmatrix}$

> [!success]- Worked Solution
> An eigenvector gives a solution $ve^{-t}$, and a generalized eigenvector $u$ gives $(tv+u)e^{-t}$.
>
> **A** is $-ve^{-t}$. **C** has the generalized-eigenvector form using $u=(0,-1)^T$. **E** is a linear combination of the two fundamental solutions. Hence these are solutions.
>
> **Answer: A, C and E.**



### AY2022/2023 Semester 1 / Question 14 / Chapter 4 / Phase Plane

#### Question

Which direction fields correspond to the SDE

$$\mathbf y'=\begin{bmatrix}2&4\\1&2\end{bmatrix}\mathbf y\ ?$$

![[Attachments/AY2223_S1_Q14_Direction_Field_Options.png]]

> [!success]- Worked Solution
> The matrix has determinant $0$ and trace $4$, hence eigenvalues $0$ and $4$. The zero-eigenvalue direction satisfies $y_1=-2y_2$; the positive-eigenvalue direction satisfies $y_1=2y_2$. Compare the equilibrium line and arrow directions with each field.
>
> **Answer: D.** This is the direction field consisting of parallel straight-line trajectories; the other diagrams show different equilibrium types.


### AY2022/2023 Semester 2 / Question 13 / Chapter 4 / Phase Plane

#### Question

The direction field of a $2\times2$ SDE $\mathbf y'=A\mathbf y$ is shown.

![[Attachments/AY2223_S2_Q13_Direction_Field.png]]

Which statements are true?

**A.** $A$ is singular.

**B.** $A$ is not diagonalizable.

**C.** $\operatorname{span}\{(1,1)\}$ is an eigenspace of $A$.

**D.** The only equilibrium point is the origin.

**E.** $A$ has a positive eigenvalue.

> [!success]- Worked Solution
> From the direction field, trajectories are parallel along an equilibrium line, and the flow points toward that line. The matrix therefore has a zero eigenvalue and a negative eigenvalue. Hence $A$ is singular and diagonalizable (two distinct eigenvalues). The line $y_1=y_2$ is the zero-eigenvalue eigenspace; there are infinitely many equilibria. The arrows move away from this line, so the other eigenvalue is positive.
>
> **Answer: A, C and E.**


### AY2023/2024 Semester 1 / Question 13 / Chapter 4 / Phase Plane

#### Question

The phase portrait of $y'=Ay$ is shown. Which matrix describes it?

**A.** $\begin{bmatrix}1&1\\-1&1\end{bmatrix}$

**B.** $\begin{bmatrix}1&-1\\1&1\end{bmatrix}$

**C.** $\begin{bmatrix}-1&1\\-1&-1\end{bmatrix}$

**D.** $\begin{bmatrix}-1&-1\\1&-1\end{bmatrix}$

**E.** None of the above.

![[Attachments/S1_Q13_Phase_Portrait.png]]

> [!success]- Worked Solution
> Determine rotation direction and whether trajectories spiral in or out from the sign of the real part of the eigenvalues; compare with the plotted phase portrait.


### AY2023/2024 Semester 2 / Question 13 / Chapter 4 / Phase Plane

#### Question

For the direction field shown, which statements are correct?

**A.** The equilibrium is a star node.

**B.** There are infinitely many equilibrium points.

**C.** $A$ has only one linearly independent eigenvector.

**D.** $(2,1)$ is an eigenvector of $A$.

**E.** $A$ is singular.

![[Attachments/S2_Q13_Direction_Field.png]]

> [!success]- Worked Solution
> The line of equilibria is an eigenspace for eigenvalue zero, so $A$ is singular. The vector $(2,1)$ lies along this equilibrium line. **Answer: B, D and E.**


### AY2024/2025 Semester 1 / Question 14 / Chapter 4 / Phase Plane

### Question

Which of the following are possible direction fields for
$$y'=\begin{bmatrix}0&a\\-1&b\end{bmatrix}y$$
for some $a,b$?

**Option i**

![[Attachments/MA1513_AY2425_S1_Q14_Option_i.png]]

**Options ii-v**

![[Attachments/MA1513_AY2425_S1_Q14_Options_ii-v.png]]

> [!success]- Worked Solution
> Use the test point $(1,0)^T$:
> $$\begin{bmatrix}0 & a\\-1 & b\end{bmatrix}\begin{bmatrix}1\\0\end{bmatrix}=\begin{bmatrix}0\\-1\end{bmatrix}.$$
> Therefore the tangent arrow at $(1,0)$ must point vertically downward. In the source diagrams, only options 1 and 2 have this behaviour.
>
> **Answer: 1 and 2.**


### AY2022/2023 Semester 1 / Question 15 / Chapter 4 / Complex Eigenvalues

#### Question

The SDE $\mathbf y'=A\mathbf y$ has the fundamental solutions

$$
\mathbf x_1=e^t\left(\begin{bmatrix}0\\1\end{bmatrix}\cos3t+\begin{bmatrix}1\\0\end{bmatrix}\sin3t\right),\qquad
\mathbf x_2=e^t\left(\begin{bmatrix}0\\1\end{bmatrix}\sin3t-\begin{bmatrix}1\\0\end{bmatrix}\cos3t\right).
$$

Which statements are true?

**A.** The equilibrium point is unstable.

**B.** The eigenvalues of $A$ are $1+3i$ and $1-3i$.

**C.** $\begin{bmatrix}1\\i\end{bmatrix}$ is an eigenvector of $A$.

**D.** The equilibrium point is a center.

**E.** The trajectories rotate counter-clockwise.

> [!success]- Worked Solution
> The real exponential factor $e^t$ implies positive real part $1$ and instability: **A true**. The trigonometric frequency $3$ implies eigenvalues $1\pm3i$: **B true**.
>
> Differentiating the fundamental solutions at $t=0$ gives $A=\begin{bmatrix}1&3\\-3&1\end{bmatrix}$. Thus $A\begin{bmatrix}1\\i\end{bmatrix}=(1+3i)\begin{bmatrix}1\\i\end{bmatrix}$, so **C true**.
>
> A center requires zero real parts, so **D false**. At $(1,0)$, the vector field points downward; the rotation is clockwise, so **E false**.
>
> **Answer: A, B and C.**


### AY2022/2023 Semester 2 / Question 15 / Chapter 4 / Complex Eigenvalues

#### Question

Given $\mathbf y'=\begin{bmatrix}2&1\\-1&2\end{bmatrix}\mathbf y$, which statements are true?

**A.** $e^{2t}\begin{bmatrix}\cos t+\sin t\\\cos t-\sin t\end{bmatrix}$ is a real solution.

**B.** $e^{2t}\begin{bmatrix}\sin t\\\cos t\end{bmatrix}$ is *not* a real solution.

**C.** $2+i$ has eigenvector $\begin{bmatrix}1\\-i\end{bmatrix}$.

**D.** The equilibrium is unstable.

**E.** The trajectories rotate counter-clockwise.

> [!success]- Worked Solution
> The eigenvalues are $2\pm i$. Two independent real solutions are
>
> $$e^{2t}\begin{bmatrix}\cos t\\-\sin t\end{bmatrix},\qquad e^{2t}\begin{bmatrix}\sin t\\\cos t\end{bmatrix}.$$
>
> **A — True.** Sum of these two solutions.
>
> **B — False.** It is one of the fundamental real solutions.
>
> **C — False.** The vector shown corresponds to $2-i$, not $2+i$.
>
> **D — True.** Positive real part implies outward spirals.
>
> **E — False.** At $(1,0)$, the velocity $(2,-1)$ points downward: clockwise.
>
> **Answer: A and D.**


### AY2023/2024 Semester 2 / Question 12 / Chapter 4 / Complex Eigenvalues

#### Question

Which are solutions of $y^\prime=\begin{bmatrix}3&-2\\2&3\end{bmatrix}y$?

**A.** $e^{3t}\begin{bmatrix}\sin2t\\cos2t\end{bmatrix}$

**B.** $e^{3t}\begin{bmatrix}\sin2t\\-\cos2t\end{bmatrix}$

**C.** $e^{3t}\begin{bmatrix}\cos2t\\sin2t\end{bmatrix}$

**D.** $e^{3t}\begin{bmatrix}-\cos2t\\sin2t\end{bmatrix}$

**E.** $e^{3t}\begin{bmatrix}\cos2t+\sin2t\\cos2t-\sin2t\end{bmatrix}$

> [!success]- Worked Solution
> The fundamental real solutions are $e^{3t}(-\sin2t,\cos2t)$ and $e^{3t}(\cos2t,\sin2t)$. **Answer: B and C.**


### AY2024/2025 Semester 2 / Question 14 / Chapter 4 / Complex Eigenvalues

### Question

Given
$$y'=\begin{bmatrix}0&1\\-2&2\end{bmatrix}y,$$
which of the following are solutions?

**A.** $y=e^t\begin{bmatrix}\frac12\cos t+\frac12\sin t\\\cos t\end{bmatrix}$

**B.** $y=e^t\begin{bmatrix}\frac12\cos t-\frac12\sin t\\\cos t\end{bmatrix}$

**C.** $y=e^t\begin{bmatrix}-\sin t+\cos t\\-2\sin t\end{bmatrix}$

**D.** $y=e^t\begin{bmatrix}\sin t+\cos t\\2\sin t\end{bmatrix}$

**E.** $y=e^t\begin{bmatrix}\frac12\sin t-\frac12\cos t\\-\sin t\end{bmatrix}$

> [!success]- Worked Solution
> The eigenvalues are $1\pm i$. Construct the two real solutions from the real and imaginary parts of the complex eigenvector solution.
>
> Matching the five expressions to those standard real forms gives **A and C**.
>
> **Answer: A and C.**


### AY2025/2026 Semester 1 / Question 12 / Chapter 4 / Complex Eigenvalues

### Question

An SDE has a solution
$$y=e^{2t}\left(\begin{bmatrix}-2\\1\end{bmatrix}\sin t+\begin{bmatrix}1\\0\end{bmatrix}\cos t\r\right).$$
Which description is correct?

A. Clockwise, towards the origin
B. Clockwise, away from the origin
C. Anti-clockwise, towards the origin
D. Anti-clockwise, away from the origin
E. Closed loops, clockwise.

> [!success]- Worked Solution
> The real part of the eigenvalue is $2>0$, so the equilibrium is an unstable spiral and trajectories move away from the origin. Reconstructing the matrix gives
> $$A=\begin{bmatrix}0&-5\\1&4\end{bmatrix}.$$
> At $(1,0)$, the tangent vector is $(0,1)^T$, which points upward, so the rotation is anti-clockwise.
>
> **Answer: D.**



### AY2022/2023 Semester 2 / Question 14 / Chapter 4 / Mixing Problem

#### Question

Two tanks initially contain $100$ litres of salt water each. Let $y_1(t),y_2(t)$ denote salt amounts in kg. Determine the entries $a,b,c,d$ in

$$\begin{bmatrix}y_1'\\y_2'\end{bmatrix}=\begin{bmatrix}a&b\\c&d\end{bmatrix}\begin{bmatrix}y_1\\y_2\end{bmatrix}.$$

![[Attachments/AY2223_S2_Q14_Tanks.png]]

Give answers to two decimal places. (FIB)

> [!success]- Worked Solution
> Tank 1 receives $2$ L/min from tank 2 and loses $12$ L/min to tank 2. Tank 2 receives $12$ L/min from tank 1 and loses $2+10=12$ L/min.
>
> $$y_1'=-\frac{12}{100}y_1+\frac{2}{100}y_2,\qquad y_2'=\frac{12}{100}y_1-\frac{12}{100}y_2.$$
>
> **Answer: $a=-0.12,\ b=0.02,\ c=0.12,\ d=-0.12$.**


### AY2023/2024 Semester 1 / Question 12 / Chapter 4 / Initial Value Problem

#### Question

Given 

$$
y=c_1e^{-7t}\begin{bmatrix}2\\1\\3\end{bmatrix}+c_2e^{3t}\begin{bmatrix}1\\2\\0\end{bmatrix}+c_3e^t\begin{bmatrix}1\\1\\-1\end{bmatrix},
$$

 and $y(0)=\begin{bmatrix}3\\1\\1\end{bmatrix}$, find $c_1,c_2,c_3$.

> [!success]- Worked Solution
> Set $t=0$ and solve the $3\times3$ linear system formed by the three column vectors. **Answer:** $c_1=1,c_2=-1,c_3=2$.



### AY2023/2024 Semester 1 / Question 14 / Chapter 4 / Higher-Order Differential Equations

#### Question

Convert $2y^{\prime\prime\prime}+6y^{\prime\prime}-4y^\prime-2y=0$ to the companion-matrix SDE with last row $(a,b,c)$. Find $a,b,c$.

> [!success]- Worked Solution
> Divide by 2: $y^{\prime\prime\prime}=-3y^{\prime\prime}+2y^\prime+y$. Therefore the last row is $(1,2,-3)$. **Answer:** $a=1,b=2,c=-3$.



### AY2023/2024 Semester 1 / Question 15 / Chapter 4 / Classification of Equilibrium Points

#### Question

The equilibrium of a $2\times2$ SDE is a star node. Which statements are true?

**A.** There are infinitely many linearly independent eigenvectors.

**B.** $y=e^{rt}\begin{bmatrix}a\\b\end{bmatrix}$ for arbitrary real $a,b$.

**C.** The underlying matrix is scalar.

**D.** All trajectories move away from the origin.

**E.** A generalized eigenvector is required.

> [!success]- Worked Solution
> For a star node the matrix is $rI$, so every nonzero vector is an eigenvector and every solution is $e^{rt}v$. Stability depends on the sign of $r$. **Answer: B and C.**


### AY2024/2025 Semester 2 / Question 15 / Chapter 4 / Classification of Equilibrium Points

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


### AY2025/2026 Semester 1 / Question 13 / Chapter 4 / Classification of Equilibrium Points

### Question

The following is a phase portrait of a $2\times2$ SDE $y'=Ay$.

![[Attachments/MA1513_AY2526_S1_Q13_Phase_Portrait.png]]

Which statements are true?

**A.** The SDE has only one linearly independent solution.

**B.** $A$ has a repeated eigenvalue.

**C.** $A$ has complex eigenvalues.

**D.** The two ends of every trajectory are parallel to the same vector.

**E.** There is no solution of the SDE that corresponds to a straight-line trajectory.

> [!success]- Worked Solution
> The portrait is a **degenerate node**. This occurs when $A$ has a repeated real eigenvalue and only one linearly independent eigenvector.
>
> A generalized eigenvector still produces a second linearly independent SDE solution, so **A is false**. The repeated eigenvalue makes **B true**, while **C is false**. Both ends of every trajectory become parallel to the guiding axis, so **D is true**. There is also a straight-line trajectory along that axis, so **E is false**.
>
> **Answer: B and D.**



### AY2023/2024 Semester 2 / Question 14 / Chapter 4 / Mass-Spring System

#### Question

For the mass-spring equation $my^{\prime\prime}+cy^\prime+ky=0$, suppose the corresponding equilibrium is a degenerate node. Which statements are correct?

**A.** The equilibrium is unstable.

**B.** The ball returns to rest as slowly as possible without oscillation.

**C.** $c/2=\sqrt{mk}$.

**D.** Damping force equals spring force.

**E.** None of the above.

> [!success]- Worked Solution
> Degenerate node corresponds to critical damping: $c^2=4mk$ and the system returns to rest as quickly as possible without oscillation. **Answer: C.**



### AY2025/2026 Semester 1 / Question 14 / Chapter 4 / Solutions of System of Differential Equations

### Question

Suppose $y'=Ay$ is a $2\times2$ SDE and $A$ has eigenvalues $r_1=0$ and $r_2\ne0$ with eigenvectors $\begin{bmatrix}a\\b\end{bmatrix}$ and $\begin{bmatrix}c\\d\end{bmatrix}$ respectively. Which of the following are solutions?

**A.** $y=\begin{bmatrix}k\\k\end{bmatrix}$ for any $k$

**B.** $y=\begin{bmatrix}a\\b\end{bmatrix}+t\begin{bmatrix}c\\d\end{bmatrix}$

**C.** $y=e^{r_2t}\begin{bmatrix}c\\d\end{bmatrix}$

**D.** $y=e^{r_2t}\begin{bmatrix}a+t\\b+t\end{bmatrix}$

**E.** $y=\begin{bmatrix}2a\\2b\end{bmatrix}-e^{r_2t}\begin{bmatrix}c\\d\end{bmatrix}$

> [!success]- Worked Solution
> A fundamental set is
>
> $$Y_1=\begin{bmatrix}a\\b\end{bmatrix},\qquad Y_2=e^{r_2t}\begin{bmatrix}c\\d\end{bmatrix}.$$
>
> Any constant linear combination of $Y_1$ and $Y_2$ is a solution. Thus **C** is $Y_2$ and **E** is $2Y_1-Y_2$.
>
> **Answer: C and E.**
