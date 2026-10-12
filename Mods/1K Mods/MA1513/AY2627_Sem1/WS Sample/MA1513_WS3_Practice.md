# MA1513 Written Submission 3 --- Practice Set

> \[!important\] This is a **practice set** modelled on the structure of
> the official WS3 sample.\
> The numerical values below are newly filled-in practice values; they
> are **not** the actual WS3 questions.

## Practice Questions

### Question 1 --- Linear Transformation

Given a linear transformation $T:\mathbb{R}^3\to\mathbb{R}^3$ such that

$$
T\left(\begin{bmatrix}1\\1\\0\end{bmatrix}\right)
=
\begin{bmatrix}3\\1\\2\end{bmatrix},
\qquad
T\left(\begin{bmatrix}0\\1\\1\end{bmatrix}\right)
=
\begin{bmatrix}2\\2\\1\end{bmatrix},
\qquad
T\left(\begin{bmatrix}1\\0\\1\end{bmatrix}\right)
=
\begin{bmatrix}1\\1\\3\end{bmatrix}.
$$

1.  Find the standard matrix for $T$ by finding the images of the
    standard basis of $\mathbb{R}^3$. Show your workings.
2.  Find the standard matrix for $T$ using the **stacking method**. Show
    your workings.

------------------------------------------------------------------------

### Question 2 --- Eigenvalues, Eigenspaces and Diagonalizability

Given

$$
A=
\begin{bmatrix}
2&1&0&0\\
1&2&0&0\\
0&0&3&0\\
0&0&0&1
\end{bmatrix}.
$$

1.  Find the eigenvalue(s) of $A$ **without using MATLAB**. Explain how
    you obtain your answers.
2.  Find a basis for each eigenspace of $A$ **without using MATLAB**.
    Show your working.
3.  Is $A$ diagonalizable? Why?

------------------------------------------------------------------------

### Question 3 --- Diagonalization

Given

$$
B=
\begin{bmatrix}
1&1&-1\\
0&2&2\\
0&0&4
\end{bmatrix}.
$$

1.  Use the symbolic version of MATLAB commands to find **three linearly
    independent eigenvectors whose entries are integers**.
2.  Using the eigenvectors from part (i), write down a matrix $P$ such
    that

$$
P^{-1}BP=D,
$$

where

$$
D=
\begin{bmatrix}
1&0&0\\
0&2&0\\
0&0&4
\end{bmatrix}.
$$

------------------------------------------------------------------------

### Question 4 --- Population Model

The current populations of a certain species are

$$
j_0=10000,\qquad a_0=15000,
$$

where $j_0$ is the juvenile population and $a_0$ is the adult
population.

Suppose the stage matrix has eigenvalues

$$
r_1=\frac65,\qquad r_2=\frac45,
$$

with corresponding eigenvectors

$$
v_1=
\begin{bmatrix}
2\\
1
\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}
1\\
-1
\end{bmatrix}.
$$

1.  Express

$$
x_0=
\begin{bmatrix}
10000\\
15000
\end{bmatrix}
$$

as a linear combination $c_1v_1+c_2v_2$. Leave $c_1$ and $c_2$ in
fractions. 2. Express the population vector

$$
x_n=
\begin{bmatrix}
j_n\\
a_n
\end{bmatrix}
$$

after $n$ years in terms of $n$. 3. Find the ratio of juveniles to
adults in the long run. Show your workings.

------------------------------------------------------------------------

### Question 5 --- Systems of Differential Equations

Given the system

$$
y'=Ay,
\qquad
A=
\begin{bmatrix}
2&1\\
2&3
\end{bmatrix},
$$

where

$$
y=
\begin{bmatrix}
y_1\\
y_2
\end{bmatrix}.
$$

1.  Find the fundamental solutions of the SDE.
2.  Write down the general solution in component form.
3.  Find the particular solution of the IVP in component form given

$$
y_1(0)=1,\qquad y_2(0)=1.
$$

------------------------------------------------------------------------

# Answer Sheet

## Question 1

### 1(i) Standard matrix from the standard basis

Let

$$
u_1=
\begin{bmatrix}1\\1\\0\end{bmatrix},
\quad
u_2=
\begin{bmatrix}0\\1\\1\end{bmatrix},
\quad
u_3=
\begin{bmatrix}1\\0\\1\end{bmatrix}.
$$

The standard basis vectors can be written as

$$
e_1=\frac12(u_1-u_2+u_3),
$$

$$
e_2=\frac12(u_1+u_2-u_3),
$$

$$
e_3=\frac12(-u_1+u_2+u_3).
$$

By linearity,

$$
T(e_1)
=
\frac12
\left(
\begin{bmatrix}3\\1\\2\end{bmatrix}
-
\begin{bmatrix}2\\2\\1\end{bmatrix}
+
\begin{bmatrix}1\\1\\3\end{bmatrix}
\right)
=
\begin{bmatrix}1\\0\\2\end{bmatrix}.
$$

Similarly,

$$
T(e_2)=
\begin{bmatrix}2\\1\\0\end{bmatrix},
\qquad
T(e_3)=
\begin{bmatrix}0\\1\\1\end{bmatrix}.
$$

Hence the standard matrix is

$$
\boxed{
[T]=
\begin{bmatrix}
1&2&0\\
0&1&1\\
2&0&1
\end{bmatrix}
}.
$$

### 1(ii) Stacking method

Stack the input vectors and their images:

$$
X=
\begin{bmatrix}
1&0&1\\
1&1&0\\
0&1&1
\end{bmatrix},
\qquad
Y=
\begin{bmatrix}
3&2&1\\
1&2&1\\
2&1&3
\end{bmatrix}.
$$

Since

$$
[T]X=Y,
$$

we have

$$
[T]=YX^{-1}.
$$

Therefore,

$$
\boxed{
[T]=
\begin{bmatrix}
1&2&0\\
0&1&1\\
2&0&1
\end{bmatrix}
}.
$$

------------------------------------------------------------------------

## Question 2

### 2(i) Eigenvalues

Compute

$$
\det(A-\lambda I)
=
\begin{vmatrix}
2-\lambda&1&0&0\\
1&2-\lambda&0&0\\
0&0&3-\lambda&0\\
0&0&0&1-\lambda
\end{vmatrix}.
$$

Thus,

$$
\det(A-\lambda I)
=
\left((2-\lambda)^2-1\right)(3-\lambda)(1-\lambda).
$$

Since

$$
(2-\lambda)^2-1
=
(1-\lambda)(3-\lambda),
$$

we obtain

$$
\det(A-\lambda I)
=
(1-\lambda)^2(3-\lambda)^2.
$$

Hence

$$
\boxed{\lambda=1,\ 3}
$$

and each has algebraic multiplicity $2$.

### 2(ii) Bases for the eigenspaces

For $\lambda=1$,

$$
(A-I)x=0
$$

gives

$$
x_1+x_2=0,\qquad x_3=0,
$$

while $x_4$ is free.

Therefore,

$$
E_1=
\operatorname{span}
\left\{
\begin{bmatrix}1\\-1\\0\\0\end{bmatrix},
\begin{bmatrix}0\\0\\0\\1\end{bmatrix}
\right\}.
$$

A basis is

$$
\boxed{
\left\{
\begin{bmatrix}1\\-1\\0\\0\end{bmatrix},
\begin{bmatrix}0\\0\\0\\1\end{bmatrix}
\right\}
}.
$$

For $\lambda=3$,

$$
(A-3I)x=0
$$

gives

$$
-x_1+x_2=0,\qquad x_4=0,
$$

while $x_3$ is free.

Therefore,

$$
E_3=
\operatorname{span}
\left\{
\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\begin{bmatrix}0\\0\\1\\0\end{bmatrix}
\right\}.
$$

A basis is

$$
\boxed{
\left\{
\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\begin{bmatrix}0\\0\\1\\0\end{bmatrix}
\right\}
}.
$$

### 2(iii) Diagonalizability

There are four linearly independent eigenvectors in total:

-   two associated with $\lambda=1$;
-   two associated with $\lambda=3$.

Since a $4\times4$ matrix with four linearly independent eigenvectors is
diagonalizable,

$$
\boxed{A\text{ is diagonalizable}.}
$$

------------------------------------------------------------------------

## Question 3

### 3(i) Integer eigenvectors

The eigenvalues are

$$
\lambda_1=1,\qquad
\lambda_2=2,\qquad
\lambda_3=4.
$$

Corresponding integer eigenvectors can be chosen as

$$
v_1=
\begin{bmatrix}1\\0\\0\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}1\\1\\0\end{bmatrix},
\qquad
v_3=
\begin{bmatrix}0\\1\\1\end{bmatrix}.
$$

Thus,

$$
\boxed{
v_1=
\begin{bmatrix}1\\0\\0\end{bmatrix},
\quad
v_2=
\begin{bmatrix}1\\1\\0\end{bmatrix},
\quad
v_3=
\begin{bmatrix}0\\1\\1\end{bmatrix}
}.
$$

### 3(ii) Matrix $P$

The columns of $P$ must be eigenvectors arranged in the same order as
the corresponding eigenvalues in $D$.

Hence,

$$
\boxed{
P=
\begin{bmatrix}
1&1&0\\
0&1&1\\
0&0&1
\end{bmatrix}
}.
$$

Then

$$
P^{-1}BP=
\begin{bmatrix}
1&0&0\\
0&2&0\\
0&0&4
\end{bmatrix}
=D.
$$

------------------------------------------------------------------------

## Question 4

### 4(i) Expressing $x_0$ using the eigenvectors

We require

$$
x_0=c_1v_1+c_2v_2.
$$

Therefore,

$$
\begin{bmatrix}
10000\\
15000
\end{bmatrix}
=
c_1
\begin{bmatrix}
2\\
1
\end{bmatrix}
+
c_2
\begin{bmatrix}
1\\
-1
\end{bmatrix}.
$$

This gives

$$
2c_1+c_2=10000,
$$

$$
c_1-c_2=15000.
$$

Adding the equations,

$$
3c_1=25000,
$$

so

$$
c_1=\frac{25000}{3}.
$$

Then

$$
c_2=c_1-15000
=
-\frac{20000}{3}.
$$

Hence

$$
\boxed{
x_0=
\frac{25000}{3}v_1
-
\frac{20000}{3}v_2
}.
$$

### 4(ii) Population after $n$ years

Since

$$
Av_1=\frac65v_1,
\qquad
Av_2=\frac45v_2,
$$

we have

$$
x_n
=
\frac{25000}{3}
\left(\frac65\right)^n v_1
-
\frac{20000}{3}
\left(\frac45\right)^n v_2.
$$

Therefore,

$$
\boxed{
x_n
=
\frac{25000}{3}
\left(\frac65\right)^n
\begin{bmatrix}2\\1\end{bmatrix}
-
\frac{20000}{3}
\left(\frac45\right)^n
\begin{bmatrix}1\\-1\end{bmatrix}
}.
$$

In component form,

$$
\boxed{
j_n=
\frac{50000}{3}\left(\frac65\right)^n
-
\frac{20000}{3}\left(\frac45\right)^n
}
$$

and

$$
\boxed{
a_n=
\frac{25000}{3}\left(\frac65\right)^n
+
\frac{20000}{3}\left(\frac45\right)^n
}.
$$

### 4(iii) Long-run juvenile-to-adult ratio

Because

$$
\left|\frac65\right|>\left|\frac45\right|,
$$

the term involving $\left(\frac65\right)^n$ dominates as $n\to\infty$.

Thus the population vector approaches the direction of

$$
v_1=
\begin{bmatrix}2\\1\end{bmatrix}.
$$

Hence,

$$
\boxed{
\lim_{n\to\infty}\frac{j_n}{a_n}=2
}.
$$

The long-run juvenile-to-adult ratio is therefore

$$
\boxed{2:1}.
$$

------------------------------------------------------------------------

## Question 5

### 5(i) Fundamental solutions

For

$$
A=
\begin{bmatrix}
2&1\\
2&3
\end{bmatrix},
$$

the characteristic equation is

$$
\det(A-\lambda I)=0.
$$

Thus,

$$
(2-\lambda)(3-\lambda)-2=0,
$$

$$
\lambda^2-5\lambda+4=0,
$$

$$
(\lambda-1)(\lambda-4)=0.
$$

Hence,

$$
\lambda_1=1,\qquad \lambda_2=4.
$$

For $\lambda_1=1$, an eigenvector is

$$
v_1=
\begin{bmatrix}1\\-1\end{bmatrix}.
$$

For $\lambda_2=4$, an eigenvector is

$$
v_2=
\begin{bmatrix}1\\2\end{bmatrix}.
$$

Therefore the fundamental solutions are

$$
\boxed{
y^{(1)}(t)
=
e^t
\begin{bmatrix}1\\-1\end{bmatrix}
}
$$

and

$$
\boxed{
y^{(2)}(t)
=
e^{4t}
\begin{bmatrix}1\\2\end{bmatrix}
}.
$$

### 5(ii) General solution

The vector-form general solution is

$$
y(t)
=
c_1e^t
\begin{bmatrix}1\\-1\end{bmatrix}
+
c_2e^{4t}
\begin{bmatrix}1\\2\end{bmatrix}.
$$

Therefore, in component form,

$$
\boxed{
y_1(t)=c_1e^t+c_2e^{4t}
}
$$

and

$$
\boxed{
y_2(t)=-c_1e^t+2c_2e^{4t}
}.
$$

### 5(iii) Particular solution

Using

$$
y_1(0)=1,\qquad y_2(0)=1,
$$

we obtain

$$
c_1+c_2=1,
$$

$$
-c_1+2c_2=1.
$$

Adding appropriately gives

$$
3c_2=2,
$$

so

$$
c_2=\frac23,
\qquad
c_1=\frac13.
$$

Hence,

$$
\boxed{
y_1(t)
=
\frac13e^t+\frac23e^{4t}
}
$$

and

$$
\boxed{
y_2(t)
=
-\frac13e^t+\frac43e^{4t}
}.
$$

------------------------------------------------------------------------

# Quick Answer Sheet

  -------------------------------------------------------------------------------------------------------
  Part                                Answer
  ----------------------------------- -------------------------------------------------------------------
  1(i)                                $[T]=\begin{bmatrix}1&2&0\\0&1&1\\2&0&1\end{bmatrix}$

  1(ii)                               Same matrix using $[T]=YX^{-1}$

  2(i)                                $\lambda=1,3$, each with algebraic multiplicity $2$

  2(ii)                               $E_1=\operatorname{span}\{(1,-1,0,0),(0,0,0,1)\}$;
                                      $E_3=\operatorname{span}\{(1,1,0,0),(0,0,1,0)\}$

  2(iii)                              Yes; there are $4$ linearly independent eigenvectors

  3(i)                                $v_1=(1,0,0)$, $v_2=(1,1,0)$, $v_3=(0,1,1)$

  3(ii)                               $P=\begin{bmatrix}1&1&0\\0&1&1\\0&0&1\end{bmatrix}$

  4(i)                                $c_1=\frac{25000}{3}$, $c_2=-\frac{20000}{3}$

  4(ii)                               $x_n=\frac{25000}{3}(\frac65)^nv_1-\frac{20000}{3}(\frac45)^nv_2$

  4(iii)                              Juvenile : adult $=2:1$

  5(i)                                $e^t(1,-1)^T$ and $e^{4t}(1,2)^T$

  5(ii)                               $y_1=c_1e^t+c_2e^{4t}$; $y_2=-c_1e^t+2c_2e^{4t}$

  5(iii)                              $y_1=\frac13e^t+\frac23e^{4t}$; $y_2=-\frac13e^t+\frac43e^{4t}$
  -------------------------------------------------------------------------------------------------------

> \[!tip\] For practice, attempt the **Practice Questions** first
> without scrolling to the **Answer Sheet**. The structure follows the
> official WS3 sample, but all filled-in numerical values in this file
> are newly created practice values.
