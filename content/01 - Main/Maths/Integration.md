#Maths/Topics/Integration

# A-Level Pure
$$\int x^n dx = \frac{x^{n+1}}{n+1} + c$$
$$\int e^x dx = e^x + c$$
$$\int \frac{1}{x} dx = \ln|x| + c$$
$$\int \cos x dx = \sin x + c$$
$$\int \sin x dx = -\cos x + c$$
$$\int \sec^2 x = \tan x + c$$
$$\int \csc(x) \cot x dx = -\csc x + c$$
$$\int \csc^2 x dx = -\cot x + c$$
$$\int \sec x \tan x dx = \sec x + c$$

 $$\int f(ax + b) dx = \frac{1}{a}f(ax + b) + c$$

Trigonometric identities can be used to integrate expressions. This allows an expression that cannot be integrated to be replaced by an identical expression that can be integrated.

To integrate expressions of the form $\int k \frac{f'(x)}{f(x)} dx$, try $\ln|f(x)|$ and differentiate to check, and then adjust any constant.

To integrate an expression of the form $\int kf'(x)(f(x))^n dx$, try $(f(x))^{n+1}$ and differentiate to check, and then adjust any constant.

Sometimes you can simplify an integral by changing the variable. This process is similar to using the chain rule in differentiation and is called integration by substitution.

The integration by parts formula is given by: $\int u \frac{dv}{dx} dx = uv - \int v \frac{du}{dx} dx$

Partial fractions can be used to integrate algebraic fractions.

The area bounded by two curves can be found using integration:
   Area of $R = \int_a^b (f(x) - g(x)) dx = \int_a^b f(x) dx - \int_a^b g(x) dx$

The trapezium rule is:
    $$\int_a^b y dx \approx \frac{1}{2}h(y_0 + 2(y_1 + y_2 + ... + y_{n-1}) + y_n)$$
    where $h = \frac{b-a}{n}$ and $y_i = f(a + ih)$.

When $\frac{dy}{dx} = f(x)g(y)$ you can write
    $$\int \frac{1}{g(y)} dy = \int f(x) dx$$


### Flashcards

#Maths/A-Level-Pure/Integration, #Maths/Topics/Integration 

What is the integration by parts formula?
?
$$\int u \frac{dv}{dx} dx = uv - \int v \frac{du}{dx} dx$$ <!--SR:!2024-10-12,54,310-->

How can you find the area bounded by two curves?
?
Area of $R = \int_a^b (f(x) - g(x)) dx = \int_a^b f(x) dx - \int_a^b g(x) dx$ <!--SR:!2024-10-16,58,310-->

What is the trapezium rule?
?
$$\int_a^b y dx \approx \frac{1}{2}h(y_0 + 2(y_1 + y_2 + ... + y_{n-1}) + y_n)$$
where $h = \frac{b-a}{n}$ and $y_i = f(a + ih)$ <!--SR:!2024-10-18,60,310-->

What technique can be used to integrate algebraic fractions?
?
Partial fractions can be used to integrate algebraic fractions. <!--SR:!2024-10-04,50,310-->

What is the integral of $x^n$?
?
$$\int x^n dx = \frac{x^{n+1}}{n+1} + c$$ <!--SR:!2024-10-03,49,310-->

What is the integral of $e^x$?
?
$$\int e^x dx = e^x + c$$ <!--SR:!2024-10-17,59,310-->

What is the integral of $\frac{1}{x}$?
?
$$\int \frac{1}{x} dx = \ln|x| + c$$ <!--SR:!2024-10-18,60,310-->

What is the integral of $\cos x$?
?
$$\int \cos x dx = \sin x + c$$ <!--SR:!2024-10-18,60,310-->

What is the integral of $\sin x$?
?
$$\int \sin x dx = -\cos x + c$$ <!--SR:!2024-10-18,60,310-->

What is the integral of $\sec^2 x$?
?
$$\int \sec^2 x = \tan x + c$$ <!--SR:!2024-09-19,5,210-->

What is the integral of $\csc x \cot x$?
?
$$\int \csc x \cot x dx = -\csc x + c$$ <!--SR:!2024-09-19,1,130-->

What is the integral of $\csc^2 x$?
?
$$\int \csc^2 x dx = -\cot x + c$$ <!--SR:!2024-09-20,2,170-->

What is the integral of $\sec x \tan x$?
?
$$\int \sec x \tan x dx = \sec x + c$$ <!--SR:!2024-09-19,1,130-->

# A-Level Further Core 2
## Improper integrals

The integral $\int_a^b f(x)dx$ is improper if:
- One or both of the limits are $\pm \infty$ or
- $f(x)$ is undefined at any point in $[a,b]$

An improper integral exists if it is convergent.

To find $\int_a^\infty f(x)dx$, consider $\int_a^t f(x)dx$ and compute the limit (if it converges) as $t \to \infty$

For an integral $\int_{-\infty}^{\infty} f(x)dx$, split into 2 integrals: $\int_{-\infty}^c f(x)dx + \int_c^{\infty} f(x)dx$ , $c \in \mathbb{R}$

## Mean Value

The mean value of a function $f(x)$ in the interval $[a,b]$ is:

$$\frac{1}{b-a} \int_a^b f(x)dx$$

This is because the integral is taking infinite samples.

If $f(x)$ has mean value $\bar{f}$ over the interval $[a,b]$ then:
- $f(x) + k$ has mean value $\bar{f} + k$
- $kf(x)$ has mean value $k\bar{f}$, $k \in \mathbb{R}$


# A-Level Further Pure 2
## Reduction Formula

The Reduction formula allows you to write an integral as a recurrence relation. This is generally used for integrals with high powers that would require many **integration by parts** iterations.

$$J_n = \int g(x,n)dx = \sum_{r=0}^{n-1} g_r(n)I_r$$

$$\int (g(x))^n g'(x) dx = \frac{1}{n+1} g(x)^{n+1}$$

You can use the reduction formula in conjunction with a substitution $r = g(x)$ and the Method of Differences to compute tricky summations.

## Arc Length

The arc length of $y = g(x)$ from $A(x_A, y_A)$ and $B(x_B, y_B)$ is:

$$s = \int_{x_A}^{x_B} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx \quad \text{or} \quad s = \int_{y_A}^{y_B} \sqrt{1 + \left(\frac{dx}{dy}\right)^2} dy$$

If the equations are parametric, $x = g(t)$, $y = g(t)$, then the arc length from $A(g(t_A), g(t_A))$ to $B(g(t_B), g(t_B))$ is:

$$s = \int_{t_A}^{t_B} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} dt$$

If the equation is given in polar form $r = g(\theta)$, then the arc length from half lines $\theta = \alpha$ to $\theta = \beta$ is:

$$s = \int_{\alpha}^{\beta} \sqrt{r^2 + \left(\frac{dr}{d\theta}\right)^2} d\theta$$


## Surface Area of Volume of Revolution
The area, $S$, of the surface generated when the arc $A B$ on the curve $C$ is rotated completely about the $x$-axis is $2 \pi \int y \mathrm{ds}$, and about the $y$-axis is $2 \pi \int x \mathrm{ds}$.
These can be used to give the following results:
- About the $x$-axis: $$S=2 \pi \int_{x_A}^{x_x} y \sqrt{1+\left(\frac{\mathrm{d} y}{\mathrm{~d} x}\right)^2} \mathrm{~d} x$$
- About the $y$-axis: $$S=2 \pi \int_{y_A}^{y_s} x \sqrt{1+\left(\frac{\mathrm{d} x}{\mathrm{~d} y}\right)^2} \mathrm{~d} y \quad \text{or} \quad S=2 \pi \int_{x_A}^{x_s} x \sqrt{1+\left(\frac{\mathrm{d} y}{\mathrm{~d} x}\right)^2} \mathrm{~d} x$$
If $C$ is given in parametric form, the results are
- About the $x$-axis: $$S=2 \pi \int_{t_A}^{t_s} y \sqrt{\left(\frac{\mathrm{d} x}{\mathrm{~d} t}\right)^2+\left(\frac{\mathrm{d} y}{\mathrm{~d} t}\right)^2} \mathrm{~d} t$$
- About the $y$-axis: $$S=2 \pi \int_{t_A}^{t_s x} \sqrt{\left(\frac{\mathrm{d} x}{\mathrm{~d} t}\right)^2+\left(\frac{\mathrm{d} y}{\mathrm{~d} t}\right)^2} \mathrm{~d} t$$
If $C$ is given in polar form, the results are
- About the initial line $\theta = 0$  $$S=2 \pi \int_\alpha^3 r \sin \theta \sqrt{r^2+\left(\frac{\mathrm{d} \theta}{\mathrm{d} r}\right)^2} \mathrm{~d} \theta$$
- About the line $\theta= \pm \frac{\pi}{2}:$ $$ S=2 \pi \int_\alpha^\beta r \cos \theta \sqrt{r^2+\left(\frac{\mathrm{d} \theta}{\mathrm{d} r}\right)^2} \mathrm{~d} \theta$$

## Flashcards

What is the Reduction Formula used for in integration? ? The Reduction Formula is used to write an integral as a recurrence relation, particularly for integrals with high powers that would require many integration by parts iterations. It is expressed as:

$$J_n = \int g(x,n)dx = \sum_{r=0}^{n-1} g_r(n)I_r$$

What is the general form of the Reduction Formula for integration? ? The general form of the Reduction Formula is:

$$J_n = \int g(x,n)dx = \sum_{r=0}^{n-1} g_r(n)I_r$$

Where $J_n$ represents the integral, $g(x,n)$ is the integrand, and $g_r(n)$ and $I_r$ are components of the recurrence relation.

What is the formula for integrating $(g(x))^n g'(x)$? ? The formula for integrating $(g(x))^n g'(x)$ is:

$$\int (g(x))^n g'(x) dx = \frac{1}{n+1} g(x)^{n+1}$$

This is a useful result that often appears in reduction formulas.

How can the reduction formula be used with other integration techniques? ? The reduction formula can be used in conjunction with a substitution $r = g(x)$ and the Method of Differences to compute tricky summations. This combination of techniques can be powerful for solving complex integrals.

What is the formula for arc length in Cartesian coordinates? ? The arc length formula for a function $y = g(x)$ from point $A(x_A, y_A)$ to $B(x_B, y_B)$ in Cartesian coordinates is:

$$s = \int_{x_A}^{x_B} \sqrt{1 + (\frac{dy}{dx})^2} dx$$

Alternatively, it can be expressed as:

$$s = \int_{y_A}^{y_B} \sqrt{1 + (\frac{dx}{dy})^2} dy$$

What is the arc length formula for parametric equations? ? For parametric equations $x = g(t)$ and $y = g(t)$, the arc length from $A(g(t_A), g(t_A))$ to $B(g(t_B), g(t_B))$ is given by:

$$s = \int_{t_A}^{t_B} \sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2} dt$$

How is arc length calculated in polar coordinates? ? In polar coordinates, for an equation $r = g(\theta)$, the arc length from half-line $\theta = \alpha$ to $\theta = \beta$ is calculated using:

$$s = \int_{\alpha}^{\beta} \sqrt{r^2 + (\frac{dr}{d\theta})^2} d\theta$$

What are the different forms of the arc length formula? ? The arc length formula has three main forms:

1. Cartesian: $s = \int_{x_A}^{x_B} \sqrt{1 + (\frac{dy}{dx})^2} dx$ or $s = \int_{y_A}^{y_B} \sqrt{1 + (\frac{dx}{dy})^2} dy$

2. Parametric: $s = \int_{t_A}^{t_B} \sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2} dt$

3. Polar: $s = \int_{\alpha}^{\beta} \sqrt{r^2 + (\frac{dr}{d\theta})^2} d\theta$

Each form is suited to different types of equations or coordinate systems.