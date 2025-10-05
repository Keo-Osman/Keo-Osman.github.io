
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
