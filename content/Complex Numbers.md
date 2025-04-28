#Maths/Complex-Numbers
# Definition
A complex number is a number that is written as $a+b i$ where $i$ is the imaginary unit defined as $\sqrt{-1}$ and $a, b \in \mathbb{R}$. *The set of all complex numbers is written as $\mathbb{C}$*, it is an extension if [[The Real Numbers]]
Complex numbers have lots of applications as they are helpful when describing waves due to their connection with the [[Trigonometric Functions]] and their use in the [[Fourier Transform]]. They are also used in physics due to their ability to describe rotations and oscillations in 2 Dimensions neatly 

---
# The Complex Conjugate
For $z = a+bi$,  $z^* = a-bi$
$z+z^*$ is always real as the imaginary parts cancel so $z+z^*=2 a$
$z+z^*$ is also always real as it’s a difference of two squares








$$
(a+b i)(a-b i)=a^2-(b i)^2=a^2-\left(b^2 i^2\right)=a^2-\left(-b^2\right)=a^2+b^2
$$









---
# Forms of Complex Numbers

## Regular $a + bi$
### Basic operations








$$
(a+b i) \pm(c+d i)=(a+c) \pm(b+d) i
$$
















$$
(a+b i)(c+d i)= a c+(b c) i+(a d) i+b d i^2 = (a c-b d)+(b c+a d)i
$$
















$$
\frac{a+b i}{c+d i}=\frac{a+b i)(c-d i)}{(c+d i)(c-d i)} = \frac{a c+b d}{c^2+d^2}+\left(\frac{b c-a d}{c^2+d^2}\right)i
$$









## Modulus Argument Form $r(\cos \theta+i \sin \theta)$ 
Complex numbers can also be written with [[Trigonometric Functions]] in the form $r(\cos \theta+i \sin \theta)$ where $\theta=\operatorname{arg}(z)$ and $r=|z|$.
The **modulus** of a complex number $z$ is written as $|z|$ and it is is defined as $\sqrt{a^2+b^2}$ where $z=a+b i$. $|z|$ is geometrically represented as the distance from the origin to $z$ on the complex plane.
The **argument** $z$ *written as $arg(z)$* is the angle $\theta$ such that $\tan \theta=\frac{y}{x}$ - it is given in radians typically given in the range $\pi -\pi<\theta \leq \pi$ *(This is called the principal argument)* This angle represents the angle rotation from the $x$-axis
### Basic Operations
#### Multiplication








$$
\left|z_1 z_2\right|=\left|z_1\right| \times\left|z_2\right| \quad \arg (z_1 z_2)=\operatorname{arg}(z_1)+\operatorname{arg}(z_2)
$$
















$$
\begin{aligned}
\underline{Proof} \\
z_1 z_2 & =r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right) \times r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1 \cos \theta_2+\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2+\mathrm{i}^2 \sin \theta_1 \sin \theta_2\right) \\
& =r_1 r_2\left(\cos \theta_1 \cos \theta_2+\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2-\sin \theta_1 \sin \theta_2\right) \\
& =r_1 r_2\left(\left(\cos \theta_1 \cos \theta_2-\sin \theta_1 \sin \theta_2\right)+\mathrm{i}\left(\sin \theta_1 \cos \theta_2+\cos \theta_1 \sin \theta_2\right)\right) \\
& =r_1 r_2\left(\cos \left(\theta_1+\theta_2\right)+\mathrm{i} \sin \left(\theta_1+\theta_2\right)\right)
\end{aligned}
$$









#### Division








$$
\left|\frac{z_1}{z_2}\right|=\frac{|z_1|}{|z_2|} \quad \operatorname{arg}\left(\frac{z_1}{z_2}\right)=\operatorname{arg}(z_1)-\operatorname{arg}(z_2)
$$
















$$
\begin{aligned}
\underline{Proof} \\
\frac{z_1}{z_2} & =\frac{r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)}{r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)} \\
& =\frac{r_1\left(\cos \theta_1+\mathrm{i} \sin \theta_1\right)}{r_2\left(\cos \theta_2+\mathrm{i} \sin \theta_2\right)} \times \frac{\left(\cos \theta_2-\mathrm{i} \sin \theta_2\right)}{\left(\cos \theta_2-\mathrm{i} \sin \theta_2\right)} \\
& =\frac{r_1\left(\cos \theta_1 \cos \theta_2-\mathrm{i} \cos \theta_1 \sin \theta_2+\mathrm{i} \sin \theta_1 \cos \theta_2-\mathrm{i}^2 \sin \theta_1 \sin \theta_2\right)}{r_2\left(\cos \theta_2 \cos \theta_2-\mathrm{i} \cos \theta_2 \sin \theta_2+\mathrm{i} \sin \theta_2 \cos \theta_2-\mathrm{i}^2 \sin \theta_2 \sin \theta_2\right)} \\
& =\frac{r_1\left(\left(\cos \theta_1 \cos \theta_2+\sin \theta_1 \sin \theta_2\right)+\mathrm{i}\left(\sin \theta_1 \cos \theta_2-\cos \theta_1 \sin \theta_2\right)\right)}{r_2\left(\cos ^2 \theta_2+\sin ^2 \theta_2\right)} \\
& =\frac{r_1}{r_2}\left(\cos \left(\theta_1-\theta_2\right)+\mathrm{i} \sin \left(\theta_1-\theta_2\right)\right)
\end{aligned}
$$









## Exponential Form $re^{i\theta}$
### Derivation
Using the [[Series Approximations#Taylor Series|Taylor Series]]








$$
\begin{aligned}
e^{ i\theta} & =1+\mathrm{i}\theta+\frac{(\mathrm{i}\theta)^{2}}{2!}+\frac{(\mathrm{i}\theta)^{3}}{3!}+\frac{(\mathrm{i}\theta)^{4}}{4!}+\frac{(\mathrm{i}\theta)^{5}}{5!}+\frac{(\mathrm{i}\theta)^{6}}{6!}+\ldots \\
 & =1+\mathrm{i}\theta+\frac{\mathrm{i}^{2}\theta^{2}}{2!}+\frac{\mathrm{i}^{3}\theta^{3}}{3!}+\frac{\mathrm{i}^{4}\theta^{4}}{4!}+\frac{\mathrm{i}^{5}\theta^{5}}{5!}+\frac{\mathrm{i}^{6}\theta^{6}}{6!}+\ldots \\
 & =1+\mathrm{i}\theta-\frac{\theta^{2}}{2!}-\frac{\mathrm{i}\theta^{3}}{3!}+\frac{\theta^{4}}{4!}+\frac{\mathrm{i}\theta^{5}}{5!}-\frac{\theta^{6}}{6!}+\ldots \\
 & =\left(1-\frac{\theta^{2}}{2!}+\frac{\theta^{4}}{4!}-\frac{\theta^{6}}{6!}+\ldots\right)+\mathrm{i}\left(\theta-\frac{\theta^{3}}{3!}+\frac{\theta^{5}}{5!}-\ldots\right) \\
\\ 
&= \cos\theta + i\sin\theta
\end{aligned}
$$









### Multiplication and Division








$$
z_1 \times z_2 = r_1r_2 e^{i(\theta_1 + \theta_2)}
$$
















$$
\frac{z_1}{z_2} = \frac{r_1}{r_2} e^{i(\theta_1 - \theta_2)}
$$









---
# De Moivre's Theorem








$$
\begin{matrix}
(r(\cos \theta + i \sin \theta))^n \equiv r^n(\cos n\theta + i \sin n\theta)
\\
\forall n  \in \mathbb{Z}
\end{matrix}
$$








*This can prove with [[Proof by Induction]]*

It can be used to find [[Trigonometric Functions#Identities|Trigonometric Identities]] by applying De Moivre's Theorem and the binomial expansion of $(\cos\theta + i\sin\theta)^n$ to express $\cos n\theta$ in terms of powers of $\cos \theta$ and same for $\sin \theta$
You can also use the following identities







$$
z=\cos\theta + i\sin\theta\Rightarrow\qquad\begin{aligned}
 &  z+\frac{1}{z}=2\cos\theta\quad z^{n}+\frac{1}{z^{n}}=2\cos n\theta \\
 &  z-\frac{1}{z}=2i\sin\theta\quad z^{n}-\frac{1}{z^{n}}=2i\sin n\theta
\end{aligned}
$$







to find other identities by binomially expanding the function in terms of $z$ and exponentiating the trig function. These identities themselves can be proved using De Moivre's Theorem.

---
# Roots of Complex Numbers
## $z^n = w$
**To Solve** $z^n = w$ $\quad z, w \in \mathbb{C}, n \in \mathbb{N}$, $z, w \neq 0$
- Assume $z$ has the form $r(\cos \theta + i \sin \theta))$ so by **[[Complex Numbers#De Moivre's Theorem|De Moivre's Theorem]]** $z^n = r^n(\cos (n\theta + 2k\pi) + i \sin (n\theta+2k\pi))$
- Compare the modulus to solve for $r$
- Then plug in $k= 1, 2, \dots, n$ and solve for $\theta$

## Roots of Unity
The roots of unity are the solutions to $z^n = 1$, 
If $n$ is a positive integer there is an $n$th root of unity *s.t* $1, \omega, \omega^2,...,\omega^{n-1}$ are the roots of unity
The roots of unity sum to 0 and **form the vertices of a regular $n$-gon**
If $z_1$ is one root of the equation $z^n = s$ then the roots of $z^n =s$ are given by $z_1, z_1\omega, z_1\omega^2,...,z_1\omega^{n-1}$