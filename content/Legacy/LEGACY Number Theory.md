# Definition
Number theory is the study of systems and properties of numbers, particularly $\mathbb{Z}$ and $\mathbb{N}$.
# A-Level Further Pure 2
## Divisibility
Given two integers $a, b$ where $a \neq 0$, then we can say $a|b$ ($a$ divides $b$ or $b$ is divisible by $a$) if an integer $k$ exists such that $b = ka$.
If $a$ does not divide $b$, it is denoted as $a \nmid b$. (This definition applies for negative divisors)
### Divisibility rules


$$
\begin{aligned}
&\forall a, b, c \in \mathbb{Z}\\ \\
&a|a, \quad a|0 \\
&a|b \wedge b|c \Rightarrow a|c\\\
&a|b \wedge a|c \Rightarrow a|(bn+cm) \quad \forall n,m \in \mathbb{Z} \\
&a|b \Leftrightarrow an|bn \quad \forall n \in \mathbb{Z}, n \neq 0 \\
&a|b \Rightarrow a \leq b \quad\forall a, b \in \mathbb{Z}^+
\end{aligned}
$$


### Division Algorithm
The division algorithm is a more rigorous way of defining division in the integers and is as follows:

Given that $a, b \in \mathbb{Z} \wedge b > 0 \Rightarrow \exists ! \space p, q$  *s.t* $a = bq + r$ with $0 \leq r < b$,
To find the quotient and remainder for any two integers
1. Begin with values $a$ and $b$
2. Set $q$ equal to the greatest integer that is $\leq \displaystyle\frac{a}{b}$
3. Set $r = a - bq$
4. $a|b \Leftrightarrow r = 0$ 
*($a$ is called the dividend, $b$ the divisor, $q$ the quotient, and $r$ the remainder)*
## Greatest Common Divisor and Bézout's Identity
The greatest common divisor of $a$ and $b$ ($\gcd(a,b)$) is the greatest $c \in \mathbb{Z}$ such that $c|a$ and $c|b$.

You can find $\gcd(a,b)$ by using prime factors; however, a faster way for large numbers $a$, $b$ is the Euclidean algorithm:
1. Apply the division algorithm to $a$, $b$ to get $a = bq_1 + r_1$. If $r_1 = 0$, then $b|a$ and $\gcd(a,b) = b$
2. If $r_1 \neq 0$, then repeat the algorithm with $b$ and $r_1$ to get $b = q_1r_1 + r_2$. If $r_2 = 0$, then $\gcd(a,b) = r_1$
3. If $r_2 \neq 0$, then keep repeating the algorithm until you get $r_{n-2} = q_{n+1}r_n + r_{n+1}$ where $r_{n+1} = 0$, then $r_n = \gcd(a,b)$
### Bezout's Identity
The identity states that given 


$$
\begin{aligned}
&a, b \in \mathbb{Z} \space a \neq b \neq 0\\
\Rightarrow& \\
&\exists x, y \in \mathbb{Z} \text{ s.t } \gcd(a,b) = ax + by
\end{aligned}
$$



You can figure out $x$ and $y$ by going through the Euclidean Algorithm backwards and collecting like terms.
### Coprime
Two integers $a$, $b$ are coprime if $\gcd(a,b) = 1$ so by Bezout's Identity $\exists x,y \in \mathbb{Z}$ *s.t* $ax + by = 1$
## Modular Arithmetic
Modular arithmetic is a system of arithmetic restricted to the remainders.
### Congruence
**Definition**
$a \equiv b \pmod{m} \Leftrightarrow m|(a-b)$,  $m \in \mathbb{Z}^+$, $a, b \in \mathbb{Z}$,
$a \equiv b \pmod{m} \Leftrightarrow \exists k \in \mathbb{Z}$ such that $a = b + km$

**Properties**
$a \equiv 0 \pmod{m} \Leftrightarrow m|a$
$a \equiv a \pmod{m}$
$a \equiv b \pmod{m} \Rightarrow b \equiv a \pmod{m}$
$(a \equiv b \pmod{m}) \wedge (b \equiv c \pmod{m}) \Rightarrow a \equiv c \pmod{m}$

Let $a, b, c, d, n, p, k \in \mathbb{Z}$ and $m, n > 0$, with $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m} \Rightarrow$
$ka \equiv kb \pmod{m}$
$a \pm c \equiv b \pm d \pmod{m}$
$ac \equiv bd \pmod{m}$
$a^n \equiv b^n \pmod{m}$
## Number Bases
You can represent a number with digits $a_n \ldots a_0$ in base $m$ as:


$$
\sum_{r=0}^n m^r a_r
$$


## Divisibility Tests
In base 10 a number is divisible by
- 3 $\Leftrightarrow$ sum of digits is divisible by 3
- 4 $\Leftrightarrow$ last 2 digits are divisible by 4
- 9 $\Leftrightarrow$ sum of digits is divisible by 9
- 11 $\Leftrightarrow$ alternating sum of digits (starts with $-$)

## Solving Congruence Equations
Equations with modular arithmetic are given in terms called congruence equations and their answers are usually given in terms of least residues.
The set of least residues $\bar{k} \pmod{m}$ is $\{0, 1, \ldots, m-1\}$

Since a solution $x \equiv n \pmod{m}$ represents an infinite number of solutions, you can write a general solution as: $\{n + km : k \in \mathbb{Z}\}$

### Congruence Equation Properties
Let $a, b, m \in \mathbb{Z}, m > 0$,  $\gcd(a,m) = d$
- $d \nmid b \Rightarrow$ the equation $ax \equiv b \pmod{m}$ has no solutions
- $d \mid b \Rightarrow$ the equation has $d$ solutions in the set of least residues
- $(ka \equiv kb \pmod{m}) \wedge (\gcd(k,m) = d) \Rightarrow a \equiv b \pmod{\frac{m}{d}}$

### Multiplicative Inverses
A multiplicative inverse of $a(\operatorname{mod} m)$ is $p \in \mathbb{Z}$ such that $ap \equiv 1(\operatorname{mod} m)$  However $\exists p \Leftrightarrow \operatorname{gcd}(a, m)=1$
You can find $p$ by using **Bezout's Identity**
**Proof**
$\gcd(a, m) = 1\Leftrightarrow \exists p, q \text{ s.t } ap +mq=1 \Rightarrow ap=1-mq \Rightarrow ap=1(mod \space m)$
## Fermat's Little Theorem
$p$ is prime and $p \nmid a \Rightarrow$ $a^{p-1} \equiv 1(\operatorname{mod} p)$

Congruence equations with prime modulo can be solved with *Fermat's Little Theorem*
$p$ is prime ^ $p \nmid a \Rightarrow gcd(a, p)=1 \Rightarrow ax=b(\operatorname{mod} p)$ has one solution.


$$
\begin{aligned}
& ax \equiv b\space(\operatorname{mod} p) \Rightarrow a^{p-2} a x \equiv a^{p-2} b(\operatorname{mod} p) \Rightarrow \\
& x \equiv a^{p-2} b(\operatorname{mod} p) 
 \text { as } a^{p-2} a=a^{p-1} \space\wedge\space a^{p-1} \equiv 1(\operatorname{mod} p) \\
\end{aligned}
$$


## Combinatorics
If a set $S$ contains $n$ elements, then the total number of possible subsets of $S$ is $2^n$.
There are $n$ ! different ways of placing $n$ items in order.
The number of possible permutations of $r$ items taken from a set of $n$ items, where $n \geqslant r$, is given by 

$$
{ }^n P_r=\frac{n!}{(n-r)!}
$$


The number of permutations of $n$ items, of which $r$ are identical is given by $\displaystyle\frac{n!}{r!}$
The number of permutations of $n$ items, of which $r_1$ are identical, $r_2$ are identical, and so on, is given by 

$$
\frac{n!}{r_{1}!\times r_{2}!\times \ldots}
$$


The number of possible combinations of $r$ items (in any order) taken from a set of $n$ items, where $n \geqslant r$, is given by 

$$
{ }^n C_r=\binom{n}{r}=\frac{n!}{r!(n-r)!}
$$



---
