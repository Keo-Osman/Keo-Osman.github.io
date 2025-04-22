#Maths/Number-Theory 
# Properties
1. $p$ is prime $\Rightarrow \gcd(p,m) = p$ or $\gcd(p,m) = 1$ 
2. If $d = \gcd(m,n)$, $m = d \cdot m'$, $n = d \cdot n' \Rightarrow \gcd(m',n') = 1$ 
3. $d = \gcd(m,n)$, $m = d \cdot m''$, $n = d \cdot n''$, $\gcd(m'',n'') = 1 \Rightarrow d' = d$
4. If $d$ is a common divisor of $m, n \Rightarrow d|\gcd(m,n)$
5. $p^k||m \text{ and } p^j||n \Rightarrow p^{\min(k,j)}||\gcd(m,n)$ 
6. $m = p_1^{\alpha_1} \cdots p_r^{\alpha_r}$, $n = p_1^{\beta_1} \cdots p_r^{\beta_r}$, $\alpha_i, \beta_i \geq 0 \Rightarrow \gcd(m,n) = p_1^{\min(\alpha_1,\beta_1)} \cdots p_r^{\min(\alpha_r,\beta_r)}$ 
7. $m = aq + r \Rightarrow \gcd(m,n) = \gcd(n,r)$

## Bézout's Identity

$\forall m,n \in \mathbb{Z}$ $\exists x,y \in \mathbb{Z}$ s.t $\gcd(m,n) = mx+ny$

1. $a|bc \text{ and } \gcd(a,b) = 1 \Rightarrow a|c$ 
2. $\gcd(a,b) = 1 \text{ and } a|c \text{ and } b|c \Rightarrow ab|c$ 
3. Let $p$ be prime and $r \in \mathbb{Z}$, $1 \leq k < p \Rightarrow p|\binom{p}{k}$