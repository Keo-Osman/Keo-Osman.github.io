#Maths/Geometry, #Maths/Linear-Algebra 
# Definition
You define any transform in 2 dimensions with the vector $\begin{pmatrix} x \\ y \end{pmatrix}$ and it describes how a point is changed. The new point is called an **image**. $S: \begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} f(x) \\ g(y) \end{pmatrix}$
A **linear transform** is a [[Vectors|Vector]] transform with only linear terms and no constants. You can describe any linear transform just by the effect it has on unit vectors as every vector is a linear combination of the unit vectors. Points/lines that don't change under the transform are called **invariant**.








$$
T: \begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} ax + by \\ cx + dy \end{pmatrix}
$$








They have the properties that:
- $\begin{pmatrix} 0 \\ 0 \end{pmatrix} \mapsto \begin{pmatrix} 0 \\ 0 \end{pmatrix}$
- They can be represented by a [[Matrices|Matrix]] 







$$
T: \begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} ax + by \\ cx + dy \end{pmatrix} = T: \begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} a & b \\ c & d  \end{pmatrix}\begin{pmatrix} x \\ y \end{pmatrix}
$$









---
# Rotations








$$
\begin{aligned}

& \stackrel{\displaystyle\text{2D About the origin}}{\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{pmatrix}}
\quad
\stackrel{\displaystyle\text{About the x-axis}}{\begin{pmatrix}
1 & 0 & 0 \\
0 & \cos\theta & -\sin\theta \\
0 & \sin\theta & \cos\theta
\end{pmatrix}}
\quad
\stackrel{\displaystyle\text{About the y-axis}}{\begin{pmatrix}
\cos\theta & 0 & \sin\theta \\
0 & 1 & 0 \\
- \sin\theta & 0 & \cos\theta
\end{pmatrix}}
\quad
\stackrel{\displaystyle\text{About the z-axis}}{\begin{pmatrix}
\cos\theta & -\sin\theta &0 \\
\sin\theta & \cos\theta&0 \\
0 & 0 & 1 
\end{pmatrix}}

\end{aligned}
$$









---
# Enlargement and Stretches
You can represent a stretch with matrix $\begin{pmatrix} a & 0 \\ 0 & b \end{pmatrix}$ It has stretch factor $a$ parallel to the $x$-axis and stretch factor $b$ parallel to the $y$-axis.
For stretches only along the $x$-axis, points on the $y$-axis are invariant and the line $x=0$ is invariant and vice versa.
For stretches in both direction the only invariance is the origin
For a linear transform by matrix $M$, $|M|$ is the scale factor of area (if it's negative the shape has been reflected)

---
# Reflections








$$
\begin{aligned}
& \stackrel{\displaystyle\text{2D reflection in y axis}}{\begin{pmatrix}
-1 & 0 \\
0 & 1
\end{pmatrix}}
\quad
& \stackrel{\displaystyle\text{2D reflection in x axis}}{\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}}
\quad
& \stackrel{\displaystyle\text{2D reflection in line y=x}}{\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}}
\quad
& \stackrel{\displaystyle\text{2D reflection in line y = -x}}{\begin{pmatrix}
0 & -1 \\
-1 & 0
\end{pmatrix}}
\end{aligned}
$$

















$$
\begin{aligned}
\quad
& \stackrel{\displaystyle\text{3D reflection in plane x = 0}}{\begin{pmatrix}
-1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}}
\quad
& \stackrel{\displaystyle\text{3D reflection in plane y = 0}}{\begin{pmatrix}
1 & 0 & 0 \\
0 & -1 & 0 \\
0 & 0 & 1
\end{pmatrix}}
\quad
& \stackrel{\displaystyle\text{3D reflection in plane z = 0}}{\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & -1
\end{pmatrix}}
\end{aligned}
$$









---
# Successive transformations
The matrix $PQ$ represents the singular transform of the result of a transform by $Q$ then $P$

---
# Inverting Transforms
Since $AA^{-1} = I$, $A^{-1}$ describes the inverse transformation of $A$