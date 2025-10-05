#Maths/Number-Theory 
*links: [[Primes]]*
# Basic Divisibility Properties
Let $x, y, z \in \mathbb{Z}$ 
1. $x|x$ *(reflexive property)* 
2. $x|y \text{ and } y|z \Rightarrow x|z$ *(transitivity property)* 
3. $x|y \text{ and } y≠0 \Rightarrow |x| \leq |y|$ 
4. $x|y \text{ and } x|z \Rightarrow x|ay+bz$ $\forall a,b \in \mathbb{Z}$ 
5. $x|y \text{ and } x|(y+z) \Rightarrow x|z$ 
6. $x|y \text{ and } y|x \Rightarrow |x|=|y|$
7. $x|y \text{ and } y≠0 \Rightarrow \frac{y}{x}|y$
8. $(z≠0) \text{ and } x|y \Leftrightarrow xz|yz$ 
9. $x$ has an even number of divisors $\Leftrightarrow \nexists n \in \mathbb{Z}$ s.t $x = n^2$
10. $p|\binom{p}{k} \quad (0<k<p)$

---
# Euclid's Division Lemma


$$
\forall a,b \in \mathbb{Z}, \ \exists q, r \in \mathbb{Z} \ \text{ s.t } \ a=bq+r, \ 0\leq r \leq b
$$



---
# GCD
## Properties
1. $p$ is prime $\Rightarrow \gcd(p,m) = p$ or $\gcd(p,m) = 1$ 
2. If $d = \gcd(m,n)$, $m = d \cdot m'$, $n = d \cdot n' \Rightarrow \gcd(m',n') = 1$ 
3. $d = \gcd(m,n)$, $m = d' \cdot m''$, $n = d' \cdot n''$, $\gcd(m'',n'') = 1 \Rightarrow d' = d$
4. If $d$ is a common divisor of $m, n \Rightarrow d|\gcd(m,n)$
5. $p^k||m \text{ and } p^j||n \Rightarrow p^{\min(k,j)}||\gcd(m,n)$ 
6. $m = p_1^{\alpha_1} \cdots p_r^{\alpha_r}$, $n = p_1^{\beta_1} \cdots p_r^{\beta_r}$, $\alpha_i, \beta_i \geq 0 \Rightarrow \gcd(m,n) = p_1^{\min(\alpha_1,\beta_1)} \cdots p_r^{\min(\alpha_r,\beta_r)}$ 
7. $\gcd(a \pm kb, b) = \gcd(a, b)$
	1. $\gcd(a, b) = d, \ \gcd(a \pm kb, b) = d'$
	2. By definition $d'|b$ and $d'|a \pm kb \Rightarrow d'|a$
	3. So $d'$ has to be a common divisor of $a$ and $b$. And $d$, by definition, is the greatest number that satisfies that. Therefore $\gcd(a \pm kb, b) = \gcd(a, b)$
8. $a = bq + r \Rightarrow \gcd(a,b) = \gcd(b,r)$
	1. $\gcd(a, b) = \gcd (bq+r, b)$
	2. By property 7, $\gcd (bq+r, b)= \gcd(bq+r-q(b), b) = \gcd(a, b)$
9. $a|bc \text{ and } \gcd(a,b) = 1 \Rightarrow a|c$ 
10. $\gcd(a,b) = 1 \text{ and } a|c \text{ and } b|c \Rightarrow ab|c$ 
11. $\gcd(a^m-1, a^n-1)=a^{\gcd(m,n)}-1$
## Euclid's Division Algorithm
By repeatedly apply property 8: $a = bq + r \Rightarrow \gcd(a,b) = \gcd(b,r)$. You can find the $\gcd$ of any 2 numbers easily

## Bézout's Identity
$\forall m,n \in \mathbb{Z}$ $\exists x,y \in \mathbb{Z}$ s.t $\gcd(m,n) = mx+ny$
You can figure out $x$ and $y$ by going through the Euclidean Algorithm backwards and collecting like terms.
Two integers $a$, $b$ are coprime if $\gcd(m,n) = 1$ so by Bezout's Identity $\exists x,y \in \mathbb{Z}$ *s.t* $mx + ny = 1$
*Proof*
1. Consider the set of $S = \{mx+ny \ | \ x, y \in \mathbb{Z}, \ mx+ny>0\}$.
2. Since $S$ consists of non-negative integers there exists a minimal element $d$. So $d=mx_0+ny_0$
3. By the division algorithm $m = qd+r$, $0\leq r < d \Rightarrow r = m - qd = m - q(mx_0+ny_0)=m(1-qx_0)+b(-qy_0)$
4. This means that $r$ is a linear combination of $m, n$. If $0<r<d$ then $r \in S$ but this contradicts the minimality of $d$ so $r=0$. 
5. Hence $d|m$. The same argument can be made to show that $d|n$ meaning $d|\gcd(m,n)=g$.
6. Since $g|m$ and $g|n$, $g|mx_0+ny_0=d$ so we get $d|g$ and $g|d$ so $d=\gcd(m,n)$

This also proves that $|mx +ny| \geq \gcd(m,n)$ as $d$ was the minimal element.

---
# LCM
1. $\operatorname{lcm}(s,t) = m$, $m \cdot s' = t'$ $\Rightarrow gcd(s',t') = 1$
2. If $m'$ is common multiple of $s$ and $t$ and $m' \cdot s' = t'$, $gcd(s',t') = 1$
3.  $m'$ is a common multiple of $s$ and $t$ $\Rightarrow m | m'$
4. $m | s$, $n | s$ $\Rightarrow \operatorname{lcm}(m,n) | s$
5. $n \in \mathbb{Z}$ $\Rightarrow n \cdot \operatorname{lcm}(s,t) = \operatorname{lcm}(ns, nt)$
6. $s = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$, $t = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$ $\Rightarrow \operatorname{lcm}(s,t) = p_1^{\textstyle\max(\alpha_1,\beta_1)} \cdots p_k^{\textstyle\max(\alpha_k,\beta_k)}$
7. $mn = \operatorname{gcd}(m,n) \cdot \operatorname{lcm}(m,n)$ $\forall m,n \in \mathbb{Z}$

---
# Number of Divisors
## Properties
1. Given $n = p_1^{\alpha_1} \cdots p_r^{\alpha_k}$ the $\tau(n) =\displaystyle\sum_{d|n}1 = (\alpha_1+1)(\alpha_2+1) \cdots (\alpha_k+1)$
2. $n = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$ $\Rightarrow$ there are $(2\alpha_1+1)(2\alpha_2+1) \cdots (2\alpha_k+1)$ distinct ordered pairs $(a,b) \in \mathbb{Z}^+$ such that $\operatorname{lcm}(a,b) = n$
3. $\forall n \in \mathbb{Z}^+$, $\displaystyle\prod_{d|n} d = n^{\textstyle\frac{\tau(n)}{2}}$
4. $\forall n \in \mathbb{Z}^+$, $\tau(n) \leq 2\sqrt{n}$
5. $\tau(n) \text{ is odd } \Leftrightarrow n=k^2$ 
6. $\tau(n)$ is [[Arithmetic Functions#Multiplicative Functions|Multiplicative]].
### Explanations
1. Given $n = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$ the $\tau(n) =\displaystyle\sum_{d|n}1 = (\alpha_1+1)(\alpha_2+1) \cdots (\alpha_k+1)$
	1. *This is because any divisor must be in the form $p_1^{\beta_1} \cdots p_k^{\beta_k}$ with $0 \leq \beta_k \leq \alpha_k$ $\forall k$. So for each $k$ there are $\alpha_k+1$ choices for $k_k$. Since they are independent you multiply.*
2.  $n = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$ $\Rightarrow$ there are $(2\alpha_1+1)(2\alpha_2+1) \cdots (2\alpha_k+1)$ distinct ordered pairs $(a,b) \in \mathbb{Z}^+$ such that $\operatorname{lcm}(a,b) = n$	
	1. *This is because $a, b$ are divisors of $n$ so they must have the form $a = p_1^{\beta_1} \cdots p_k^{\beta_k}$ and $p_1^{\gamma_1} \cdots p_k^{\gamma_k}$ since $\operatorname{\operatorname{lcm}}(a,b) =  p_1^{\textstyle\max(\beta_1,\gamma_1)} \cdots p_k^{\textstyle\max(\beta_k,\gamma_k)}$ there are $2\alpha_1+1$ options for each $(\beta_k,\gamma_k)$: 

$$
\underbrace{(0,\alpha_k), (1,\alpha_k),...,}_{\alpha \text{ terms}} (\alpha_k,\alpha_k)\underbrace{,...,(\alpha_k,0)}_{\alpha \text{ terms}}
$$

 So you multiply number of choices together.
3. $\forall n \in \mathbb{Z}^+$, $\displaystyle\prod_{d|n} d = n^{\textstyle\frac{\tau(n)}{2}}$
	1. $n=a^2$
		1. You can split the divisors into $\textstyle\frac{\tau(n)}{2}-1$ pairs $(d, \textstyle\frac{n}{d})$ so their product is $n$ multiplying all together you get $n^{\textstyle\frac{\tau(n)-1}{2}}$ Then multiply by $\sqrt{n}$ yielding $n^{\textstyle\frac{\tau(n)}{ 2}}$
	2. $n\neq a^2$
		1. You can split the divisors into $\textstyle\frac{\tau(n)}{2}$ pairs $(d, \textstyle\frac{n}{d})$ so their product is $n$ multiplying all together you get $n^{\textstyle\frac{\tau(n)}{2}}$
4. $\forall n \in \mathbb{Z}^+$, $\tau(n) \leq 2\sqrt{n}$
	1. Let $d_1, d_2, ..., d_k$ be the divisors of $n \leq \sqrt{n}$. The rest of the divisors are $\frac{n}{d_1}, \frac{n}{d_2}, ..., \frac{n}{d_k}$. In each set there are $k$ numbers so $\tau(n) = 2k$ (or $2k-1$ if $n$ is a perfect square) Since $d_i$ are distinct positive integers $\leq \sqrt{n}$ there can be at most $\lfloor\sqrt{n}\rfloor$ so $k \leq \sqrt{n}$ $\Rightarrow$ $\tau(n) \leq 2k \leq 2\sqrt{n}$
5. $\tau(n) \text{ is odd } \Leftrightarrow n=k^2$ 
	1.  Using $\tau(n) = (\alpha_1+1)(\alpha_2+1) \cdots (\alpha_k+1)$ we can deduce that $\tau(n) \text{ is odd } \Leftrightarrow \alpha_n \text { is even } \forall n$ therefore $n$ is square. 
6. $\tau(n)$ is [[Arithmetic Functions#Multiplicative Functions|Multiplicative]].
	1. Let $a =p_1^{\alpha_1} \cdots p_k^{\alpha_k}$ and $b=P_1^{\beta_1} \cdots P_r^{\beta_r}$ with $\gcd(a,b) = 1$ meaning the share no prime factors.
	2. $\tau(a) = (1+\alpha_1)\cdots (1+\alpha_k)$ and $\tau(b) = (1+\beta_1) \cdots (1+\beta_r)$
	3. $ab = p_1^{\alpha_1} \cdots p_k^{\alpha_k} P_1^{\beta_1} \cdots P_r^{\beta_r}$ since they share no prime factors $P_i \neq p_j  \ \forall i, j$ so there is no crossover in primes and this is the proper prime factorisation. *(If a, b weren't coprime they would share factors and this would not be the proper prime factorisation: you could get $p_i^{\alpha_i +\beta_j}$ terms. This means that $\tau$ is not completely multiplicative)*
	4. $\tau(a)\tau(b)=\tau(ab)=(1+\alpha_1)\cdots (1+\alpha_k)(1+\beta_1) \cdots (1+\beta_r)$

---
# Sum of Divisors
## Definition
$\sigma(n)$ is defined as the sum of divisors of $n$. This can be written as 

$$
\forall n \in \mathbb{Z}^+ \quad\sigma(n) = \sum_{d|n} d
$$


## Properties
1. $\displaystyle\sigma(n) = \frac{p_1^{\alpha_1+1} - 1}{p_1 - 1} \cdots \frac{p_k^{\alpha_k+1} - 1}{p_k - 1} = \prod_{i=1}^k \frac{p_i^{\alpha_i+1} - 1}{p_i - 1}$
2. $\sigma(n)$ is [[Arithmetic Functions#Multiplicative Functions|Multiplicative]]
## Explanations
1. $\displaystyle\sigma(n) = \frac{p_1^{\alpha_1+1} - 1}{p_1 - 1} \cdots \frac{p_k^{\alpha_k+1} - 1}{p_k - 1} = \prod_{i=1}^k \frac{p_i^{\alpha_i+1} - 1}{p_i - 1}$
	1. Let $n = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$ then the divisors will have the form $d = p_1^{\beta_1} \cdot p_k^{\beta_k}$ $0 \leq \beta_i \leq \alpha_i$ $\forall i$. Every possible divisor appears exactly once so each combination of $k_i$ will appear exactly once which can be written as $(1 + p_1 + ... + p_1^{\alpha_1}) \cdot (1 + p_k + ... + p_k^{\alpha_k})$ which are geometric series, therefore 

$$
\sigma(n) = \frac{p_1^{\alpha_1+1} - 1}{p_1 - 1} \cdots \frac{p_k^{\alpha_k+1} - 1}{p_k - 1} = \prod_{i=1}^k \frac{p_i^{\alpha_i+1} - 1}{p_i - 1}
$$


2. $\sigma(n)$ is [[Arithmetic Functions#Multiplicative Functions|Multiplicative]]
    1. Let $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}\cdots p_k^{\alpha_k}$ 
	2. Every positive divisor $d = p_1^{\beta_1} \cdot p_2^{\beta_2} \cdots p_k^{\beta_k} \quad 0 \leq \beta_i \leq \alpha_i\ \forall i$.
	3. Therefore, the sum of all positive divisors of $n$ is given by  $\displaystyle\sigma(n) = \sum_{0 \leq \beta_1 \leq \alpha_1} \sum_{0 \leq \beta_2 \leq \alpha_2} \dots \sum_{0 \leq \beta_k \leq \alpha_k} p_1^{\beta_1} \cdot p_2^{\beta_2} \cdots p_k^{\beta_k}$.
    4. This multiple summation can be factored into a product of separate geometric series:  $\displaystyle\sigma(n) = \left( \sum_{0 \leq \beta_1 \leq \alpha_1} p_1^{\beta_1} \right) \left( \sum_{0 \leq \beta_2 \leq \alpha_2} p_2^{\beta_2} \right) \cdots  \left( \sum_{0 \leq \beta_k \leq \alpha_k} p_k^{\beta_k} \right)$
    5. Now suppose $a$ and $b$ are two positive integers with $\gcd(a, b) = 1$, and let  $\displaystyle a = \prod_{i=1}^r p_i^{\alpha_i}$ and $\displaystyle b = \prod_{j=1}^s q_j^{\gamma_j}$ where the $p_i$ and $q_j$ are distinct primes (since $a$ and $b$ are coprime).
    6. Then $\displaystyle ab = \prod_{i=1}^r p_i^{\alpha_i} \cdot \prod_{j=1}^s q_j^{\gamma_j}$, and using the previous identity for $\sigma(n)$, we get: $\displaystyle\sigma(ab) = \left( \prod_{i=1}^r \sum_{0 \leq \beta_i \leq \alpha_i} p_i^{\beta_i} \right) \left( \prod_{j=1}^s \sum_{0 \leq \delta_j \leq \gamma_j} q_j^{\delta_j} \right) = \tau(a)\tau(b)$
