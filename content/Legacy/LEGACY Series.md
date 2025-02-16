# A-Level Further Core 1
## Common Results and Basic Techniques
 $$
 \begin{aligned}
 &\sum_{r=1}^n m=mn \\
 &\sum_{r=1}^n r=\frac{1}{2} n(n+1) \\
&\sum_{r=k}^n f(r)=\sum_{r=1}^n f(r)-\sum_{r=1}^{k-1} f(r) \\
& \sum_{r=1}^n k f(r)= k\sum_{r=1}^n f(r) \\
& \sum_{r=1}^n(f(r)+g(r))=\sum_{r=1}^n f(r)+\sum_{r=1}^n g(r)\\
&\sum_{r=1}^n r^2=\frac{1}{6}n(n+1)(2 n+1)\\
&\sum_{r=1}^n r^3=\frac{1}{4} n^2(n+1)^2\\
\end{aligned}
$$

***

# A-Level Further Core 2
## The Method of Difference

If the general term of a series can be describes as $u_r = f(r) - f(r+1)$ then $$\sum_{r=1}^{n}{u_r} = f(1) - f(n+1)$$
This is because when summing the $-f(n+1)$ for $n = a$ cancels with the next term’s: $f(n)$ where $n = a+1$ so you get $f(a+1) - f(a+1) = 0$ so every term cancels except the first and last.
You can apply this to $u_n = f(n) - f(n+k)$ but less terms will cancel.

## Maclaurin Series
The Maclaurin series of a function is an approximation for a function at x=0. *(many common functions are exactly equal their Maclaurin expansion and are called analytical functions)*
The Maclaurin series for a function $f(x)$ that is infinitely differentiable at $x = 0$ is given by:
$$f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \frac{f'''(0)}{3!}x^3 + ... = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$

---
# A-Level Further Pure 1
## Taylor Series
A Taylor series is simply just a [[LEGACY Series#Maclaurin Series|Maclaurin series]] that is centred at some value $x=a$ rather than $x=0$ and is given by the formula:

$$
f(x) = \sum_{n=0}^N \frac{f^{(n)}(a)}{n!}(x-a)^n
$$
where $a$ is the $x$ value for which the Taylor Series is centred.

This expansion only if $f^{(n)}(a)$ exists $\forall n \in \mathbb{N}$ and for values of $x$ for which the series converges.
## Series Solutions of Differential Equations
You can use Taylor series to approximate solutions to [[LEGACY Differential Equations]] that can't be solved with other techniques.

Suppose you have the equation $\displaystyle\frac{dy}{dx} = f(x,y)$ and you have initial conditions $x = x_0, y = y_0$ Then you can calculate $\displaystyle\frac{dy}{dx}\bigg|_{\displaystyle x_0}$ by substitution into $f(x,y)$.
By successive differentiation of the original equation and substitution of previously found values, you can find values of $\displaystyle\frac{d^ny}{dx^n}\bigg|_{\displaystyle x_0}$
Therefore the series expansion of $\displaystyle\frac{dy}{dx} = f(x, y)$ is $$y = \sum_{n=1}^N \frac{(x-x_0)^n}{n!}\frac{d^ny}{dx^n}\bigg|_{\displaystyle x_0}$$

---
# Flashcards
## A-Level Further Core 1
#z_Legacy/Maths/A-Levels/Further-Core/Series 

What is the sum of the first $n$ natural numbers?
?
The sum of the first $n$ natural numbers is:
$\displaystyle\sum_{r=1}^n r=\frac{1}{2} n(n+1)$ 

---
## A-Level Further Core 2
#z_Legacy/Maths/A-Levels/Further-Core/Series, #Maths/Topics/Series

What is the method of difference used for in series?
?
If the general term of a series can be describes as $u_r = f(r) - f(r+1)$ then $$\sum_{r=1}^{n}{u_r} = f(1) - f(n+1)$$
This is because when summing the $-f(n+1)$ for $n = a$ cancels with the next term’s: $f(n)$ where $n = a+1$ so you get $f(a+1) - f(a+1) = 0$ so every term cancels except the first and last.
You can apply this to $u_n = f(n) - f(n+k)$ but less terms will cancel.  

---
## A-Level Further Pure 1
#Maths/Topics/Series, #z_Legacy/Maths/A-Levels/Further-Pure/Taylor-Series

What are the conditions for the existence of a Taylor series expansion?
?
A Taylor series expansion exists if:
1. $f^{(n)}(a)$ exists for all $n \in \mathbb{N}$
2. The series converges for the values of $x$ being considered 

How can Taylor series be used to compute limits that result in indeterminate forms?
?
To compute a limit that results in an indeterminate form, you can find the limit of its Taylor/Maclaurin series, provided that the function is analytic (meaning it exactly equals its expansion).  

How can Taylor series be used to solve differential equations $\frac{dy}{dx} = f(x,y)$?
?
Taylor series can be used to approximate solutions to differential equations that can't be solved with other techniques. For a differential equation $\frac{dy}{dx} = f(x,y)$ with initial conditions $x = x_0, y = y_0$:
1. Calculate $\frac{dy}{dx}|_{x_0}$ by substituting into $f(x,y)$
2. Use successive differentiation of the original equation and substitute previously found values to find $\frac{d^ny}{dx^n}|_{x_0}$
3. Use these values to construct the Taylor series approximation of the solution
This leads to the general solution $$y = \sum_{n=1}^N \frac{(x-x_0)^n}{n!}\frac{d^ny}{dx^n}\bigg|_{\displaystyle x_0}$$ 