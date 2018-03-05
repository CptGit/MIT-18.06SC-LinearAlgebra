<!-- <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script> -->

Unit I: $A\boldsymbol{x} = \boldsymbol{b}$ and the Four Subspaces
============

Seesion 1.1: The Geometry of Linear Equations
----------------

We have a system of equations:
$$
\left\\{
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

### Matrx Picture

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
