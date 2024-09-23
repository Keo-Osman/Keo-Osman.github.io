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

$$\frac{h}{3}\left(y_0 + 4\sum_{k=1}^{n-1} y\_{2k-1} + 2\sum_{k=1}^{n-1} y\_{2k} + y\_{2n}\right)$$

where $2n$ is the number of strips used to approximate the area and $h$ is the width of each strip.
This formula is derived by using quadratic curves and using the result that area of quadratic curve passing through $(x_0, y_0)$, $(x_0 + h, y_1)$, $(x_0 + 2h, y_2)$ is $\frac{1}{3}h(y_0 + 4y_1 + y_2)$.

Other forms:

$$\frac{1}{3}h(\text{endpoints} + 4 \times \text{odd values} + 2 \times \text{even values})$$

$$\frac{1}{3}h(y_0 + 4(y_1 + y_3 + \ldots + y\_{2n-1}) + 2(y_2 + y_4 + \ldots + y\_{2n-2}) + y\_{2n})$$

This formula approximates the area under the curve by using quadratic curves to fit the function, providing a more accurate estimate than simpler methods like the trapezoidal rule.

