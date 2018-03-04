Unit I: Ax = b and the Four Subspaces
=====================================

Seesion 1.1: The Geometry of Linear Equations
---------------------------------------------

We have a system of equations:

.. math::


   \begin{aligned}
   2x - y &= 0 \\\\
   -x + 2y &= 3
   \end{aligned}

Row Picture
~~~~~~~~~~~

Line :math:`2x - y = 0` and line :math:`-x + 2y = 0` intersects at the
point :math:`(1, 2)`, so :math:`(1, 2)` is the solution of the system of
equations. > Maybe I should draw a X-Y coordinates here…

Column Picture
~~~~~~~~~~~~~~

We rewrite the system of linear equations as a single equation:

.. math::


   x\begin{bmatrix}2 \\\\ -1\end{bmatrix} + y\begin{bmatrix}-1 \\\\ 2\end{bmatrix} = \begin{bmatrix}0 \\\\ 3\end{bmatrix}

We see :math:`x` and :math:`y` as coefficients of column vectors:
:math:`\boldsymbol{v_1} = \begin{bmatrix}2 \\\\ -1\end{bmatrix}` and
:math:`\boldsymbol{v_2} = \begin{bmatrix}-1 \\\\ 2\end{bmatrix}`, and
the sum :math:`x\boldsymbol{v_1} + y\boldsymbol{v_2}` is called a
*linear combination* of :math:`\boldsymbol{v_1}` and
:math:`\boldsymbol{v_2}`.

Geometrically, we can find one copy of :math:`\boldsymbol{v_1}` added to
two copies of :math:`\boldsymbol{v_2}` just equals the vector
:math:`\begin{bmatrix}0 \\\\ 3\end{bmatrix}`. Then the solution should
be :math:`x = 1, y =2`. > I will add a figure when time is available >_>

Matrx Picture
~~~~~~~~~~~~~

We rewrite the equations in our example as a compact form,

.. math::


   A\boldsymbol{x} = \boldsymbol{b},

that is

.. math::


   \begin{bmatrix}2 & -1 \\\\ -1 & 2\end{bmatrix}\begin{bmatrix}x \\\\ y\end{bmatrix} = \begin{bmatrix}0 \\\\ 3\end{bmatrix}

Matrix Multiplication
~~~~~~~~~~~~~~~~~~~~~

.. math::


   \begin{aligned}
   \begin{bmatrix}2 & -1 \\\\ -1 & 2\end{bmatrix} \begin{bmatrix}1 \\\\ 2\end{bmatrix} = 1\begin{bmatrix}2 \\\\ -1\end{bmatrix} + 2\begin{bmatrix}-1 \\\\ 2\end{bmatrix} = \begin{bmatrix}0 \\\\ 3\end{bmatrix}
   \end{aligned}

A matrix times by a vector is just **a linear combination of the column
vectors of the matrix**.
