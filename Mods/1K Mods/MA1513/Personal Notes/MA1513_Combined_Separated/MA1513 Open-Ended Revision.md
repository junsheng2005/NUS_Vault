# MA1513 Open-Ended Revision

# Chapter 1

### AY2022/2023 Semester 1 / LQ1 / Chapter 1 / Traffic Flow

### Question

The diagram gives one-way traffic flow in vehicles per hour. The unknown street flows are $x_1,x_2,x_3,x_4,x_5$.

![[Attachments/AY2223_S1_LQ1_Traffic_Flow.png]]

(a) Set up $A\mathbf x=\mathbf b$ using the junctions $A,B,C,D$ in that order and variables $x_1,\ldots,x_5$.

(b) Find the general solution.

(c) Find the largest possible $x_3$ when all flows are non-negative.

(d) If the street between $A$ and $D$ closes, determine the range of $x_1$.

> [!success]- Worked Solution
> **(a)** Conservation of traffic at each junction gives
>
> $$\begin{aligned}A:&\ x_1=x_3+x_4+40,\\B:&\ x_1+x_2=200,\\C:&\ x_2+x_3=x_5+100,\\D:&\ x_4+x_5=60.\end{aligned}$$
>
> Therefore
>
> $$A=\begin{bmatrix}1&0&-1&-1&0\\1&1&0&0&0\\0&1&1&0&-1\\0&0&0&1&1\end{bmatrix},\quad \mathbf b=\begin{bmatrix}40\\200\\100\\60\end{bmatrix}.$$
>
> **(b)** Row reduction gives the equivalent equations
>
> $$\begin{aligned}x_1-x_3+x_5&=100,\\x_2+x_3-x_5&=100,\\x_4+x_5&=60.\end{aligned}$$
>
> Let $x_3=s$ and $x_5=t$. Then
>
> $$\boxed{\begin{cases}x_1=100+s-t\\x_2=100-s+t\\x_3=s\\x_4=60-t\\x_5=t.\end{cases}}$$
>
> **(c)** Non-negativity gives $0\le t\le60$ and $s\le100+t\le160$. The upper bound is attainable, so **$x_3^{\max}=160$ vehicles/hour**.
>
> **(d)** Closing the street sets $x_4=0$, hence $t=60$. Then $x_1=40+s$ with $0\le s\le160$, giving **$40\le x_1\le200$**.



### AY2022/2023 Semester 2 / LQ1 / Chapter 1 / Application of Linear Systems

### Question

A company produces vacuum cleaners A, B and C. The resource costs per unit (dollars) are:

| Model | Labour | Material | Miscellaneous |
|---|---:|---:|---:|
| A | 30 | 10 | 20 |
| B | 30 | 20 | 30 |
| C | 40 | 20 | 20 |

**(i)** Express the budget for producing 300 units of A, 400 of B and 500 of C as a matrix product; find the three costs.

**(ii)** With budgets $40{,}000$ for labour, $20{,}000$ for material and $30{,}000$ for miscellaneous, find the quantities of A, B and C that exhaust the budgets.

**(iii)** Model D requires $40, $30 and $30 for the respective resources. With the same budgets, find the maximum feasible number of units of D.

> [!success]- Worked Solution
> **(i)** Arrange resources as rows and models as columns:
>
> $$\begin{bmatrix}30&30&40\\10&20&20\\20&30&20\end{bmatrix}\begin{bmatrix}300\\400\\500\end{bmatrix}=\begin{bmatrix}41000\\21000\\28000\end{bmatrix}.$$
>
> The three budgets are $\$41{,}000$, $\$21{,}000$, $\$28{,}000$.
>
> **(ii)** Solve
>
> $$\begin{bmatrix}30&30&40\\10&20&20\\20&30&20\end{bmatrix}\begin{bmatrix}a\\b\\c\end{bmatrix}=\begin{bmatrix}40000\\20000\\30000\end{bmatrix}.$$
>
> Gaussian elimination gives **$a=500,\ b=500,\ c=250$.**
>
> **(iii)** Include model D:
>
> $$\left[\begin{array}{cccc|c}30&30&40&40&40000\\10&20&20&30&20000\\20&30&20&30&30000\end{array}\right]\sim\left[\begin{array}{cccc|c}1&0&0&-1&500\\0&1&0&1&500\\0&0&1&1&250\end{array}\right].$$
>
> Let $d=t$. Then $a=500+t$, $b=500-t$, $c=250-t$. Nonnegative production requires $0\le t\le250$.
>
> **Answer: Maximum D production is $250$ units.**



### AY2024/2025 Semester 1 / Question 16 / Chapter 1 / Linear System Modelling

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



### AY2024/2025 Semester 2 / Question 16 / Chapter 1 / Traffic Flow Model

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



### AY2025/2026 Semester 1 / Question 16 / Chapter 1 / Matrix Model

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

# Chapter 2



# Chapter 2

### AY2022/2023 Semester 1 / LQ2 / Chapter 2 / Least Squares

### Question

Company Z models revenue by $y=mx+nx^2$, where $x$ measures hundreds of units sold and $y$ measures hundreds of dollars. Observed data are $(1,1.8),(2,2.7),(3,3.4),(4,3.8),(5,3.9)$.

(a) Set up the five-equation system for $m,n$.

(b) Find the least-squares values of $m,n$ to four decimal places.

(c) Predict revenue from selling 500 units to the nearest dollar.

(d) Would selling more than 500 units increase revenue? Explain.

> [!success]- Worked Solution
> **(a)** Substitute each data point into $mx+nx^2=y$:
>
> $$\begin{bmatrix}1&1\\2&4\\3&9\\4&16\\5&25\end{bmatrix}\begin{bmatrix}m\\n\end{bmatrix}=\begin{bmatrix}1.8\\2.7\\3.4\\3.8\\3.9\end{bmatrix}.$$
>
> **(b)** Use the normal equations $A^TA\mathbf x=A^T\mathbf b$:
>
> $$\begin{bmatrix}55&225\\225&979\end{bmatrix}\begin{bmatrix}m\\n\end{bmatrix}=\begin{bmatrix}52.1\\201.5\end{bmatrix}.$$
>
> Solving gives **$m\approx1.7604$, $n\approx-0.1988$**.
>
> **(c)** At 500 units, $x=5$:
>
> $$y=5m+25n\approx3.8329.$$
>
> Revenue is measured in hundreds of dollars, so the predicted revenue is **about $383**.
>
> **(d)** Since $n<0$, the parabola opens downwards. Its maximum is at
>
> $$x=-\frac{m}{2n}\approx4.4276,$$
>
> or about 443 units. Selling more than 500 units would **decrease**, not increase, the modelled revenue.


### AY2022/2023 Semester 2 / LQ2 / Chapter 2 / Least Squares

### Question

A hyperboloid with circular horizontal cross-sections has equation

$$ax^2+ay^2+bz^2=1.$$

Measured points are $(2.65,1.53,1)$, $(2.80,1.62,2)$, $(3.03,1.75,3)$, $(3.33,1.92,4)$, $(3.67,2.12,5)$.

**(i)** Set up the $5\times2$ linear system $A\mathbf x=B$ for $a,b$.

**(ii)** Find the least-squares coefficients and best-fit surface equation, to four decimal places.

**(iii)** Estimate the cross-sectional radius at $z=10$, to four decimal places.

> [!success]- Worked Solution
> **(i)** Each point gives $(x_i^2+y_i^2)a+z_i^2b=1$. Thus
>
> $$A=\begin{bmatrix}9.3634&1\\10.4644&4\\12.2434&9\\14.7753&16\\17.9633&25\end{bmatrix},\quad \mathbf x=\begin{bmatrix}a\\b\end{bmatrix},\quad B=\begin{bmatrix}1\\1\\1\\1\\1\end{bmatrix}.$$
>
> **(ii)** Solve the normal equations $A^TA\mathbf x=A^TB$:
>
> $$\mathbf x=(A^TA)^{-1}A^TB\approx\begin{bmatrix}0.1109\\-0.0397\end{bmatrix}.$$
>
> The fitted surface is **$0.1109x^2+0.1109y^2-0.0397z^2=1$.**
>
> **(iii)** At $z=10$, let $r^2=x^2+y^2$. Then
>
> $$0.1109r^2-0.0397(100)=1,\qquad r=\sqrt{\frac{1+3.97}{0.1109}}\approx6.6944.$$
>
> **Answer: $r\approx6.6944$.**



### AY2023/2024 Semester 1 / Question 16 / Chapter 2 / Solving System of Linear Equations

#### Question

The plane $P$ has equation $ax+by+cz=d$ and contains $(1,1,3)$ and $(2,-1,-2)$.

(i) Set up and solve the linear system for $a,b,c,d$.

(ii) Give a basis for the solution space.

(iii) Find an equation of $P$ if it also contains the origin.

> [!success]- Worked Solution
> **(i)** Substituting the points gives
>
> 

$$
\begin{cases}a+b+3c-d=0\\2a-b-2c-d=0.\end{cases}
$$


>
> The RREF is
>
> 

$$
\left[\begin{array}{cccc|c}1&0&\frac13&-\frac23&0\\0&1&\frac83&-\frac13&0\end{array}\right].
$$


>
> Let $c=s,d=t$. Then $a=-\frac13s+\frac23t$ and $b=-\frac83s+\frac13t$.
>
> **(ii)** A basis is
>
> 

$$
\left\{\begin{bmatrix}-\frac13\\-\frac83\\1\\0\end{bmatrix},\begin{bmatrix}\frac23\\frac13\\0\\1\end{bmatrix}\right\}.
$$


>
> **(iii)** If the plane contains the origin, $d=0$. Set $s=3$ to obtain $a=-1,b=-8,c=3$. **Answer:** $x+8y-3z=0$.


### AY2023/2024 Semester 2 / Question 16 / Chapter 2 / Solving System of Linear Equations

#### Question

Three planes have equations $x+y-z=0$, $2x-y+z=0$, and $x+2y-2z=0$.

(i) Set up and solve the homogeneous system.

(ii) Describe the intersection geometrically and as a span.

(iii) For parallel planes with right-hand sides $a,b,c$, find the condition for a common intersection.

> [!success]- Worked Solution
> **(i)** The coefficient matrix is
>
> 

$$
A=\begin{bmatrix}1&1&-1\\2&-1&1\\1&2&-2\end{bmatrix}.
$$


>
> The equations give $x=0$ and $y=z$, so $(x,y,z)=t(0,1,1)$.
>
> **(ii)** The three planes intersect along the line $\operatorname{span}\{(0,1,1)\}$.
>
> **(iii)** The third row is $\frac53$ times the first row minus $\frac13$ times the second row. Thus the right-hand sides must satisfy **$3c=5a-b$**.



### AY2023/2024 Semester 1 / Question 17 / Chapter 2 / Least Squares Solutions

#### Question

The quantities $x,y,z$ satisfy the constraints



$$
\begin{cases}x+2y=900\\y+z=600\\x-2z=300.\end{cases}
$$



(i) Show the system is inconsistent.

(ii) Find its least-squares solutions.

(iii) If $x,y,z$ must be positive integers, find the least-squares solution minimizing $x+y+z$.

> [!success]- Worked Solution
> **(i)** The augmented RREF has an inconsistent row:
>
> 

$$
\left[\begin{array}{ccc|c}1&0&-2&0\\0&1&1&0\\0&0&0&1\end{array}\right].
$$


>
> **(ii)** Let $A=\begin{bmatrix}1&2&0\\0&1&1\\1&0&-2\end{bmatrix}$ and $b=\begin{bmatrix}900\\600\\300\end{bmatrix}$. Solve $A^TAu=A^Tb$ to get
>
> 

$$
\begin{cases}x=200+2t\\y=400-t\\z=t.\end{cases}
$$


>
> **(iii)** Positivity requires $1\le t\le399$ for integer $t$. Since $x+y+z=600+2t$, choose $t=1$. **Answer:** $(202,399,1)$.


### AY2023/2024 Semester 2 / Question 17 / Chapter 2 / Least Squares Solutions

#### Question

Measurements $(X,Y)$ are $(2,10)$, $(3,16)$, $(4,25)$, $(5,36)$, and the model is $X^2+aX+b=Y$.

(i) Set up the linear system for $a,b$.

(ii) Find the least-squares best-fitting quadratic.

(iii) Find the shortest distance between the data vector and the column space of the coefficient matrix, to four decimals.

> [!success]- Worked Solution
> **(i)** Subtract $X^2$ from $Y$ to get $B=(6,7,9,11)$ and
>
> 

$$
A=\begin{bmatrix}2&1\\3&1\\4&1\\5&1\end{bmatrix}.
$$


>
> **(ii)** Solve $(A^TA)\begin{bmatrix}a\\b\end{bmatrix}=A^TB$. This gives $a=1.7$ and $b=2.3$, hence **$Y=X^2+1.7X+2.3$**.
>
> **(iii)** The residual is $B-A\begin{bmatrix}1.7\\2.3\end{bmatrix}=(0.3,-0.4,-0.1,0.2)$. Its Euclidean norm is **$\sqrt{0.3}=0.5477$**.



### AY2024/2025 Semester 1 / Question 17 / Chapter 2 / Projection and Linear Approximation

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


### AY2025/2026 Semester 1 / Question 17 / Chapter 2 / Projection and Linear Approximation

### Question

Let $P_1$ and $P_2$ be the planes
$$x+y-2z=0,\qquad 2x-y+z=0.$$

**(i)** Solve their simultaneous equations.

**(ii)** Express their line of intersection $L_1$ as a span.

**(iii)** Let $P_3:x+y+z=0$. Express $P_3$ as a span.

**(iv)** Project $L_1$ onto $P_3$ and express the projected line $L_2$ as a span.

> [!success]- Worked Solution
> **(i)** Gaussian elimination gives
> $$x=\frac t3,\qquad y=\f\frac{5t}{3},\qquad z=t.$$
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



# Chapter 3

### AY2022/2023 Semester 1 / LQ3 / Chapter 3 / Population Model

### Question

A car rental company operates at an airport, train terminal and downtown. Each week: 90% of airport cars return to the airport, 9% to the train terminal and 1% downtown; 90% of train-terminal cars return there, 9% to the airport and 1% downtown; 90% of downtown cars return downtown, 9% to the airport and 1% to the train terminal.

(a) Find the transition matrix $A$ for $\mathbf y_n=A\mathbf y_{n-1}$, where $\mathbf y_n=\begin{bmatrix}a_n\\t_n\\d_n\end{bmatrix}$.

(b) Find a matrix $P$ diagonalizing $A$ and the corresponding $D$.

(c) Find $\lim_{n\to\infty}A^n$.

(d) Determine the steady-state proportions at the three locations.

> [!success]- Worked Solution
> **(a)** Each column describes where cars from one starting location are returned:
>
> $$A=\begin{bmatrix}0.90&0.09&0.09\\0.09&0.90&0.01\\0.01&0.01&0.90\end{bmatrix}.$$
>
> **(b)** One valid diagonalization is
>
> $$P=\begin{bmatrix}-1&99/19&0\\1&91/19&-1\\0&1&1\end{bmatrix},\qquad D=\begin{bmatrix}81/100&0&0\\0&1&0\\0&0&89/100\end{bmatrix},$$
>
> where $A=PDP^{-1}$.
>
> **(c)** The other two eigenvalues have absolute value less than one, so
>
> $$\lim_{n\to\infty}D^n=\begin{bmatrix}0&0&0\\0&1&0\\0&0&0\end{bmatrix}.$$
>
> Therefore
>
> $$\boxed{\lim_{n\to\infty}A^n=\begin{bmatrix}9/19&9/19&9/19\\91/209&91/209&91/209\\1/11&1/11&1/11\end{bmatrix}.}$$
>
> **(d)** The long-run proportions are **airport $9/19$, train terminal $91/209$, downtown $1/11$**. They sum to one.


### AY2022/2023 Semester 2 / LQ3 / Chapter 3 / Population Model

### Question

Three telecommunications companies X, Y and Z exchange clients monthly. Of X's customers, 2% switch to Y and 4% to Z. Of Y's customers, 3% switch to X and 3% to Z. Of Z's customers, 4% switch to X and 2% to Y.

**(i)** Let $\mathbf v_n=\begin{bmatrix}x_n\\y_n\\z_n\end{bmatrix}$. Find $A$ such that $\mathbf v_{n+1}=A\mathbf v_n$.

**(ii)** Write $A^n=PD^nP^{-1}$, where $D$ is diagonal.

**(iii)** Does the market share stabilise? Find its long-run ratio.

**(iv)** Explain how the long-run market share is related to $A$.

> [!success]- Worked Solution
> **(i)** Retained proportions are 94% for each company. Incoming proportions give
>
> $$A=\begin{bmatrix}0.94&0.03&0.04\\0.02&0.94&0.02\\0.04&0.03&0.94\end{bmatrix}.$$
>
> **(ii)** A valid eigenvector matrix and diagonal matrix are
>
> $$P=\begin{bmatrix}-1&1&1\\0&2/3&-2\\1&1&1\end{bmatrix},\qquad D=\begin{bmatrix}9/10&0&0\\0&1&0\\0&0&23/25\end{bmatrix}.$$
>
> Therefore
>
> $$A^n=P\begin{bmatrix}(9/10)^n&0&0\\0&1&0\\0&0&(23/25)^n\end{bmatrix}P^{-1}.$$
>
> **(iii)** Since $(9/10)^n\to0$ and $(23/25)^n\to0$,
>
> $$\lim_{n\to\infty}A^n=\begin{bmatrix}3/8&3/8&3/8\\1/4&1/4&1/4\\3/8&3/8&3/8\end{bmatrix}.$$
>
> **Answer: Market shares stabilise at X:Y:Z = $3:2:3$.**
>
> **(iv)** The steady-state vector $\begin{bmatrix}3\\2\\3\end{bmatrix}$ is an eigenvector of $A$ for eigenvalue $1$.


### AY2023/2024 Semester 1 / Question 18 / Chapter 3 / Population Model

#### Question

Three video-streaming services A-flix, B-plus and C-prime share 63,000 subscribers. Monthly transfers: A-flix loses 4% to B-plus and 1% to C-prime; B-plus loses 6% to A-flix and 4% to C-prime; C-prime loses 4% to each of the other two.

(i) Find the transition matrix $A$ for $v_{n+1}=Av_n$.

(ii) Find the long-run limit of $A^n$.

(iii) Find initial subscriber numbers that remain unchanged each month.

(iv) Can the three services have equal long-run market shares?

> [!success]- Worked Solution
> **(i)** The columns are the monthly destination proportions:
>
> 

$$
A=\begin{bmatrix}0.95&0.06&0.04\\0.04&0.90&0.04\\0.01&0.04&0.92\end{bmatrix}.
$$


>
> **(ii)** The eigenvalues are $1$, $91/100$, and $43/50$. The non-unit modes vanish as $n$ increases. The limiting matrix is
>
> 

$$
\lim_{n\to\infty}A^n=\begin{bmatrix}\frac{32}{63}&\frac{32}{63}&\frac{32}{63}\\frac27&\frac27&\frac27\\frac{13}{63}&\frac{13}{63}&\frac{13}{63}\end{bmatrix}.
$$


>
> **(iii)** The steady vector is proportional to $(32,18,13)$. Since the sum is 63,000, **Answer:** $(32000,18000,13000)$.
>
> **(iv)** No. The long-run proportions are fixed at $32:18:13$, regardless of initial distribution.


### AY2023/2024 Semester 2 / Question 18 / Chapter 3 / Population Model

#### Question

Each year 15% of Town A moves to Town B and 10% of Town B moves to Town A.

(i) Find the transition matrix.

(ii) Express $A^n$ as $BCB^{-1}$ with diagonal $C$.

(iii) If both towns initially have 100,000 residents, find $a_n,b_n$.

(iv) Explain why the long-run population ratio is independent of the initial distribution.

> [!success]- Worked Solution
> **(i)** 

$$
A=\begin{bmatrix}0.85&0.10\\0.15&0.90\end{bmatrix}.
$$


>
> **(ii)** The eigenvalues are $1$ and $0.75$, with eigenvectors $(2,3)$ and $(1,-1)$. Set
>
> 

$$
B=\begin{bmatrix}2&1\\3&-1\end{bmatrix},\qquad C=\begin{bmatrix}1&0\\0&(0.75)^n\end{bmatrix},\qquad A^n=BCB^{-1}.
$$


>
> **(iii)** The initial vector $(100000,100000)$ is $40000(2,3)+20000(1,-1)$. Therefore
>
> 

$$
a_n=80000+20000(0.75)^n,\qquad b_n=120000-20000(0.75)^n.
$$


>
> **(iv)** The decaying mode vanishes, leaving the eigenvector $(2,3)$ and the fixed long-run ratio **$2:3$**.


### AY2024/2025 Semester 1 / Question 18 / Chapter 3 / Population Model

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
> \f\frac{6}{5}:1=\boxed{6:5}.$$


### AY2025/2026 Semester 1 / Question 18 / Chapter 3 / Population Model

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
> \f\frac{12000}{a_{2025}}=
> \f\frac{4}{3}.$$
> Therefore
> $$\boxed{a_{2025}=9000}.$$
>
> **(iii)** No. The dominant eigenvalue is $3/2>1$, so the populations grow by a factor approaching $1.5$ per year, although their ratio tends to $4:3$.



### AY2024/2025 Semester 2 / Question 18 / Chapter 3 / Market Share Model

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

# Chapter 4



# Chapter 4

### AY2022/2023 Semester 1 / LQ4 / Chapter 4 / Phase Plane

### Question

A particle follows the SDE

$$\mathbf y'=\begin{bmatrix}4&-5\\-2&1\end{bmatrix}\mathbf y.$$

(a) Find the general solution.

(b) Sketch the phase portrait, indicating the eigenvector axes and trajectory directions.

(c) Find the solution with $\mathbf y(0)=\begin{bmatrix}2.9\\2.6\end{bmatrix}$, giving fractions.

(d) Can a particle starting away from the origin move towards the origin? Justify.

> [!success]- Worked Solution
> **(a)** The characteristic equation is
>
> $$\det(A-rI)=(4-r)(1-r)-10=r^2-5r-6=(r+1)(r-6).$$
>
> Eigenvalues are $r_1=-1$ and $r_2=6$ with eigenvectors $\begin{bmatrix}1\\1\end{bmatrix}$ and $\begin{bmatrix}-5/2\\1\end{bmatrix}$. Thus
>
> $$\boxed{\mathbf y(t)=c_1e^{-t}\begin{bmatrix}1\\1\end{bmatrix}+c_2e^{6t}\begin{bmatrix}-5/2\\1\end{bmatrix}.}$$
>
> **(b)** One eigenvalue is negative and the other positive, so the origin is a **saddle**. Trajectories approach along the stable eigenvector and depart along the unstable eigenvector.
>
> ![[Attachments/AY2223_S1_LQ4_Phase_Portrait.png]]
>
> **(c)** At $t=0$,
>
> $$\begin{bmatrix}2.9\\2.6\end{bmatrix}=c_1\begin{bmatrix}1\\1\end{bmatrix}+c_2\begin{bmatrix}-5/2\\1\end{bmatrix}.$$
>
> Solving gives $c_1=94/35$ and $c_2=-3/35$. Therefore
>
> $$\boxed{\mathbf y(t)=\frac{94}{35}e^{-t}\begin{bmatrix}1\\1\end{bmatrix}-\frac{3}{35}e^{6t}\begin{bmatrix}-5/2\\1\end{bmatrix}.}$$
>
> **(d)** Yes. A nonzero starting point on the stable eigenvector line $y_2=y_1$ has $c_2=0$, so its trajectory decays as $e^{-t}$ towards the origin.


### AY2023/2024 Semester 2 / Question 19 / Chapter 4 / Phase Plane

#### Question

Consider the SDE



$$
y'=\begin{bmatrix}-1&4\\2&1\end{bmatrix}y.
$$



(i) Find a fundamental set of solutions.

(ii) Solve the IVP $y_1(0)=1$, $y_2(0)=0$.

(iii) Classify the equilibrium and its stability.

(iv) Sketch the phase portrait, indicating the IVP trajectory.

(v) Give a solution that approaches the equilibrium.

> [!success]- Worked Solution
> **(i)** The eigenvalues are $3$ and $-3$. Corresponding eigenvectors may be chosen as $(1,1)$ and $(-2,1)$. Thus
>
> 

$$
y^{(1)}=e^{3t}\begin{bmatrix}1\\1\end{bmatrix},\qquad y^{(2)}=e^{-3t}\begin{bmatrix}-2\\1\end{bmatrix}.
$$


>
> **(ii)** Let $y=c_1y^{(1)}+c_2y^{(2)}$. The initial condition yields $c_1-2c_2=1$, $c_1+c_2=0$, hence $c_1=1/3,c_2=-1/3$.
>
> 

$$
\boxed{y(t)=\frac13e^{3t}\begin{bmatrix}1\\1\end{bmatrix}-\frac13e^{-3t}\begin{bmatrix}-2\\1\end{bmatrix}}.
$$


>
> **(iii)** Opposite-sign eigenvalues give an **unstable saddle**.
>
> **(iv)** The stable eigendirection is $(-2,1)$ and the unstable direction is $(1,1)$. The IVP trajectory passes through $(1,0)$, approaching the unstable eigendirection as $t$ grows.

![[Attachments/S2_Q19_Solution_Phase_Portrait.png]]
>
> **(v)** One such solution is $e^{-3t}\begin{bmatrix}-2\\1\end{bmatrix}$.


### AY2024/2025 Semester 1 / Question 19 / Chapter 4 / Phase Plane

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
> \f\frac{\pi}{4}
> \r\right)=3\sqrt2e^{-\pi/4}\begin{bmatrix}1\\0\end{bmatrix}.$$
> Therefore the tangent vector is
> $$Ay=3\sqrt2e^{-\pi/4}\begin{bmatrix}0\\-2\end{bmatrix}.$$



### AY2023/2024 Semester 1 / Question 19 / Chapter 4 / Mixing Problem

#### Question

Two connected tanks initially contain 20 L of water with 50 g chlorine in Tank 1, and 10 L with 50 g chlorine in Tank 2. Pure water enters Tank 1 at 3 L/min. Use the flow rates in the accompanying tank diagram.

![[Attachments/S1_Q19_Tank_Diagram.png]]

(i) Set up the SDE for chlorine amounts $y_1(t),y_2(t)$.

(ii) Solve the initial value problem.

(iii) Sketch the trajectory corresponding to the IVP.

(iv) Can any choice of initial chlorine amounts leave chlorine in the tanks in the long run? Justify.

> [!success]- Worked Solution
> **(i)** From the flow rates in the official diagram,
>
> 

$$
\begin{cases}y_1'=-\frac6{20}y_1+\frac3{10}y_2\\y_2'=\frac4{20}y_1-\frac4{10}y_2.\end{cases}
$$


>
> Thus $A=\begin{bmatrix}-0.3&0.3\\0.2&-0.4\end{bmatrix}$ and $y(0)=\begin{bmatrix}50\\50\end{bmatrix}$.
>
> **(ii)** Diagonalize $A$ and use $y(t)=e^{At}y(0)$; the eigenvalues are $-0.1$ and $-0.6$, with corresponding eigenvectors $(3,2)$ and $(1,-1)$. Solving for coefficients gives
>
> 

$$
y(t)=20e^{-t/10}\begin{bmatrix}3\\2\end{bmatrix}-10e^{-3t/5}\begin{bmatrix}1\\-1\end{bmatrix}.
$$


>
> **(iii)** The trajectory starts at $(50,50)$ and moves towards the origin, becoming tangent to the slower-decaying eigendirection $(3,2)$.

![[Attachments/S1_Q19_Solution_Trajectory.png]]

**(iv)** No. Both eigenvalues are negative, so both exponential terms tend to zero for any finite initial chlorine amounts.



### AY2022/2023 Semester 2 / LQ4 / Chapter 4 / Damped Mass-Spring System

### Question

A damped mass-spring system satisfies $my''+cy'+ky=0$, with $m=4$ kg and $k=4$ N/m.

**(i)** Find $c$ for critical damping (return to equilibrium without oscillation).

**(ii)** Convert the ODE into a $2\times2$ SDE and find a fundamental set of solutions.

**(iii)** Sketch the phase portrait with trajectory directions.

**(iv)** Explain why a damped mass-spring system cannot have a saddle equilibrium for any damping constant.

> [!success]- Worked Solution
> **(i)** Critical damping requires $c^2=4mk=64$. For nonnegative damping, **$c=8$.**
>
> **(ii)** Put $y_1=y$, $y_2=y'$. Then
>
> $$\begin{bmatrix}y_1'\\y_2'\end{bmatrix}=\underbrace{\begin{bmatrix}0&1\\-1&-2\end{bmatrix}}_A\begin{bmatrix}y_1\\y_2\end{bmatrix}.$$
>
> The characteristic polynomial is $(\lambda+1)^2$. An eigenvector is $\begin{bmatrix}-1\\1\end{bmatrix}$ and a generalised eigenvector is $\begin{bmatrix}-1\\0\end{bmatrix}$. Hence a fundamental set is
>
> $$\mathbf y^{(1)}=e^{-t}\begin{bmatrix}-1\\1\end{bmatrix},\qquad \mathbf y^{(2)}=e^{-t}\begin{bmatrix}-t-1\\t\end{bmatrix}.$$
>
> **(iii)** The origin is an asymptotically stable **degenerate node**. The phase portrait is sketched below; trajectories point inward toward the origin and are tangent to the eigendirection.
>
> ![[Attachments/AY2223_S2_LQ4_Phase_Portrait.png]]
>
> **(iv)** For the general system the characteristic polynomial is $\lambda^2+(c/m)\lambda+k/m$. The product of eigenvalues is $k/m>0$, whereas a saddle requires real eigenvalues of opposite signs, whose product would be negative. Thus **a saddle is impossible**.


### AY2024/2025 Semester 2 / Question 17 / Chapter 4 / Damped Mass-Spring System

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


### AY2025/2026 Semester 1 / Question 19 / Chapter 4 / Damped Mass-Spring System

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
> \f\frac{1}{2}c_2e^{-t/2},$$
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



### AY2024/2025 Semester 2 / Question 19 / Chapter 4 / Solutions and Mixing Problem

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

