
# A-Level Further Core 1
## Basics
You define any transform in 2 dimensions with the vector $\begin{pmatrix} x \\ y \end{pmatrix}$ and it describes how a point is changed. The new point is called an image.

$S: \begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} ax + by + c \\ dx + ey + f \end{pmatrix}$

A linear transform is a vector transform with only linear terms and no constants. For example:

$T: \begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} ax + by \\ cx + dy \end{pmatrix}$

Linear transforms have a few key distinctive properties:

- They always map the origin onto itself
- It can be represented by a [[Matrices|matrix]]:

$$\begin{pmatrix} a & b \\ c & d \end{pmatrix}$$

Since multiplying by the vector $\begin{pmatrix} x \\ y \end{pmatrix}$ gives back the original transformation vector.

## Reflections and Rotations

- You can describe any linear transform by the effect it has on unit vectors $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$
- Points/lines that don't change under the transform are called invariant
- The matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ maps $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$ to $\begin{pmatrix} a \\ c \end{pmatrix}$ and $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$ to $\begin{pmatrix} b \\ d \end{pmatrix}$
- The matrix of a rotation through angle θ anticlockwise about the origin:

$$\begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$$
## Enlargement and Stretches

- You can represent a stretch with matrix $\begin{pmatrix} a & 0 \\ 0 & b \end{pmatrix}$ It has stretch factor a parallel to the x-axis and stretch factor b parallel to the y-axis; if a=b then it has scale factor a
- For stretches only along the x-axis, points on the y-axis are invariant and the line x=0 is invariant and vice versa
- For stretches in both direction the only invariance is the origin
- For a linear transform by matrix M, |M| is the scale factor of area (if it's negative the shape has been reflected)

## Successive transformations

The matrix PQ represents the singular transform of the result of a transform by Q then P

## Linear Transforms in 3D

- Any 3D linear transform can be defined by the effect it has on the 3 unit vectors $\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$, $\begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}$, $\begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}$. A transform by a given 3x3 Matrix

$$\begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix}$$

maps the following:

$$\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} \rightarrow \begin{pmatrix} a \\ d \\ g \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} \rightarrow \begin{pmatrix} b \\ e \\ h \end{pmatrix}, \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} \rightarrow \begin{pmatrix} c \\ f \\ i \end{pmatrix}$$
## Inverting Transforms
Since $AA^{-1} = I$, $A^{-1}$ describes the inverse transformation of $A$

