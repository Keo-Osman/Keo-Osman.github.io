
# A-Level Further Core
## Matrices Basics
### Matrices
- A matrix is an array of elements organised in rows and columns
- The size of on array can be described by row $\times$ columns such as a $2 \times 4:\left(\begin{array}{cccc}1 & 4 & -1 & 1 \\ 2 & 3 & 0 & 2\end{array}\right)$
- A square matrix is on $n \times n$ matrix
- A zero matrix is a matrix with all elements as 0
- An identity matrix is a square matrix where all elements are 0 except the diagonal for top left down. It is denoted as $I_n$ where $n$ is the matrix size
### Matrix Operations
- To add or subtract matrices just add or subtract each element. You can add or subtract some square matrices. Matrices which are the same size are called additively conformable
- To multiply by a Scalar multiply each element by the Scalar

### Matrix Multiplication
- Matrices A, B can be multiplied of A has dimensions $m \times n$, and $B$ has dimensions $n \times k$
- The product matrix $B$ has dimensions $m \times k$.
- The order you multiply matters $A B \neq B A$ (in general)
- If $AB$ exists $BA$ does not necessarily exists
- However Matrices are associative so $(AB)C \equiv A(BC)$
- If $A B$ exists then $A$ is said to be multiplicatively conformable with $B$
- To multiply a Matrix multiply each row in $A$ by the corresponding element in $B$ then sum the results example:
$$
\left(\begin{array}{ccc}
5 & -1 & 2 \\
8 & 3 & -4
\end{array}\right) \times\left(\begin{array}{cc}
2 & 2 \\
9 & -3 \\
7 & 4
\end{array}\right)=\left(\begin{array}{cc}
15 & 21 \\
15 & -9
\end{array}\right)
$$
Take the top right element. $5 \times 2 +(-1 \times 9) + 2 \times 7 = 15$


## Determinant
### Determinant of a Matrix
- You can easily calculate the determinant of a square matrix
- The determinant is a scalar value associated with that matrix
- If $\operatorname{det} M=0, M$ is a singular matrix
- If $\operatorname{det} M \neq 0, M$ is non - singular
- The determinant car also be written as $|M|, \left\lvert\, \begin{array}{ll}a & b \\ c & d\end{array}\right\rvert$, or $\triangle$
- The determinant of a $2 \times 2$ matrix $\left(\begin{array}{ll}a & b \\ c & d\end{array}\right)$ is a $ad-bc$
### 3x3 Determinant
- For a $3 \times 3$ the determinant $=a \times\left|a_m\right|-b \times\left|b_m\right|+c \times\left|c_m\right|$ Where a $b, c$ are the top row of elements and $x_m$ denotes the minor matrix of $x$
- A minor matrix of an element in a $3 \times 3$ is the $2 \times 2$ matrix left after the row and column the element is in have been removed

## Inverting a Matrix
- You can find the inverse of any non-singular matrix denoted as $M^{-1}$. $M^{-1}$ is the matrix such that $MM^{-1} \equiv M^{-1}M \equiv I$
- If $A, B$ are non singular matrices then $(AB)^{-1} = B^{-1}A^{-1}$

### 2x2 Matrices
 $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, then $M^{-1} = \frac{1}{|M|} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$
### 3x3 Matrices
Finding the inverse of a $3 \times 3$ matrix is more complicated. You need to know the following definition.
- **The transpose of a matrix is found by interchanging the rows and the columns.**

 For example, if $A = \begin{pmatrix} 1 & 2 \\ 4 & 3 \end{pmatrix}$, $A^{T} = \begin{pmatrix} 1 & 4 \\ 2 & 3 \end{pmatrix}$.
**Notation** The transpose of the matrix $M$ is written as $M^{T}$.    
**Finding the inverse of a $3 \times 3$ matrix $A$ usually consists of the following 5 steps.**
-  **Step 1** 
	Find the determinant of $A$, $\det A$.
-  **Step 2**:
	Form the matrix of the minors of $A$. In this chapter, the symbol $M$ is used for the matrix of the minors unless this causes confusion with another matrix in the question. In forming the matrix of minors, $M$, each of the nine elements of the matrix $A$ is replaced by its minor.
- **Step 3** 
	From the matrix of minors, form the matrix of cofactors by changing the signs of some elements of the matrix of minors according to the rule of alternating signs illustrated by the pattern
    $$\begin{pmatrix} + & - & + \\ - & + & - \\ + & - & + \end{pmatrix}​$$​​
	You leave the elements of the matrix of minors corresponding to the $+$ signs in this pattern unchanged. You change the signs of the elements corresponding to the $-$ signs.
- **Step 4**
	Write down the transpose, $C^{T}$, of the matrix of cofactors.
- **Step 5** 
	The inverse of the matrix $A$ is given by the formula $A^{-1}=\frac{1}{|A|}C^{T}$. 
	*Each element of the matrix $C^{T}$ is divided by the determinant of $A$.



## Solving systems of linear equations

- If $A\begin{pmatrix} x \\ y \\ z \end{pmatrix} = v$ then $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = A^{-1}v$
- If A is non-singular then a unique solution for $\begin{pmatrix} x \ y \ z \end{pmatrix}$ can be found for any vector v
- To solve a given system of equations for x, y, z: $$\begin{aligned} ax + by + cz = j \\ dx + ey + fz = k \\ gx + hy + iz = l\end{aligned}$$ $$\begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} j \\ k \\ l \end{pmatrix}$$ Inverse the Matrix on the left and multiply on both sides to get $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} j \\ k \\ l \end{pmatrix} A^{-1}$  this gives values for $\begin{pmatrix} x \\ y \\ z \end{pmatrix}$ in the form $\begin{pmatrix} m \\ n \\ o \end{pmatrix}$
### Linear Equation Consistency
- A system of linear equations is consistent if at least one set of values that satisfy all equations simultaneously.
- If the matrix corresponding to a system is non-singular then the system has one solution and is consistent.
- If it is singular then either:
    - The system is consistent and has infinitely many solutions
    - It is inconsistent with no solutions
- You can visualize these different situations with different planes - 1 for each equation (this works as an equation $ax + by + cz = d$ forms a plane)
    - If the planes meet at a singular point the system is consistent with one unique solution
    - If the planes form a sheaf then the system is consistent with infinitely many solutions
    - If the planes form a prism then the system is inconsistent with no solutions
    - If two or more planes are parallel and non-identical the system is inconsistent with no solutions
    - If all 3 equations represent the same plane the system is consistent with infinitely many solutions.


## Flashcards
#Maths/A-Level-Further-Core/Matrices, #Maths/Topics/Matrices    

What is a matrix?
?
A matrix is an array of elements organized in rows and columns. <!--SR:!2024-10-22,55,310-->

How is the size of a matrix described?
?
The size of a matrix is described by rows × columns, such as 2 × 4 $$\begin{pmatrix}
a & b & c & d \\
e & f & g & h
\end{pmatrix}$$ <!--SR:!2024-09-27,31,270-->

What is an identity matrix?
?
An identity matrix is a square matrix where all elements are 0 except for the diagonal from top left down, which contains 1s. It is denoted as $I_n$ where n is the matrix size. <!--SR:!2024-11-03,60,310-->

How do you add or subtract matrices?
?
To add or subtract matrices, you add or subtract each corresponding element. The matrices must be the same size (additively conformable). <!--SR:!2024-09-25,33,290-->

How do you multiply a matrix by a scalar?
?
To multiply a matrix by a scalar, multiply each element of the matrix by that scalar. <!--SR:!2024-10-21,54,310-->

What are the conditions for matrix multiplication?
?
Matrices A and B can be multiplied if A has dimensions $m × n$, and B has dimensions $n × k$. The resulting product matrix will have dimensions $m × k$. <!--SR:!2024-10-29,55,310-->

What is the determinant of a matrix?
?
The determinant is a scalar value associated with a square matrix. It can be written as det M, |M|, or Δ. <!--SR:!2024-10-19,53,310-->

How do you calculate the determinant of a 2×2 matrix?
?
For a 2×2 matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is $ad - bc$. <!--SR:!2024-11-03,60,310-->

What is the inverse of a matrix?
?
The inverse of a matrix M, denoted as $M^{-1}$, is the matrix such that $MM^{-1} \equiv M^{-1}M \equiv I$, where I is the identity matrix. <!--SR:!2024-10-16,42,290-->

How do you find the inverse of a 2×2 matrix?
?
For a 2×2 matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the inverse is $M^{-1} = \frac{1}{|M|} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$, where |M| is the determinant. <!--SR:!2024-09-20,6,230-->

What is the transpose of a matrix?
?
The transpose of a matrix is found by interchanging its rows and columns. It is denoted as $M^T$. <!--SR:!2024-10-21,55,310-->

How can you solve a system of linear equations using matrices?
?
If $A\begin{pmatrix} x \\ y \\ z \end{pmatrix} = v$, then $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = A^{-1}v$. Multiply both sides by the inverse of A to find the solution. <!--SR:!2024-10-08,24,290-->

What does it mean for a system of linear equations to be consistent?
?
A system of linear equations is consistent if there exists at least one set of values that satisfy all equations simultaneously. <!--SR:!2024-11-13,60,290-->

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
- Find Eigen vectors of A
- Form matrix P which consists of these Eigen vectors
- Find $P^{-1}$
- The diagonal matrix D is given as $P^{-1}AP$

When diagonalizing $A \rightarrow D$, D has the eigen values of A on the leading diagonal

If $A = A^T$ (if A is symmetric about the leading diagonal) then you can find D quicker by:
- Finding normalized eigen vectors of A
- Form matrix P with these vectors
- Find $P^T$
- $D = P^T AP$

This is called orthogonal diagonalization

For diagonal matrix $D = \begin{pmatrix} a & 0 \\ 0 & d \end{pmatrix}$, $D^k = \begin{pmatrix} a^k & 0 \\ 0 & d^k \end{pmatrix}$ (This generalizes to any n×n matrix)

To find higher powers of any matrix A you can use:
$A = PDP^{-1} \Rightarrow A^k = (PDP^{-1})^k = (PDP^{-1})(PDP^{-1})...(PDP^{-1}) \Rightarrow PD^kP^{-1}$

## Cayley-Hamilton Theorem

This theorem states that any matrix M satisfies its own characteristic equation:

$a\lambda^2 + b\lambda + c = 0 \Rightarrow aM^2 + bM + cI = 0$ where $\lambda$ is an eigen value of A.

This theorem can be used to find various variations of M such as $M^{-1}$ and $M^k$

## Flashcards
#Maths/Topics/Matrices, #Maths/A-Level-Further-Pure/Matrix-Algebra

What is a diagonal matrix?
?
A diagonal matrix is a square matrix where every element except those on the leading diagonal are 0. <!--SR:!2024-09-19,4,298-->

How do you diagonalize a matrix $A$?
?
To diagonalize matrix $A$:
1. Find Eigen vectors of $A$
2. Form matrix P consisting of these Eigen vectors
3. Find $P^{-1}$
4. Calculate the diagonal matrix D as $D = P^{-1}AP$
But for an easier calculation you can simply for a diagonal matrix where every element is an Eigen value of $A$ (The eigen value of a specific column should correspond to the eigen vector in that specific column of $P$) <!--SR:!2024-09-20,4,278-->

How can you diagonalize a symmetric matrix $A$ more efficiently?
?
For a symmetric matrix A (where $A = A^T$):
1. Find normalized eigen vectors of $A$
2. Form matrix $P$ with these vectors
3. Find $P^T$
4. Calculate $D = P^T AP$
This process is called orthogonal diagonalization. <!--SR:!2024-10-02,14,298-->

What is the general form of a diagonal matrix $D$ raised to the power $k$?
?
For a diagonal matrix $D = \begin{pmatrix} a & 0 \\ 0 & d \end{pmatrix}$,
$D^k = \begin{pmatrix} a^k & 0 \\ 0 & d^k \end{pmatrix}$
This generalizes to any $n×n$ diagonal matrix. <!--SR:!2024-09-19,4,298-->

How can you calculate higher powers of any matrix $A$ using diagonalization?
?
To find $A^k$:
1. Diagonalize $A$ as $A = PDP^{-1}$
2. Then $A^k = (PDP^{-1})^k = PD^kP^{-1}$ <!--SR:!2024-09-19,3,258-->

What does the Cayley-Hamilton Theorem state?
?
The Cayley-Hamilton Theorem states that any matrix $M$ satisfies its own characteristic equation.
If $a\lambda^2 + b\lambda + c = 0$ is the characteristic equation, then $aM^2 + bM + cI = 0$, where $\lambda$ is an eigen value of $A$. <!--SR:!2024-09-19,4,298-->

What is an Eigen vector?
?
An Eigen vector of Matrix $A$ is a non-zero Column Vector $x$ that satisfies the equation:
$Ax = \lambda x$
where $\lambda$ is a scalar called the eigen value corresponding to the eigen vector $x$. <!--SR:!2024-09-19,4,298-->

What does an Eigen vector represent geometrically?
?
An Eigen vector represents the invariant vector under the linear transform $A$ (although its magnitude may change). The straight line passing through the origin in the direction of the Eigen vector is called the invariant line. <!--SR:!2024-09-19,4,298-->

What is the significance of an Eigen value of 1?
?
If the Eigen value is 1, then every point on the invariant line (defined by the corresponding Eigen vector) remains unchanged under the transformation. <!--SR:!2024-09-19,4,298-->

How are Eigen values related to the characteristic equation of a matrix?
?
The solutions to the characteristic equation of A, given by $det(A-\lambda I) = 0$, are the Eigen values of A. <!--SR:!2024-09-19,4,298-->

How do you find Eigen vectors and Eigen values for a $n \times n$ matrix?
?
1. Solve the characteristic equation $det(A-\lambda I) = 0$, which simplifies to a polynomial of degree $n$ in terms of $\lambda$
2. Solve this polynomial to find the Eigen values $\lambda$
3. For each $\lambda$, solve $Ax = \lambda x$ to find the corresponding Eigen vector x <!--SR:!2024-09-19,4,298-->

How do you normalize an Eigen vector?
?
Given an Eigen vector $a = \begin{pmatrix} a \\ b \end{pmatrix}$, the normalized Eigen vector $\hat{a}$ is:
$\hat{a} = \begin{pmatrix} \frac{a}{\sqrt{a^2+b^2}} \\ \frac{b}{\sqrt{a^2+b^2}} \end{pmatrix}$ <!--SR:!2024-09-19,4,298-->

How do you find Eigen vectors and Eigen values for 3×3 matrices?
?
For 3×3 matrices:
1. Solve the characteristic equation, which simplifies to a cubic equation
2. Solve this cubic equation to find the Eigen values (there will always be at least one real solution)
3. For each Eigen value, solve $Ax = \lambda x$ to find the corresponding Eigen vector <!--SR:!2024-09-19,4,298-->