# A-Level Further Core 2 (Solving)

## First order differential equations

### Separating The Variables

Equations in the form $\frac{dy}{dx} = f(x)g(y)$ can be solved with

$$\int \frac{1}{g(y)} dy = \int f(x) dx$$
This is called *separating the variables*

### Integrating Factor

Equations in the form $$\frac{dy}{dx} + P(x)y = Q(x)$$ can be solved by multiplying by an integrating factor $f(x)$ to obtain $$f(x)\frac{dy}{dx} + f(x)P(x)y = f(x)Q(x)$$ and with the correct integrating factor this gets: $$f(x)\frac{dy}{dx} + f'(x)y = G(x)$$

as you by using reverse chain rule you get $LHS = \frac{d}{dx}(f(x)y)$

So by integrating and dividing through by $f(x)$ you get

$$y = \frac{\int f(x)Q(x)dx}{f(x)}$$

you can use any $f(x)$ so long as $f'(x)P(x) = f(x)$ but the general solution is: $f(x) = e^{\int P(x)dx}$

### Flashcards

\#Maths/Topics/Differential-Equations, #Maths/A-Level-Further-Core/Differential-Equations 

How can you solve a first-order differential equation of the form $\frac{dy}{dx} = f(x)g(y)$?
?
You can solve it by separating variables and integrating:
$$\int \frac{1}{g(y)} dy = \int f(x) dx$$ <!--SR:!2024-11-03,60,310-->

What is the general form of a linear first-order differential equation?
?
The general form is:
$$\frac{dy}{dx} + P(x)y = Q(x)$$ <!--SR:!2024-10-22,48,290-->

What is an integrating factor used for in solving differential equations?
?
An integrating factor is used to transform a linear first-order differential equation into an exact differential equation, making it easier to solve. <!--SR:!2024-11-02,59,310-->

How do you apply an integrating factor $f(x)$ to a differential equation?
?
Multiply both sides of the equation by $f(x)$:
$$f(x)\frac{dy}{dx} + f(x)P(x)y = f(x)Q(x)$$ <!--SR:!2024-10-28,54,310-->

What form should the equation take after applying the correct integrating factor?
?
It should take the form:
$$f(x)\frac{dy}{dx} + f'(x)y = G(x)$$ <!--SR:!2024-10-29,55,310-->

What is the significance of the left-hand side of the equation after applying the integrating factor?
?
The left-hand side becomes the derivative of a product:
$$LHS = \frac{d}{dx}(f(x)y)$$ <!--SR:!2024-10-25,51,310-->

What is the general solution for a linear first-order differential equation using an integrating factor?
?
The general solution is:
$$y = \frac{\int f(x)Q(x)dx}{f(x)}$$ <!--SR:!2024-11-03,60,310-->

What is the general form of the integrating factor $f(x)$?
?
The general form is:
$$f(x) = e^{\int P(x)dx}$$ <!--SR:!2024-11-03,60,310-->

What condition must be satisfied for an integrating factor $f(x)$?
?
The condition is:
$$f'(x)P(x) = f(x)$$ <!--SR:!2024-10-24,50,290-->

## Second Order Homogeneous Differential Equations

### Equation Form

A second order homogeneous differential equation is just a linear differential equation with a 2nd derivative term, and the whole thing equals zero:

$$
a \frac{d^2 y}{dx^2} + b \frac{dy}{dx} + c y = 0
$$

### Solution

It has the general solution in the form of:

$$
y = Ae^{\lambda x} + Be^{\mu x}
$$

where  $A$ and $B$ are arbitrary constants, and $\lambda$ and $\mu$ are constants to be determined *(so $A$ and $B$ are like  $C_1$ and $C_2$ and represent different solutions, but $\lambda$ and $\mu$) are fixed)*

Plugging in $y$into the differential equation, we get that $\lambda$ and $\mu$ are solutions to the quadratic equation:

$$
a \lambda^2 + b \lambda + c = 0
$$
*(This comes from the original differential equation.)*

### Auxiliary Equation

The equation $a \lambda^2 + b \lambda + c = 0$ is called the **auxiliary equation**.
*Often written as  $a m^2 + bm + c = 0$*
This quadratic equation leads to three cases:

#### Case 1: $b^2 > 4ac$

There are two real roots, so the general solution is:

$$
y = Ae^{\lambda x} + Be^{\mu x}
$$

#### Case 2: $b^2 = 4ac$

There is one repeated root $\alpha$, so the general solution is:

$$
y = (A + Bx) e^{\alpha x}
$$

#### Case 3: $b^2 \< 4ac$

There are two complex conjugate roots, so let $\alpha, \beta = p \pm qi$. The general solution is:

$$
y = e^{px} \left( A \cos qx + B \sin qx \right)
$$

### Flashcards

\#Maths/Topics/Differential-Equations, #Maths/A-Level-Further-Core/Differential-Equations 

What is a second order homogeneous differential equation?
?
A second order homogeneous differential equation is a linear differential equation with a 2nd derivative term, and the equation is set equal to zero:
$$a \frac{d^2 y}{dx^2} + b \frac{dy}{dx} + c y = 0$$ <!--SR:!2024-11-03,60,310-->

What is the auxiliary equation associated with a second order homogeneous differential equation
?
The auxiliary equation is the quadratic equation:
$$
am^2 + bm + c = 0
$$
This equation is derived from the differential equation and is used to determine the roots $\lambda$ and  $\mu$ <!--SR:!2024-11-03,60,310-->

What are the three cases based on the discriminant of the auxiliary equation?
?

* Case 1: $b^2 > 4ac$
  There are two real roots, so the general solution is:
  $$
  y = Ae^{\lambda_1 x} + Be^{\lambda_2 x}
  $$
* Case 2: $b^2 = 4ac$
  There is one repeated root $\alpha$, so the general solution is:
  $$
  y = (A + Bx) e^{\alpha x}
  $$
* Case 3: $b^2 \< 4ac$
  There are two complex conjugate roots, so let $\alpha, \beta = p \pm qi$. The general solution is:
  $$
  y = e^{px} \left( A \cos qx + B \sin qx \right)
  $$ <!--SR:!2024-10-11,37,290-->

## Second Order Non-Homogeneous Differential Equations

### Form

$$a \frac{d^2y}{dx^2} + b \frac{dy}{dx} + c y = f(x)$$

### Particular Integral

The particular integral (P.I.) is a specific function that satisfies the differential equation.
To find the P.I, assume a P.I. $g(x)$ that has the same form as $f(x)$, then plug it into the original equation to find the coefficients.

If the standard form is part of the complementary function, e.g., $f(x) = p e^{rx}$, where $r$ is a root of the auxiliary equation, you have to adjust the P.I. In this case, use $x e^{rx}$ rather than just $e^{rx}$.

### Complementary Function

The complementary function (C.F.) is a second-order homogeneous differential equation that shares the same coefficients:

$$a \frac{d^2y}{dx^2} + b \frac{dy}{dx} + c y = 0$$

### Solution

The general solution to a second-order non-homogeneous differential equation is:

$$y = \text{C.F.} + \text{P.I.}$$

### Flashcards

\#Maths/Topics/Differential-Equations, #Maths/A-Level-Further-Core/Differential-Equations 

What is the general form of a second-order non-homogeneous differential equation?
?
$$a \frac{d^2y}{dx^2} + b \frac{dy}{dx} + c y = f(x)$$ <!--SR:!2024-10-14,40,290-->

What is the particular integral (P.I.) in the context of differential equations?
?
A specific function that satisfies the differential equation. <!--SR:!2024-11-01,58,310-->

What is the complementary function (C.F.)?
?
The solution to the second-order homogeneous differential equation that shares the same coefficients with the non-homogeneous equation. <!--SR:!2024-10-28,54,310-->

What is the general solution for a second-order non-homogeneous differential equation?
?
$$y = \text{C.F.} + \text{P.I.}$$ <!--SR:!2024-11-01,58,310-->

How do you find the particular integral (P.I.) for a non-homogeneous differential equation?
?
Assume a P.I. that has the same form as $f(x)$ and substitute it into the original equation to determine the coefficients. <!--SR:!2024-11-03,60,310-->

What adjustment must be made to the P.I. if the form of $f(x)$ is part of the complementary function?
?
Use $x e^{rx}$ instead of $e^{rx}$ when $f(x) = p e^{rx}$ and $r$ is a root of the auxiliary equation. <!--SR:!2024-10-18,44,290-->

# A-Level Further Core 2 (Modelling)

## Simple Harmonic Motion

Dot notation - you can use dots to represent derivatives with respect to time:

$$\dot{x} = \frac{dx}{dt}, \quad \ddot{x} = \frac{d^2x}{dt^2}$$

Simple harmonic motion **(S.H.M)** is motion in which acceleration is always towards a fixed point $O$ *(the centre of oscillation)*, and the acceleration is proportional to the displacement *(basically oscillating through a point)*.

**S.H.M** can be modelled with $$\ddot{x} = -\omega^2 x$$ *(where $\omega$ is angular velocity - Further Mechanics 2)*
Given that $\ddot{x} = \frac{dv}{dt}$, you can derive $$\ddot{x} = v\frac{dv}{dt}$$
You can model displacement with $x = A \sin(\omega t + \alpha)$ where $A$ is the maximum amplitude and $\alpha$ is an arbitrary constant \*This comes from the auxiliary  equation having purely imaginary roots so the general solution is $y = A \cos \omega x + B \sin \omega x$ which simplifies to  $x = A \sin(\omega t + \alpha)$ .
When $x = 0$, then $\alpha = 0$; if $x = A$ when $t = 0$, then $\alpha = \frac{\pi}{2}$.

## Damped & Forced Harmonic Motion

You can refine and make more accurate models for harmonic motion by adding an additional damping force. This gives the equation:

$$\frac{d^2x}{dt^2} + k \frac{dx}{dt} + \omega^2 x = 0\quad \text{or}\quad\ddot{x} + k \dot{x} + \omega^2 x = 0$$

where $k$ and $\omega^2$ are positive constants.

The auxiliary equation leads to 3 cases:

1. $k^2 > 4\omega^2$: Known as **heavy damping** - no oscillations as resistive force is large compared to restoring force.
1. $k^2 = 4\omega^2$: Known as **critical damping** - again no oscillations performed.
1. $k^2 \< 4\omega^2$: Known as **light damping** - only case where oscillations are seen. The amplitude of oscillations decreases exponentially over time.

For heavy and critical damping, the exact nature of the motion depends on initial conditions. For light damping, the period of observed oscillations can be calculated.

## Flashcards

\#Maths/Topics/Differential-Equations, #Maths/A-Level-Further-Core/Differential-Equations

What is simple harmonic motion (SHM)and what’s its equation?
?
Motion in which acceleration is always directed toward a fixed point and is proportional to the displacement. Given by equation $$\ddot{x} = -\omega^2 x$$ <!--SR:!2024-10-29,55,310-->

What does the solution $x = A \sin(\omega t + \alpha)$ represent in SHM?
?
The displacement in simple harmonic motion, where $A$ is the maximum amplitude and $\alpha$ is an arbitrary constant. <!--SR:!2024-10-17,43,290-->

How is harmonic motion refined to include damping?
?
By adding a damping force to the equation, resulting in the differential equation $$\ddot{x} + k \dot{x} + \omega^2 x = 0$$. <!--SR:!2024-09-28,14,290-->

What are the three cases of damping in harmonic motion?
?

1. Heavy damping: No oscillations due to a large resistive force.
1. Critical damping: No oscillations occur.
1. Light damping: Oscillations occur with amplitude decreasing exponentially over time. <!--SR:!2024-10-27,53,310-->

# A-Level Further Pure 1

## Reducible Differential Equations

* You can use a substitution to reduce a first-order differential equation into a form that you know how to solve, either by separating the variables, or by using an integrating factor.
* You can use a given substitution to reduce second-order differential equations into differential equations of the form
  $$a\frac{d^2y}{dx^2}+b\frac{dy}{dx}+cy=f(x)$$
