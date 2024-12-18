# Definition
A Taylor series is simply just a [[Series#Maclaurin Series|Maclaurin series]] that is centred at some value $x=a$ rather than $x=0$ and is given by the formula:

$$
f(x) = \sum_{n=0}^N \frac{f^{(n)}(a)}{n!}(x-a)^n
$$

where $a$ is the $x$ value for which the Taylor Series is centred.

This expansion only if $f^{(n)}(a)$ exists $\forall n \in \mathbb{N}$ and for values of $x$ for which the series converges.
# A-Level Further Pure 1
## Finding Limits
Given $\lim_{x \to a}f(x) = L$ & $\lim_{x \to a}g(x) = M$ then:

- $\lim_{x \to a}[f(x) + g(x)] = L + M$
- $\lim_{x \to a}[cf(x)] = cL$, $c \in \mathbb{R}$
- $\lim_{x \to a}[f(x)g(x)] = LM$
- $\lim_{x \to a}\frac{f(x)}{g(x)} = \frac{L}{M}$, $M \neq 0$

To compute a limit that results in an indeterminate form you can find the limit of its Taylor/Maclaurin series (providing the function is analytic - meaning it exactly equals its expansion)

## Series Solutions of Differential Equations

- You can use Taylor series to approximate solutions to differential equations that can't be solved with other techniques.
- Suppose you have the equation $\frac{dy}{dx} = f(x,y)$ and you have initial conditions $x = x_0, y = y_0$ Then you can calculate $\frac{dy}{dx}|_{x_0}$ by substitution into $f(x,y)$.
- By successive differentiation of the original equation and substitution of previously found values, you can find values of $\frac{d^ny}{dx^n}|_{x_0}$.

Therefore the series expansion of $\frac{dy}{dx} = f(x, y)$ is:
$$y = \sum_{n=1}^N \frac{(x-x_0)^n}{n!}\frac{d^ny}{dx^n}\bigg|_{\displaystyle x_0}$$


