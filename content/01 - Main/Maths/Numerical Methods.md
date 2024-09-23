# A-Level Further Pure

## First order differential equations

Some differential equations can not be solved analytically; however, they can be accurately approximated with Euler's Method:

$$y\_{r+1} \approx y_r + h \left.\frac{dy}{dx}\right|*{\displaystyle x_r}$$
$$ r \in \mathbb{N},\space x_r = x*{r-1}+h, \space h \in \mathbb{R}$$

*The way this works is that you are given initial conditions $(x_0, y_0)$. So you can compute $\left.\frac{dy}{dx}\right|*{x_0}$, then you can approximate the coordinates some $h$ away from $x_0$ by using a straight line with gradient $\left.\frac{dy}{dx}\right|*{x_0}$. To get a more accurate approximation, you can calculate the next point with smaller steps $h$. As a result, you have to do more iterations to get a point some distance from $x_0$*

You could also use the **Midpoint Formula**:

$$y\_{r+1} \approx y\_{r-1} + 2h \left.\frac{dy}{dx}\right|\_{x_r}$$

## Second order differential equation

You can extend Euler's method to second order differential equations with:

$$y\_{r+1} \approx 2y_r - y\_{r-1} + h^2 \left.\frac{d^2y}{dx^2}\right|*{\displaystyle x_r}$$
$$\left.\frac{d^2y}{dx^2}\right|*{\displaystyle x_0} \approx \frac{y_1 - 2y_0 + y\_{-1}}{h^2}$$

## Simpson's Rule

You can approximate $\int_a^b g(x) dx$ with the formula:

$$\frac{h}{3}\left(y_0 + 4\sum\_{k=1}^{n-1} y\_{2k-1} + 2\sum\_{k=1}^{n-1} y\_{2k} + y\_{2n}\right)$$

where $2n$ is the number of strips used to approximate the area and $h$ is the width of each strip.
This formula is derived by using quadratic curves and using the result that area of quadratic curve passing through $(x_0, y_0)$, $(x_0 + h, y_1)$, $(x_0 + 2h, y_2)$ is $\frac{1}{3}h(y_0 + 4y_1 + y_2)$.

Other forms:

$$\frac{1}{3}h(\text{endpoints} + 4 \times \text{odd values} + 2 \times \text{even values})$$

$$\frac{1}{3}h(y_0 + 4(y_1 + y_3 + \ldots + y\_{2n-1}) + 2(y_2 + y_4 + \ldots + y\_{2n-2}) + y\_{2n})$$

This formula approximates the area under the curve by using quadratic curves to fit the function, providing a more accurate estimate than simpler methods like the trapezoidal rule.

## Flashcards

\#Maths/Topics/Differential-Equations, #Maths/A-Level-Further-Pure/Numerical-Methods, #Maths/Topics/Numerical-Methods 

What is the formula for Euler's Method for first-order differential equations?
?
Euler's Method for first-order differential equations is given by:
$$y\_{r+1} \approx y_r + h \left.\frac{dy}{dx}\right|*{x_r}$$
where $r \in \mathbb{N}$, $x_r = x*{r-1}+h$, and $h \in \mathbb{R}$. This formula approximates the next point $(x\_{r+1}, y\_{r+1})$ using the current point $(x_r, y_r)$ and the derivative at that point.  It provides a numerical technique to estimate the value of a function at future points given an initial condition and the derivative of the function. <!--SR:!2024-09-19,1,210-->

How does reducing the step size $h$ affect the accuracy of Euler's Method?
?
Reducing the step size $h$ in Euler's Method generally increases the accuracy of the approximation. Smaller steps lead to more frequent recalculations of the derivative, resulting in a closer approximation to the true solution curve. However, this comes at the cost of requiring more iterations to cover the same distance from the initial point. <!--SR:!2024-09-19,4,270-->

What is the midpoint formula in the context of numerical methods for differential equations? ?
The midpoint formula is an alternative to Euler's Method for approximating solutions to first-order differential equations. It is given by:
$$y\_{r+2} \approx y\_{r-1} + 2h \left.\frac{dy}{dx}\right|\_{x_r}$$

How can Euler's Method be extended to solve second-order differential equations?
?
Euler's Method can be extended to second-order differential equations using the formula:
$$y\_{r+1} \approx 2y_r - y\_{r-1} + h^2 \left.\frac{d^2y}{dx^2}\right|\_{x_r}$$
This extension allows for the approximation of solutions to more complex differential equations involving second derivatives. <!--SR:!2024-09-19,1,210-->

What is the formula for approximating the second derivative at the initial point in numerical methods for second-order differential equations?
?
The second derivative at the initial point can be approximated using the formula:
$$\left.\frac{d^2y}{dx^2}\right|*{x_0} \approx \frac{y_1 - 2y_0 + y*{-1}}{h^2}$$
This approximation is useful when extending Euler's Method to second-order differential equations. <!--SR:!2024-09-19,1,207-->

\#Maths/A-Level-Further-Pure/Numerical-Methods, #Maths/Topics/Integrals, #Maths/Topics/Numerical-Methods 

How is Simpson's Rule of approximating $\int_a^b g(x) dx$ derived?
?
Simpson's Rule is derived by using quadratic curves to approximate the function being integrated. The key steps are:

1. Divide the integration interval into an even number of strips (2n).
1. For each pair of adjacent strips, fit a quadratic curve through the three points.
1. Use the result that the area under a quadratic curve passing through $(x_0, y_0)$, $(x_0 + h, y_1)$, and $(x_0 + 2h, y_2)$ is given by: $$\frac{1}{3}h(y_0 + 4y_1 + y_2)$$
1. Sum up these areas for all pairs of strips to get the final formula. <!--SR:!2024-09-27,9,270-->

What is the equation for Simpsons Rule of approximating $\int_a^b g(x) dx$?
?
Simpson's Rule can be expressed in several equivalent forms:

1. Standard formula:
   $$\frac{h}{3}\left(y_0 + 4\sum\_{k=1}^{n-1} y\_{2k-1} + 2\sum\_{k=1}^{n-1} y\_{2k} + y\_{2n}\right)$$ where:

* $h$ is the width of each strip
* $2n$ is the number of strips used
* $y_k$ represents the function value at the $k$-th point

2. Using endpoints, odd, and even values:
   $$\frac{1}{3}h(\text{endpoints} + 4 \times \text{odd values} + 2 \times \text{even values})$$
2. Expanded sum notation:
   $$\frac{1}{3}h(y_0 + 4(y_1 + y_3 + \ldots + y\_{2n-1}) + 2(y_2 + y_4 + \ldots + y\_{2n-2}) + y\_{2n})$$ <!--SR:!2024-09-19,1,210-->
