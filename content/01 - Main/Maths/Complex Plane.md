# Definitions
Complex Numbers can be represented on a cartesian plane *(Called the complex plane or an Argand diagram)* as a point$(x, y)$ or vector $\begin{pmatrix} x \\ y \end{pmatrix}$ where $z=x+y$. Therefore the $x$-axis is the real axis and the $y$-axis is the imaginary axis.
# A-Level Further Core 1
## Modulus-Argument form
For any complex number $a+b i$ it can be written as: $r(\cos \theta+i \sin \theta)$ where $\theta=\operatorname{arg}(z)$ and $r=|z|$.
#### Modulus
The modulus of a complex number $z$ is written as $|z|$ and it is is defined as $\sqrt{a^2+b^2}$ where $z=a+b i$. $|z|$ is geometrically represented as the distance from the origin to $z$ on the complex plane.
#### Argument 
The argument $z$ *written as $arg(z)$* is the angle $\theta$ such that $\tan \theta=\frac{y}{x}$ - it is given in radians typically given in the range $\pi -\pi<\theta \leq \pi$ *(This is called the principal argument)* This angle  represents the angle rotation from the $x$-axis

### Basic Operations
#### Multiplication
Using this form you can obtain the results that for complex numbers $z_1$ and $z_2$
$$\left|z_1 z_2\right|=\left|z_1\right| \times\left|z_2\right|$$$$\arg (z_1 z_2)=\operatorname{arg}(z_1)+\operatorname{arg}(z_2)$$ allowing for easy multiplication of complex numbers in the modulus-argument form.

> [!example]- Proof
To prove these results, consider $z_1$ and $z_2$ in modulus-argument form: $$z_1=r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right) \text { and } z_2=r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)$$
Multiplying these numbers together, you get$$
\begin{aligned}
z_1 z_2 & =r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right) \times r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1 \cos \theta_2+\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2+\mathrm{i}^2 \sin \theta_1 \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1 \cos \theta_2+\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2-\sin \theta_1 \sin \theta_2\right) \\
& =r_1 r_2\left(\left(\cos \theta_1 \cos \theta_2-\sin \theta_1 \sin \theta_2\right)+\mathrm{i}\left(\sin \theta_1 \cos \theta_2+\cos \theta_1 \sin \theta_2\right)\right) \\
& =r_1 r_2\left(\cos \left(\theta_1+\theta_2\right)+\mathrm{i} \sin \left(\theta_1+\theta_2\right)\right)
\end{aligned}$$
The last step works with the [[Trig Identities|Trig Addition Formulae]]
$\sin (A \pm B) \equiv \sin A \cos B \pm \cos A \sin B$
$\cos (A \pm B) \equiv \cos A \cos B \mp \sin A \sin B$
This complex number is in modulus-argument form, with modulus $r_1 r_2$ and argument $\theta_1+\theta_2$, as required.

#### Division
You can also prove that: $$\left|\frac{z_1}{z_2}\right|=\frac{|z_1|}{|z_2|}$$$$\operatorname{arg}\left(\frac{z_1}{z_2}\right)=\operatorname{arg}(z_1)-\operatorname{arg}(z_2)$$

> [!example]- Proof
To prove these results, again consider $z_1$ and $z_2$ in modulus-argument form:
> $$z_1=r_1\left(\cos \theta_1+i \sin \theta_1\right) \text { and } z_2=r_2\left(\cos \theta_2+i \sin \theta_2\right)$$ 
> $$\begin{aligned}
\frac{z_1}{z_2} & =\frac{r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)}{r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)} \\
& =\frac{r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)}{r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)} \times \frac{\left(\cos \theta_2-\mathrm{i} \sin \theta_2\right)}{\left(\cos \theta_2-\mathrm{i} \sin \theta_2\right)} \\
& =\frac{r_1\left(\cos \theta_1 \cos \theta_2-\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2-\mathrm{i}^2 \sin \theta_1 \sin \theta_2\right)}{r_2\left(\cos \theta_2 \cos \theta_2-\mathrm{i} \cos \theta_2 \sin \theta_2+\mathrm{i} \sin \theta_2 \cos \theta_2-\mathrm{i}^2 \sin \theta_2 \sin \theta_2\right)} \\
& =\frac{r_1\left(\left(\cos \theta_1 \cos \theta_2+\sin \theta_1 \sin \theta_2\right)+\mathrm{i}\left(\sin \theta_1 \cos \theta_2-\cos \theta_1 \sin \theta_2\right)\right)}{r_2\left(\cos ^2 \theta_2+\sin ^2 \theta_2\right)} \\
& =\frac{r_1}{r_2}\left(\cos \left(\theta_1-\theta_2\right)+\mathrm{i} \sin \left(\theta_1-\theta_2\right)\right)
\end{aligned}$$
The last step works with the [[Trig Identities|Trig Addition Formulae]] $\sin ^2 \theta+\cos ^2 \theta \equiv 1$
This complex number is in modulus-argument form, with modulus $\frac{r_1}{r_2}$ and argument $\theta_1-\theta_2$, as required.


## Loci
- For 2 [[Complex Numbers]] $z_1, z_2$ $|z_2-z_1|$ represents the distance between points $z_1, z_2$ on [[Complex Plane]].
- You can replace $z_2$ with the general point $z$ to obtain a locus of points described by $\left|z-z_1\right|=r$. This locus forms a circle with centre $\left(z_1.x, z_1.y\right)$ with radius $r$, you can then derive the cartesian equation $\left(z.x - z_1.x\right)^2+\left(z.y - z_1.y\right)^2=r^2$. Also written as $\left(x-x_1\right)^2+\left(y-y_1\right)^2=1^2$
- For any 2 complex numbers $z_1, z_2$ the locus $\left|z-z_1\right|=\left|z-z_2\right|$ is the perpendicular bisector of the line segment connecting $z_1, z_2$
- Given complex number $z_1$ the locus of points described by $\arg \left(z-z_1\right)=\theta$  forms a straight half-line that makes angle $\theta$ with the line extending from $z_1$ that is parallel to the real axis but does not include $z_1$ this is shown by drawing a hollow circle at $z_1$. The straight line described by the locus only extents one way as the condition $\arg \left(z-z_1\right)=\theta$ specifies a specific direction determined by $\theta$. 
# A-Level Further Pure 2
## Locus On Complex Plane

### $|z-a| = k|z-b|$ 
The locus of points $z$ that satisfy $|z-a| = k|z-b|$ where $a,b \in \mathbb{C}$, $k\in \mathbb{R}, k>0, k\neq 1$ is a circle. You can find the equation by splitting $z$ into $x+iy$ then squaring both sides (which gets rid of modulus and $i$ terms) and solving from there.
The locus in words: The locus of points that are $k$ times further from $a$ than they are from $b$.

*(When $k=1$ it's a straight line perpendicular bisector which can be thought of as a circle with infinite radius)*

### $\arg(\frac{z-a}{z-b}) = \theta$
The Locus $\arg(\frac{z-a}{z-b}) = \theta$ is an arc of a circle with end points $A,B$. The arc is drawn **anticlockwise** from $A$ to $B$. You can find the equation of a circle by considering the $z$ congruent isosceles triangles formed by $ACM$, $BCM$ where $C$ is the circle centre and $M$ is the midpoint of $AB$.

###  $\theta_1 \leq \arg(z-z_1) \leq \theta$
The Locus of $\theta_1 \leq \arg(z-z_1) \leq \theta_2$ describes the region enclosed by 2 half lines $\arg(z-z_1) = \theta_1$ and $\arg(z-z_1) = \theta_2$.

## Transformations on the Complex Plane

- You can transform loci by mapping the $z$ plane onto a $w$ plane to get $z = x+iy \rightarrow w = u+iv$
- $w = z+a+ib$ represents translation by $\begin{pmatrix} a \\ b \end{pmatrix}$, $a,b \in \mathbb{R}$
- $w = kz$, $k\in \mathbb{R}$ represents enlargement with scale factor $k$ centre $(0,0)$
- $w = iz$ represents anti-clockwise rotation of $\frac{\pi}{2}$ about $(0,0)$
### Möbius transformations

They are transformations in the form $w = \frac{az+b}{cz+d}$, $a,b,c,d \in \mathbb{C}$
You can solve by rearranging into a familiar form.
