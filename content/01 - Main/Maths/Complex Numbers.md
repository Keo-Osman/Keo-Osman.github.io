# Definition

A complex number is a number that is written as: $a+b i$ where $i$ is the imaginary unit defined as $\sqrt{-1}$ and $a, b \in \mathbb{R}$. *The set of all complex numbers is written as $\mathbb{C}$*

# A-Level Further Core 1

## The complex conjugate

* If complex number $z$ is defined as $a+b_i$ then $z^\*$ (the complex conjugate) is defined as $a-b i$
* Let $z=a+bi$ then
  * $z+z^*$ is always real as the imaginary parts cancel so $z+z^*=2 a$
  * $z+z^\*$ is also always real as it’s a difference of two squares
    $$
    (a+b i)(a-b i)=a^2-(b i)^2=a^2-\left(b^2 i^2\right)=a^2-\left(-b^2\right)=a^2+b^2
    $$

## Basic operations

### Addition & Subtraction

* For addition and subtraction you combine real and imaginary terms separately$(a+b i) \pm(c+d i)=(a+c) \pm(b+d) i$

### Multiplication

* For multiplication just expand brackets ex. $(a+b i)(c+d i)=$ $a c+(b c) i+(a d) i+b d i^2$ since $i^2=-1$ this is equivalent to $(a c-b d)+(b c+a d)i$

### Division

* For division multiply the numerator and denominator by the complex conjugate of the numerator.
  $$\frac{a+b i}{c+d i}=\frac{a+b i)(c-d i)}{(c+d i)(c-d i)} = \frac{a c+b d}{c^2+d^2}+\left(\frac{b c-a d}{c^2+d^2}\right)i
  $$

## Roots of a polynomials.

* For any quadratic equation $a x^2+b x+c$ where $a, b, c \in \mathbb{R}$, if a complex number $z$ is a root then $z^\*$ is also a root *this is called a conjugate pair*
* For any cubic equation $a x^3+b x^2+c x+d$ where $a, b, c, d \in \mathbb{R}$ it will have 3 roots either all real or 1 real root and a complex conjugate pair
* For any quartic equation $a x^4+b x^3+c x^2+d x+e$ where $a, b, c, d, e \in \mathbb{R}$ it will hare 4 roots either all real, 2 real roots and complex conjugate pair or 2 complex conjugate pairs

## Flashcards

\#Maths/A-Level-Further-Core/Complex-Numbers/1, #Maths/Topics/Complex-Numbers

For a given complex number $z$ defined as $a + bi$ what is $z^\*$
?
The complex conjugate. Defined as $a - bi$ <!--SR:!2024-10-13,51,310-->

How do you divide complex numbers $\frac{z_1}{z_2}$ in $a+bi$ form
?
Write as a fraction then multiply the numerator and denominator by $z_2^\*$, then the denominator becomes a real number <!--SR:!2024-10-19,55,310-->

# A-Level Further Core 2

## Exponential Form Of Complex Numbers

^265d2f

* By using the Taylor expansion of $e^x$ and plugging in $x = i\theta$, you can split the series to obtain $e^{i\theta} = \cos \theta + i \sin \theta$

* Then multiply by $r$ to get the general form of $z = re^{i\theta}$
  where $r = |z|$ and $\theta = \arg(z)$

* To multiply or divide in this form:
  $$z_1 \times z_2 = r_1r_2 e^{i(\theta_1 + \theta_2)}$$
  $$\frac{z_1}{z_2} = \frac{r_1}{r_2} e^{i(\theta_1 - \theta_2)}$$

## De Moivre's theorem

For any integer $n$:

$$(r(\cos \theta + i \sin \theta))^n = r^n(\cos n\theta + i \sin n\theta)$$

*(insert proof in obsidian)*

* This is proved with induction or Euler's relation
* You can use De Moivre's theorem to prove trig identities by using the binomial expansion of $(\cos \theta + i \sin \theta)^n$ to express $\cos n\theta$ and $\sin n\theta$ in terms of powers of $\cos \theta$ and $\sin \theta$

## Sum of Geometric Series

For $w, z \in \mathbb{C}$, the geometric series summation formulae are valid:

$$\sum\_{r=0}^{n-1} wz^r = \frac{w(z^n-1)}{z-1}, \quad |z| \< 1$$

$$\sum\_{r=0}^{\infty} wz^r = \frac{w}{z-1}, \quad |z| \< 1$$

## $n^{th}$ root of complex numbers

* For any equation $z^n = w$, $z, w \in \mathbb{C}$, $z, w \neq 0$, $n \in \mathbb{N}$
  the equation has $n$ distinct roots
* For any number $z \in \mathbb{C}$, $z = r(\cos \theta + i \sin \theta)$, you can write $z = r(\cos(\theta + 2k\pi) + i \sin(\theta + 2k\pi))$, $k \in \mathbb{Z}$ as both $\sin, \cos$ have period $2\pi$
* You can solve the equation $z^n = w$ by writing $z^n$ in the form
  $|w|^{\frac{1}{n}}(\cos(\frac{\theta + 2k\pi}{n}) + i \sin(\frac{\theta + 2k\pi}{n}))$, where $\theta = \arg(w)$ for $k = 0,1,2,...,n-1$ varying $k$ to get all $n$ roots in the interval $\[-\pi, \pi\]$

## Flashcards

\#Maths/A-Level-Further-Core/Complex-Numbers/2, #Maths/Topics/Complex-Numbers

What is Euler's formula for complex numbers?
?
$e^{i\theta} = \cos \theta + i \sin \theta$ <!--SR:!2024-09-28,36,294-->

What is the general exponential form of a complex number?
?
$z = re^{i\theta}$, where $r = |z|$ and $\theta = \arg(z)$ <!--SR:!2024-10-15,49,294-->

How do you multiply complex numbers in exponential form?
?
$z_1 \times z_2 = r_1r_2 e^{i(\theta_1 + \theta_2)}$ <!--SR:!2024-10-25,60,314-->

How do you divide complex numbers in exponential form?
?
$\frac{z_1}{z_2} = \frac{r_1}{r_2} e^{i(\theta_1 - \theta_2)}$ <!--SR:!2024-10-22,58,314-->

What is De Moivre's theorem?
?
$(r(\cos \theta + i \sin \theta))^n = r^n(\cos n\theta + i \sin n\theta)$ <!--SR:!2024-10-16,54,314-->

What is the formula for the sum of a finite geometric series in complex numbers?
?
$\sum\_{r=0}^{n-1} wz^r = \frac{w(z^n-1)}{z-1}$, for $|z| \< 1$ <!--SR:!2024-09-21,5,234-->

What is the formula for the sum of an infinite geometric series in complex numbers?
?
$\sum\_{r=0}^{\infty} wz^r = \frac{w}{z-1}$, for $|z| \< 1$ <!--SR:!2024-09-26,8,234-->

How many distinct roots does the equation $z^n = w$ have?
?
$n$ distinct roots <!--SR:!2024-10-24,60,314-->

What is the general form of the $n^{th}$ roots of a complex number?
?
$|w|^{\frac{1}{n}}(\cos(\frac{\theta + 2k\pi}{n}) + i \sin(\frac{\theta + 2k\pi}{n}))$, where $\theta = \arg(w)$ $k = 0,1,2,...,n-1$ <!--SR:!2024-11-07,54,274-->

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNTQxNTQ0OTFdfQ==
-->
