# Brilliant Linear Algebra Course
## Vector Space
A vector space $V$ is a non-empty set of objects $|v\rangle$ with some kind of
addition and scalar multiplication that satisfy the following:
- Additive associativity: $|u\rangle+(|v\rangle+|w\rangle)=(|u\rangle+|v\rangle)+|w\rangle$
- Multiplicative associativity: $a\left(b|v\rangle\right)=(ab)|v\rangle$ 
- Additive commutativity: $|v\rangle+|w\rangle=|w\rangle+|v\rangle$
- Existence of $|0\rangle:|v\rangle+|0\rangle=|v\rangle,|v\rangle+(-1)|v\rangle=|0\rangle$
- Multiplicative identity: $1|v\rangle=|v\rangle$ for all elements in $V$ 
- Scalar distributivity: $a\left(|v\rangle+|w\rangle\right)=a|v\rangle+a|w\rangle$
- Vector distributivity: $(a+b)|v\rangle=a|v\rangle+b|v\rangle$

## Waves as Vectors
The notation from the last animation is called a **ket**. It's a “wrapper” used to indicate that an object is a vector by writing "object" as $| \text{"object"}\rangle$. Waves wrapped in ket notation to emphasize their “vector” nature.

## Signals 
A **Signal** is the process and result of transmitting data over *time*. Generally real-valued function $f(t)$ and the set of all these functions is $F$.

All waves $\in F$ but the are special since they obey the property $w(t+1) = w(t)$ we note this subset of $F$ as $W$ *($W \subset F$)*.

**Both** $F$ and $W$ are **Vector Spaces** *This means you can call $W$ a **Subspace** of $F$*. 

TO approximate a signal we can ask. What $|w \rangle \in W$ is as close to $|f \rangle \in F$? 

## Cartesian Plane
The plane is made up of all real number pairs $(x, y)$ and addition and scalar multiplication are defined as follows $$(x_1, y_1) + (x_2, y_2) = (x_1+x_2, y_1+y_2)$$$$c(x, y) = (cx, cy)$$
This makes the Cartesian Plane a **Vector Space**
### Lines
Lines that pass through the origin in the cartesian plane, is a **Subspace** of the Cartesian Plane

## The Gauss-Jordan Process 
A **Linear System** is a collection of one or more linear equations in the same set of variables $x_1, \dotsc, x_n$ in the form
$$a_{i1}x_1+a_{i2}x_2 + \dots + a_{in}x_n=b_i$$  
$$\left\{\begin{array}{c}a_{11}x_1+\cdots+a_{1n}x_n=b_1\\\vdots\\a_{m1}x_1+\cdots+a_{mn}x_n=b_m\end{array}\right.\mapsto\left(\begin{array}{ccc|c}a_{11}&\dots&a_{1n}&b_1\\\vdots&\vdots&\vdots&\vdots\\a_{m1}&\dots&a_{mn}&b_m\end{array}\right)$$

