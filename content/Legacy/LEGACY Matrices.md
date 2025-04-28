# Definition
A matrix is an array of elements organised in rows and columns
The size of on array can be described by row $\times$ columns such as a 2 x 4 matrix 








$$
\left(\begin{array}{cccc}1 & 4 & -1 & 1 \\ 2 & 3 & 0 & 2\end{array}\right)
$$










---
# A-Level Further Core 1
## Identity Matrix
The identity matrix is the matrix $I$ that is all zero apart from having 1's on the leading diagonal.









$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
$$









It has the unique property that $AI = IA = A$ for all matrices. This makes it the [[LEGACY Groups#Axioms of Groups|Identity Element]] of a [[LEGACY Groups|Group]] of matrices under the operation of multiplication hence the name
## Matrix Operations
### Addition
To add two matrices simply add the corresponding elements
### Multiplication by a Scalar
To multiply a matrix by a scalar simply multiply every individual element by the scalar
### Matrix Multiplication
Matrices $A$, $B$ can be multiplied if $A$ has dimensions $n \times m$, and $B$ has dimensions $m \times k$. The resulting matrix will have dimensions $n \times k$ *(If this condition is met then $A$ is said to be multiplicatively conformable with $B$).* Matrix multiplication is associative but not commutative.

To compute a matrix multiplication, take the dot product of each row of the first matrix with each column of the second matrix.
Also worded as: For $AB = C$, each element $C_{ij}$ is the dot product of the $i$-th row of $A$and the $j$-th column of $B$
For example 









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









## Minor
A minor of a element $a_{ij}$  is the determinant of the submatrix formed by removing the $i$th row and the $j$th column often denoted as $M_{ij}$ 
## Determinant
The determinant is a scalar value associated with that matrix and is the volume enclosed by the [[LEGACY Vectors|Vectors]] that make up the matrix. It is denoted as $|A|$ or $\det(A)$
If $|A|=0$, $A$ is a **singular** matrix, however if $|A| \neq 0$, $A$ is ***non-singular***
### 2x2
The determinant of a $2 \times 2$ matrix $\left(\begin{array}{ll}a & b \\ c & d\end{array}\right)$ is a $ad-bc$
### 3x3
For a $3 \times 3$ the determinant $=A_{11}M_{11} - A_{12}M_{12}+ A_{13}M_{13}$ 
## Transpose
The transpose of a matrix is found by interchanging the rows and the columns. For example, if $A = \begin{pmatrix} 1 & 2 \\ 4 & 3 \end{pmatrix}$, $A^{T} = \begin{pmatrix} 1 & 4 \\ 2 & 3 \end{pmatrix}$.
## Matrix Inverses
The inverse of any non-singular matrix $A^{-1}$ is the matrix such that $AA^{-1} \equiv A^{-1}A \equiv I$
If $A, B$ are non singular matrices then $(AB)^{-1} = B^{-1}A^{-1}$
### 2x2 
 $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, then $A^{-1} = \frac{1}{|A|} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$ 
### 3x3 
For a given $3 \times 3$ matrix $A$, $A^{-1} =\displaystyle\frac{1}{|A|}C^{T}$ where $C$ is the matrix of cofactors.
To find $C$
- Form the matrix of the minors. This is where each of the nine elements of the matrix is replaced by its minor
- Change the signs of some elements with alternating signs as shown 








$$
\begin{pmatrix} + & - & + \\ - & + & - \\ + & - & + \end{pmatrix}​
$$









## Solving Systems of Linear Equations
If $A\begin{pmatrix} x \\ y \\ z \end{pmatrix} = v$ then $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = A^{-1}v$
If A is non-singular then a unique solution for $\begin{pmatrix} x \ y \ z \end{pmatrix}$ can be found for any vector v
To solve a given system of equations for x, y, z: 








$$
\begin{aligned} ax + by + cz& = j \\
dx + ey + fz& = k \\ 
gx + hy + iz& = l
\\
\begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} &= \begin{pmatrix} j \\ k \\ l 
\end{pmatrix} 
\\
\end{aligned}
$$


















$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix}^{-1} \begin{pmatrix} j \\ k \\ l 
\end{pmatrix}
$$









## Linear Equation Consistency
A system of linear equations is consistent if at least one set of values that satisfy all equations simultaneously. If the matrix corresponding to a system is non-singular then the system has one solution and is consistent.

However if it is singular then either
- The system is consistent and has infinitely many solutions
- It is inconsistent with no solutions
![[Linear-Equation-Consistency-1.png]]
![[Linear-Equation-Consistency-2.png]]

---
# A-Level Further Pure 2
## Eigenvectors and Eigenvalues
An **Eigenvector** of **Matrix** A is a non-zero column [[LEGACY Vectors|Vector]] $x$ that satisfies $Ax = \lambda x$ where $\lambda$ is a scalar. The value of $\lambda$ is the **eigenvalue** corresponding to the **eigen vector** x.

An eigenvector is an invariant vector under the linear transform $A$. The corresponding eigenvalue $\lambda$ can be thought of as the magnitude scale factor for the eigenvector 

### Characteristic Equation









$$
\begin{aligned}
&Ax = \lambda x = \lambda Ix \\
&Ax - \lambda Ix  = (A- \lambda I)x = 0\\
\Rightarrow&\det(A-\lambda I) = 0
\end{aligned}
$$









The solutions of $\lambda$ are the eigenvalues of $A$
## Reducing Matrices to Diagonal Form
A diagonal matrix is a square matrix such that every element except those which lie on the leading diagonal are $0$ they can be use to solved [[LEGACY Recurrence Relations|Recurrence Relations]] or [[LEGACY Differential Equations|Coupled Differential Equations]]

To diagonalize a matrix $A$
- Find eigenvectors of A
- Form matrix $P$ which consists of these *column* eigenvectors
- Find $P^{-1}$
- The diagonal matrix $D$ is given as $P^{-1}AP$

If $A = A^T$ (if A is symmetric about the leading diagonal) then you can find D quicker by orthogonal diagonalization.
- Find normalized eigenvectors of $A$
- Form matrix $P$ with these vectors
- Find $P^T$
- $D = P^TAP$
When diagonalizing $A \rightarrow D$, $D$ has the eigen values of A on the leading diagonal *(the eigenvalue in column $n$ corresponds to the eigenvector in column $n$ in $P$)

## Powers of Matrices
For any $n \times n$ diagonal matrix $D = \begin{pmatrix} a & 0 \\ 0 & d \end{pmatrix}$, $D^k = \begin{pmatrix} a^k & 0 \\ 0 & d^k \end{pmatrix}$ 
To find higher powers of any general matrix $A$ you can use:









$$
\begin{aligned}
A &= PDP^{-1}\\ 
\Rightarrow A^k &= (PDP^{-1})^k\\
&= (PDP^{-1})(PDP^{-1})...(PDP^{-1})\\
&=PD(P^{-1}P)D(P^{-1}P)...(P^{-1}P)DP^{-1}\\
&= PD^kP^{-1}
\end{aligned}
$$









## Cayley-Hamilton Theorem
All matrices $M$ satisfy their own characteristic equation 









$$
\begin{aligned}
&\det(M-\lambda I) = 0 \\
\Rightarrow &a_n{\lambda}^{n} + a_{n-1}{\lambda}^{n-1} + \cdots a_2{\lambda}^2 + a_1{\lambda} + a_0  = 0 \\
\Rightarrow &a_n{M}^{n} + a_{n-1}{M}^{n-1} + \cdots a_2{M}^2 + a_1{M} + a_0 I = 0
\end{aligned}
$$









This theorem can be used to find various variations of M such as $M^{-1}$ and $M^k$  by multiplying or dividing through by $M$ and using the fact that $I = MM^{-1} \Rightarrow I \div M = M^{-1}$ 

---
