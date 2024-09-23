# A-Level Further Core 1

## Straight Line Vectors

The equation of a straight line vector passing through point $a$ and position vector $b$ is: $$r = a + \lambda b$$ where $r$ is the **position** vector of a general point on the line so by taking varying values of $\lambda$ you can find the position vectors of varying points that lie on the straight line

The equation of a straight line vector passing through points $C, D$ is: $r = C + \lambda(D-C)$ this is because you can use the first form but take $b$ to be the vector $\overrightarrow{CD}$ which is given by $D-C$ 

If the equation of a straight line in 3 dimensions given by the vector equation $r = a + \lambda b$ with vectors $\begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix}$, $\begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix}$, the Cartesian equation is:

$$\frac{x-a_1}{b_1} = \frac{y-a_2}{b_2} = \frac{z-a_3}{b_3}$$
***Colinear***: Points are said to be *collinear* if they all lie on the same straight line

## Plane Vectors

The vector of a plane that through position vector $a$ is: $$r = a + \lambda b + \mu c$$
where r is the **position** vector of a general point on the plane with $a$ being the position vector of a *fixed* arbitrary point on the plane and $b, c$ are *non-parallel, non-zero* vectors *on the plane* and $\lambda, \mu$ being scalars to obtain varying points on the plane.
*The intuition of this is that $a$ gets you from the origin onto the plane and $\lambda b, \mu c$ allow you to move across the plane*

The Cartesian equation of a plane is $ax + by + cz = d$ where the normal vector to the plane is $$\begin{pmatrix} a \\ b \\ c \end{pmatrix}$$ *this result can be proved with the scalar product*

## Scalar Product

The ***scalar*** product (also called dot product) between 2 vectors $a, b$ is given by the equation $$a\cdot b = |a||b| \cos \theta$$
where $\theta$ is the angle between $a$ and $b$. *When measuring $\theta$ make sure that $a$ & $b$ are both facing away from X*
The dot product is commutative as although when switching a, b the angle changes from $\theta$ to $360 - \theta$ this simplifies to $\cos (360- \theta) = \cos (\theta)$

You can also derive that $$\cos (\angle AOB) = \frac{a \cdot b}{|a||b|} =\frac{a_1b_1 + a_2b_2 + a_3b_3}{|a||b|}$$

* The non-zero vectors $a$ and $b$ are perpendicular if and only if $a \cdot b = 0$
* If $a$ and $b$ are are parallel then $a.b$ = $|a||b|$ = $a \cdot a$ = ${|a|}^{2}$ 

If $a = a_1i + a_2j + a_3k$ and $b = b_1i + b_2j + b_3k$ then

$$a \cdot b = \begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix} \cdot \begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix} = a_1b_1 + a_2b_2 + a_3b_3$$
*(This is derived by multiplying a and b by expanding then brackets and taking the dot product for every term the using the results from the dot product of unit vectors to cancel terms as $a \cdot (b+c) \equiv a \cdot b + a \cdot c$)*

 > 
 > \[!example\]- Proof
 > $$\begin{aligned}
 > a \cdot b= & \left(a_1 \mathbf{i}+a_2 \mathbf{j}+a_3 \mathbf{k}\right) \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) \\
 > = & a_1 \mathbf{i} \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) \\
 > & +a_2 \mathbf{j} \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) \\
 > & +a_3 \mathbf{k} \cdot\left(b_1 \mathbf{i}+b_2 \mathbf{j}+b_3 \mathbf{k}\right) \\
 > = & \left(a_1 \mathbf{i}\right) \cdot\left(b_1 \mathbf{i}\right)+\left(a_1 \mathbf{i}\right) \cdot\left(b_2 \mathbf{j}\right)+\left(a_1 \mathbf{i}\right) \cdot\left(b_3 \mathbf{k}\right) \\
 > & +\left(a_2 \mathbf{j}\right) \cdot\left(b_1 \mathbf{i}\right)+\left(a_2 \mathbf{j}\right) \cdot\left(b_2 \mathbf{j}\right)+\left(a_2 \mathbf{j}\right) \cdot\left(b_3 \mathbf{k}\right) \\
 > & +\left(a_3 \mathbf{k}\right) \cdot\left(b_1 \mathbf{i}\right)+\left(a_3 \mathbf{k}\right) \cdot\left(b_2 \mathbf{j}\right)+\left(a_3 \mathbf{k}\right) \cdot\left(b_3 \mathbf{k}\right) \\
 > = & \left(a_1 b_1\right) \mathbf{i} \cdot \mathbf{i}+\left(a_1 b_2\right) \mathbf{i} \cdot \mathbf{j}+\left(a_1 b_3\right) \mathbf{i} \cdot \mathbf{k} \\
 > & +\left(a_2 b_1\right) \mathbf{j} \cdot \mathbf{i}+\left(a_2 b_2\right) \mathbf{j} \cdot \mathbf{j}+\left(a_2 b_3\right) \mathbf{j} \cdot \mathbf{k} \\
 > & +\left(a_3 b_1\right) \mathbf{k} \cdot \mathbf{i}+\left(a_3 b_2\right) \mathbf{k} \cdot \mathbf{j}+\left(a_3 b_3\right) \mathbf{k} \cdot \mathbf{k} \\
 > = & a_1 b_1+a_2 b_2+a_3 b_3
 > \\end{aligned}$$

You can use the scalar product to write the equation of a plane efficiently with the equations $$\quad r \cdot n = k \quad \begin{pmatrix} x \\y \\z \end{pmatrix} \cdot \begin{pmatrix} n_1 \\ n_2 \\n_3 \end{pmatrix} = k \quad n_1x+n_2y+n_3z = k$$ \*where $k = a \cdot n$ with $a$ being any point on the plane

## Angles Between Vectors and Planes

* The ***Acute*** angle $\theta$ between 2 intersecting ***Straight Lines*** *(with direction vectors $a, b$)* is given with the formula $$\cos \theta = \left|\frac{a \cdot b}{|a||b|}\right|$$
* The ***Acute*** angle $\theta$ between ***Straight Line*** *(with direction vectors $r = a + \lambda b$)* and ***Plane*** *(with equation $r.n = k$)* is given with the formula $$\sin \theta = \left|\frac{b \cdot n}{|b||n|}\right|$$
* The ***Acute*** angle $\theta$ between 2 intersecting ***Planes*** *(with equations vectors $r.n_1 = k_1$ and $r.n_2 = k_2$)* is given with the formula $$\cos \theta = \left|\frac{n_1 \cdot n_2}{|n_1||n_2|}\right|$$
  ***In all of these formulae the modulus sign around the whole expression ensures you get the acute angles***

## Plane $\Uppi$

Give: $\left|\frac{x-a_1}{b_1}\right| = \left|\frac{y-a_2}{b_2}\right| = \left|\frac{z-a_3}{b_3}\right|$

The perpendicular distance from a point $(x_0, y_0, z_0)$ to the plane $ax + by + cz = d$ when $\vec{n} = (a,b,c)$ is a unit vector is:

$$\frac{|ax_0 + by_0 + cz_0 - d|}{\sqrt{a^2 + b^2 + c^2}}$$

The distance between two parallel planes $ax + by + cz = d_1$ and $ax + by + cz = d_2$ is:

$$\frac{|d_1 - d_2|}{\sqrt{a^2 + b^2 + c^2}}$$

## Flashcards

\#Maths/A-Level-Further-Core/Vectors, #Maths/Topics/Vectors

How do you calculate the perpendicular distance from a point $(x_0, y_0, z_0)$ to a plane $ax + by + cz = d$ when $\vec{n} = (a,b,c)$ is a unit vector?
?
$$\frac{|ax_0 + by_0 + cz_0 - d|}{\sqrt{a^2 + b^2 + c^2}}$$ <!--SR:!2024-09-19,1,130-->

How do you calculate the distance between two parallel planes $ax + by + cz = d_1$ and $ax + by + cz = d_2$?
?
$$\frac{|d_1 - d_2|}{\sqrt{a^2 + b^2 + c^2}}$$ <!--SR:!2024-09-19,1,130-->

# A-Level Further Pure 1

## Vector Cross Product

The cross product of vectors $a$ and $b$ is:

$$a \times b = |a||b| \sin \theta \hat{n}$$

where $\theta$ is the angle measured counter clockwise between $a$ and $b$, and $\hat{n}$ is the unit vector perpendicular to both $a$ and $b$ (think that $a$ and $b$ lie on a flat plane - $\hat{n}$ is the normal to that plane where $a$ and $b$ intersect).

The direction of $\hat{n}$ depends on the right-hand rule (also what direction a screw would move if it's twisted from $a$ to $b$).

So going from $a$ to $b$ yields $\hat{n}$ but $b$ to $a$ yields $-\hat{n}$. This leads to:

$$a \times b \neq b \times a$$
$$a \times b = -b \times a$$

If $a \times b = 0$ either $a$ or $b = 0$ or $\sin \theta = 0$, so $\theta = 0$ or $180°$, so $a$ and $b$ are parallel.

By using the distributive law of $a \times (b+c) = (a \times b) + (b \times c)$ for the cross product with the results of the cross products of unit vectors $\hat{i}, \hat{j}, \hat{k}$ $(\hat{i}, \hat{j}, \hat{k})$ and writing vectors $a$, $b$ as column vectors you can obtain that for vectors $a$, $b$:

$$a = \begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix}, b = \begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix}$$

$$\begin{aligned}
a \times b &= (a_2b_3 - a_3b_2)\hat{i} + (a_3b_1 - a_1b_3)\hat{j} + (a_1b_2 - a_2b_1)\hat{k} \\
a \times b &= \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix} = \hat{i} \begin{vmatrix} a_2 & a_3 \\ b_2 & b_3 \end{vmatrix} - \hat{j} \begin{vmatrix} a_1 & a_3 \\ b_1 & b_3 \end{vmatrix} + \hat{k} \begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix}
\\end{aligned}$$

The second is simply the determinant of matrix with vectors $(\hat{i}, \hat{j}, \hat{k})$, $a$, $b$.

Here's the transcription of the note with LaTeX formatting and added flashcards:

## Finding Areas

The area of triangle OAB with vectors $a$ and $b$ is:

$$\text{area} = \frac{1}{2}|a \times b|$$

For triangle ABC you get:

$$\text{area} = \frac{1}{2}|\overrightarrow{AB} \times \overrightarrow{AC}| = \frac{1}{2}|(b-a) \times (c-a)| = \frac{1}{2}|(b \times c) + (c \times a) + (a \times b)|$$

To get formula for the corresponding parallelogram simply drop the $\frac{1}{2}$ in front.

## Scalar Triple Product / Finding Volumes

You can find the scalar triple product of 3 vectors $a$, $b$, $c$ to find the volume of a parallelepiped (a 3D parallelogram) and a tetrahedron.

The scalar triple product is given by:

$$a \cdot (b \times c) = a_1(b_2c_3 - b_3c_2) + a_2(b_3c_1 - c_3b_1) + a_3(b_1c_2 - b_2c_1)$$

and

$$a \cdot (b \times c) = \begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix}$$

*(The difference of the determinant form being $a_i + a_j + a_k$ whereas the top is $d + e + f$ is because in the middle they flipped $b_2c_3 - b_3c_1$ to $b_3c_1 - c_3b_1$ to negate it to have all addition as $- \times - = +$)*

## Flashcards

\#Maths/Topics/Vectors, #Maths/A-Level-Further-Pure/Vectors

What is the formula for the cross product of vectors $a$ and $b$?
?
The cross product of vectors $a$ and $b$ is given by:
$$a \times b = |a||b| \sin \theta \hat{n}$$
where $\theta$ is the angle measured counter clockwise between $a$ and $b$, and $\hat{n}$ is the unit vector perpendicular to both $a$ and $b$. <!--SR:!2024-09-18,3,244-->

What does the unit vector $\hat{n}$ represent in the cross product formula?
?
In the cross product formula $a \times b = |a||b| \sin \theta \hat{n}$, the unit vector $\hat{n}$ represents the vector perpendicular to both $a$ and $b$. It is the normal vector to the plane containing $a$ and $b$. <!--SR:!2024-09-18,3,244-->

How does the direction of $\hat{n}$ in the cross product depend on the order of vectors?
?
The direction of $\hat{n}$ depends on the right-hand rule. Going from $a$ to $b$ yields $\hat{n}$, but going from $b$ to $a$ yields $-\hat{n}$. This leads to the property $a \times b = -b \times a$. <!--SR:!2024-09-18,3,244-->

What is the relationship between $a \times b$ and $b \times a$?
?
The relationship between $a \times b$ and $b \times a$ is:
$$a \times b \neq b \times a$$
$$a \times b = -b \times a$$
This means that the cross product is anti-commutative. <!--SR:!2024-09-18,3,244-->

When does the cross product $a \times b$ equal zero?
?
The cross product $a \times b = 0$ in the following cases:

1. Either $a$ or $b$ is zero
1. $\sin \theta = 0$, which means $\theta = 0$ or $180°$
   In other words, the cross product is zero when the vectors are parallel or when one of them is zero. <!--SR:!2024-09-18,3,244-->

What is the distributive law for cross products?
?
The distributive law for cross products states:
$$a \times (b+c) = (a \times b) + (b \times c)$$
This law is used to derive the component form of the cross product. <!--SR:!2024-09-16,1,204-->

How can the cross product be expressed in terms of vector components?
?
For vectors $a = (a_1, a_2, a_3)$ and $b = (b_1, b_2, b_3)$, the cross product can be expressed as:
$$a \times b = (a_2b_3 - a_3b_2)\hat{i} + (a_3b_1 - a_1b_3)\hat{j} + (a_1b_2 - a_2b_1)\hat{k}$$ <!--SR:!2024-09-16,1,204-->

How can the cross product be represented using a determinant?
?
The cross product can be represented using a determinant as follows:
$$a \times b = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix}$$
This determinant can be expanded to obtain the component form of the cross product. <!--SR:!2024-09-18,3,244-->

What is the formula for the area of a triangle OAB given vectors $a$ and $b$?
?
The area of triangle OAB with vectors $a$ and $b$ is given by:
$$\text{area} = \frac{1}{2}|a \times b|$$
where $|a \times b|$ is the magnitude of the cross product of vectors $a$ and $b$. <!--SR:!2024-09-17,2,224-->

How can you calculate the area of a triangle ABC using vector cross products?
?
The area of triangle ABC can be calculated using the formula:
$$\text{area} = \frac{1}{2}|\overrightarrow{AB} \times \overrightarrow{AC}| = \frac{1}{2}|(b-a) \times (c-a)| = \frac{1}{2}|(b \times c) + (c \times a) + (a \times b)|$$
where $a$, $b$, and $c$ are the position vectors of points A, B, and C respectively. <!--SR:!2024-09-18,3,244-->

How does the formula for the area of a parallelogram differ from that of a triangle?
?
The formula for the area of a parallelogram is the same as that for a triangle, but without the factor of $\frac{1}{2}$. So, for a parallelogram with sides represented by vectors $a$ and $b$, the area is:
$$\text{area} = |a \times b|$$ <!--SR:!2024-09-18,3,244-->

What is the scalar triple product used for in geometry?
?
The scalar triple product of vectors $a$, $b$, and $c$ is used to find the volume of a parallelepiped (a 3D parallelogram) and a tetrahedron. It represents the signed volume of the parallelepiped defined by these three vectors. <!--SR:!2024-09-18,3,244-->

What is the formula for the scalar triple product?
?
The scalar triple product of vectors $a$, $b$, and $c$ can be calculated using two equivalent formulas: <!--SR:!2024-09-16,1,204-->

1. Using cross and dot products:
   $$a \cdot (b \times c) = a_1(b_2c_3 - b_3c_2) + a_2(b_3c_1 - c_3b_1) + a_3(b_1c_2 - b_2c_1)$$

1. Using a determinant:
   $$a \cdot (b \times c) = \begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix}$$

Why is there a difference in sign between the expanded form and the determinant form of the scalar triple product?
?
The difference in sign between the expanded form and the determinant form of the scalar triple product is due to a rearrangement of terms. In the middle term of the expanded form, $b_2c_3 - b_3c_1$ is flipped to $b_3c_1 - c_3b_1$ to negate it. This is done to have all additions in the form of $- \times - = +$, making the overall expression consistent in terms of sign. <!--SR:!2024-09-16,1,204-->

How is the volume of a tetrahedron related to the scalar triple product?
?
The volume of a tetrahedron formed by vectors $a$, $b$, and $c$ from a common point is given by:
$$V\_{tetrahedron} = \frac{1}{6}|a \cdot (b \times c)|$$
where $a \cdot (b \times c)$ is the scalar triple product. The factor of $\frac{1}{6}$ is used because the scalar triple product gives the volume of the parallelepiped, which is six times the volume of the tetrahedron. <!--SR:!2024-09-18,3,244-->
