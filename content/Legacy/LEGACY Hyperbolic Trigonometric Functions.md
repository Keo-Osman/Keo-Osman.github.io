# Definitions

Hyperbolic functions are functions with similar properties to [[Trigonometric Functions]] but are defined in terms of exponentials:









$$
\sinh(x) \equiv \frac{e^x - e^{-x}}{2} \quad \quad
\cosh(x) \equiv \frac{e^x + e^{-x}}{2}\quad \quad
\tanh(x) \equiv \frac{\sinh(x)}{\cosh(x)} = \frac{e^{2x} - 1}{e^{2x} + 1}
$$


















$$
\begin{aligned}
\text{cosech}(x) \equiv &\frac{1}{\sinh(x)} = \frac{2}{e^x - e^{-x}} \quad \quad 
\text{sech}(x) \equiv \frac{1}{\cosh(x)} = \frac{2}{e^x + e^{-x}} \\
&\coth(x) \equiv \frac{1}{\tanh(x)} = \frac{\cosh(x)}{\sinh(x)} = \frac{e^{2x} + 1}{e^{2x} - 1}
\end{aligned}
$$










---
# A-Level Further Core 2
## Properties
### Parity
$\sinh(x)$ is odd, so $\sinh(-x) = -\sinh(x), a \in \mathbb{R}$
$\cosh(x)$ is even, so $\cosh(-x) = \cosh(x), a \in \mathbb{R}$
$\tanh(x)$ is odd, so $\tanh(-x) = -\tanh(x), a \in \mathbb{R}$
### Range and Domain
$\sinh(x)$ -  $x \in \mathbb{R}, y \in \mathbb{R}$
$\cosh(x)$ -  $x \in \mathbb{R}, y \in \mathbb{R}, y \geq 1$
$\tanh(x)$ -  $x \in \mathbb{R}, y \in \mathbb{R}, -1 < y < 1$
## Inverse Hyperbolic Functions
| Hyperbolic function      | Inverse                                         | Natural Log Form                                                              |
| ------------------------ | ----------------------------------------------- | ----------------------------------------------------------------------------- |
| $y = \sinh(x)$           | $y = \text{arsinh}(x)$                          | $\text{arsinh}(x) = \ln(x + \sqrt{x^2 + 1})$                                  |
| $y = \cosh(x), x \geq 0$ | $y = \text{arcosh}(x), x \geq 1$                | $\text{arcosh}(x) = \pm\ln(x + \sqrt{x^2 - 1})$                               |
| $y = \tanh(x)$           | $y = \text{artanh}(x)$, $\lvert x \rvert$ $< 1$ | $\displaystyle\text{artanh}(x) = \frac{1}{2}\ln \left(\frac{1+x}{1-x}\right)$ |
## Identities and Equations
Generally given a trig identity you can find the corresponding hyperbolic identity with **Osborn's Rule**









$$
\cos(x) \rightarrow \cosh(x) \quad \sin(x) \rightarrow \sinh(x) \quad \sin^2(x) \rightarrow -\sinh^2(x) \quad\sin A \sin B \rightarrow -\sinh(A)\sinh(B)
$$









## Calculus With Hyperbolic Functions
Most found in formula booklet
### Differentiation









$$
\begin{aligned}
&\frac{d}{dx} \sinh(x) = \cosh(x) &&\frac{d}{dx} \cosh(x) = \sinh(x) \\
&\frac{d}{dx} \tanh(x) = \text{sech}^2(x) &&\frac{d}{dx} \text{arsinh}(x) = \frac{1}{\sqrt{x^2+1}} \\
&\frac{d}{dx} \text{arcosh}(x) = \frac{1}{\sqrt{x^2-1}} &&\frac{d}{dx} \text{artanh}(x) = \frac{1}{1-x^2}
\end{aligned}
$$









### Integration









$$
\begin{aligned}
&\int \sinh(x) \, dx = \cosh(x) + C &&\int \frac{1}{\sqrt{a^2+x^2}} \, dx = \text{arsinh}\left(\frac{x}{a}\right) + C \\
&\int \cosh(x) \, dx = \sinh(x) + C &&\int \frac{1}{\sqrt{x^2-a^2}} \, dx = \text{arcosh}\left(\frac{x}{a}\right) + C\\
&\int \tanh(x) \ dx = \ln(\cosh(x)) + C &&\int \frac{1}{1-x^2} \, dx = \text{artanh}(x) + C 
\end{aligned}
$$










