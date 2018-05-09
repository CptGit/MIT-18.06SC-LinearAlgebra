Unit I: $A\boldsymbol{x} = \boldsymbol{b}$ and the Four Subspaces
=============

Session 1.1: The Geometry of Linear Equations
----------------

<!--more-->

We have a system of equations:
$$
\left\{
\begin{aligned}
2x - y &= 0 \\
-x + 2y &= 3
\end{aligned}
\right .
$$

### Row Picture

Line $2x - y = 0$ and line $-x + 2y = 0$ intersects at the point $(1, 2)$, so $(1, 2)$ is the solution of the system of equations.

> Maybe I should draw a X-Y coordinates here \>\_\>

### Column Picture

We rewrite the system of linear equations as a single equation:

$$
x\begin{bmatrix}2 \\ -1\end{bmatrix} + y\begin{bmatrix}-1 \\ 2\end{bmatrix} = \begin{bmatrix}0 \\ 3\end{bmatrix}
$$

We see $x$ and $y$ as scalars of column vectors: $\boldsymbol{v_1} = \begin{bmatrix}2 \\ -1\end{bmatrix}$ and $\boldsymbol{v_2} = \begin{bmatrix}-1 \\ 2\end{bmatrix}$, and the sum $x\boldsymbol{v_1} + y\boldsymbol{v_2}$ is called a *linear combination* of $\boldsymbol{v_1}$ and $\boldsymbol{v_2}$.

Geometrically, we can find one copy of $\boldsymbol{v_1}$ added to two copies of $\boldsymbol{v_2}$ just equals the vector $\begin{bmatrix}0 \\ 3\end{bmatrix}$. Then the solution should be $x = 1, y =2$.

> I will add a figure when time is available \>\_\>

### Matrix Picture

We rewrite the equations in our example as a compact form,

$$
A\boldsymbol{x} = \boldsymbol{b},
$$

that is

$$
\begin{bmatrix}2 & -1 \\ -1 & 2\end{bmatrix}\begin{bmatrix}x \\ y\end{bmatrix} = \begin{bmatrix}0 \\ 3\end{bmatrix}
$$

### Matrix Multiplication

$$
\begin{aligned}
\begin{bmatrix}2 & -1 \\ -1 & 2\end{bmatrix} \begin{bmatrix}1 \\ 2\end{bmatrix} = 1\begin{bmatrix}2 \\ -1\end{bmatrix} + 2\begin{bmatrix}-1 \\ 2\end{bmatrix} = \begin{bmatrix}0 \\ 3\end{bmatrix}
\end{aligned}
$$

A matrix times by a vector is just **a linear combination of the column vectors of the matrix**.

------------------------

Session 1.2: An Overview of Key Ideas
------------------

### Vectors
Let us take linear combinations of vectors.

### Matrices
The product of a matrix and a vector is
a combination of the columns of the matrix. 

### Subspaces
All combinations of column vectors creates a subspace.
The subspaces of $\mathbb{R}^3$ are:

- the origin,
- a line through the origin,
- a plane through the origin,
- all of $\mathbb{R}^3$.


### Conclusion
- $A$ is invertible

    $\Leftrightarrow$ $A\boldsymbol{x} = \boldsymbol{b}$ has the unique solution $\boldsymbol{x}$ for each $\boldsymbol{b}$

    $\Leftrightarrow$ $A\boldsymbol{x} = \boldsymbol{0}$ has no non-zero solution $\boldsymbol{x}$

    $\Leftrightarrow$ The columns of $A$ are *independent*

    $\Leftrightarrow$ All vectors $A\boldsymbol{x}$ cover the whole vector space

    Example: $A = \begin{bmatrix}1 & 0 & 0 \\ -1 & 1 & 0 \\ 0 & -1 & 1\end{bmatrix}$

- $A$ is not invertible

    $\Leftrightarrow$ $A\boldsymbol{x} = \boldsymbol{b}$ has a solution $\boldsymbol{x}$ only for some of $\boldsymbol{b}$ in the vector space

    $\Leftrightarrow$ $A\boldsymbol{x} = \boldsymbol{0}$ has non-zero solutions $\boldsymbol{x}$

    $\Leftrightarrow$ The columns of $A$ are *dependent*

    $\Leftrightarrow$ All vectors $A\boldsymbol{x}$ lies in only a subspace of the vector space

    Example: $A = \begin{bmatrix}1 & 0 & -1 \\ -1 & 1 & 0 \\ 0 & -1 & 1\end{bmatrix}$

------------------

Session 1.3: Elimination with Matrices
--------------

### Method of Elimination

We have an example $A\boldsymbol{x} = \boldsymbol{b}$,

$A = \begin{bmatrix}1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1\end{bmatrix}$ and $\boldsymbol{b} = \begin{bmatrix}2 \\ 12 \\2\end{bmatrix}$.

Steps of Elimination:

- Step 1: subtract $3$ times row 1 from row 2;
- Step 2: subtract $2$ times row 2 from row 3.

$$
A = \begin{bmatrix}1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1\end{bmatrix}
\rightarrow \begin{bmatrix}1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1\end{bmatrix}
\rightarrow U = \begin{bmatrix}1 & 2 & 1 \\ 0 & 1 & -2 \\ 0 & 0 & 5\end{bmatrix}
$$

$$
\boldsymbol{b} = \begin{bmatrix}2 \\ 12 \\ 2\end{bmatrix}
\rightarrow \cdots \rightarrow \begin{bmatrix}2 \\ 6 \\ -10\end{bmatrix}
$$

Thus, we can easily solve the systems of equations, $\begin{bmatrix}x \\ y  \\ z\end{bmatrix} = \begin{bmatrix}2 \\ 1  \\ -2\end{bmatrix}$.

### Elimination Matrices

The product of a matrix (3x3) and a column vector (3x1) is a column vector
(3x1) that is a linear combination of the columns of the matrix.

The product of a row vector (1x3) and a matrix (3x3) is a row vector (1x3) that is a linear
combination of the rows of the matrix.

For example,

$$
\begin{bmatrix}1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}
\begin{bmatrix}1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1\end{bmatrix}
= \begin{bmatrix}1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1\end{bmatrix}.
$$

Multiplying on the left by a permutation matrix exchanges the rows of a matrix, while multiplying on the right exchanges the columns. For example,

$$
P = \begin{bmatrix}0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1\end{bmatrix}.
$$

$P$ is a *permutation matrix* and the first and second rows of the matrix $PA$ are the second and first rows of the matrix $A$.

Note, matrix multiplication is *associative* but *not commutative*.

### Inverses
We have a matrix:

$$
E_{21} = \begin{bmatrix}1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}
$$

which subtracts $3$ times row 1 from row 2. To "**undo**" this operation we must add $3$ times row 1 to row 2 using the inverse matrix:

$$
E_{21}^{-1} = \begin{bmatrix}1 & 0 & 0 \\ 3 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}.
$$

In fact, $E_{21}^{-1}E_{21} = I$.

-------------------

Session 1.4: Multiplication and Inverse Matrices
------------------

### Four and a half ways we see matrix multiplication

We have $AB = C$. $A$ is an $m \times n$ matrix and $B$ is an $n \times p$ matrix, then $C$ is an $m \times p$ matrix. We use $c_{ij}$ to denote the entry in row $i$ and column $j$ of matrix $C$ and the same denotation applies to $a_{ij}$ and $b_{ij}$.

#### Row times column 

$c_{ij} = \sum_{k=1}^n a_{ik}b_{kj}$

#### Columns

The product of matrix $A$ and column $j$ of matrix $B$ equals column $j$ of matrix $C$. This tells us that the columns of $C$ are combinations of columns of $A$.

$$
A
\begin{bmatrix}
| & | & | \\
column 1 & column 2 & column 3 \\
| & | & |
\end{bmatrix}
=\begin{bmatrix}
| & | & | \\
A(column 1) & A(column 2) & A(column 3) \\
| & | & |
\end{bmatrix}
$$

#### Rows
The product of row $i$ of matrix $A$ and matrix $B$ equals row $i$ of matrix $C$. So the rows of $C$ are combinations of rows of $B$. 

$$
\left[
\begin{matrix}
--- & row 1 & --- \\
--- & row 2 & --- \\
--- & row 3 & ---
\end{matrix}
\right]
B
=\left[
\begin{matrix}
--- & (row 1)B & --- \\
--- & (row 2)B & --- \\
--- & (row 3)B & ---
\end{matrix}
\right]
$$

#### Column times row

$$
AB = \sum_{k=1}{n}
\begin{bmatrix}a_{1k} \\ \vdots \\ a_{mk}\end{bmatrix}
\begin{bmatrix}b_{k1} & \cdots & b_{kp}\end{bmatrix}
$$

>note: Here I fixed a typo in the [lecture summary (PDf)](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/ax-b-and-the-four-subspaces/multiplication-and-inverse-matrices/MIT18_06SCF11_Ses1.3sum.pdf) of this session: $b_{kp}$ instead of the original $b_{kn}$.

#### Blocks

$$
\begin{bmatrix}A_1 & A_2 \\ A_3 & A_4 \end{bmatrix}
\begin{bmatrix}B_1 & B_2 \\ B_3 & B_4 \end{bmatrix}
=\begin{bmatrix}
A_1B_1+A_2B_3 & A_1B_2+A_2B_4 \\
A_3B_1+A_4B_3 & A_3B_2+A_4B_4
\end{bmatrix}
$$

### Inverses

If $A$ is *singular* or *not invertible*,

then A does not have an inverse,

and we can find some non-zero vector $\boldsymbol{x}$ for which $A\boldsymbol{x} = \boldsymbol{0}$

#### Gauss-Jordan Elimination

$$
E
\left[
\begin{array}{c|c}
A & I
\end{array}
\right]
=\left[
\begin{array}{c|c}
I & E
\end{array}
\right]
$$
If $EA = I$, then $E = A^{-1}$.

----------------------

Session 1.5: Factorization into $A = LU$
------------

### Inverse of a product

$$(AB)^{-1} = B^{-1}A^{-1}$$

### Transpose of a product

$$(AB)^{T} = B^{T}A^{T}, \quad (A^{T})^{-1} = (A^{-1})^{T}$$

### $A = LU$

We can use elimination to convert $A$ into an upper triangular matrix $U$, that is $EA = U$, and further we can also convert this to a factorization $A = LU$ in which $L = E^{-1}$.

For example, in a three dimensional case, if $E_{32}E_{31}E_{21}A = U$ then $A=E_{21}^{-1}E_{31}^{-1}E_{32}^{-1}U = LU$. Suppose $E_{31}$ is the identity matrix and $E_{32}$ and $E_{21}$ are as shown below:

$$
\begin{array}{cccc}
E_{32} & E_{21} & & E \\
\begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -5 & 1\end{bmatrix}
& \begin{bmatrix}1 & 0 & 0 \\ -2 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}
& = & \begin{bmatrix}1 & 0 & 0 \\ -2 & 1 & 0 \\ 10 & -5 & 1\end{bmatrix}
\end{array}.
$$

Here $L = E^{-1} = E_{21}^{-1}E_{32}^{-1}$:

$$
\begin{array}{cccc}
E_{21}^{-1} & E_{32}^{-1} & & L \\
\begin{bmatrix}1 & 0 & 0 \\ \underline{2} & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}
& \begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & \underline{5} & 1\end{bmatrix}
& = & \begin{bmatrix}1 & 0 & 0 \\ \underline{2} & 1 & 0 \\ 0 & \underline{5} & 1\end{bmatrix}
\end{array}
$$

Notice the 0 in row three column one of $L$, where $E$ had a $10$. The factorization $A = LU$ is preferable to the statement $EA = U$ because the combination of row subtractions does not have the effect on $L$ that it did on $E$.

**If there are no row exchanges, the multipliers from the elimination matrices are copied directly into $L$.**

### Cost of elimination

If we define a typical operation is to multiply one row and then subtract it from another, then the total number of operations needed to factor $n \times n$ $A$ into $LU$ is on the order of $n^3$:

$$1^2 + 2^2 + \cdots + (n - 1)^2 + n^2 = \sum_{i = 1}^{n}i^2 \approx \int_0^n x\,\mathrm{d}x = \frac{1}{3}n^3.$$

While we’re factoring $A$ we’re also operating on $\boldsymbol{b}$. That costs about $n^2$ operations, which is hardly worth counting compared to $1/3n^3$. 

### Row exchanges

The inverse of any permutation matrix $P$ is $P^{-1} = P^{T}$.

There are $n!$ different ways to permute the rows of an $n \times n$ matrix (including the permutation that leaves all rows unfixed) so there are $n!$ permutation matrices. These matrices form a *multiplicative group*.

-----------------

Session 1.6: Transpose, Permutation, Vector Spaces $\mathbb{R}^n$
----------------

### Permutations

>Nothing new here.

### Transposes

$$(A^\mathrm{T})_{ij} = A_{ji}$$

Given any matrix $R$ the product $R^\mathrm{T}R$ is always *symmetric*, which means the transpose of a matrix equals itself, because $(R^\mathrm{T}R)^\mathrm{T} = R^\mathrm{T}(R^\mathrm{T})^\mathrm{T} = R^\mathrm{T}R$.

### Vector spaces

#### Closure

A collection of vectors has to satisfy two conditions:

1. closed under addition, which means the sum of any two vectors in the collection lies again in the collection,

2. closed under multiplication by any real numbers, that is to say that multiplying any vector in the collection by any real number will not give a vector beyond the collection,

or, to put it in another way, closed under linear combinations.

s.t. we call the collection a *vector space*.

#### Subspaces
A vector space that is contained inside of another vector space is called a *subspace* of that space. For example,

the subspaces of $\mathbb{R}^2$ are:

1. all of $\mathbb{R}^2$,

2. any line through the zero vector and

3. the zero vector alone.

**Every subspace must contain the zero vector.**

#### Column space

Given a matrix $A$, all the linear combinations of the columns of $A$ form a subspace. This is the *column space* $C(A)$.

For example, if $A = \begin{bmatrix}1 & 3 \\ 2 & 3 \\ 4 & 1\end{bmatrix}$, the column space of $A$ is the plane through the origin in $\mathbb{R}^3$ containing $\begin{bmatrix}1 \\ 2 \\ 4\end{bmatrix}$ and $\begin{bmatrix}3 \\ 3 \\ 1\end{bmatrix}$.

-----------------

Session 1.7: Column Space and Nullspace
--------------

>A typo in both [Problems (PDF)](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/ax-b-and-the-four-subspaces/column-space-and-nullspace/MIT18_06SCF11_Ses1.6prob.pdf) and [Solutions (PDF)](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/ax-b-and-the-four-subspaces/column-space-and-nullspace/MIT18_06SCF11_Ses1.6sol.pdf) of this session:
>
>>Problem 6.2: $x - 3y - x = 0$ should be $x -3y - z = 0$.

### Review of subspaces

The union of two subspaces is generally not a subspace, but the intersection of two subspaces is a subspace.

### Column space of $A$ and solving $A\boldsymbol{x} = \boldsymbol{b}$

Given a matrix $A$, the system of linear equations $A\boldsymbol{x} = \boldsymbol{b}$ is solvable exactly when $\boldsymbol{b}$ is a vector in the *column space* of $A$.

### Nullspace of $A$

The *nullspace* of a matrix $A$ is the collection $x$ to the equation $A\boldsymbol{x} = \boldsymbol{0}$.

For example,

$$
\begin{bmatrix}1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5\end{bmatrix}\begin{bmatrix}x_1 \\ x_2 \\ x_3\end{bmatrix} = \begin{bmatrix}0 \\ 0 \\ 0 \\ 0\end{bmatrix},
$$

the nullspace $N(A)$ consists of all multiples of $\begin{bmatrix}1 \\ 1 \\ -1\end{bmatrix}$. This nullspace is a line in $\mathbb{R}^3$.

Attention, a nullspace is a vector space because it obviously satisfies the requirements about addition and scale multiplication. That is to say that any sum or multiple of solutions of $A\boldsymbol{x} = \boldsymbol{0}$ is also a solution: $A(\boldsymbol{x}_1 + \boldsymbol{x}_2) = \boldsymbol{0} + \boldsymbol{0} = \boldsymbol{0}$ and $A(c\boldsymbol{x}) = cA\boldsymbol{x} = c\boldsymbol{0} = \boldsymbol{0}$.

#### Other values of $\boldsymbol{b}$

The solutions to the equation:

$$
\begin{bmatrix}1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5\end{bmatrix}\begin{bmatrix}x_1 \\ x_2 \\ x_3\end{bmatrix} = \begin{bmatrix}1 \\ 2 \\ 3 \\ 4\end{bmatrix},
$$

do not form a subspace. This conclusion is obvious since the zero vector is not a solution to the equation. Actually, the set of solutions forms a line in $\mathbb{R}^3$ that pass through the points $\begin{bmatrix}1 \\ 0 \\ 0\end{bmatrix}$ and $\begin{bmatrix}0 \\ -1 \\ 1\end{bmatrix}$, but not $\begin{bmatrix}0 \\ 0 \\ 0\end{bmatrix}$.

-----------------

Session 1.8:  Solving $A\boldsymbol{x} = \boldsymbol{0}$: Pivot Variables, Special Solutions
----------------

>A typo in [Solutions (PDF)](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/ax-b-and-the-four-subspaces/solving-ax-0-pivot-variables-special-solutions/MIT18_06SCF11_Ses1.7sol.pdf) of this session:
>
>>Problem 7.1: $- 23/4$ in rref of $A$ should be $23/4$, and $23/4$ in the solution $\boldsymbol{x}$ should be $-23/4$.

### Computing the nullspace

Just like the way we eliminate the invertible square matrix, we can do the same thing for any matrix $A$.

Suppose:
$$
A = \begin{bmatrix}
1 & 2 & 2 & 2 \\
2 & 4 & 6 & 8\\
3 & 6 & 8 & 10
\end{bmatrix}.
$$

The elimination gives us:

$$
A = \begin{bmatrix}
1 & 2 & 2 & 2 \\
2 & 4 & 6 & 8 \\
3 & 6 & 8 & 10
\end{bmatrix}
\rightarrow
\begin{bmatrix}
1 & 2 & 2 & 2 \\
0 & 0 & 2 & 4 \\
0 & 0 & 2 & 4
\end{bmatrix}
\rightarrow
\begin{bmatrix}
1 & 2 & 2 & 2 \\
0 & 0 & 2 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix}
= U
$$

We call U in *echelon* form. The *rank* of a matrix $A$ is the number of pivots it has. In this example, the rank of $A$ is $2$.

### Special solutions

We can use back-substitution to find the solution $\boldsymbol{x}$ to the equation $U\boldsymbol{x} = \boldsymbol{0}$. In the example, column 1 and 3 are *pivot columns*, column 2 and 4 are *free columns*. We can assign any value to $x_2$ and $x_4$; we call them *free variables*. Yes, $x_1$ and $x_3$ are *pivot variables*.

Suppose $x_2 = 1$ and $x_4 = 0$, then: $x_3 = 0$ and $x_1 = -2$. So that gives us one solution $\boldsymbol{x} = \begin{bmatrix}-2 \\ 1 \\ 0 \\ 0\end{bmatrix}$. Similarly, if $x_2 = 0$ and $x_4 = 1$, then we'll get another solution $\boldsymbol{x} = \begin{bmatrix}2 \\ 0 \\ -2 \\ 1\end{bmatrix}$. **The nullspace of $A$ is the collection of all linear combinations of these "special solution" vectors.**

A fact we should note is that the *rank* of $A$ equals the number of pivot columns, so the number of free columns is the number of columns minus the number of pivot columns, which is also the number of special solution vectors and the dimension of the nullspace.

### Reduced row echelon form

*Reduced row echelon form* (rref form) means pivots equal to 1 and zeros above and below the pivots. Eliminating U gives us a rref form matrix $R$:

$$
U = \begin{bmatrix}
1 & 2 & 2 & 2 \\
0 & 0 & 2 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix}
\rightarrow
\begin{bmatrix}
1 & 2 & 0 & -2 \\
0 & 0 & 2 & 4 \\
0 & 0 & 0 & 0
\end{bmatrix}
\rightarrow
\begin{bmatrix}
1 & 2 & 0 & -2 \\
0 & 0 & 1 & 2 \\
0 & 0 & 0 & 0
\end{bmatrix}
= R.
$$
Generally, $R$ can be rewritten with  a copy of the identity matrix in the upper left corner and some free columns on the right, possibly followed by the lower rows filled with zeros:
$$
R = \begin{bmatrix}
I & F \\
\boldsymbol{0} & \boldsymbol{0}
\end{bmatrix}.
$$

Here $I$ is an $r \times r$ square matrix and $F$ is an $r \times (n - r)$ matrix.

And we can find the nullspace matrix $N = \begin{bmatrix}-F \\ I\end{bmatrix}$ s.t. $RN = \boldsymbol{0}$. Here $I$ is an $(n - r) \times (n - r)$ square matrix and $F$ is an $r \times (n - r)$ matrix. The columns of $N$ are the special solutions.

--------------------

Session 1.9: Solving $A\boldsymbol{x} = \boldsymbol{b}$: Reduced Row Form R
---------------

### Solvability conditions on $\boldsymbol{b}$

We again the example in the example in the previous session:
$$
A = \begin{bmatrix}
1 & 2 & 2 & 2\\
2 & 4 & 6 & 8\\
3 & 6 & 8 & 10
\end{bmatrix}.
$$
Using Gauss-Jordan elimination:
$$
\left[
\begin{array}{c|c}
\begin{matrix}
1 & 2 & 2 & 2\\
2 & 4 & 6 & 2\\
3 & 6 & 8 &10
\end{matrix}
&
\begin{matrix}
b_1 \\ b_2 \\ b_3
\end{matrix}
\end{array}
\right]
\rightarrow\cdots\rightarrow
\left[
\begin{array}{c|l}
\begin{matrix}
1 & 2 & 2 & 2\\
0 & 0 & 2 & 4 \\
0 & 0 & 0 & 0
\end{matrix}
&
\begin{array}{l}
b_1 \\ b_2 - 2b_1 \\ b_3-b_2-b_1
\end{array}
\end{array}
\right].
$$
In our example, row 3 of $A$ is completely eliminated. So if $A\boldsymbol{x} = \boldsymbol{b}$ has a solution, then $b_3 - b_2 - b_1 = 0$.

From an earlier lecture, we know that $A\boldsymbol{x} = \boldsymbol{b}$ is solvable exactly when $\boldsymbol{b}$ is in the column space $C(A)$. In fact this condition is equivalent with $b_3 - b_2 - b_1 = 0$ here.

### Computing solution

The complete solution is a particular solution plus all the vectors in the nullspace. That is $\boldsymbol{x}_{complete} = \boldsymbol{x}_p + \boldsymbol{x}_n$, where $\boldsymbol{x}_p$ is a particular solution and $\boldsymbol{x}_n$ is a generic vector in the nullspace. To see this, we add $A\boldsymbol{x}_p = \boldsymbol{b}$ to $A\boldsymbol{x}_n = 0$ and get $A(\boldsymbol{x}_p + \boldsymbol{x}_n) = \boldsymbol{b}$ for every vector $\boldsymbol{x}_n$ in the nullspace.

#### A particular solution

For our matrix $A$, we choose $\boldsymbol{b} = \begin{bmatrix}1 \\ 5 \\ 6\end{bmatrix}$, then we get a particular solution $\boldsymbol{x} = \begin{bmatrix}-2 \\ 0 \\ 3/2 \\ 0\end{bmatrix}$ when we let all free variables $x_2$ and $x_4$ equal $0$. (We would get another particular solution when assigning different $x_2$ or $x_4$. This will not affect the complete solution.)

#### Combined with nullspace

From last lecture we learned that the nullspace of $A$ is the collection of all combinations of the special solutions $\begin{bmatrix}-2 \\ 1 \\ 0 \\ 0\end{bmatrix}$ and $\begin{bmatrix}2 \\ 0 \\ -2 \\ 1\end{bmatrix}$. Adding our particular solution to the vectors in the nullspace, we get the complete solution to the equation $A\boldsymbol{x} = \begin{bmatrix}1 \\ 5 \\6\end{bmatrix}$ is:
$$
\boldsymbol{x}_{complete} = \begin{bmatrix}-2 \\ 0 \\ 3/2 \\ 0\end{bmatrix} + c_1 \begin{bmatrix}-2 \\ 1 \\ 0 \\ 0\end{bmatrix} + c_2 \begin{bmatrix}-2 \\ 0 \\ -2 \\ 1\end{bmatrix},
$$
where $c_1$ and $c_2$ are any real numbers.

>A typo in the [lecture summary (PDF)](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/ax-b-and-the-four-subspaces/solving-ax-b-row-reduced-form-r/MIT18_06SCF11_Ses1.8sum.pdf) of this session:
>
>>$c_1$ is missing here...

The nullspace is a two dimensional subspace of $\mathbb{R}^4$, and the complete solution form a plane parallel to that through $\boldsymbol{x}_p = \begin{bmatrix}-2 \\ 0 \\ 3/2 \\ 0\end{bmatrix}$.

### Rank

The rank of a matrix equals the number of pivots of that matrix. If $A$ is an $m$ by $n$ matrix of rank $r$, we know $r \le m$ and $r \le n$. Actually the rank tells us all the information about solutions to the equation $A\boldsymbol{x} = \boldsymbol{b}$.

$$
\begin{array}{|c|c|c|c|c|}
\hline
& r = m = n & r = n < m & r = m < n & r < m, r < n \\
\hline
R & I & \begin{bmatrix}I \\ \boldsymbol{0}\end{bmatrix} & \begin{bmatrix}I & F\end{bmatrix} & \begin{bmatrix}I & F \\ \boldsymbol{0} & \boldsymbol{0}\end{bmatrix} \\
\hline
\text{Solutions to }A\boldsymbol{x} = \boldsymbol{b} & 1 & 0\text{ or }1 & \infty & 0\text{ or }\infty \\
\hline
\end{array}
$$

------------

Session 1.10: Independence, Basis and dimension
----------

### Linear Independence

$\sum_i c_i\boldsymbol{x}_i = \boldsymbol{0}$ only when $c_1, c_2, \dots, c_n$ are all $0$.

$\Leftrightarrow$ The only solution to $A\boldsymbol{x} = \boldsymbol{0}$ is $\boldsymbol{x} = \boldsymbol{0}$, which means that the nullspace of $A$ contains only the zero vector.

$\Leftrightarrow$ The rank of $A$ is $n$ so there are no free variables.

### Spanning a space

Vectors $\boldsymbol{v}_1, \boldsymbol{v}_2, \dots, \boldsymbol{v}_k$ *span* a space when the space consists of all combinations of those vectors. The space spanned is also the smallest space containing those vectors.

### Basis and dimension

A *basis* for a vector space is a sequence of vectors $\boldsymbol{v}_1, \boldsymbol{v}_2, \dots, \boldsymbol{v}_d$ with two properties:

- $\boldsymbol{v}_1, \boldsymbol{v}_2, \dots, \boldsymbol{v}_d$ are independent;
- $\boldsymbol{v}_1, \boldsymbol{v}_2, \dots, \boldsymbol{v}_d$ span the vector space.

The number of vectors in a basis for a vector space is the *dimension* of the space. There are exactly $n$ vectors in every basis for $\mathbb{R}^n$.

### Basis of a column space and nullspace

$$\text{dimension of }C(A)  = \text{number of pivot columns of }A = \text{rank}(A)$$

$$\text{dimension of }N(A)  = \text{number of free variables of }A = \text{number of columns of }A - \text{rank}(A)$$

-------------

Session 1.11: The Four Fundamental Subspaces
----------

### Four subspaces and their basis and dimension

Any $m$ by $n$ matrix $A$ determines four subspaces (possibly containing only the zero vector):

#### Column space $C(A)$

All combinations of the columns of $A$

A subspace of $\mathbb{R}^m$

The $r$ pivot columns form a basis

$\text{dim }C(A) = r$

#### Nullspace $N(A)$

All solutions $\boldsymbol{x}$ of the equation $A\boldsymbol{x} = \boldsymbol{0}$

A subspace of $\mathbb{R}^n$

The $n - r$ special solutions from a basis

$\text{dim }N(A) = n - r$

#### Row space $C(A^\mathrm{T})$

All combinations of the rows of  $A$

A subspace of $\mathbb{R}^n$

The  first $r$ rows of  $R$ (the reduced row echelon form of $A$) form a basis

$\text{dim }C(A^\mathrm{T}) = r$

#### Left nullspace $N(A^\mathrm{T})$

All solutions $\boldsymbol{y}$ of the equation $\boldsymbol{y}^\mathrm{T}A = \boldsymbol{0}$

A subspace of $\mathbb{R}^m$

The bottom $m - r$ of $E$ form a basis

$\text{dim }N(A^\mathrm{T}) = m - r$

##### how to find a basis for $N(A^\mathrm{T})$

First we get $E$ through Gauss-Jordan elimination:
$$
E_{m \times n} \left[
\begin{array}{c|c}A_{m \times n} & I_{m \times n}\end{array}
\right]
=\left[
\begin{array}{c|c}R_{m \times n} & E_{m \times n}\end{array}
\right]
$$
Then the bottom $m - r$ rows of $E$ describe linear dependencies of rows of $A$ since the bottom $m - r$ rows of $R$ are zero. For example:
$$
EA = \begin{bmatrix}
-1 & 2 & 0 \\
1 & -1 & 0 \\
1 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 2 & 3 & 1 \\
1 & 1 & 2 & 1 \\
1 & 2 &3 & 1
\end{bmatrix}
= \begin{bmatrix}
1 & 0 & 1 & 1 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix} = R
$$
In this example, The last row of $E$ satisfy the equation $\boldsymbol{y}^\mathrm{T}A = \boldsymbol{0}$ and thus form a basis for the left nullspace of $A$.

### New vector space

We put all $3$ by $3$ matrices together and see the  collection as a new vector space; we call it M.

Some subspace of $M$ include:

- all upper triangular matrices
- all symmetric matrices
- $D$, all diagonal matrices

$D$ is the intersection of the first two space. It also has a dimension of $3$ and a basis for $D$ is:
$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix},
\begin{bmatrix}
1 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 0
\end{bmatrix},
\begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 7
\end{bmatrix}.
$$

-----------------

Session 1.12: Matrix Spaces; Rank one; Small World Graphs
------

### New vector spaces

#### $3$ by $3$ matrices

We identified $M$, the space of all $3$ by $3$ matrices; S, the space of all symmetric $3$ by $3$ matrices; U, the space of all upper triangular $3$ by $3$ matrices and D, the space of all diagonal $3$ by $3$ matrices.

The dimension of $M$ is $9$. A good choice of basis is:
$$
\begin{bmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\dots,
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 1 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1\end{bmatrix}.
$$
The dimension of $S$ is 6 and one basis is:
$$
\begin{bmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 1 \\ 0 & 0 & 0 \\ 1 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 1 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1\end{bmatrix}.
$$
The dimension of $U$ is also 6 and a basis for $U$ is:
$$
\begin{bmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1\end{bmatrix}.
$$
The subspace $D = S  \cap U$ has dimension 3. A good basis is:
$$
\begin{bmatrix}1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{bmatrix},
\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1\end{bmatrix}.
$$
$S \cup U$ is NOT a subspace of $M$. However, $S + U$, which means all possible sums of elements of $S$ and elements of $U$, is a subspace of $M$. In fact, the subspace is just $M$ itself. We can find that dimensions follow this rule:
$$
\text{dim }S + \text{dim }U = \text{dim }(S + U) + \text{dim }(S \cap U).
$$

> A typo in the [lecture summary (PDF)](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/ax-b-and-the-four-subspaces/matrix-spaces-rank-1-small-world-graphs/MIT18_06SCF11_Ses1.11sum.pdf) of this session:
>
> > $S \cup U$ should be $S + U$ in the equation about dimensions.

#### Differential equations

We can think of the solutions $y$ to $\dfrac{\mathrm{d}^2y}{\mathrm{d}x^2} + y = 0$ as the elements of a nullspace.

The complete solution is:
$$
y = c_1\cos x + c_2\sin x,
$$
where $c_1$ and $c_2$ can be any complex numbers. The solution space is a two dimensional vector space with basis vectors $\cos x$ and $\sin x$.

#### Rank $4$ matrices

Now let $M$ be the space of $5$ by $17$ matrices. The subspace of $M$ containing all rank $4$ matrices is not a subspace, even if we include the zero matrix, because the sum of two rank $4$ matrices may not have rank $4$.

In $\mathbb{R}^4$, the set of all vectors $\boldsymbol{v} = \begin{bmatrix}v_1 \\ v_2 \\ v_3 \\ v_4\end{bmatrix}$for $v_1 + v_2 + v_3 + v_4 = 0$ is a subspace. Actually, the space is the  nullspace of the matrix $\begin{bmatrix}1 & 1 & 1 & 1\end{bmatrix}$, so the dimension is $n - r  = 3$.

### Rank one matrices

$$
A = \begin{bmatrix}1 & 4 & 5 \\ 2 & 8 & 10\end{bmatrix} = \begin{bmatrix}1 \\ 2\end{bmatrix}\begin{bmatrix}1 & 4 & 5\end{bmatrix}.
$$

A has rank $1$ because each of its columns is a multiple of the first column.

Every rank 1 matrix $A$ can be written $A = \boldsymbol{u}\boldsymbol{v}^\mathrm{T}$, where $\boldsymbol{u}$ and $\boldsymbol{v}$ are column vectors. We can use rank $1 matrices as building blocks for more complex matrices.

### Small world graphs

A *graph* $G$ is a collection of nodes joined by edges:
$$
G = \{\text{nodes}, \text{edges}\}.
$$
Well, you know the "six degrees of separation" theory. That's what Prof. Strang means when saying "small world graphs".

