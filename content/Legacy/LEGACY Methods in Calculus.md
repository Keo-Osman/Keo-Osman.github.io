
# A-Level Further Pure 1
## Finding Limits
*(From FP1 [[LEGACY Series#Taylor Series|Taylor Series]] chapter but more suitable here)*
Given $\lim_{x \to a}f(x) = L$, $\lim_{x \to a}g(x) = M$ then:
- $\lim_{x \to a}[f(x) + g(x)] = L + M$
- $\lim_{x \to a}[cf(x)] = cL$, $c \in \mathbb{R}$
- $\lim_{x \to a}[f(x)g(x)] = LM$
- $\lim_{x \to a}\frac{f(x)}{g(x)} = \frac{L}{M}$, $M \neq 0$
## Leibnitz's Theorem and nth Derivatives
For $y=uv$

$$
\frac{d^n y}{dx^n} = \sum_{k=0}^n \binom{n}{k} \frac{d^k u}{dx^k} \frac{d^{n-k} v}{dx^{n-k}}
$$
*(This can be proved with induction with repeated differentiation)*
## L'Hôpital's Rule
If either $\displaystyle \lim_{x \to a} f(x) = \lim_{x \to a} g(x) = 0$ **OR** $\displaystyle \lim_{x \to a} f(x) = \pm \infty$ & $\displaystyle \lim_{x \to a} g(x) = \pm \infty$
$$
\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{f'(x)}{g'(x)} \quad \text{(provided that } \lim_{x \to a} \frac{f(x)}{g(x)} \text{ exists)}
$$

---
# Flashcards
## A-Level Further Pure 1
#z_Legacy/Maths/A-Levels/Further-Pure/Methods-In-Calculus

What is Leibnitz's Theorem for the nth derivative of a product of two functions $y=uv$?
?
Leibnitz's Theorem states that for $y=UV$, the nth derivative is given by:
$$\frac{d^n y}{dx^n} = \sum_{k=0}^n \binom{n}{k} \frac{d^ku}{dx^k} \frac{d^{n-k}v}{dx^{n-k}}$$
This formula allows us to calculate higher-order derivatives of product functions.  

#z_Legacy/Maths/A-Levels/Further-Pure/Methods-In-Calculus

What does L'Hôpital's Rule state?
?
L'Hôpital's Rule states that under certain conditions:
$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{f'(x)}{g'(x)}$$
provided that the limit of the ratio of derivatives exists.
L'Hôpital's Rule can be applied under two conditions:
1. When $\lim_{x \to a} f(x) = \lim_{x \to a} g(x) = 0$ (0/0 form)
2. When $\lim_{x \to a} f(x) = \pm \infty$ & $\lim_{x \to a} g(x) = \pm \infty$ ($\infty/\infty$ form)  


