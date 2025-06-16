#Maths/Calculus  
# Definition
$f(x)$ is continuous at $a \Leftrightarrow \lim_{x \to a} f(x) = f(a)$

*This also implicitly requires that:*
- $f(a)$ is defined
- $\lim_{x \to a} f(x)$ exists

A function is continuous on an interval $\Leftrightarrow$ it is continuous at **every** number in that interval.
Continuity has **sidedness**. A function can be continuous from the left or right if the limit is one sided.

---
# Laws of Continuity
If $f$ and $g$ are continuous at $a$ then the following are continuous at $a$









$$
\begin{aligned}
&f+g &&f-g\\
&cf &&fg\\
&\frac{f}{g}, \quad(g(a) \neq0)
\end{aligned}
$$









$g$ is continuous at $a \wedge f$ is continuous at $g(a) \Rightarrow (f \circ g)(x)$ is continuous at $a$
$f$ is continuous at $b$ $\wedge \displaystyle\lim_{x \to a} g(x) = b \Rightarrow \lim_{x \to a} f(g(x)) = b$

---
# Continuous Functions
[[Polynomials]], Rational, Root and [[Trigonometric Functions]] are all continuous for all numbers in their domain.

---
# Theorems
## Intermediate Value Theorem









$$
f\text{ is continuous on }[a,b] \wedge f(a) \neq f(b)\Rightarrow\forall N \text{ s.t. }  \text{min}\{f(a), f(b)\} < N < \text{max}\{f(a), f(b)\} \quad\exists c \text{ s.t. } f(c) = N
$$









## Extreme Value Theorem









$$
f\text{ is continuous on }[a,b] \Rightarrow f\text{ attains a global maximum and minimum value on } [a, b]
$$








