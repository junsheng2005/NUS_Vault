> [!warning] Coverage notice
> This file currently contains the reconstructed AY2024/25 and AY2025/26 questions only. Earlier papers still require mathematical reconstruction from the original PDF pages. Do not treat this as the complete seven-paper revision collection.

# MA1513 Open-Ended Revision Compilation

> [!info] Formatting
> All equations, vectors, matrices and systems have been reconstructed in Obsidian-compatible MathJax. Exam instructions and answer-booklet boilerplate are excluded.

> [!info] Organisation
> Questions are grouped by question type, using terminology from the supplied MA1513 notes.

# Linear System Modelling

## AY2024/2025 Semester 1 / Question 16 / Chapter 1 / Linear System Modelling

### Question

A manufacturer makes furniture A, B, C and D using 2600 units of wood, 600 units of upholstery and 2400 units of labour. Resource requirements are:

| Resource | A | B | C | D |
|---|---:|---:|---:|---:|
| Wood | 4 | 4 | 3 | 4 |
| Upholstery | 0 | 1 | 0 | 2 |
| Labour | 2 | 3 | 4 | 4 |

**(i)** Set up a linear system for the numbers $a,b,c,d$ produced.

**(ii)** Solve the system.

**(iii)** Find the possible range of $d$.

> [!success]- Worked Solution
> **(i)** Resource balance gives
> $$
> \begin{cases}
> 4a+4b+3c+4d=2600\\
> b+2d=600\\
> 2a+3b+4c+4d=2400
> \end{cases}
> $$
>
> **(ii)** Row reduction gives
> $$
> \operatorname{RREF}=
> \begin{bmatrix}
> 1&0&0&-1&-100\\
> 0&1&0&2&600\\
> 0&0&1&0&200
> \end{bmatrix}.
> $$
> Let $d=t$. Then
> $$a=-100+t,\qquad b=600-2t,\qquad c=200,\qquad d=t.$$
>
> **(iii)** Production quantities must be non-negative:
> $$-100+t\ge0,\qquad 600-2t\ge0,\qquad t\ge0.$$
> Hence
> $$\boxed{100\le d\le300}.$$


# Traffic Flow Model

## AY2024/2025 Semester 2 / Question 16 / Chapter 1 / Traffic Flow Model

### Question

![[Attachments/MA1513_AY2425_S2_Q16_Traffic_Diagram.png]]

A one-way traffic network has unknown flows $x,y,z$ and external flows $a,b,c$.

**(i)** For $a=100$, $b=150$, $c=50$, form $Ax=b$ using the junction equations in the order A, B, C.

**(ii)** Find the general solution.

**(iii)** Find the smallest possible value of $y$.

**(iv)** For general $a,b,c$, find the condition for the system to be consistent.

> [!success]- Worked Solution
> **(i)** Flow conservation gives
> $$-x+y=100,\qquad -x+z=150,\qquad -y+z=50.$$
> Thus
> $$A=\begin{bmatrix}-1 & 1 & 0\\-1 & 0 & 1\\0 & -1 & 1\end{bmatrix},\qquad b=\begin{bmatrix}100\\150\\50\end{bmatrix}.$$
>
> **(ii)** Row reduction gives
> $$x=t-150,\qquad y=t-50,\qquad z=t.$$
>
> **(iii)** Since all flows are non-negative, $t\ge150$, so
> $$y_{\min}=150-50=\boxed{100}.$$
>
> **(iv)** With general right-hand side $\begin{bmatrix}a\\b\\c\end{bmatrix}$, elimination produces the consistency condition
> $$\boxed{c-b+a=0}.$$


# Matrix Model

## AY2025/2026 Semester 1 / Question 16 / Chapter 1 / Matrix Model

### Question

![[Attachments/MA1513_AY2526_S1_Q16_Beam_Diagram.png]]

A horizontal elastic beam has force vector $f=\begin{bmatrix}f_1\\f_2\\f_3\\f_4\end{bmatrix}$ and deflection vector $y=\begin{bmatrix}y_1\\y_2\\y_3\\y_4\end{bmatrix}$. Its flexibility matrix is
$$D=\begin{bmatrix}0.004 & 0.003 & 0.002 & 0.001\\0.001 & 0.004 & 0.003 & 0.002\\0.002 & 0.001 & 0.004 & 0.003\\0.003 & 0.002 & 0.001 & 0.004\end{bmatrix}.$$

**(i)** Find the deflections when all four downward forces are 10 N.

**(ii)** Find forces producing $y=(0,0,0,0.2)^T$ cm.

**(iii)** Can two different force combinations produce the same deflection vector?

> [!success]- Worked Solution
> The model is $y=Df$.
>
> **(i)**
> $$y=D\begin{bmatrix}10\\10\\10\\10\end{bmatrix}=\begin{bmatrix}0.1\\0.1\\0.1\\0.1\end{bmatrix}	ext{ cm}.$$
>
> **(ii)** Since $D$ is invertible,
> $$f=D^{-1}y=\begin{bmatrix}5\\5\\-45\\55\end{bmatrix}	ext{ N}.$$
> So the third force is 45 N upward; the others are downward.
>
> **(iii)** No. Because $D$ is non-singular, $Df=y$ has a unique solution $f$ for each fixed $y$.


# Projection and Linear Approximation

## AY2024/2025 Semester 1 / Question 17 / Chapter 2 / Projection and Linear Approximation

### Question

Let
$$A=\begin{bmatrix}1 & 2 & 1 & 0\\2 & 4 & 0 & -2\\1 & 2 & 2 & 1\end{bmatrix},\qquad b=\begin{bmatrix}2\\1\\0\end{bmatrix}.$$

**(i)** Find a basis and the dimension of $\operatorname{Col}(A)$.

**(ii)** Find the projection of $b$ onto $\operatorname{Col}(A)$.

**(iii)** Find a unit vector orthogonal to every vector in $\operatorname{Col}(A)$.

> [!success]- Worked Solution
> **(i)**
> $$\operatorname{RREF}(A)=\begin{bmatrix}1 & 2 & 0 & -1\\0 & 0 & 1 & 1\\0 & 0 & 0 & 0\end{bmatrix}.$$
> Pivot columns are 1 and 3, so a basis is
> $$\left\{\begin{bmatrix}1\\2\\1\end{bmatrix},\begin{bmatrix}1\\0\\2\end{bmatrix}
> \right\},\qquad \dim\operatorname{Col}(A)=2.$$
>
> **(ii)** A least-squares solution may be chosen as
> $$x_0=\begin{bmatrix}2/3\\0\\0\\0\end{bmatrix}.$$
> Therefore
> $$p=Ax_0=\begin{bmatrix}2/3\\4/3\\2/3\end{bmatrix}.$$
>
> **(iii)**
> $$p-b=\begin{bmatrix}-4/3\\1/3\\2/3\end{bmatrix}.$$
> Its norm is $\sqrt{21}/3$, so a unit normal vector is
> $$\boxed{\begin{bmatrix}-4/\sqrt{21}\\1/\sqrt{21}\\2/\sqrt{21}\end{bmatrix}}$$
> (or its negative).


## AY2025/2026 Semester 1 / Question 17 / Chapter 2 / Projection and Linear Approximation

### Question

Let $P_1$ and $P_2$ be the planes
$$x+y-2z=0,\qquad 2x-y+z=0.$$

**(i)** Solve their simultaneous equations.

**(ii)** Express their line of intersection $L_1$ as a span.

**(iii)** Let $P_3:x+y+z=0$. Express $P_3$ as a span.

**(iv)** Project $L_1$ onto $P_3$ and express the projected line $L_2$ as a span.

> [!success]- Worked Solution
> **(i)** Gaussian elimination gives
> $$x=\frac t3,\qquad y=\frac{5t}{3},\qquad z=t.$$
>
> **(ii)** Taking $t=3$ gives the direction $(1,5,3)$, so
> $$L_1=\operatorname{span}\{(1,5,3)\}.$$
>
> **(iii)** Two independent vectors satisfying $x+y+z=0$ are $(1,-1,0)$ and $(0,1,-1)$:
> $$P_3=\operatorname{span}\{(1,-1,0),(0,1,-1)\}.$$
>
> **(iv)** Let
> $$A=\begin{bmatrix}1&0\\-1&1\\0&-1\end{bmatrix},\qquad v=\begin{bmatrix}1\\5\\3\end{bmatrix}.$$
> Solve the normal equations
> $$A^TAx=A^Tv.$$
> This gives
> $$x_0=\begin{bmatrix}-2\\0\end{bmatrix},\qquad Ax_0=\begin{bmatrix}-2\\2\\0\end{bmatrix}.$$
> Hence
> $$\boxed{L_2=\operatorname{span}\{(-2,2,0)\}}.$$


# Population Model

## AY2024/2025 Semester 1 / Question 18 / Chapter 3 / Population Model

### Question

A species has juvenile and adult stages. Each year an adult produces 1.2 juveniles, 50% of juveniles become adults, and 40% of adults survive. Let
$$x_n=\begin{bmatrix}j_n\\a_n\end{bmatrix}.$$

**(i)** Find the stage matrix $A$ such that $x_{n+1}=Ax_n$.

**(ii)** Diagonalize $A^n$.

**(iii)** Starting from $(j_0,a_0)=(10000,8000)$, determine the long-run population.

**(iv)** Does the juvenile:adult ratio stabilize regardless of the initial populations?

> [!success]- Worked Solution
> **(i)**
> $$j_{n+1}=1.2a_n,\qquad a_{n+1}=0.5j_n+0.4a_n,$$
> so
> $$A=\begin{bmatrix}0 & 1.2\\0.5 & 0.4\end{bmatrix}.$$
>
> **(ii)** Eigenvalues are $-0.6$ and $1$ with eigenvectors $\begin{bmatrix}-2\\1\end{bmatrix}$ and $\begin{bmatrix}6/5\\1\end{bmatrix}$. Thus
> $$P=\begin{bmatrix}-2 & 6/5\\1 & 1\end{bmatrix},\qquad D=\begin{bmatrix}-0.6 & 0\\0 & 1\end{bmatrix},$$
> $$A^n=PD^nP^{-1}.$$
>
> **(iii)** Since $(-0.6)^n\to 0$,
> $$A^n\to \begin{bmatrix}3/8 & 3/4\\5/16 & 5/8\end{bmatrix}.$$
> Hence
> $$x_n\to \begin{bmatrix}9750\\8125\end{bmatrix}.$$
>
> **(iv)** Yes. The long-run state is proportional to the eigenvector $\begin{bmatrix}6/5\\1\end{bmatrix}$, so
> $$j:a=
> \frac{6}{5}:1=\boxed{6:5}.$$


## AY2025/2026 Semester 1 / Question 18 / Chapter 3 / Population Model

### Question

A species has juvenile and adult stages. Each year an adult produces 2 juveniles, half the juveniles become adults, and $5/6$ of adults survive.

**(i)** Find the stage matrix $A$.

**(ii)** If $j_{2025}=12000$, find $a_{2025}$ so that the juvenile:adult proportion remains unchanged in following years.

**(iii)** Do the populations stabilize in the long run?

> [!success]- Worked Solution
> **(i)**
> $$A=\begin{bmatrix}0 & 2\\1/2 & 5/6\end{bmatrix}.$$
>
> **(ii)** The eigenvalues are $-2/3$ and $3/2$, with eigenvectors $\begin{bmatrix}-3\\1\end{bmatrix}$ and $\begin{bmatrix}4/3\\1\end{bmatrix}$. A fixed population proportion must follow a positive eigenvector, so use $(4/3,1)^T$:
> $$
> \frac{12000}{a_{2025}}=
> \frac{4}{3}.$$
> Therefore
> $$\boxed{a_{2025}=9000}.$$
>
> **(iii)** No. The dominant eigenvalue is $3/2>1$, so the populations grow by a factor approaching $1.5$ per year, although their ratio tends to $4:3$.


# Market Share Model

## AY2024/2025 Semester 2 / Question 18 / Chapter 3 / Market Share Model

### Question

Three coffee brands A, B and C serve 30,000 households. Monthly market shares satisfy
$$x_{n+1}=Ax_n,\qquad x_n=\begin{bmatrix}a_n\\b_n\\c_n\end{bmatrix}.$$
Observed shares are:

| Brand | Jan | Feb | Mar | Apr |
|---|---:|---:|---:|---:|
| A | 10000 | 11200 | 11740 | 11968 |
| B | 8000 | 9800 | 10760 | 11282 |
| C | 12000 | 9000 | 7500 | 6750 |

**(i)** Find $A$.

**(ii)** Find matrices $P,D$ with $P^{-1}AP=D$.

**(iii)** Find the long-run market shares.

**(iv)** Can all three brands have equal long-run market shares for any initial shares?

> [!success]- Worked Solution
> **(i)** Stacking consecutive month vectors gives
> $$A=\begin{bmatrix}0.8 & 0.1 & 0.2\\0.1 & 0.8 & 0.2\\0.1 & 0.1 & 0.6\end{bmatrix}.$$
>
> **(ii)** One valid diagonalization is
> $$P=\begin{bmatrix}-1 & 2 & -1/2\\1 & 2 & -1/2\\0 & 1 & 1\end{bmatrix},\qquad D=\begin{bmatrix}7/10 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1/2\end{bmatrix}.$$
>
> **(iii)** As $n	o\infty$, $(7/10)^n$ and $(1/2)^n$ vanish. Thus
> $$A^n\to \begin{bmatrix}2/5 & 2/5 & 2/5\\2/5 & 2/5 & 2/5\\1/5 & 1/5 & 1/5\end{bmatrix}.$$
> For total market size 30,000,
> $$x_n\to \begin{bmatrix}12000\\12000\\6000\end{bmatrix}.$$
>
> **(iv)** True: equal long-run shares are impossible. The limiting ratio is always $2:2:1$, independent of the initial split (for the fixed total).


# Damped Mass-Spring System

## AY2024/2025 Semester 2 / Question 17 / Chapter 4 / Damped Mass-Spring System

### Question

A damped mass-spring system satisfies
$$my''+cy'+ky=0.$$
For $m=1$ kg, measurements are:

| Set | $y$ | $y'$ | $y''$ |
|---|---:|---:|---:|
| 1 | 0 | 1.5 | -12.5 |
| 2 | 0.5 | 0.5 | -15 |
| 3 | 0.2 | -1 | 10 |

**(i)** Set up $Ax=b$ for $x=(c,k)^T$.

**(ii)** Find the least-squares best-fit ODE.

**(iii)** Is the system over-damped or under-damped?

**(iv)** Convert the ODE to an SDE.

> [!success]- Worked Solution
> **(i)** Substitution gives
> $$1.5c=12.5,\quad 0.5c+0.5k=15,\quad -c+0.2k=-10.$$
> Thus
> $$A=\begin{bmatrix}1.5 & 0\\0.5 & 0.5\\-1 & 0.2\end{bmatrix},\qquad b=\begin{bmatrix}12.5\\15\\-10\end{bmatrix}.$$
>
> **(ii)** The least-squares solution is
> $$\begin{bmatrix}c\\k\end{bmatrix}=(A^TA)^{-1}A^Tb\approx \begin{bmatrix}10.11\\17.22\end{bmatrix}.$$
> Therefore
> $$\boxed{y''+10.11y'+17.22y=0}.$$
>
> **(iii)**
> $$c^2\approx102.21>4km\approx68.88,$$
> so the system is **over-damped**.
>
> **(iv)** With $y_1=y$, $y_2=y'$,
> $$\boxed{\mathbf y'=\begin{bmatrix}0 & 1\\-17.22 & -10.11\end{bmatrix}\mathbf y}.$$


## AY2025/2026 Semester 1 / Question 19 / Chapter 4 / Damped Mass-Spring System

### Question

A damped mass-spring ODE
$$my''+cy'+ky=0$$
has general solution
$$y=c_1e^{-2t}+c_2e^{-t/2}.$$

**(i)** Find the general solution of the associated SDE.

**(ii)** Determine the type and stability of the equilibrium point.

**(iii)** Describe the motion before equilibrium.

**(iv)** If $m=2$, find $c$ and $k$.

**(v)** Describe/sketch the phase portrait.


> [!success]- Worked Solution
> **(i)** Let $y_1=y$ and $y_2=y'$. Then
> $$y_2=-2c_1e^{-2t}-
> \frac{1}{2}c_2e^{-t/2},$$
> so
> $$\boxed{\mathbf y=c_1e^{-2t}\begin{bmatrix}1\\-2\end{bmatrix}+c_2e^{-t/2}\begin{bmatrix}1\\-1/2\end{bmatrix}}.$$
>
> **(ii)** The eigenvalues are $-2$ and $-1/2$: both real, distinct and negative. The equilibrium is an **asymptotically stable node**.
>
> **(iii)** The system is over-damped, so the ball returns to equilibrium without oscillating.
>
> **(iv)** Using eigenvectors $\begin{bmatrix}1\\-2\end{bmatrix}$ and $\begin{bmatrix}1\\-1/2\end{bmatrix}$,
> $$A=PDP^{-1}=\begin{bmatrix}0 & 1\\-1 & -2.5\end{bmatrix}.$$
> Compare with
> $$A=\begin{bmatrix}0 & 1\\-k/m & -c/m\end{bmatrix}.$$
> For $m=2$,
> $$\boxed{k=2,\qquad c=5}.$$
>
> **(v)** The phase portrait is a stable node. Trajectories approach the origin and are asymptotically tangent to the eigenvector associated with the slower-decaying eigenvalue $-1/2$.
>
> ![[Attachments/MA1513_AY2526_S1_Q19_Phase_Portrait_Solution.png]]
>
> *Phase portrait reconstructed from the SDE matrix in the worked solution (not copied from an annotated answer key).*


# Phase Plane

## AY2024/2025 Semester 1 / Question 19 / Chapter 4 / Phase Plane

### Question

A particular solution of $y'=Ay$ is
$$y=3e^{-t}\begin{bmatrix}-\cos t+\sin t\\2\cos t\end{bmatrix}-3e^{-t}\begin{bmatrix}-\sin t-\cos t\\2\sin t\end{bmatrix}.$$

**(i)** Find $A$.

**(ii)** State the type and stability of the equilibrium point.

**(iii)** Describe the trajectory and its initial point at $t=0$.

**(iv)** Find the tangent vector when the trajectory first crosses the horizontal $y_1$-axis after $t=0$.

> [!success]- Worked Solution
> **(i)** The complex eigenvalues are $-1\pm i$. Reconstructing from the real/imaginary eigenvector parts gives
> $$\boxed{A=\begin{bmatrix}0 & 1\\-2 & -2\end{bmatrix}}.$$
>
> **(ii)** Since the real part is negative and the eigenvalues are complex, the equilibrium is an **asymptotically stable spiral**.
>
> **(iii)** At $t=0$,
> $$y(0)=\begin{bmatrix}0\\6\end{bmatrix}.$$
> The trajectory spirals **clockwise inward** through $(0,6)$.
>
> **(iv)** Crossing the $y_1$-axis means $y_2=0$:
> $$6e^{-t}(\cos t-\sin t)=0\Rightarrow \tan t=1.$$
> The first time after 0 is $t=\pi/4$. The point is
> $$y\left(
> \frac{\pi}{4}
> \right)=3\sqrt2e^{-\pi/4}\begin{bmatrix}1\\0\end{bmatrix}.$$
> Therefore the tangent vector is
> $$Ay=3\sqrt2e^{-\pi/4}\begin{bmatrix}0\\-2\end{bmatrix}.$$


# Solutions and Mixing Problem

## AY2024/2025 Semester 2 / Question 19 / Chapter 4 / Solutions and Mixing Problem

### Question

**(a)** Consider
$$y'=\begin{bmatrix}-5 & 4\\-4 & 5\end{bmatrix}y,$$
with eigenvectors $v_1=\begin{bmatrix}1\\2\end{bmatrix}$ and $v_2=\begin{bmatrix}2\\1\end{bmatrix}$.

1. Find a fundamental set of solutions.
2. Solve the IVP $y_1(0)=3$, $y_2(0)=0$.
3. Classify/describe the phase portrait.

**(b)** Three 100 L mixing tanks have the flow diagram given in the paper.

![[Attachments/MA1513_AY2425_S2_Q19_Tank_Diagram.png]] Set up the $3\times3$ SDE for salt amounts $y_1,y_2,y_3$.

> [!success]- Worked Solution
> **(a1)**
> $$A\begin{bmatrix}1\\2\end{bmatrix}=3\begin{bmatrix}1\\2\end{bmatrix},\qquad A\begin{bmatrix}2\\1\end{bmatrix}=-3\begin{bmatrix}2\\1\end{bmatrix}.$$
> Hence a fundamental set is
> $$y^1=\begin{bmatrix}1\\2\end{bmatrix}e^{3t},\qquad y^2=\begin{bmatrix}2\\1\end{bmatrix}e^{-3t}.$$
>
> **(a2)** The general solution is
> $$y=c_1\begin{bmatrix}1\\2\end{bmatrix}e^{3t}+c_2\begin{bmatrix}2\\1\end{bmatrix}e^{-3t}.$$
> Using $y(0)=(3,0)^T$ gives $c_1=-1$, $c_2=2$:
> $$\boxed{y=-\begin{bmatrix}1\\2\end{bmatrix}e^{3t}+2\begin{bmatrix}2\\1\end{bmatrix}e^{-3t}}.$$
>
> **(a3)** The eigenvalues have opposite signs, so the equilibrium is a **saddle point**. The eigenvector directions are the straight-line trajectories.
>
> **(b)** From inflow minus outflow for each tank,
> $$\boxed{\mathbf y'=\begin{bmatrix}-0.08 & 0.04 & 0\\0.08 & -0.1 & 0.02\\0 & 0.06 & -0.06\end{bmatrix}\mathbf y}.$$

