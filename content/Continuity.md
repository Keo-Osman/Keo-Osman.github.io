---
tags:
  - Maths/Calculus
---
# Definition
$f(x)$ is continuous at $\displaystyle a \Leftrightarrow \lim_{x \to a} f(x) = f(a)$

*This also implicitly requires that:*
1. $f(a)$ is defined
2. $\lim_{x \to a} f(x)$ exists

A function is continuous on an interval $\Leftrightarrow$ it is continuous at **every** number in that interval.
Continuity has **sidedness**. A function can be continuous from the left or right if the limit is one sided.
***
# Laws of Continuity
1. If $f$ and $g$ are continuous at $a$ then the following are continuous at $a$. $\displaystyle f\pm g,cf,f\cdot g, \frac{f}{g}$
2. $g$ is continuous at $a$  and $f$ is continuous at $g(a) \Rightarrow (f \circ g)(x)$ is continuous at $a$
3. $f$ is continuous at $b$ and $\displaystyle\lim_{x \to a} g(x) = b \Rightarrow \lim_{x \to a} f(g(x)) = b$
***
# Continuous Functions
[[Polynomials]], Rational, Root and [[Trigonometric Functions]] are all continuous for all numbers in their domain.
***
# Intermediate Value Theorem
$f$ is continuous on $[a,b]$ and $f(a) \neq f(b)$ 
$\Rightarrow\forall N \text{ s.t. }  \operatorname{min}\{f(a), f(b)\} < N < \operatorname{max}\{f(a), f(b)\} \quad\exists c \text{ s.t. } f(c) = N$
***
# Extreme Value Theorem
$f$ is continuous on $[a,b] \Rightarrow f$ attains a global maximum and minimum value on $[a, b]$