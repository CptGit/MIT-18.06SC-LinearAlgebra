<!-- <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script> -->

[TOC]

Unit I: $A\boldsymbol{x} = \boldsymbol{b}$ and the Four Subspaces
============

Session 1.1: The Geometry of Linear Equations
----------------

We have a system of equations:
$$
\left\{
\begin{aligned}
2x - y &= 0 \\\\
-x + 2y &= 3
\end{aligned}
\right .
$$

### Row Picture

Line $2x - y = 0$ and line $-x + 2y = 0$ intersects at the point $(1, 2)$, so $(1, 2)$ is the solution of the system of equations.

>Maybe I should draw a X-Y coordinates here...

### Column Picture

We rewrite the system of linear equations as a single equation:

$$
x\begin{bmatrix}2 \\\\ -1\end{bmatrix} + y\begin{bmatrix}-1 \\\\ 2\end{bmatrix} = \begin{bmatrix}0 \\\\ 3\end{bmatrix}
$$

We see $x$ and $y$ as scalars of column vectors: $\boldsymbol{v_1} = \begin{bmatrix}2 \\\\ -1\end{bmatrix}$ and $\boldsymbol{v_2} = \begin{bmatrix}-1 \\\\ 2\end{bmatrix}$, and the sum $x\boldsymbol{v_1} + y\boldsymbol{v_2}$ is called a *linear combination* of $\boldsymbol{v_1}$ and $\boldsymbol{v_2}$.

Geometrically, we can find one copy of $\boldsymbol{v_1}$ added to two copies of $\boldsymbol{v_2}$ just equals the vector $\begin{bmatrix}0 \\\\ 3\end{bmatrix}$. Then the solution should be $x = 1, y =2$.

>I will add a figure when time is available >_>

### Matrix Picture

We rewrite the equations in our example as a compact form,

$$
A\boldsymbol{x} = \boldsymbol{b},
$$

that is

$$
\begin{bmatrix}2 & -1 \\\\ -1 & 2\end{bmatrix}\begin{bmatrix}x \\\\ y\end{bmatrix} = \begin{bmatrix}0 \\\\ 3\end{bmatrix}
$$

### Matrix Multiplication

$$
\begin{aligned}
\begin{bmatrix}2 & -1 \\\\ -1 & 2\end{bmatrix} \begin{bmatrix}1 \\\\ 2\end{bmatrix} = 1\begin{bmatrix}2 \\\\ -1\end{bmatrix} + 2\begin{bmatrix}-1 \\\\ 2\end{bmatrix} = \begin{bmatrix}0 \\\\ 3\end{bmatrix}
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

    $\Leftrightarrow$ $A\boldsymbol{x} = 0$ has no non-zero solution $\boldsymbol{x}$

    $\Leftrightarrow$ The columns of $A$ are *independent*

    $\Leftrightarrow$ All vectors $A\boldsymbol{x}$ cover the whole vector space

    Example: $A = \begin{bmatrix}1 & 0 & 0 \\\\ -1 & 1 & 0 \\\\ 0 & -1 & 1\end{bmatrix}$

- $A$ is not invertible

    $\Leftrightarrow$ $A\boldsymbol{x} = \boldsymbol{b}$ has a solution $\boldsymbol{x}$ only for some of $\boldsymbol{b}$ in the vector space

    $\Leftrightarrow$ $A\boldsymbol{x} = 0$ has non-zero solutions $\boldsymbol{x}$

    $\Leftrightarrow$ The columns of $A$ are *dependent*

    $\Leftrightarrow$ All vectors $A\boldsymbol{x}$ lies in only a subspace of the vector space

    Example: $A = \begin{bmatrix}1 & 0 & -1 \\\\ -1 & 1 & 0 \\\\ 0 & -1 & 1\end{bmatrix}$

------------------

Session 1.3: Elimination with Matrices
--------------

### Method of Elimination

We have an example $A\boldsymbol{x} = \boldsymbol{b}$,

$A = \begin{bmatrix}1 & 2 & 1 \\\\ 3 & 8 & 1 \\\\ 0 & 4 & 1\end{bmatrix}$ and $\boldsymbol{b} = \begin{bmatrix}2 \\\\ 12 \\\\2\end{bmatrix}$.

Steps of Elimination:

- Step 1: subtract $3$ times row 1 from row 2;
- Step 2: subtract $2$ times row 2 from row 3.

$$
A = \begin{bmatrix}1 & 2 & 1 \\\\ 3 & 8 & 1 \\\\ 0 & 4 & 1\end{bmatrix}
\rightarrow \begin{bmatrix}1 & 2 & 1 \\\\ 0 & 2 & -2 \\\\ 0 & 4 & 1\end{bmatrix}
\rightarrow U = \begin{bmatrix}1 & 2 & 1 \\\\ 0 & 1 & -2 \\\\ 0 & 0 & 5\end{bmatrix}
$$

$$
\boldsymbol{b} = \begin{bmatrix}2 \\\\ 12 \\\\ 2\end{bmatrix}
\rightarrow \cdots \rightarrow \begin{bmatrix}2 \\\\ 6 \\\\ -10\end{bmatrix}
$$

Thus, we can easily solve the systems of equations, $\begin{bmatrix}x \\\\ y  \\\\ z\end{bmatrix} = \begin{bmatrix}2 \\\\ 1  \\\\ -2\end{bmatrix}$.

### Elimination Matrices

The product of a matrix (3x3) and a column vector (3x1) is a column vector
(3x1) that is a linear combination of the columns of the matrix.

The product of a row vector (1x3) and a matrix (3x3) is a row vector (1x3) that is a linear
combination of the rows of the matrix.

For example,

$$
\begin{bmatrix}1 & 0 & 0 \\\\ -3 & 1 & 0 \\\\ 0 & 0 & 1\end{bmatrix}
\begin{bmatrix}1 & 2 & 1 \\\\ 3 & 8 & 1 \\\\ 0 & 4 & 1\end{bmatrix}
= \begin{bmatrix}1 & 2 & 1 \\\\ 0 & 2 & -2 \\\\ 0 & 4 & 1\end{bmatrix}.
$$

Multiplying on the left by a permutation matrix exchanges the rows of a matrix, while multiplying on the right exchanges the columns. For example,

$$
P = \begin{bmatrix}0 & 1 & 0 \\\\ 1 & 0 & 0 \\\\ 0 & 0 & 1\end{bmatrix}.
$$

$P$ is a *permutation matrix* and the first and second rows of the matrix $PA$ are the second and first rows of the matrix $A$.

Note, matrix multiplication is *associative* but *not commutative*.

### Inverses
We have a matrix:

$$
E_{21} = \begin{bmatrix}1 & 0 & 0 \\\\ -3 & 1 & 0 \\\\ 0 & 0 & 1\end{bmatrix}
$$

which subtracts $3$ times row 1 from row 2. To "**undo**" this operation we must add $3$ times row 1 to row 2 using the inverse matrix:

$$
E_{21}^{-1} = \begin{bmatrix}1 & 0 & 0 \\\\ 3 & 1 & 0 \\\\ 0 & 0 & 1\end{bmatrix}.
$$

In fact, $E_{21}^{-1}E_{21} = I$.

-------------------

Session 1.4: Multiplication and Inverse Matrices
------------------

### Four and a half ways we see matrix multiplication

We have $AB = C$. $A$ is an $m \times n$ matrix and $B$ is an $n \times p$ matrix, then $C$ is an $m \times p$ matrix. We use $c_{ij}$ to denote the entry in row $i$ and column $j$ of matrix $C$ and the same denotation applies to $a_{ij}$ and $b_{ij}$.

#### 1. Row times column

$c_{ij} = \sum_{k=1}^n a_{ik}b_{kj}$

#### 2. Columns

The product of matrix $A$ and column $j$ of matrix $B$ equals column $j$ of matrix $C$. This tells us that the columns of $C$ are combinations of columns of $A$.

$$
A
\begin{bmatrix}
| & | & | \\\\
column 1 & column 2 & column 3 \\\\
| & | & |
\end{bmatrix}
=\begin{bmatrix}
| & | & | \\\\
A(column 1) & A(column 2) & A(column 3) \\\\
| & | & |
\end{bmatrix}
$$

#### 3.Rows
The product of row $i$ of matrix $A$ and matrix $B$ equals row $i$ of matrix $C$. So the rows of $C$ are combinations of rows of $B$. 

$$
\left[
\begin{matrix}
--- & row 1 & --- \\\\
--- & row 2 & --- \\\\
--- & row 3 & ---
\end{matrix}
\right]
B
=\left[
\begin{matrix}
--- & (row 1)B & --- \\\\
--- & (row 2)B & --- \\\\
--- & (row 3)B & ---
\end{matrix}
\right]
$$

#### 4. Column times row

$$
AB = \sum_{k=1}{n}
\begin{bmatrix}a_{1k} \\\\ \vdots \\\\ a_{mk}\end{bmatrix}
\begin{bmatrix}b_{k1} & \cdots & b_{kp}\end{bmatrix}
$$

>note: a typo in the MIT's lecture summary here: $b_{kp}$, not $b_{kn}$.

#### 5. Blocks

$$
\begin{bmatrix}A_1 & A_2 \\\\ A_3 & A_4 \end{bmatrix}
\begin{bmatrix}B_1 & B_2 \\\\ B_3 & B_4 \end{bmatrix}
=\begin{bmatrix}
A_1B_1+A_2B_3 & A_1B_2+A_2B_4 \\\\
A_3B_1+A_4B_3 & A_3B_2+A_4B_4
\end{bmatrix}
$$

### Inverses

If $A$ is *singular* or *not invertible*,

then A does not have an inverse,

and we can find some non-zero vector $\boldsymbol{x}$ for which $A\boldsymbol{x} = 0$

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
E_{32} & E_{21} & & E \\\\
\begin{bmatrix}1 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & -5 & 1\end{bmatrix}
& \begin{bmatrix}1 & 0 & 0 \\\\ -2 & 1 & 0 \\\\ 0 & 0 & 1\end{bmatrix}
& = & \begin{bmatrix}1 & 0 & 0 \\\\ -2 & 1 & 0 \\\\ 10 & -5 & 1\end{bmatrix}
\end{array}.
$$

Here $L = E^{-1} = E_{21}^{-1}E_{32}^{-1}$:

$$
\begin{array}{cccc}
E_{21}^{-1} & E_{32}^{-1} & & L \\\\
\begin{bmatrix}1 & 0 & 0 \\\\ \underline{2} & 1 & 0 \\\\ 0 & 0 & 1\end{bmatrix}
& \begin{bmatrix}1 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & \underline{5} & 1\end{bmatrix}
& = & \begin{bmatrix}1 & 0 & 0 \\\\ \underline{2} & 1 & 0 \\\\ 0 & \underline{5} & 1\end{bmatrix}
\end{array}
$$

Notice the 0 in row three column one of $L$, where $E$ had a $10$. The factorization $A = LU$ is preferable to the statement $EA = U$ because the combination of row subtractions does not have the effect on $L$ that it did on $E$.

**If there are no row exchanges, the multipliers from the elimination matrices are copied directly into $L$.**

### Cost of elimination

If we define a typical operation is to multiply one row and then subtract it from another, then the total number of operations needed to factor $n \times n$ $A$ into $LU$ is on the order of $n^3$:

$$1^2 + 2^2 + \cdots + (n - 1)^2 + n^2 = \sum_{i = 1}^{n}i^2 \approx \int_0^n x\,\mathrm{d}x = \frac{1}{3}n^3.$$

While we’re factoring $A$ we’re also operating on $\boldsymbol{b}$. That costs about $n^2$ operations, which is hardly worth counting compared to $1/3n^3$. 

### Row exchanges

- The inverse of any permutation matrix $P$ is $P^{-1} = P^{T}$.

- There are $n!$ different ways to permute the rows of an $n \times n$ matrix (including the permutation that leaves all rows unfixed) so there are $n!$ permutation matrices. These matrices form a *multiplicative group*.