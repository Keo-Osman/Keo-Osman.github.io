# A-Level Further Core 2 - Solving
## First order differential equations
### Separating The Variables
Equations in the form $\displaystyle \frac{dy}{dx} = f(x)g(y)$ can be solved with $$\int \frac{1}{g(y)} dy = \int f(x) dx$$
### Integrating Factor
An integrating factor is an $f(x)$ that you multiply through by to solve differential equations in the form $\displaystyle \frac{dy}{dx} + P(x)y = Q(x)$. The general integrating factor is $f(x) = \displaystyle e^{\int P(x)dx}$ but it can be other functions
$$
\begin{aligned}
& \displaystyle \frac{dy}{dx} + P(x)y = Q(x) \\
&& \times f(x) \\
& \displaystyle f(x)\frac{dy}{dx} + f(x)P(x)y = f(x)Q(x) \\
&& \text{by properties of integrating factor} \\
& \displaystyle f(x)\frac{dy}{dx} + f'(x)y = G(x) \\
&& \text{revese chain rule} \\
& LHS = \frac{d}{dx}(f(x)y) \\
&& \text{intgrating and dividing through by} f(x) \\
& y = \frac{\int G(x)dx}{f(x)}
\end{aligned}
$$
## Second Order Homogeneous Differential Equations
A second order homogeneous differential equation is a linear differential equation with a 2nd derivative term that equals zero
$$a \frac{d^2 y}{dx^2} + b \frac{dy}{dx} + c y = 0$$
It has the general solution $y = Ae^{\lambda x} + Be^{\mu x}$ where  $A$ and $B$ are arbitrary constants, and $\lambda$ and $\mu$ are constants to be determined.
Plugging in $y = Ae^{\lambda x} + Be^{\mu x}$ into the differential equation, we get that $\lambda$ and $\mu$ are solutions to the quadratic equation $am^2 + bm + c = 0$ this is called the ***auxiliary equation*.** 

This quadratic leads to 3 cases.
- The auxiliary equation has 2 real root. $y = Ae^{\lambda x} + Be^{\mu x}$
- The auxiliary equation has 1 repeated root $\alpha$. $y = (A + Bx) e^{\alpha x}$
- The auxiliary equation has two complex conjugate roots $\alpha, \beta = p \pm qi$. $y = e^{px} \left( A \cos qx + B \sin qx \right)$ - *This is equivalent to the first case with complex $\lambda$ and $\mu$*
## Second Order Non-Homogeneous Differential Equations
A second order non-homogeneous differential equation is a linear differential equation with a 2nd derivative term that equals some function of $x$
$$a \frac{d^2y}{dx^2} + b \frac{dy}{dx} + c y = f(x)$$
It has the general solution  $y = C.F + P.I$. Where $C.F$ is the solution to the corresponding homogenous function and $P.I$ is a **particular integral**
### Particular Integral
The particular integral $(P.I)$ is a specific function that satisfies the differential equation.
To find the $P.I$, assume  $P.I = g(x)$ that has the same form as $f(x)$, then plug it into the original equation to find the coefficients.

If the standard form is part of the complementary function, e.g., $f(x) = p e^{rx}$, where $r$ is a root of the auxiliary equation, you have to adjust the $P.I$ In this case, use $x e^{rx}$ rather than just $e^{rx}$.

| Form of $f(x)$                    | Form of $P.I$                             |
| --------------------------------- | ----------------------------------------- |
| $p$                               | $\lambda$                                 |
| $p+q x$                           | $\lambda+\mu x$                           |
| $p+q x+r x^2$                     | $\lambda+\mu x+v x^2$                     |
| $p \mathrm{e}^{k x}$              | $\lambda \mathrm{e}^{k x}$                |
| $p \cos \omega x+q \sin \omega x$ | $\lambda \cos \omega x+\mu \sin \omega x$ |

---
# A-Level Further Core 2 (Modelling)
## Simple Harmonic Motion
$$\dot{x} = \frac{dx}{dt}, \quad \ddot{x} = \frac{d^2x}{dt^2}$$
 Simple harmonic motion **(S.H.M)** is motion in which acceleration is always towards a fixed point $O$ *(the centre of oscillation)*, and proportional to the displacement *(basically oscillating through a point)*.
 
**S.H.M** is modelled with $\ddot{x} = -\omega^2 x$, where $\omega$ is angular velocity 

$$\ddot{x} = \frac{dv}{dt} = \frac{dx}{dt} \times \frac{dv}{dx} = v\frac{dv}{dx} $$
$$\begin{matrix}
\displaystyle \frac{d^2x}{dt^2} + \omega^2 = 0 \\
m^2+\omega^2 = 0 \\
m =\pm \omega i \\
x = A\cos\omega t + B\sin \omega t \\
x = R\sin(\omega t + \alpha)
\end{matrix}$$
## Damped and Forced Harmonic Motion
You can refine and make more accurate models for harmonic motion by adding an additional damping force. $$\frac{d^2x}{dt^2} + k \frac{dx}{dt} + \omega^2 x = 0\quad \text{or}\quad\ddot{x} + k \dot{x} + \omega^2 x = 0$$
The auxiliary equation leads to 3 cases:
- $k^2 > 4\omega^2$: Known as **heavy damping** - *no oscillations as resistive force is large compared to restoring force*
-  $k^2 = 4\omega^2$: Known as **critical damping** - *again no oscillations performed*
- $k^2 < 4\omega^2$: Known as **light damping** - *there are oscillations of which the amplitude  decreases exponentially over time*

For heavy and critical damping, the exact nature of the motion depends on initial conditions. For light damping, the period of observed oscillations can be calculated.

---
# A-Level Further Pure 1
## Reducible Differential Equations
You can use a substitution to reduce a differential equation into a form you know.

---
