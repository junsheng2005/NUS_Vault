																						# MA1513 — WS2 Practice Set

> [!warning] Practice only
> This is a **new practice version** based on the structure of the WS2 sample. It is **not** the actual WS2 assignment. The sample states that the actual questions differ by tutorial group and that LLM use is not allowed during the assignment.

---

## Question 1 — Determinants, Non-singularity, and Homogeneous Systems

Given

$$
A=\begin{pmatrix}
1&2&0\\
0&1&1\\
2&0&1
\end{pmatrix},
\qquad
B=\begin{pmatrix}
1&2&3\\
2&4&6\\
0&1&1
\end{pmatrix}.
$$

### 1(i)
Without using MATLAB, find $\det(A)$ and determine whether $A$ is non-singular. Show your working.

### 1(ii)
Without using MATLAB, find $\det(B)$ and determine whether $B$ is non-singular. Show your working.

### 1(iii)
Without performing Gaussian elimination, determine which of

$$
A^2x=0,\qquad B^Tx=0,\qquad BAx=0
$$

have non-trivial solutions. Briefly explain your answers.

---

## Question 2 — Linear Combinations and Spans

Let

$$
u=(1,1,0,0),\qquad v=(0,0,1,1),\qquad w=(1,0,1,0).
$$

Use

$$
x=(2,1,3,2),\qquad y=(1,0,0,1).
$$

### 2(i)
Is $x$ a linear combination of $u,v,w$? Why?

### 2(ii)
Does $y$ belong to $\operatorname{span}\{u,v,w\}$? Why?

### 2(iii)
Which of the following spans are equal?

$$
\operatorname{span}\{u,v,w\},
$$

$$
\operatorname{span}\{u,v,w,x\},
$$

$$
\operatorname{span}\{u,v,w,y\},
$$

$$
\operatorname{span}\{u,v,w,x,y\}.
$$

Justify your answer.

---

## Question 3 — Homogeneous Linear System

Given

$$
x+y+z+w=0,
$$

$$
2x+y+3z+2w=0.
$$

### 3(i)
Find the general solution of the homogeneous system.

### 3(ii)
Find a basis for the solution space. Show how you obtain your answer.

### 3(iii)
Express the solution space as a linear span.

---

## Question 4 — Row Space, Least Squares, and Projection

Let

$$
A=\begin{pmatrix}
1&0&1\\
0&1&1\\
1&1&2\\
1&-1&0
\end{pmatrix},
\qquad
x=\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix},
\qquad
b=\begin{pmatrix}1\\2\\2\\0\end{pmatrix}.
$$

### 4(i)
Find a basis for the row space of $A$. Explain how you obtain your answer.

### 4(ii)
Find a least-squares solution of $Ax=b$. Show your working.

### 4(iii)
Find the projection of $b$ onto the column space of $A$. Show your working.

---

# Answer Sheet

## Answers to Question 1

### 1(i)

Expanding along the first row,

$$
\det(A)
=1\begin{vmatrix}1&1\\0&1\end{vmatrix}
-2\begin{vmatrix}0&1\\2&1\end{vmatrix}
=1-2(-2)=5.
$$

Therefore,

$$
\boxed{\det(A)=5}
$$

and $A$ is **non-singular** because $\det(A)\ne0$.

### 1(ii)

The second row of $B$ is twice the first row. Therefore its rows are linearly dependent, so

$$
\boxed{\det(B)=0}.
$$

Hence $B$ is **singular**.

### 1(iii)

- $A^2x=0$: since $A$ is non-singular, $A^2$ is also non-singular. Hence only the trivial solution exists.
- $B^Tx=0$: since $B$ is singular, $B^T$ is singular. Hence a non-trivial solution exists.
- $BAx=0$: $A$ is invertible but $B$ is singular, so $BA$ is singular. Hence a non-trivial solution exists.

Therefore,

$$
\boxed{B^Tx=0\text{ and }BAx=0\text{ have non-trivial solutions.}}
$$

---

## Answers to Question 2

A general linear combination is

$$
au+bv+cw
=(a+c,a,b+c,b).
$$

### 2(i)

For $x=(2,1,3,2)$, compare

$$
(a+c,a,b+c,b)=(2,1,3,2).
$$

This gives

$$
a=1,\qquad b=2,\qquad c=1,
$$

and all four coordinates agree. Thus

$$
\boxed{x=u+2v+w}.
$$

So $x\in\operatorname{span}\{u,v,w\}$.

### 2(ii)

For $y=(1,0,0,1)$, we would require

$$
a=0,\qquad b=1.
$$

The first coordinate then requires $c=1$, but the third coordinate would be

$$
b+c=2\ne0.
$$

Therefore the equations are inconsistent and

$$
\boxed{y\notin\operatorname{span}\{u,v,w\}}.
$$

### 2(iii)

Since $x\in\operatorname{span}\{u,v,w\}$, adding $x$ does not enlarge the span:

$$
\boxed{\operatorname{span}\{u,v,w\}=\operatorname{span}\{u,v,w,x\}}.
$$

Since $y$ is not in the original span, adding $y$ enlarges it. Adding $x$ afterward makes no further difference because $x$ was already in the original span. Hence

$$
\boxed{\operatorname{span}\{u,v,w,y\}=\operatorname{span}\{u,v,w,x,y\}}.
$$

The two groups above are not equal to each other.

---

## Answers to Question 3

The system is

$$
x+y+z+w=0,
$$

$$
2x+y+3z+2w=0.
$$

Subtract twice the first equation from the second:

$$
-y+z=0,
$$

so

$$
y=z.
$$

From the first equation,

$$
x=-2z-w.
$$

Let

$$
z=s,\qquad w=t.
$$

### 3(i)

The general solution is

$$
\boxed{(x,y,z,w)=(-2s-t,s,s,t),\qquad s,t\in\mathbb R.}
$$

Equivalently,

$$
\begin{pmatrix}x\\y\\z\\w\end{pmatrix}
=s\begin{pmatrix}-2\\1\\1\\0\end{pmatrix}
+t\begin{pmatrix}-1\\0\\0\\1\end{pmatrix}.
$$

### 3(ii)

A basis for the solution space is

$$
\boxed{
\left\{
\begin{pmatrix}-2\\1\\1\\0\end{pmatrix},
\begin{pmatrix}-1\\0\\0\\1\end{pmatrix}
\right\}.
}
$$

### 3(iii)

The solution space is

$$
\boxed{
\operatorname{span}\left\{
\begin{pmatrix}-2\\1\\1\\0\end{pmatrix},
\begin{pmatrix}-1\\0\\0\\1\end{pmatrix}
\right\}.
}
$$

---

## Answers to Question 4

### 4(i)

The rows are

$$
r_1=(1,0,1),\quad r_2=(0,1,1),\quad r_3=(1,1,2),\quad r_4=(1,-1,0).
$$

Observe that

$$
r_3=r_1+r_2,
$$

and

$$
r_4=r_1-r_2.
$$

Thus every row is generated by $r_1,r_2$, which are linearly independent. A basis is

$$
\boxed{\{(1,0,1),(0,1,1)\}}.
$$

### 4(ii)

The columns of $A$ satisfy

$$
c_3=c_1+c_2.
$$

Hence $Ax$ depends on $x_1+x_3$ and $x_2+x_3$. Write

$$
p=x_1+x_3,\qquad q=x_2+x_3.
$$

Then

$$
Ax=pc_1+qc_2.
$$

The reduced least-squares normal equations are

$$
\begin{pmatrix}3&0\\0&3\end{pmatrix}
\begin{pmatrix}p\\q\end{pmatrix}
=
\begin{pmatrix}3\\4\end{pmatrix},
$$

so

$$
p=1,\qquad q=\frac43.
$$

Therefore all least-squares solutions satisfy

$$
x_1+x_3=1,
$$

$$
x_2+x_3=\frac43.
$$

Let $x_3=t$. Then

$$
\boxed{
\hat x=
\begin{pmatrix}
1-t\\[2pt]
\frac43-t\\[2pt]
t
\end{pmatrix},\qquad t\in\mathbb R.
}
$$

For example, taking $t=0$ gives one least-squares solution

$$
\boxed{
\hat x=
\begin{pmatrix}1\\[2pt]\frac43\\[2pt]0\end{pmatrix}.
}
$$

### 4(iii)

The projection is

$$
\operatorname{proj}_{\operatorname{Col}(A)}b=A\hat x.
$$

Using $p=1$ and $q=\frac43$,

$$
A\hat x
=c_1+\frac43c_2
=
\begin{pmatrix}
1\\[2pt]
\frac43\\[2pt]
\frac73\\[2pt]
-\frac13
\end{pmatrix}.
$$

Therefore,

$$
\boxed{
\operatorname{proj}_{\operatorname{Col}(A)}b=
\begin{pmatrix}
1\\[2pt]
\frac43\\[2pt]
\frac73\\[2pt]
-\frac13
\end{pmatrix}.
}
$$

---

## Quick Answer Summary

| Part | Answer |
|---|---|
| 1(i) | $\det(A)=5$; $A$ is non-singular |
| 1(ii) | $\det(B)=0$; $B$ is singular |
| 1(iii) | $B^Tx=0$ and $BAx=0$ have non-trivial solutions |
| 2(i) | Yes; $x=u+2v+w$ |
| 2(ii) | No |
| 2(iii) | $\operatorname{span}\{u,v,w\}=\operatorname{span}\{u,v,w,x\}$ and $\operatorname{span}\{u,v,w,y\}=\operatorname{span}\{u,v,w,x,y\}$ |
| 3(i) | $(x,y,z,w)=(-2s-t,s,s,t)$ |
| 3(ii) | Basis $\{(-2,1,1,0),(-1,0,0,1)\}$ |
| 3(iii) | Span of the same two basis vectors |
| 4(i) | Basis $\{(1,0,1),(0,1,1)\}$ |
| 4(ii) | $\hat x=(1-t,\frac43-t,t)^T$; e.g. $(1,\frac43,0)^T$ |
| 4(iii) | $(1,\frac43,\frac73,-\frac13)^T$ |
