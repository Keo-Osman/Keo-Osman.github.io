# Definition
A complex number is a number that is written as: $a+b i$ where $i$ is the imaginary unit defined as $\sqrt{-1}$ and $a, b \in \mathbb{R}$. *The set of all complex numbers is written as $\mathbb{C}$*

---
# A-Level Further Core 1
## The Complex Conjugate
For $z = a+bi$,  $z^* = a-bi$
$z+z^*$ is always real as the imaginary parts cancel so $z+z^*=2 a$
$z+z^*$ is also always real as it’s a difference of two squares
$$(a+b i)(a-b i)=a^2-(b i)^2=a^2-\left(b^2 i^2\right)=a^2-\left(-b^2\right)=a^2+b^2$$
## Basic operations
### Addition and Subtraction
For addition and subtraction you combine real and imaginary terms separately$(a+b i) \pm(c+d i)=(a+c) \pm(b+d) i$
### Multiplication
For multiplication just expand brackets ex. $(a+b i)(c+d i)=$ $a c+(b c) i+(a d) i+b d i^2$ since $i^2=-1$ this is equivalent to $(a c-b d)+(b c+a d)i$
### Division
 For division multiply the numerator and denominator by the complex conjugate of the numerator.
$$\frac{a+b i}{c+d i}=\frac{a+b i)(c-d i)}{(c+d i)(c-d i)} = \frac{a c+b d}{c^2+d^2}+\left(\frac{b c-a d}{c^2+d^2}\right)i
$$
## Roots of Polynomials
The possible cases of roots of polynomials are as follows:
**Quadratic:**  
- $\alpha, \beta \in \mathbb{R}$ 
- $\alpha = z,\space \beta = z^*$ 
**Cubic:**
- $\alpha, \beta, \gamma \in \mathbb{R}$ 
- $\alpha \in \mathbb{R}, \space \beta = z, \gamma = z^*$ 
**Quartic:** 
- $\alpha, \beta, \gamma, \delta \in \mathbb{R}$
- $\alpha, \beta \in \mathbb{R}, \space \gamma = z, \delta = z^*$ 
- $\alpha = w, \space \beta = w^* \space \gamma = z, \delta = z^*$ 

## Modulus Argument Form
For any complex number $a+b i$ it can be written as: $r(\cos \theta+i \sin \theta)$ where $\theta=\operatorname{arg}(z)$ and $r=|z|$.
#### Modulus
The modulus of a complex number $z$ is written as $|z|$ and it is is defined as $\sqrt{a^2+b^2}$ where $z=a+b i$. $|z|$ is geometrically represented as the distance from the origin to $z$ on the complex plane.
#### Argument 
The argument $z$ *written as $arg(z)$* is the angle $\theta$ such that $\tan \theta=\frac{y}{x}$ - it is given in radians typically given in the range $\pi -\pi<\theta \leq \pi$ *(This is called the principal argument)* This angle  represents the angle rotation from the $x$-axis

### Basic Operations
#### Multiplication
$$\left|z_1 z_2\right|=\left|z_1\right| \times\left|z_2\right| \quad \arg (z_1 z_2)=\operatorname{arg}(z_1)+\operatorname{arg}(z_2)$$
$$
\begin{aligned}
z_1 z_2 & =r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right) \times r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1 \cos \theta_2+\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2+\mathrm{i}^2 \sin \theta_1 \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1 \cos \theta_2+\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2-\sin \theta_1 \sin \theta_2\right) \\
& =r_1 r_2\left(\left(\cos \theta_1 \cos \theta_2-\sin \theta_1 \sin \theta_2\right)+\mathrm{i}\left(\sin \theta_1 \cos \theta_2+\cos \theta_1 \sin \theta_2\right)\right) \\
& =r_1 r_2\left(\cos \left(\theta_1+\theta_2\right)+\mathrm{i} \sin \left(\theta_1+\theta_2\right)\right)
\end{aligned}$$

#### Division
You can also prove that: $$\left|\frac{z_1}{z_2}\right|=\frac{|z_1|}{|z_2|} \quad \operatorname{arg}\left(\frac{z_1}{z_2}\right)=\operatorname{arg}(z_1)-\operatorname{arg}(z_2)$$
$$\begin{aligned}
\frac{z_1}{z_2} & =\frac{r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)}{r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)} \\
& =\frac{r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)}{r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)} \times \frac{\left(\cos \theta_2-\mathrm{i} \sin \theta_2\right)}{\left(\cos \theta_2-\mathrm{i} \sin \theta_2\right)} \\
& =\frac{r_1\left(\cos \theta_1 \cos \theta_2-\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2-\mathrm{i}^2 \sin \theta_1 \sin \theta_2\right)}{r_2\left(\cos \theta_2 \cos \theta_2-\mathrm{i} \cos \theta_2 \sin \theta_2+\mathrm{i} \sin \theta_2 \cos \theta_2-\mathrm{i}^2 \sin \theta_2 \sin \theta_2\right)} \\
& =\frac{r_1\left(\left(\cos \theta_1 \cos \theta_2+\sin \theta_1 \sin \theta_2\right)+\mathrm{i}\left(\sin \theta_1 \cos \theta_2-\cos \theta_1 \sin \theta_2\right)\right)}{r_2\left(\cos ^2 \theta_2+\sin ^2 \theta_2\right)} \\
& =\frac{r_1}{r_2}\left(\cos \left(\theta_1-\theta_2\right)+\mathrm{i} \sin \left(\theta_1-\theta_2\right)\right)
\end{aligned}$$

---
# A-Level Further Core 2
## Exponential Form of Complex Numbers
### Derivation
By using the Taylor expansion of $e^x$ and plugging in $x = i\theta$, you can split the series to obtain $e^{i\theta} = \cos \theta + i \sin \theta$
$$\begin{aligned}
e^{i\theta} & =1+\mathrm{i}\theta+\frac{(\mathrm{i}\theta)^{2}}{2!}+\frac{(\mathrm{i}\theta)^{3}}{3!}+\frac{(\mathrm{i}\theta)^{4}}{4!}+\frac{(\mathrm{i}\theta)^{5}}{5!}+\frac{(\mathrm{i}\theta)^{6}}{6!}+\ldots \\
 & =1+\mathrm{i}\theta+\frac{\mathrm{i}^{2}\theta^{2}}{2!}+\frac{\mathrm{i}^{3}\theta^{3}}{3!}+\frac{\mathrm{i}^{4}\theta^{4}}{4!}+\frac{\mathrm{i}^{5}\theta^{5}}{5!}+\frac{\mathrm{i}^{6}\theta^{6}}{6!}+\ldots \\
 & =1+\mathrm{i}\theta-\frac{\theta^{2}}{2!}-\frac{\mathrm{i}\theta^{3}}{3!}+\frac{\theta^{4}}{4!}+\frac{\mathrm{i}\theta^{5}}{5!}-\frac{\theta^{6}}{6!}+\ldots \\
 & =\left(1-\frac{\theta^{2}}{2!}+\frac{\theta^{4}}{4!}-\frac{\theta^{6}}{6!}+\ldots\right)+\mathrm{i}\left(\theta-\frac{\theta^{3}}{3!}+\frac{\theta^{5}}{5!}-\ldots\right)
\end{aligned}$$
Then multiply by $r$ to get the general form of $z = re^{i\theta}$ where $r = |z|$ and $\theta = \arg(z)$

### Multiplication and Division
$$z_1 \times z_2 = r_1r_2 e^{i(\theta_1 + \theta_2)}$$
$$\frac{z_1}{z_2} = \frac{r_1}{r_2} e^{i(\theta_1 - \theta_2)}$$
## De Moivre's theorem
$$\begin{matrix}
(r(\cos \theta + i \sin \theta))^n \equiv r^n(\cos n\theta + i \sin n\theta)
\\
\forall n  \in \mathbb{Z}
\end{matrix}
$$
## Sum of Geometric Series
$$\sum_{r=0}^{n-1} wz^r = \frac{w(z^n-1)}{z-1}, \quad |z| < 1$$
$$\sum_{r=0}^{\infty} wz^r = \frac{w}{z-1}, \quad |z| < 1$$

## Nth Root of Complex Numbers
$z^n = w$ $\quad z, w \in \mathbb{C}, n \in \mathbb{N}$, $z, w \neq 0$
**To Solve**
- $z$ has the form $r(\cos \theta + i \sin \theta))$ so by [[Complex Numbers#De Moivre's theorem|De Moivre's Theorem]] $z^n = r^n(\cos (n\theta + 2k\pi) + i \sin (n\theta+2k\pi))$
- Compare the modulus to solve for $r$
- Then plug in $k= 1, 2, \dots, n$ and solve for $\theta$

---
