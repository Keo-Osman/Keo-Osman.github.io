#Maths/Trigonometry 
# Function Definitions and Properties 
## Sin
### **$sin(x)$**
Defined as the fraction of 








$$
\frac{Opposite}{Hypotonuese}
$$








 for a given right angle triangle with angle $x$
- Domain of $x \in  \mathbb{R}$
- Range of $-1 \le y \le 1$
- Period of $2 \pi$ radians
![[Sin-Gaph.png|600]]

### **$cosec(x)$**
Defined as 








$$
\frac{1}{sin(x)}
$$









- Domain $x \in \mathbb{R}, x \ne \frac{(2n+1)\pi}{2}, n \in \mathbb{z}$
- Range of $y \ge 1 , y \le -1$
- Period of $2 \pi$ radians
![[Cosecant-Graph.png|600]]
### **$arcsin(x)$**
Defined as the inverse function of $sin(x)$
- Domain $-1 \le x \le 1$, *This restricted domain exists because $sin(x) < -1, sin(x) > 1$ has no solutions for $x \in \mathbb{R}$*
- Range is $-\frac{\pi}{2} \le y \le \frac{\pi}{2}$,  *This range is due to the one-to-one mapping to only the principal root to ensure the function exists*
![[Arcsin-Graph.png|200]]
## Cosine
### **$cos(x)$**
Defined as the fraction of 








$$
\frac{Adjacent}{Hypotonuese}
$$








for a given right angle triangle with angle $x$
- Domain of $x \in  \mathbb{R}$
- Range of $-1 \le y \le 1$
- Period of $2 \pi$ radians
![[Cosine-Graph.png|600]]
### **$sec(x)$**
Defined as 








$$
\frac{1}{cos(x)}
$$









- Domain $x \in \mathbb{R}, x \ne \frac{(2n+1)\pi}{2}, n \in \mathbb{z}$
- Range of $y \ge 1 , y \le -1$
- Period of $2 \pi$ radians
![[Secant-Graph.png|600]]
### **$arccos(x)$**
Defined as the inverse function of $cos(x)$
- Domain $-1 \le x \le 1$, *This restricted domain exists because $cos(x) < -1, cos(x) > 1$ has no solutions for $x \in \mathbb{R}$*
- Range is $-\frac{\pi}{2} \le y \le \frac{\pi}{2}$,  *This range is due to the one-to-one mapping to only the principal root to ensure the function exists*
![[Arccos-Graph.png|200]]
## Tangent
### $tan(x)$
Defined as 








$$
\frac{Opposite}{Adjacent}
$$








 for a given right-angle triangle with angle $x$
- Domain $x \in \mathbb{R}, x \ne \frac{(2n+1)\pi}{2}, n \in \mathbb{Z}$
- Range $y \in \mathbb{R}$
- Period of $\pi$ radians
![[Tangent-Graph.png|600]]

### $cot(x)$
Defined as 








$$
\frac{1}{tan(x)}
$$









- Domain $x \in \mathbb{R}, x \ne n\pi, n \in \mathbb{Z}$
- Range $y \in \mathbb{R}$
- Period of $\pi$ radians
![[Cotangent-Graph.png|600]]

### $arctan(x)$
Defined as the inverse function of $tan(x)$
- Domain $x \in \mathbb{R}$
- Range $\frac{-\pi}{2} \le y \le \frac{\pi}{2}$
- Non-Periodic
 ![[Arctan-Graph.png|600]]

---

# Identities
## $\cos^2x + \sin^2x \equiv 1$

> [!example]- Proof
> - Consider a right triangle with an angle $x$. 
>- Let the hypotenuse be of length 1. 
>- According to the definitions of sine and cosine, we have: 









$$
\sin x = \frac{\text{opposite}}{\text{hypotenuse}} = \frac{a}{1} = a
$$








 and 








$$
\cos x = \frac{\text{adjacent}}{\text{hypotenuse}} = \frac{b}{1} = b,
$$









> - By the Pythagorean theorem, we know that in a right triangle: 








$$
a^2 + b^2 = 1^2
$$








 Substituting the values of $a$ and $b$ in terms of $\sin x$ and $\cos x$, we get:  








$$
\sin ^2(x) + \cos^2(x) = 1
$$










## $1 + \tan^2(x) \equiv \sec^2(x)$
> [!example]- Proof
>- Take 








$$
\sin ^2(x) + \cos^2(x) = 1
$$









>- Divide by $sin^2(x)$ to get 








$$
\frac{sin ^2(x)}{sin ^2(x)} + \frac{cos^2(x)}{sin ^2(x)} = \frac{1}{sin ^2(x)}
$$









>- Rearrange to get 








$$
1 + \left (\frac{cos(x)}{sin(x)} \right)^2 \equiv \left (\frac{1}{sin(x)} \right)^2
$$









>- Simplify to get 








$$
1 + tan^2(x) \equiv sec^2(x)
$$










## $a\sin(x) \pm b\cos(x)\equiv R\sin(x \pm \alpha), R\cos(x \pm \alpha)$ 
> [!example]- Equation









$$
sign(a)*\left(\sqrt{a^{2}+b^{2}}\right)\sin\left(x + \arctan\left(\frac{b}{a}\right)\right)
$$









or









$$
sign(b)*\left(\sqrt{a^{2}+b^{2}}\right)\cos\left(x-\arctan\left(\frac{a}{b}\right)\right)
$$










# T-Formulae
## Definitions/Equations
The t-formulae are formulae for the trigonometric functions using the substitution $t = \tan \left(\frac{\theta}{2}\right)$ to obtain the following formulae:










$$
\begin{aligned}
&\tan \left(\frac{\theta}{2}\right) = t  && \tan \theta = \frac{2t}{1-t^2}\\
& \sin \left(\frac{\theta}{2}\right) = \frac{t}{\sqrt{1+t^2}} && \sin \theta = \frac{2t}{1+t^2}\\
&\cos \left(\frac{\theta}{2}\right) = \frac{1}{\sqrt{1+t^2}} && \cos \theta = \frac{1-t^2}{1+t^2}
\end{aligned}
$$










## Solving Equations
To solve questions, you need to find $\tan \left(\frac{\theta}{2}\right)$ if not directly given, then use the t-formula for what you're trying to find. You generally find $\tan \left(\frac{\theta}{2}\right)$ 
 Finding $\sin \left(\frac{\theta}{2}\right)$ or $\cos \left(\frac{\theta}{2}\right)$ *it will either be given in the question or the reciprocal function* Then using the identity $\sin^2 + \cos^2 = 1$ to obtain the other function *Either sine or cosine* then choose the correct sign for the square root based on boundary conditions for $\theta$ in the problem. Then use $\tan (\theta) = \frac{\sin(\theta)}{\cos(\theta)}$
## Weierstrass Substitution For Integrals
You can use the t-formulae as a substitution for integrals it should be self explanatory from there but a key fact to remember is 








$$
dx = \frac{2}{1+t^2}dt
$$








 
