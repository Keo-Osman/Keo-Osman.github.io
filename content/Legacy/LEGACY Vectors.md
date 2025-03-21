
# A-Level Further Core 1
## Straight Line Vectors $r = a + \lambda b$
The equation of a straight line vector passing through point $a$ and is parallel to vector $b$ is $r = a + \lambda b$ where $r$ is the **position** vector of a general point on the line. 
*So by taking varying values of $\lambda$ you can find the position vectors of varying points that lie on the straight line.*
The line has cartesian equation $\displaystyle \frac{x-a_1}{b_1} = \frac{y-a_2}{b_2} = \frac{z-a_3}{b_3} =\lambda$
***Colinear***: Points are said to be *collinear* if they all lie on the same straight line
## Plane Vectors $r = a + \lambda b + \mu c$
The vector of a plane that through position vector $a$ is: $r = a + \lambda b + \mu c$ where r is the **position** vector of a general point on the plane with $a$ being the position vector of a *fixed* arbitrary point on the plane and $b, c$ are *non-parallel, non-zero* vectors ***on the plane***
*The intuition of this is that $a$ gets you from the origin onto the plane and $\lambda b, \mu c$ allow you to move across the plane*

The cartesian equation of a plane is $px + qy + rz = s$ where the normal vector to the plane is $(p, q, r)$. You can find the cartesian equation given the vector equation using the cross product *(only for needed FP1)*
## Dot Product $a\cdot b = |a||b| \cos \theta$
The ***dot*** product *(also called scalar product)* between 2 vectors $a, b$ is given by the equation $a\cdot b = |a||b| \cos \theta$ where $\theta$ is the acute angle between $a$ and $b$ *(when they are pointing away from their intersection).* 

The scalar product is **Commutative**







$$
\begin{aligned}
a \cdot b &= |a||b|\cos\theta \\
b \cdot a &= |b||a|\cos(360 - \theta) \\
& = |a||b|\cos\theta \\
a \cdot b & = b \cdot a
\end{aligned}
$$







The dot product is also **Distributive** meaning that you can compute the scalar product without $\theta$







$$
\begin{aligned}
a \cdot b= & \space \left(a_1 \mathbf{i}+a_2 \mathbf{j}+a_3 \mathbf{k}\right) \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) \\
= & \space\space a_1 \mathbf{i} \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right)  +a_2 \mathbf{j} \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) +a_3 \mathbf{k} \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) \\
\\
= & \space\left(a_1 \mathbf{i}\right) \cdot\left(b_1 \mathbf{i}\right)+\left(a_1 \mathbf{i}\right) \cdot\left(b_2 \mathbf{j}\right)+\left(a_1 \mathbf{i}\right) \cdot\left(b_3 \mathbf{k}\right) \\
& +\left(a_2 \mathbf{j}\right) \cdot\left(b_1 \mathbf{i}\right)+\left(a_2 \mathbf{j}\right) \cdot\left(b_2 \mathbf{j}\right)+\left(a_2 \mathbf{j}\right) \cdot\left(b_3 \mathbf{k}\right) \\
& +\left(a_3 \mathbf{k}\right) \cdot\left(b_1 \mathbf{i}\right)+\left(a_3 \mathbf{k}\right) \cdot\left(b_2 \mathbf{j}\right)+\left(a_3 \mathbf{k}\right) \cdot\left(b_3 \mathbf{k}\right) \\
\\
= & \space \left(a_1 b_1\right) \mathbf{i} \cdot \mathbf{i}+\left(a_1 b_2\right) \mathbf{i} \cdot \mathbf{j}+\left(a_1 b_3\right) \mathbf{i} \cdot \mathbf{k} \\
& +\left(a_2 b_1\right) \mathbf{j} \cdot \mathbf{i}+\left(a_2 b_2\right) \mathbf{j} \cdot \mathbf{j}+\left(a_2 b_3\right) \mathbf{j} \cdot \mathbf{k} \\
& +\left(a_3 b_1\right) \mathbf{k} \cdot \mathbf{i}+\left(a_3 b_2\right) \mathbf{k} \cdot \mathbf{j}+\left(a_3 b_3\right) \mathbf{k} \cdot \mathbf{k} \\
\\
a \cdot b= & \space a_1 b_1+a_2 b_2+a_3 b_3
\end{aligned}
$$







Using this you can compute the angle with just a simple expression






$$
\cos (\theta) = \frac{a \cdot b}{|a||b|} =\frac{a_1b_1 + a_2b_2 + a_3b_3}{|a||b|}
$$







## Planes in The Form $r \cdot n = k$
Suppose a plane $\Uppi$ passes through $A$ and has normal vector $n$ and let $R$ be an arbitrary point on $\Uppi$. Then $\overrightarrow {AR} = r - a$. Since $\overrightarrow {AR}$ lies on $\Uppi$, $\overrightarrow {AR}\cdot n = 0$ so $(r-a) \cdot n = 0 \Rightarrow r \cdot n = a \cdot n$ where $a \cdot n$ is a constant so $a\cdot n = k$. This can also be written as $n_1x+n_2y+n_3z = k$. Where $k$ represents the [[LEGACY Vectors#Perpendicular Distances|perpendicular distance]] from the origin to the place if $n = \hat{n}$
## Angles Between Vectors and Planes
The ***Acute*** angle $\theta$ between 2 intersecting ***Straight Lines*** *(with direction vectors $a, b$)* is given with the formula $\displaystyle\cos \theta = \left|\frac{a \cdot b}{|a||b|}\right|$

The ***Acute*** angle $\theta$ between ***Straight Line*** *(with direction vectors $r = a + \lambda b$)* and ***Plane*** *(with equation $r.n = k$)* is given with the formula $\displaystyle\sin \theta = \left|\frac{b \cdot n}{|b||n|}\right|$

The ***Acute*** angle $\theta$ between 2 intersecting ***Planes*** *(with equations vectors $r.n_1 = k_1$ and $r.n_2 = k_2$)* is given with the formula $\displaystyle\cos \theta = \left|\frac{n_1 \cdot n_2}{|n_1||n_2|}\right|$
## Points of Intersection
To find if 2 lines $l_1: r = a + \lambda b$ and $l_2: r = c + \mu d$ intersect set them equal and solve the system of equations, if solutions for $\mu$ and $\lambda$ exist then they intersect, if not then there is no intersection.
Two lines are **skew** if they do not intersect but are parallel meaning solutions for  $\mu$ and $\lambda$ don't exist but their direction vectors are scalar multiples of each other.

To find the intersection of a plane and a line have the plane in the form $r.n = k$ then sub in the vector equation $r = a + \lambda b$ into the plane equation. 

## Perpendicular Distances
To find the shortest/perpendicular distance between 2 lines $l_1: r = a + \lambda b$ and $l_2: r = c + \mu d$, Let $A$ be a point on $l_1$ and $B$ be a point on $l_2$ then shortest/perpendicular distance between $l_1$ and $l_2$ will be the straight line segment $AB$ that is perpendicular to both lines. So $l_1 \cdot AB = l_2 \cdot AB = 0$ you can then solve for $\mu$ and $\lambda$
To find shortest distance between a line $l$ and a point $A$, Let $B$ be a point on $l$ then $l \cdot AB = 0$. You can then find the coordinates of $B$ so you can find the distance
The perpendicular distance from the origin to the plane $r\cdot \hat n = k$ is simply k
The perpendicular distance from a point $(x_0, y_0, z_0)$ to the plane $ax + by + cz = d$ is 







$$
\frac{|ax_0 + by_0 + cz_0 - d|}{\sqrt{a^2 + b^2 + c^2}}
$$







The distance between two parallel planes $ax + by + cz = d_1$ and $ax + by + cz = d_2$ is 






$$
\frac{|d_1 - d_2|}{\sqrt{a^2 + b^2 + c^2}}
$$








---
# A-Level Further Pure 1
## Vector Cross Product $a \times b = |a||b| \sin (\theta) \hat{n}$
### Definition 
The cross product is defined as $a \times b = |a||b| \sin (\theta) \hat{n}$.
It is **Commutative** and **Distributive**







$$
\begin{aligned}
a\times b & =(a_{1}\mathbf{i}+a_{2}\mathbf{j}+a_{3}\mathbf{k})\times(b_{1}\mathbf{i}+b_{2}\mathbf{j}+b_{3}\mathbf{k}) \\
 & =a_{1}b_{1}(\mathbf{i}\times\mathbf{i})+a_{1}b_{2}(\mathbf{i}\times\mathbf{j})+a_{1}b_{3}(\mathbf{i}\times\mathbf{k}) \\
 & +a_2b_1(\mathbf{j}\times\mathbf{i})+a_2b_2(\mathbf{j}\times\mathbf{j})+a_2b_3(\mathbf{j}\times\mathbf{k}) \\
 & +a_3b_1(\mathbf{k}\times\mathbf{i})+a_3b_2(\mathbf{k}\times\mathbf{j})+a_3b_3(\mathbf{k}\times\mathbf{k} \\
 & =a_{1}b_{2}\mathbf{k}+a_{1}b_{3}(-\mathbf{j})+a_{2}b_{1}(-\mathbf{k})+a_{2}b_{3}(\mathbf{i})+a_{3}b_{1}(\mathbf{j})+a_{3}b_{2}(-\mathbf{i}) \\\\
 a\times b& =(a_{2}b_{3}-a_{3}b_{2})\mathbf{i}+(a_{3}b_{1}-a_{1}b_{3})\mathbf{j}+(a_{1}b_{2}-a_{2}b_{1})\mathbf{k}\\ \\
a \times b & =
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
a_1 & a_2 & a_3 \\
b_1 & b_2 & b_3
\end{vmatrix}=\mathbf{i}
\begin{vmatrix}
a_2 & a_3 \\
b_2 & b_3
\end{vmatrix}-\mathbf{j}
\begin{vmatrix}
a_1 & a_3 \\
b_1 & b_3
\end{vmatrix}+\mathbf{k}
\begin{vmatrix}
a_1 & a_2 \\
b_1 & b_2
\end{vmatrix} \\ \\
 & =(a_2b_3-a_3b_2)\mathbf{i}+(a_3b_1-a_1b_3)\mathbf{j}+(a_1b_2-a_2b_1)\mathbf{k}
 \end{aligned}
$$







$\theta$ is the angle between $a$ and $b$ where $0 \leq \theta \leq 180 \degree$. And $\hat{n}$ is the unit vector perpendicular to both $a$ and $b$ 
### Right Hand Rule
The direction of $\hat{n}$ depends on the right-hand rule 
![[Vectors-Right-Hand-Rule.png|400]]


Swapping $a$ and $b$ means that $\hat{n} \mapsto -\hat{n}$ therefore $b \times a = |b||a| \sin (\theta) (-\hat{n}) = - a\times b$
## Areas







$$
\text{Triangle Area} = \frac{1}{2}|a \times b| \quad \text{Parellelogram Area} = |a \times b|
$$







## Finding Volumes - Scalar Triple Product $a \cdot (b \times c)$







$$
a \cdot (b \times c) \equiv\begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix}\equiv a_1(b_2c_3 - b_3c_2) + a_2(b_3c_1 - c_3b_1) + a_3(b_1c_2 - b_2c_1)
$$







## Straight Lines $(r-a)\times b = 0$
Suppose $a$ is the position vector of a point on a line and the line is parallel to $b$. Let $r$ be the position vector of a general point on the line. so $\overrightarrow{AR} = \overrightarrow{OR} - \overrightarrow{OA} = r-a$. Since $\overrightarrow{AR}$ is parallel to $b$, $\overrightarrow{AR} \times b = 0$ so $(r-a)\times b = 0$
## Direction of Cosines
If a line is parallel to the vector $a = xi +yj+zk$ the direction ratios are $x:y:z$ and the direction of cosines of the line are 






$$
\cos \theta_x = \frac{x}{|a|} = l \quad \cos \theta_y = \frac{y}{|a|} = m \quad \cos \theta_z = \frac{z}{|a|} = n
$$







The sum of the squares of the direction cosines is always one 






$$
l^2 + m^2+n^2 = \frac{x^2+y^2+z^2}{|a|^2} = \frac{|a|^2}{|a|^2}= 1
$$








---
