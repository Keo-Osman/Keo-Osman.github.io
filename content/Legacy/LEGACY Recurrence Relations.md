# Definition
A Recurrence Relation describes a term of a sequence as in terms of previous terms.
They can use varying amounts of previous terms (go back further) and you can describe this by the order which is defined as the difference between the lowest & highest subscript.
They are strongly related to [[LEGACY Differential Equations|Differential Equations]] and are often solved in the same/similar ways as recurrence relations are basically discrete differential equations 

---
# A-Level Further Pure 2
## First Order Recurrence Relations
First order linear recurrence relations are in the form
$$u_n = au_{n-1} + g(n)$$
### Homogenous
If $g(n) = 0$ then the equation is **homogeneous** and the general solution is
$$u_n = a^nu_0 \quad \text{or} \quad u_n = a^{n-1}u_{1}$$
This is proved by **back substitution** *or more rigorously with **[[Proof by Induction]]***$$\begin{aligned}
u_{n} & =au_{n-1} \\
 & =a\times au_{n-2}=a^2u_{n-2} \\
 & =a^2\times au_{n-3}=a^3u_{n-3} \\
 & \vdots \\
 & =a^{n-1}u_1 \\
 & =a^nu_0
\end{aligned}$$
### Non-Homogenous
For $u_n = u_{n-1} + g(n)$, the general solution is $u_n = u_0 + \sum_{i=0}^n g(i)$

To find the general solution to $u_n = au_{n-1} + g(n)$ where $a \neq 1$ is $C.F + P.S$, Where $C.F$ is the solution to $u_n = au_{n-1}$ which is $a^nu_0$ and $P.S$ is a particular solution to the equation.

| Form of $g(n)$     | Form of $P.S$     |
| ------------------ | ----------------- |
| $p, a \neq 1$      | $\lambda$         |
| $pn + q, a \neq 1$ | $\lambda n + \mu$ |
| $kp^n, p \neq a$   | $\lambda k^n$     |
| $ka^n$             | $\lambda na^n$    |
## Solving Second Order Recurrence Relations
A 2nd order linear recurrence relation can be written in the form
$$u_n = au_{n-1} + bu_{n-2} + g(n)$$
If $u_n = F(n)$ and $u_n = G(n)$ are particular solutions to a linear recurrence relation then $u_n = aF(n) + bG(n)$ is a solution.

### Homogenous
The general solution to a homogeneous 2nd order linear recurrence relation of
$u_n = au_{n-1} + bu_{n-2}$ depends on the auxiliary equation $r^2 - ar - b = 0$

This quadratic leads to 3 cases.
- The auxiliary equation has 2 real root $\Rightarrow u_n = A\alpha^n + B\beta^n$
- The auxiliary equation has 1 repeated root $\alpha$. $\Rightarrow u_n = (A + Bn)\alpha^n$
- The auxiliary equation has two complex conjugate roots $re^{\pm i \theta}$ $\Rightarrow u_n = r^n(A \cos n\theta + B \sin n\theta) = C\alpha^n + D\beta^n$
### Non-Homogeneous
For non-homogeneous the general solution is
$$u_n = C.F + P.S$$

| Form of $\mathbf{g}(\boldsymbol{n})$  | Form of particular solution |
| :-----------------------------------: | :-------------------------: |
|    $p$ with $\alpha, \beta \neq 1$    |          $\lambda$          |
| $p n+q$, with $\alpha, \beta \neq 1$  |       $\lambda n+\mu$       |
|  $k p^n$ with $p \neq \alpha, \beta$  |        $\lambda p^n$        |
|   $p$ with $\alpha=1, \beta \neq 1$   |         $\lambda n$         |
| $p n+q$ with $\alpha=1, \beta \neq 1$ |     $\lambda n^2+\mu n$     |
|       $p$ with $\alpha=\beta=1$       |        $\lambda n^2$        |
|     $p n+q$ with $\alpha=\beta=1$     |    $\lambda n^3+\mu n^2$    |
| $k \alpha^n$ with $\alpha \neq \beta$ |    $\lambda n \alpha^n$     |
|   $k \alpha^n$ with $\alpha=\beta$    |   $\lambda n^2 \alpha^n$    |
*(When $\alpha =1$ or $\beta =1$ you have to multiply the $P.S$ by $n$ so otherwise there will be redundancy and overlap and $C.F$ and $P.S$ are supposed to be linearly independent. This stacks if $\alpha= \beta = 1$ then multiply by $n$ twice which is the same as multiplying by $n^2$)*
## Proving closed forms
You can rigorously prove a closed for $u_n = f(n)$ by using [[Proof by Induction]]. This will require multiple base cases if the order of the relationship is $>1$. In general for an $n$ ordered recurrence relation, you will need to prove the base case for the first $n$ terms

---
# Flashcards
## A-Level Further Pure 2
#z_Legacy/Maths/A-Levels/Further-Pure/Recurrence-Relations
What is the general solution for a homogeneous first-order linear recurrence relation?
?
For a homogeneous first-order linear recurrence relation ($g(n) = 0$), the general solution is:
$$u_n = a^nu_0 \quad \text{or} \quad u_n = a^{n-1}u_{1}$$ 


How do you find the general solution for a non-homogeneous first-order linear recurrence relation where $a \neq 1$?
?
To find the general solution for $u_n = au_{n-1} + g(n)$ where $a \neq 1$:
1. Find the solution to the complementary function (C.F): $u_n = au_{n-1}$
2. Find the particular solution (P.S) based on the form of $g(n)$
3. Add C.F and P.S to get the general solution   



What is the auxiliary equation for a homogeneous second-order linear recurrence relation $u_n = au_{n-1} + bu_{n-2}$, ?
?
For a homogeneous second-order linear recurrence relation $u_n = au_{n-1} + bu_{n-2}$, the auxiliary equation is:
$$r^2 - ar - b = 0$$   

What are the three cases for the general solution of a homogeneous second-order linear recurrence relation?
?
The three cases are:
1. Two real roots: $u_n = A\alpha^n + B\beta^n$
2. Repeated root: $u_n = (A + Bn)\alpha^n$
3. Complex roots $re^{\pm i \theta}$:
   $u_n = r^n(A \cos n\theta + B \sin n\theta)$ or $u_n = A\alpha^n + B\beta^n$   

How do you prove a closed form solution for a recurrence relation?
?
To prove a closed form solution:
1. Show that it's true for 2 consecutive numbers
2. Assume the closed form is true for $n=k$ and $n=k-1$
3. Show it's true for $n=k+1$ (inductive step)   

What is the general solution for a non-homogeneous second-order linear recurrence relation?
?
The general solution for a non-homogeneous second-order linear recurrence relation is:
$$u_n = C.F + P.S$$
Where C.F is the complementary function (solution to the homogeneous equation) and P.S is the particular solution.
The particular integral $(P.S)$ is a specific function that satisfies the recurrence relation.
To find the $P.S$, assume  $P.I = f(n)$ that has the same form as $g(n)$, then plug it into the original equation to find the coefficients.
*(When $\alpha =1$ or $\beta =1$ you have to multiply the $P.S$ by $n$ so otherwise there will be redundancy and overlap and $C.F$ and $P.S$ are supposed to be linearly independent. This stacks if $\alpha= \beta = 1$ then multiply by $n$ twice which is the same as multiplying by $n^2$)*  


