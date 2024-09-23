# A-Level Further Core 2

## Hyperbolic Functions

Hyperbolic functions are functions with similar properties to [Trigonometric Functions](Trigonometric%20Functions.md) but are defined in terms of exponentials: ^542b73

$$\sinh(x) \equiv \frac{e^x - e^{-x}}{2}$$
$$\cosh(x) \equiv \frac{e^x + e^{-x}}{2}$$
$$\tanh(x) \equiv \frac{\sinh(x)}{\cosh(x)} = \frac{e^{2x} - 1}{e^{2x} + 1}$$

There are also hyperbolic reciprocal functions: ^2d4eda

$$\text{cosech}(x) \equiv \frac{1}{\sinh(x)} = \frac{2}{e^x - e^{-x}}$$
$$\text{sech}(x) \equiv \frac{1}{\cosh(x)} = \frac{2}{e^x + e^{-x}}$$
$$\coth(x) \equiv \frac{1}{\tanh(x)} = \frac{\cosh(x)}{\sinh(x)} = \frac{e^{2x} + 1}{e^{2x} - 1}$$

Another property of hyperbolic functions that follows the trig functions is that:

* $\sinh(x)$ is odd, so $\sinh(-x) = -\sinh(x), a \in \mathbb{R}$
* $\cosh(x)$ is even, so $\cosh(-x) = \cosh(x), a \in \mathbb{R}$

Range and domain:

* $\sinh(x) = y$: $x \in \mathbb{R}, y \in \mathbb{R}$
* $\cosh(x) = y$: $x \in \mathbb{R}, y \in \mathbb{R}, y \geq 1$
* $\tanh(x) = y$: $x \in \mathbb{R}, y \in \mathbb{R}, -1 \< y \< 1$

## Inverse Hyperbolic Functions

Each hyperbolic function has an inverse:

|Hyperbolic function|Inverse|
|-------------------|-------|
|$y = \sinh(x)$|$y = \text{arsinh}(x)$|
|$y = \cosh(x), x \geq 0$|$y = \text{arcosh}(x), x \geq 1$|
|$y = \tanh(x)$|$y = \text{artanh}(x)$, $\lvert x \rvert$ $\< 1$|

*WATCH OUT: prefix of inverse functions is "ar-" not "arc-" although "arc-" will be understood.*

You can also write inverse hyperbolic functions in terms of $\ln$ (the intuition is that ln is the inverse of $e^x$):

$$\text{arsinh}(x) = \ln(x + \sqrt{x^2 + 1})$$
$$\text{arcosh}(x) = \ln(x + \sqrt{x^2 - 1}), x \geq 1$$
$$\text{artanh}(x) = \frac{1}{2}\ln \left(\frac{1+x}{1-x}\right), |x| \< 1$$

## Identities & Equations:

Generally given a trig identity you can find the corresponding hyperbolic identity with Osborn's rule:

$\cos(x) \rightarrow \cosh(x)$ 
$\sin(x) \rightarrow \sinh(x)$

Only change product of 2 sin terms from the sign:

$\sin^2(x) \rightarrow -\sinh^2(x)$
$\sin A \sin B \rightarrow -\sinh(A)\sinh(B)$

## Calculus With Hyperbolic Functions

### Differentiation

$$\begin{aligned}
\\frac{d}{dx} \sinh(x) &= \cosh(x) \\
\\frac{d}{dx} \cosh(x) &= \sinh(x) \\
\\frac{d}{dx} \tanh(x) &= \text{sech}^2(x) \\
\\frac{d}{dx} \text{arsinh}(x) &= \frac{1}{\sqrt{x^2+1}} \\
\\frac{d}{dx} \text{arcosh}(x) &= \frac{1}{\sqrt{x^2-1}} \\
\\frac{d}{dx} \text{artanh}(x) &= \frac{1}{1-x^2}
\\end{aligned}$$

### Integration

$$\begin{aligned}
\\int \sinh(x) , dx &= \cosh(x) + C \\
\\int \cosh(x) , dx &= \sinh(x) + C \\
\\int \frac{1}{\sqrt{1+x^2}} , dx &= \text{arsinh}(x) + C \\
\\int \frac{1}{\sqrt{x^2-1}} , dx &= \text{arcosh}(x) + C \\
\\int \frac{1}{1-x^2} , dx &= \text{artanh}(x) + C \\
\\int \tanh(x) , dx &= \ln(\cosh(x)) + C \\
\\int \frac{1}{\sqrt{a^2+x^2}} , dx &= \text{arsinh}\left(\frac{x}{a}\right) + C \\
\\int \frac{1}{\sqrt{x^2-a^2}} , dx &= \text{arcosh}\left(\frac{x}{a}\right) + C
\\end{aligned}$$

## Flashcards

\#Maths/Topics/Hyperbolic-Trig, #Maths/Topics/Differentiation, #Maths/A-Level-Further-Core/Hyperbolic-Trig 

What is the derivative of $\sinh(x)$?
?
The derivative of $\sinh(x)$ is $\cosh(x)$.
$$\frac{d}{dx} \sinh(x) = \cosh(x)$$ <!--SR:!2024-11-04,51,310-->

What is the derivative of $\cosh(x)$?
?
The derivative of $\cosh(x)$ is $\sinh(x)$.
$$\frac{d}{dx} \cosh(x) = \sinh(x)$$ <!--SR:!2024-11-13,60,310-->

What is the derivative of $\tanh(x)$?
?
The derivative of $\tanh(x)$ is $\text{sech}^2(x)$.
$$\frac{d}{dx} \tanh(x) = \text{sech}^2(x)$$ <!--SR:!2024-11-13,60,290-->

What is the derivative of $\text{arsinh}(x)$?
?
The derivative of $\text{arsinh}(x)$ is $\frac{1}{\sqrt{x^2+1}}$.
$$\frac{d}{dx} \text{arsinh}(x) = \frac{1}{\sqrt{x^2+1}}$$ <!--SR:!2024-10-24,40,290-->

What is the derivative of $\text{arcosh}(x)$?
?
The derivative of $\text{arcosh}(x)$ is $\frac{1}{\sqrt{x^2-1}}$.
$$\frac{d}{dx} \text{arcosh}(x) = \frac{1}{\sqrt{x^2-1}}$$ <!--SR:!2024-09-23,9,230-->

What is the derivative of $\text{artanh}(x)$?
?
The derivative of $\text{artanh}(x)$ is $\frac{1}{1-x^2}$.
$$\frac{d}{dx} \text{artanh}(x) = \frac{1}{1-x^2}$$ <!--SR:!2024-09-26,8,230-->

\#Maths/Topics/Hyperbolic-Trig, #Maths/Topics/Integration , #Maths/A-Level-Further-Core/Hyperbolic-Trig 

What is the integral of $\sinh(x)$?
?
The integral of $\sinh(x)$ is $\cosh(x) + C$.
$$\int \sinh(x) , dx = \cosh(x) + C$$ <!--SR:!2024-11-12,59,310-->

What is the integral of $\cosh(x)$?
?
The integral of $\cosh(x)$ is $\sinh(x) + C$.
$$\int \cosh(x) , dx = \sinh(x) + C$$ <!--SR:!2024-11-11,58,310-->

What is the integral of $\frac{1}{\sqrt{1+x^2}}$?
?
The integral of $\frac{1}{\sqrt{1+x^2}}$ is $\text{arsinh}(x) + C$.
$$\int \frac{1}{\sqrt{1+x^2}} , dx = \text{arsinh}(x) + C$$ <!--SR:!2024-10-10,26,270-->

What is the integral of $\frac{1}{\sqrt{x^2-1}}$?
?
The integral of $\frac{1}{\sqrt{x^2-1}}$ is $\text{arcosh}(x) + C$.
$$\int \frac{1}{\sqrt{x^2-1}} , dx = \text{arcosh}(x) + C$$ <!--SR:!2024-11-08,55,310-->

What is the integral of $\frac{1}{1-x^2}$?
?
The integral of $\frac{1}{1-x^2}$ is $\text{artanh}(x) + C$.
$$\int \frac{1}{1-x^2} , dx = \text{artanh}(x) + C$$ <!--SR:!2024-10-02,14,290-->

What is the integral of $\tanh(x)$?
?
The integral of $\tanh(x)$ is $\ln(\cosh(x)) + C$.
$$\int \tanh(x) , dx = \ln(\cosh(x)) + C$$ <!--SR:!2024-09-26,12,210-->

What is the integral of $\frac{1}{\sqrt{a^2+x^2}}$?
?
The integral of $\frac{1}{\sqrt{a^2+x^2}}$ is $\text{arsinh}\left(\frac{x}{a}\right) + C$.
$$\int \frac{1}{\sqrt{a^2+x^2}} , dx = \text{arsinh}\left(\frac{x}{a}\right) + C$$ <!--SR:!2024-09-19,1,210-->

What is the integral of $\frac{1}{\sqrt{x^2-a^2}}$?
?
The integral of $\frac{1}{\sqrt{x^2-a^2}}$ is $\text{arcosh}\left(\frac{x}{a}\right) + C$.
$$\int \frac{1}{\sqrt{x^2-a^2}} , dx = \text{arcosh}\left(\frac{x}{a}\right) + C$$ <!--SR:!2024-11-13,60,310-->
