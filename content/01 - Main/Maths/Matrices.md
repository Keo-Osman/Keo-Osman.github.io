# A-Level Further Core

## Matrices Basics

### Matrices

* A matrix is an array of elements organised in rows and columns
* The size of on array can be described by row $\times$ columns such as a $2 \times 4:\left(\begin{array}{cccc}1 & 4 & -1 & 1 \\ 2 & 3 & 0 & 2\end{array}\right)$
* A square matrix is on $n \times n$ matrix
* A zero matrix is a matrix with all elements as 0
* An identity matrix is a square matrix where all elements are 0 except the diagonal for top left down. It is denoted as $I_n$ where $n$ is the matrix size

### Matrix Operations

* To add or subtract matrices just add or subtract each element. You can add or subtract some square matrices. Matrices which are the same size are called additively conformable
* To multiply by a Scalar multiply each element by the Scalar

### Matrix Multiplication

* Matrices A, B can be multiplied of A has dimensions $m \times n$, and $B$ has dimensions $n \times k$
* The product matrix $B$ has dimensions $m \times k$.
* The order you multiply matters $A B \neq B A$ (in general)
* If $AB$ exists $BA$ does not necessarily exists
* However Matrices are associative so $(AB)C \equiv A(BC)$
* If $A B$ exists then $A$ is said to be multiplicatively conformable with $B$
* To multiply a Matrix multiply each row in $A$ by the corresponding element in $B$ then sum the results example:
  $$
  \\left(\begin{array}{ccc}
  5 & -1 & 2 \\
  8 & 3 & -4
  \\end{array}\right) \times\left(\begin{array}{cc}
  2 & 2 \\
  9 & -3 \\
  7 & 4
  \\end{array}\right)=\left(\begin{array}{cc}
  15 & 21 \\
  15 & -9
  \\end{array}\right)
  $$
  Take the top right element. $5 \times 2 +(-1 \times 9) + 2 \times 7 = 15$

## Determinant

### Determinant of a Matrix

* You can easily calculate the determinant of a square matrix
* The determinant is a scalar value associated with that matrix
* If $\operatorname{det} M=0, M$ is a singular matrix
* If $\operatorname{det} M \neq 0, M$ is non - singular
* The determinant car also be written as $|M|, \left\lvert, \begin{array}{ll}a & b \\ c & d\end{array}\right\rvert$, or $\triangle$
* The determinant of a $2 \times 2$ matrix $\left(\begin{array}{ll}a & b \\ c & d\end{array}\right)$ is a $ad-bc$

### 3x3 Determinant

* For a $3 \times 3$ the determinant $=a \times\left|a_m\right|-b \times\left|b_m\right|+c \times\left|c_m\right|$ Where a $b, c$ are the top row of elements and $x_m$ denotes the minor matrix of $x$
* A minor matrix of an element in a $3 \times 3$ is the $2 \times 2$ matrix left after the row and column the element is in have been removed

## Inverting a Matrix

* You can find the inverse of any non-singular matrix denoted as $M^{-1}$. $M^{-1}$ is the matrix such that $MM^{-1} \equiv M^{-1}M \equiv I$
* If $A, B$ are non singular matrices then $(AB)^{-1} = B^{-1}A^{-1}$

### 2x2 Matrices

$M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, then $M^{-1} = \frac{1}{|M|} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$

### 3x3 Matrices

Finding the inverse of a $3 \times 3$ matrix is more complicated. You need to know the following definition.

* **The transpose of a matrix is found by interchanging the rows and the columns.**

For example, if $A = \begin{pmatrix} 1 & 2 \\ 4 & 3 \end{pmatrix}$, $A^{T} = \begin{pmatrix} 1 & 4 \\ 2 & 3 \end{pmatrix}$.
**Notation** The transpose of the matrix $M$ is written as $M^{T}$.  
**Finding the inverse of a $3 \times 3$ matrix $A$ usually consists of the following 5 steps.**

* **Step 1** 
  Find the determinant of $A$, $\det A$.
* **Step 2**:
  Form the matrix of the minors of $A$. In this chapter, the symbol $M$ is used for the matrix of the minors unless this causes confusion with another matrix in the question. In forming the matrix of minors, $M$, each of the nine elements of the matrix $A$ is replaced by its minor.
* **Step 3** 
  From the matrix of minors, form the matrix of cofactors by changing the signs of some elements of the matrix of minors according to the rule of alternating signs illustrated by the pattern
  $$\begin{pmatrix} + & - & + \\ - & + & - \\ + & - & + \end{pmatrix}​$$​​
  You leave the elements of the matrix of minors corresponding to the $+$ signs in this pattern unchanged. You change the signs of the elements corresponding to the $-$ signs.
* **Step 4**
  Write down the transpose, $C^{T}$, of the matrix of cofactors.
* **Step 5** 
  The inverse of the matrix $A$ is given by the formula $A^{-1}=\frac{1}{|A|}C^{T}$. 
  \*Each element of the matrix $C^{T}$ is divided by the determinant of $A$.

## Solving systems of linear equations

* If $A\begin{pmatrix} x \\ y \\ z \end{pmatrix} = v$ then $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = A^{-1}v$
* If A is non-singular then a unique solution for $\begin{pmatrix} x \ y \ z \end{pmatrix}$ can be found for any vector v
* To solve a given system of equations for x, y, z: $$\begin{aligned} ax + by + cz = j \\ dx + ey + fz = k \\ gx + hy + iz = l\end{aligned}$$ $$\begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} j \\ k \\ l \end{pmatrix}$$ Inverse the Matrix on the left and multiply on both sides to get $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} j \\ k \\ l \end{pmatrix} A^{-1}$  this gives values for $\begin{pmatrix} x \\ y \\ z \end{pmatrix}$ in the form $\begin{pmatrix} m \\ n \\ o \end{pmatrix}$

### Linear Equation Consistency

* A system of linear equations is consistent if at least one set of values that satisfy all equations simultaneously.
* If the matrix corresponding to a system is non-singular then the system has one solution and is consistent.
* If it is singular then either:
  * The system is consistent and has infinitely many solutions
  * It is inconsistent with no solutions
* You can visualize these different situations with different planes - 1 for each equation (this works as an equation $ax + by + cz = d$ forms a plane)
  * If the planes meet at a singular point the system is consistent with one unique solution
  * If the planes form a sheaf then the system is consistent with infinitely many solutions
  * If the planes form a prism then the system is inconsistent with no solutions
  * If two or more planes are parallel and non-identical the system is inconsistent with no solutions
  * If all 3 equations represent the same plane the system is consistent with infinitely many solutions.

# A-Level Further Pure 2 (Matrix Algebra)

## Eigen Vectors & Eigen Values

An Eigen vector of Matrix A is a non-zero Column Vector x that satisfies:

$Ax = \lambda x$

where $\lambda$ is a scalar. The value of $\lambda$ is the eigen value corresponding to the eigen vector x.

The eigen vector represents the invariant vector under the linear transform A (however the magnitude of the vector can be changed). The straight line that passes through the origin in the direction of x is the invariant line.

If the eigen value is 1 then every point on the line is invariant.

As by definition x is non-zero The matrix $(A-\lambda I)$ is singular and $det(A-\lambda I) = 0$

This means solutions to the characteristic equation of A: $det(A-\lambda I) = 0$ are eigen values of A

For a 2×2 matrix the characteristic equation simplifies to a quadratic to solve for $\lambda$. To solve for x then plug $\lambda$ into $Ax = \lambda x$ and solve for x.

Given eigen vector of A as $a = \begin{pmatrix} a \\ b \end{pmatrix}$ the normalized eigen vector $\hat{a}$ is $\begin{pmatrix} \frac{a}{\sqrt{a^2+b^2}} \\ \frac{b}{\sqrt{a^2+b^2}} \end{pmatrix}$

Sometimes the Characteristic Equation has complex solutions so the corresponding eigen vectors and eigen values are complex

You can also find eigen vectors/values for 3×3 matrices by solving the characteristic equation which simplifies to cubic meaning there will always be a real solution

## Reducing Matrices to Diagonal Form

A diagonal matrix is a square matrix such that every element except those which lie on the leading diagonal are 0.

To diagonalize a matrix A:

* Find Eigen vectors of A
* Form matrix P which consists of these Eigen vectors
* Find $P^{-1}$
* The diagonal matrix D is given as $P^{-1}AP$

When diagonalizing $A \rightarrow D$, D has the eigen values of A on the leading diagonal

If $A = A^T$ (if A is symmetric about the leading diagonal) then you can find D quicker by:

* Finding normalized eigen vectors of A
* Form matrix P with these vectors
* Find $P^T$
* $D = P^T AP$

This is called orthogonal diagonalization

For diagonal matrix $D = \begin{pmatrix} a & 0 \\ 0 & d \end{pmatrix}$, $D^k = \begin{pmatrix} a^k & 0 \\ 0 & d^k \end{pmatrix}$ (This generalizes to any n×n matrix)

To find higher powers of any matrix A you can use:
$A = PDP^{-1} \Rightarrow A^k = (PDP^{-1})^k = (PDP^{-1})(PDP^{-1})...(PDP^{-1}) \Rightarrow PD^kP^{-1}$

## Cayley-Hamilton Theorem

This theorem states that any matrix M satisfies its own characteristic equation:

$a\lambda^2 + b\lambda + c = 0 \Rightarrow aM^2 + bM + cI = 0$ where $\lambda$ is an eigen value of A.

This theorem can be used to find various variations of M such as $M^{-1}$ and $M^k$

