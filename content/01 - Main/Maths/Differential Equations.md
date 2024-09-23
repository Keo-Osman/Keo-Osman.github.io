
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

#### Case 3: $b^2 < 4ac$

There are two complex conjugate roots, so let $\alpha, \beta = p \pm qi$. The general solution is:

$$
y = e^{px} \left( A \cos qx + B \sin qx \right)
$$



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





# A-Level Further Core 2 (Modelling)
## Simple Harmonic Motion

Dot notation - you can use dots to represent derivatives with respect to time:

$$\dot{x} = \frac{dx}{dt}, \quad \ddot{x} = \frac{d^2x}{dt^2}$$

 Simple harmonic motion **(S.H.M)** is motion in which acceleration is always towards a fixed point $O$ *(the centre of oscillation)*, and the acceleration is proportional to the displacement *(basically oscillating through a point)*.

**S.H.M** can be modelled with $$\ddot{x} = -\omega^2 x$$ *(where $\omega$ is angular velocity - Further Mechanics 2)*
Given that $\ddot{x} = \frac{dv}{dt}$, you can derive $$\ddot{x} = v\frac{dv}{dt}$$
You can model displacement with $x = A \sin(\omega t + \alpha)$ where $A$ is the maximum amplitude and $\alpha$ is an arbitrary constant *This comes from the auxiliary  equation having purely imaginary roots so the general solution is $y = A \cos \omega x + B \sin \omega x$ which simplifies to  $x = A \sin(\omega t + \alpha)$ .
  When $x = 0$, then $\alpha = 0$; if $x = A$ when $t = 0$, then $\alpha = \frac{\pi}{2}$.

## Damped & Forced Harmonic Motion

You can refine and make more accurate models for harmonic motion by adding an additional damping force. This gives the equation:

$$\frac{d^2x}{dt^2} + k \frac{dx}{dt} + \omega^2 x = 0\quad \text{or}\quad\ddot{x} + k \dot{x} + \omega^2 x = 0$$

where $k$ and $\omega^2$ are positive constants.

The auxiliary equation leads to 3 cases:
  1. $k^2 > 4\omega^2$: Known as **heavy damping** - no oscillations as resistive force is large compared to restoring force.
  2. $k^2 = 4\omega^2$: Known as **critical damping** - again no oscillations performed.
  3. $k^2 < 4\omega^2$: Known as **light damping** - only case where oscillations are seen. The amplitude of oscillations decreases exponentially over time.

For heavy and critical damping, the exact nature of the motion depends on initial conditions. For light damping, the period of observed oscillations can be calculated.



# A-Level Further Pure 1
## Reducible Differential Equations
- You can use a substitution to reduce a first-order differential equation into a form that you know how to solve, either by separating the variables, or by using an integrating factor.
- You can use a given substitution to reduce second-order differential equations into differential equations of the form
$$a\frac{d^2y}{dx^2}+b\frac{dy}{dx}+cy=f(x)$$
