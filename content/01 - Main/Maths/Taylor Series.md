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


## Flashcards
#Maths/Topics/Series, #Maths/A-Level-Further-Pure/Taylor-Series

What is a Taylor series and how is it defined mathematically?
?
A Taylor series is a Maclaurin series centred at $x=a$ instead of $x=0$. It is defined as: $$f(x) = \sum_{n=0}^N \frac{f^{(n)}(a)}{n!}(x-a)^n$$
where $f^{(n)}(a)$ is the nth derivative of $f$ evaluated at $a$, and the series converges for values of $x$ in a neighbourhood of $a$. <!--SR:!2024-09-19,4,273-->




What are the conditions for the existence of a Taylor series expansion? 
? 
A Taylor series expansion exists if:
1. $f^{(n)}(a)$ exists for all $n \in \mathbb{N}$
2. The series converges for the values of $x$ being considered <!--SR:!2024-09-18,4,270-->

How does the algebra of limits work for the sum of two functions? ? Given $\lim_{x \to a}f(x) = L$ and $\lim_{x \to a}g(x) = M$, then:
?
$$\lim_{x \to a}[f(x) + g(x)] = L + M$$
This is known as the sum rule for limits. <!--SR:!2024-09-18,4,270-->

What is the limit rule for the product of two functions? ? Given $\lim_{x \to a}f(x) = L$ and $\lim_{x \to a}g(x) = M$, then:
?
$$\lim_{x \to a}[f(x)g(x)] = LM$$This is known as the product rule for limits. <!--SR:!2024-09-18,4,270-->

How can you find the limit of a quotient of two functions?
?
Given $\lim_{x \to a}f(x) = L$ and $\lim_{x \to a}g(x) = M$, then: $$\lim_{x \to a}\frac{f(x)}{g(x)} = \frac{L}{M}$$where $M \neq 0$This is known as the quotient rule for limits. <!--SR:!2024-09-19,4,278-->

How can Taylor series be used to compute limits that result in indeterminate forms?
?
To compute a limit that results in an indeterminate form, you can find the limit of its Taylor/Maclaurin series, provided that the function is analytic (meaning it exactly equals its expansion). <!--SR:!2024-09-18,4,270-->

How can Taylor series be used to solve differential equations $\frac{dy}{dx} = f(x,y)$?
?
Taylor series can be used to approximate solutions to differential equations that can't be solved with other techniques. For a differential equation $\frac{dy}{dx} = f(x,y)$ with initial conditions $x = x_0, y = y_0$:
1. Calculate $\frac{dy}{dx}|_{x_0}$ by substituting into $f(x,y)$
2. Use successive differentiation of the original equation and substitute previously found values to find $\frac{d^ny}{dx^n}|_{x_0}$
3. Use these values to construct the Taylor series approximation of the solution 
This leads to the general solution $$y = \sum_{n=1}^N \frac{(x-x_0)^n}{n!}\frac{d^ny}{dx^n}\bigg|_{\displaystyle x_0}$$ <!--SR:!2024-09-18,3,250-->

