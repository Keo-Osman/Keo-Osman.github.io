# Definition

A recurrence relation describes a term of a sequence as in terms of previous terms.

They can use varying amounts of previous terms (go back further) and you can describe this by the order which is defined as the difference between the lowest & highest subscript.

# A-Level Further Pure 2

## Solving First Order Recurrence Relations

First order linear recurrence relations are in the form
$$U_n = aU\_{n-1} + g(n)$$

If $g(n) = 0$ then the equation is homogeneous and the general solution is

$$U_n = a^nU_0 \quad \text{or} \quad U_n = a^nC$$
*(Where $C$ is a constant to be found depending on initial conditions)*
You can do this by repeatedly substituting previous terms and the result can be rigorously proved with induction.
*(This is very similar to differential equations as recurrence relations are basically discrete cases of [Differential Equations](Differential%20Equations.md))*

You can use this back/substitution to get the general solution of $U_n = U\_{n-1} + g(n)$ is

$$U_n = U_0 + \sum_{i=0}^n g(i)$$

### Non-Homogenous

To find the general solution to $U_n = aU\_{n-1} + g(n)$ where $a \neq 1$ you find the solution to the C.F: $U_n = aU\_{n-1}$ and add the P.S (particular solution).

The form of P.S depends on $g(n)$

|Form of $g(n)$|Form of P.S|
|--------------|-----------|
|$p, a \neq 1$|$k$|
|$pn + q, a \neq 1$|$kn + l$|
|$kp^n, p \neq a$|$kr^n$|
|$ka^n$|$kna^n$|

## Solving Second Order Recurrence Relations

A 2nd order linear recurrence relation can be written in the form
$$U_n = aU\_{n-1} + bU\_{n-2} + g(n)$$
If $U_n = F(n)$ and $U_n = G(n)$ are solutions then $U_n = aF(n) + bG(n)$ where $a, b$ are constants is a solution.

The general solution to a homogeneous 2nd order linear recurrence relation of
$$U_n = aU\_{n-1} + bU\_{n-2}$$
depends on the auxiliary equation
$$r^2 - ar - b = 0$$

#### Case 1: 2 real roots

$$U_n = A\alpha^n + B\beta^n$$

#### Case 2: Repeated root

$$U_n = (A + Bn)\alpha^n$$

#### Case 3: Complex roots:

$$U_n = r^n(A \cos n\theta + B \sin n\theta)$$
or
$$U_n = A\alpha^n + B\beta^n$$

### Non-Homogeneous

For non-homogeneous the general solution is
$$U_n = C.F + P.S$$

|Form of $\mathbf{g}(\boldsymbol{n})$|Form of particular solution|
|:----------------------------------:|:-------------------------:|
|$p$ with $\alpha, \beta \neq 1$|$\lambda$|
|$p n+q$, with $\alpha, \beta \neq 1$|$\lambda n+\mu$|
|$k p^n$ with $p \neq \alpha, \beta$|$\lambda p^n$|
|$p$ with $\alpha=1, \beta \neq 1$|$\lambda n$|
|$p n+q$ with $\alpha=1, \beta \neq 1$|$\lambda n^2+\mu n$|
|$p$ with $\alpha=\beta=1$|$\lambda n^2$|
|$p n+q$ with $\alpha=\beta=1$|$\lambda n^3+\mu n^2$|
|$k \alpha^n$ with $\alpha \neq \beta$|$\lambda n \alpha^n$|
|$k \alpha^n$ with $\alpha=\beta$|$\lambda n^2 \alpha^n$|

## Proving closed forms:

* Show that it's true for 2 consecutive numbers
* Assume the closed form is true for $n=k, n=k-1$
* Show it's true for $n=k+1$ (inductive step)

