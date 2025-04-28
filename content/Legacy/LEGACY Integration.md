# A-Level Pure
## Common Results









$$
\begin{aligned}
&\int x^n dx = \frac{x^{n+1}}{n+1} + c &&\int e^x dx = e^x + c\\
&\int \frac{1}{x} dx = \ln|x| + c &&\int \cos x dx = \sin x + c \\
&\int \sin x dx = -\cos x + c &&\int \sec^2 x = \tan x + c\\
&\int \csc(x) \cot x dx = -\csc x + c &&\int \csc^2 x dx = -\cot x + c\\
&\int \sec x \tan x dx = \sec x + c
\end{aligned}
$$









## Reverse Chain Rule
 








$$
\int f(ax + b) dx = \frac{1}{a}f(ax + b) + c \quad \int \frac{f'(x)}{f(x)} dx = \ln{f(x)}\quad\int f'(x)(f(x))^n dx= \frac{1}{n+1}(f(x))^{n+1}
$$








 
## Substitution
Sometimes you can simplify an integral by changing the variable. This process is similar to using the chain rule in differentiation and is called integration by substitution.
## Integration By Parts









$$
\int u \frac{dv}{dx} dx = uv - \int v \frac{du}{dx} dx
$$










---
# A-Level Further Core 2
## Improper integrals
The integral $\int_a^b f(x)dx$ is improper if:
- One or both of the limits are $\pm \infty$ or
- $f(x)$ is undefined at any point in $[a,b]$

To find $\int_a^\infty f(x)dx$, consider $\int_a^t f(x)dx$ and compute the limit (if it converges) as $t \to \infty$
For an integral $\int_{-\infty}^{\infty} f(x)dx$, split into 2 integrals: $\int_{-\infty}^c f(x)dx + \int_c^{\infty} f(x)dx$ , $c \in \mathbb{R}$
## Mean Value
The mean value of a function $f(x)$ in the interval $[a,b]$ is:









$$
\frac{1}{b-a} \int_a^b f(x)dx
$$









This is because the integral is taking infinite samples.
If $f(x)$ has mean value $\bar{f}$ over the interval $[a,b]$ then:
- $f(x) + k$ has mean value $\bar{f} + k$
- $kf(x)$ has mean value $k\bar{f}$, $k \in \mathbb{R}$

---
# A-Level Further Pure 2
## Reduction Formula
The Reduction formula allows you to write an integral as a recurrence relation. This is generally used for integrals with high powers that would require many **integration by parts** iterations.









$$
I_n = \int g(x,n)dx = \sum_{r=0}^{n-1} g_r(n)I_r
$$









You can use the reduction formula in conjunction with a substitution $r = g(x)$ and the Method of Differences to compute tricky summations.

## Arc Length
### Cartesian
The arc length of $y = g(x)$ from $A(x_A, y_A)$ and $B(x_B, y_B)$ is: 








$$
s = \int_{\displaystyle x_A}^{\displaystyle x_B} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx \quad \text{or} \quad s = \int_{\displaystyle y_A}^{\displaystyle y_B} \sqrt{1 + \left(\frac{dx}{dy}\right)^2} dy
$$









### Parametric
For $x = f(t)$, $y = g(t)$, the arc length from $A(f(t_A), g(t_A))$ to $B(f(t_B), g(t_B))$ is: 








$$
s = \int_{\displaystyle t_A}^{\displaystyle t_B} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} dt
$$









### Polar
For $r = g(\theta)$, the arc length from half lines $\theta = \alpha$ to $\theta = \beta$ is: 








$$
s = \int_{\displaystyle \alpha}^{\displaystyle \beta} \sqrt{r^2 + \left(\frac{dr}{d\theta}\right)^2} d\theta
$$









## Surface Area of Volume of Revolution
The area, $S$, of the surface generated when the arc $A B$ on the curve $C$ is rotated completely about the $x$-axis is $2 \pi \int y \mathrm{ds}$, and about the $y$-axis is $2 \pi \int x \mathrm{ds}$.
### Cartesian
**About the $x$-axis:** 








$$
S=2 \pi \int_{\displaystyle x_A}^{\displaystyle x_B} y \sqrt{1+\left(\frac{\mathrm{d} y}{\mathrm{~d} x}\right)^2} \mathrm{~d} x
$$









**About the $y$-axis:** 








$$
S=2 \pi \int_{\displaystyle y_A}^{\displaystyle y_B} x \sqrt{1+\left(\frac{\mathrm{d} x}{\mathrm{~d} y}\right)^2} \mathrm{~d} y \quad \text{or} \quad S=2 \pi \int_{\displaystyle x_A}^{\displaystyle x_B} x \sqrt{1+\left(\frac{\mathrm{d} y}{\mathrm{~d} x}\right)^2} \mathrm{~d} x
$$









### Parametric
**About the $x$-axis:** 








$$
S=2 \pi \int_{\displaystyle t_A}^{\displaystyle t_B} y \sqrt{\left(\frac{\mathrm{d} x}{\mathrm{~d} t}\right)^2+\left(\frac{\mathrm{d} y}{\mathrm{~d} t}\right)^2} \mathrm{~d} t
$$









**About the $y$-axis:** 








$$
S=2 \pi \int_{\displaystyle t_A}^{\displaystyle t_B}x \sqrt{\left(\frac{\mathrm{d} x}{\mathrm{~d} t}\right)^2+\left(\frac{\mathrm{d} y}{\mathrm{~d} t}\right)^2} \mathrm{~d} t
$$









### Polar
**About the initial line $\theta = 0$**  








$$
S=2 \pi \int_{\displaystyle \alpha}^{\displaystyle \beta} r \sin \theta \sqrt{r^2+\left(\frac{\mathrm{d} \theta}{\mathrm{d} r}\right)^2} \mathrm{~d} \theta
$$









**About the line $\theta= \displaystyle\pm \frac{\pi}{2}:$** 








$$
S=2 \pi \int_{\displaystyle \alpha}^{\displaystyle \beta} r \cos \theta \sqrt{r^2+\left(\frac{\mathrm{d} \theta}{\mathrm{d} r}\right)^2} \mathrm{~d} \theta
$$










---
