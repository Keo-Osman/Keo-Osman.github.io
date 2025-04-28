#Maths/Number-Theory 
# Divisibility

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

---
# Division Algorithm

$\forall a, b \in \mathbb{Z} \ \exists q, r \quad \text{ s.t } \quad b = aq + r, \ (0 \leq r < a)$

---
# LCM
1. $\operatorname{lcm}(s,t) = m$, $m \cdot s' = t'$ $\Rightarrow gcd(s',t') = 1$
2. If $m'$ is common multiple of $s$ and $t$ and $m' \cdot s' = t'$, $gcd(s',t') = 1$
3.  $m'$ is a common multiple of $s$ and $t$ $\Rightarrow m | m'$
4. $m | s$, $n | s$ $\Rightarrow \operatorname{lcm}(m,n) | s$
5. $n \in \mathbb{Z}$ $\Rightarrow n \cdot \operatorname{lcm}(s,t) = \operatorname{lcm}(ns, nt)$
6. $s = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$, $t = p_1^{\beta_1} \cdot p_2^{\beta_2}$ $\Rightarrow \operatorname{lcm}(s,t) = p_1^{\textstyle\max(\alpha_1,\beta_1)} \cdots p_2^{\textstyle\max(\alpha_2,\beta_2)}$
7. $mn = \operatorname{gcd}(m,n) \cdot \operatorname{lcm}(m,n)$ $\forall m,n \in \mathbb{Z}$

---
# Number of Divisors
## Properties
1. Given $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$ the $\tau(n) =\displaystyle\sum_{d|n}1 = (\alpha_1+1)(\alpha_2+1) \cdots (\alpha_k+1)$
2.  $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$ $\Rightarrow$ there are $(2\alpha_1+1)(2\alpha_2+1) \cdots (2\alpha_1+1)$ distinct ordered pairs $(a,b) \in \mathbb{Z}^+$ such that $\operatorname{lcm}(a,b) = n$	
3. $\forall n \in \mathbb{Z}^+$, $\displaystyle\prod_{d|n} d = n^{\textstyle\frac{\tau(n)}{2}}$
4. $\forall n \in \mathbb{Z}^+$, $\tau(n) \leq 2\sqrt{n}$

### Explanations
1. Given $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$ the $\tau(n) =\displaystyle\sum_{d|n}1 = (\alpha_1+1)(\alpha_2+1) \cdots (\alpha_k+1)$ *This is because any divisor must be in the form $p_1^{\beta_1} \cdot p_2^{\beta_2}$ with $0 \leq \beta_k \leq \alpha_k$ $\forall k$. So for each $k$ there are $\alpha_k+1$ choices for $k_k$. Since they are independent you multiply.*
2. $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$ $\Rightarrow$ there are $(2\alpha_1+1)(2\alpha_2+1) \cdots (2\alpha_1+1)$ distinct ordered pairs $(a,b) \in \mathbb{Z}^+$ such that $\operatorname{lcm}(a,b) = n$ *This is because $a, b$ are divisors of $n$ so they must have the form $a = p_1^{\beta_1} \cdot p_2^{\beta_k}$ and $p_1^{\gamma_1} \cdot p_2^{\gamma_k}$ since $\operatorname{\operatorname{lcm}}(a,b) = n$ $\max(\beta_k,\gamma_k) = \alpha_1$ there are $2\alpha_1+1$ options for $(\beta_k,\gamma_k)$: 

$$
\underbrace{(0,\alpha_1), (1,\alpha_1),...,}_{\alpha \text{ terms}} (\alpha_1,\alpha_1)\underbrace{,...,(\alpha_1,0)}_{\alpha \text{ terms}}
$$

So you multiply number of choices together.*
3. If $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$ there are $\tau(n)$ divisors you can split into $\textstyle\frac{\tau(n)}{2}$ pairs $(d, \textstyle\frac{n}{d})$ so their product is $n$ multiplying all together you get $n^{\textstyle\frac{\tau(n)-1}{2}}$. Then multiply by $n^2$ yielding $n^{\textstyle\frac{\tau(n)}{ 2}}$
4. Let $d_1, d_2, ..., d_k$ be the divisors of $n \leq \sqrt{n}$. The rest of the divisors are $\frac{n}{d_1}, \frac{n}{d_2}, ..., \frac{n}{d_k}$. In each set there are $k$ numbers so $\tau(n) = 2k$ (or $2k-1$ if $n$ is a perfect square) Since $d_i$ are distinct positive integers $\leq \sqrt{n}$ there can be at most $\lfloor\sqrt{n}\rfloor$ so $k \leq \sqrt{n}$ $\Rightarrow$ $\tau(n) \leq 2k \leq 2\sqrt{n}$

---
# Sum of Divisors
## Definition
$\sigma(n)$ is defined as the sum of divisors of $n$. This can be written as 

$$
\forall n \in \mathbb{Z}^+ \quad\sigma(n) = \sum_{d|n} d
$$


## Properties
1. 

$$
\sigma(n) = \frac{p_1^{\alpha_1+1} - 1}{p_1 - 1} \cdot \frac{p_2^{\alpha_2+1} - 1}{p_2 - 1} = \prod_{1}^k \frac{p_k^{\alpha_k+1} - 1}{p_k - 1}
$$


### Explanations
1. Let $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}$ then the divisors will have the form $d = p_1^{k_1} \cdot p_2^{k_2}$ $0 \leq k_i \leq \alpha_i$ $\forall i$. Every possible divisor appears exactly once so each combination of $k_i$ will appear exactly once which can be written as $(1 + p_1 + ... + p_1^{\alpha_1}) \cdot (1 + p_2 + ... + p_2^{\alpha_2})$ which are geometric series, therefore 

$$
\sigma(n) = \frac{p_1^{\alpha_1+1} - 1}{p_1 - 1} \cdot \frac{p_2^{\alpha_2+1} - 1}{p_2 - 1} = \prod_{i} \frac{p_i^{\alpha_i+1} - 1}{p_i - 1}
$$



---
---
