#Maths/Number-Theory 
# Definition
*Modular arithmetic is a system of arithmetic restricted to the remainders.*
$a \equiv b \pmod{m} \Leftrightarrow m|(a-b)$,  $m \in \mathbb{Z}^+$, $a, b \in \mathbb{Z}$,
$a \equiv b \pmod{m} \Leftrightarrow \exists k \in \mathbb{Z}$ such that $a = b + km$, *([[Divisibility#Euclid's Division Lemma|Euclid's Division Lemma]])*
# Basic Properties
1. $a \equiv 0 \pmod{m} \Leftrightarrow m|a$
2. $a \equiv a \pmod{m}$
3. $a \equiv b \pmod{m} \Rightarrow b \equiv a \pmod{m}$
4. $(a \equiv b \pmod{m}) \wedge (b \equiv c \pmod{m}) \Rightarrow a \equiv c \pmod{m}$
5. Let $a, b, c, d, n, p, k \in \mathbb{Z}$ and $m, n > 0$, with $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m} \Rightarrow$
	1. $ka \equiv kb \pmod{m}$
	2. $a \pm c \equiv b \pm d \pmod{m}$
	3. $ac \equiv bd \pmod{m}$
	4. $a^n \equiv b^n \pmod{m}$

---
# Reduced Residue System
## Prime Reduced Residue System
Let $S_1 = \{0, a, 2a, \dots\} \pmod{p}$ where $p$ is prime. Then $S_1 = \{0, 1, \dots, (n-1)\}$.
*Proof*
1. Since $ai \equiv (p+i)a \pmod{p}$, $S_1= \{0, a, 2a, \dots, (p-1)a\}$. 
2. To prove that no 2 elements in $S_1$ are equal assume $\exists i, j \quad 0 \leq i \neq j, \leq (p-1) \text{ s.t } ai \equiv aj \pmod{p} \Rightarrow a(i-j) \equiv 0 \pmod{p} \Rightarrow i-j | p$ but $|i-j| < p \Rightarrow i-j \nmid n$. 
3. Therefore $S = \{0, 1, \dots, (n-1)\}$.
4. Meaning you could write $aS_1 \equiv S_1 \pmod{p}$.

Since $0\times a = 0$, you can remove $0$ as it maps to itself from $S_1$ to $aS_1$ so you can remove $0$ from both sets to obtain a more useful set $S$ ***The Reduced Residue System $\pmod{p}$***.
## Full Definition
The full definition of a reduced residue system $\text{ mod n}$ is the set of integers *less than $n$, coprime to $n$ and distinct $\text{ mod n}$*. So $aS \equiv S \pmod{n}$. However $|S| < n$ if $n$ is composite as $ka \pmod{n}$ is not guaranteed to be coprime to with $n$ as with $n$ being composite, some $k$ will divide $n$ so $\gcd(ka, n) \neq 1 \Rightarrow \gcd(ka\pmod{n}, n)\neq 1$.
$1$ and $n-1$ are always guaranteed to be in the set as $\gcd(1, n) = \gcd(n-1, n) = 1$.

*The construction is the exact same as with prime modulo.*
$|S|\equiv \varphi(n)$ *([[Divisibility#Euler's Totient Function|Euler's Totient Function]])*

---
# Fermat's Little Theorem
Let $p$ be prime and $\gcd(a, p) = 1$, then 
$$
a^{p-1} \equiv 1\pmod {p}
$$

**Proof 1**
Using the *Reduced Residue System* $\text{(mod p): }S$. 
$a \cdot 2a \cdots (p-1)a \equiv 1 \cdot 2 \cdot (p-1) \pmod{p}$ This gives $a^{p-1} \cdot (p-1)! \equiv (p-1)!$ Since $\gcd((p-1)! \ , p) = 1$, you get $a^{p-1} \equiv 1\pmod {p}$. 

**Proof 2** *by Induction*
1. *Base case:* $1^p\equiv 1 \pmod{p}$
2. *Induction forwards*. Assume $a^p \equiv a \pmod{p}$, then $(a+1)^p \equiv a^p+1^p\equiv (a+1)\pmod{p}$ by assumption.
3. *Induction backwards*. Assume $a^p\equiv a\pmod{p}$, then $(a-1)^p\equiv a^p+(-1)^p$. For $p>2 ,\ p$ is odd. so we get $a^p-1$ which by our assumption $\equiv (a-1)\pmod{p}$. For $p=2$, we get $(a-1)^2=a^2-2a+1$ which by our our assumption $\equiv a-2a+1\equiv-a+1 +(2a-1)\equiv (a-1) \pmod{2}$.
4. Therefore we get the fact that $a^p\equiv a \pmod{p}$. If $a$ has an inverse you get $a^{p-1}\equiv 1 \pmod{p}$.

## Euler's Theorem
*([[Divisibility#Euler's Totient Function|Euler's Totient Function]])*
Euler's Theorem is a more general case of Fermat's Little Theorem. It states that 
$$
a^{\varphi(n)}\equiv 1 \pmod{n} \quad \gcd(a,n)=1
$$
In the case of $n$ being prime $\varphi(n)= n-1$ and it simplifies to Fermat's Little Theorem.
*Proof*
1. By considering the elements of $S$ *(The reduced residue system $\text{mod n}$)*, multiplying them together. $(a\cdot 1)\cdots(a\cdot(n-1)) \equiv 1 \cdots (n-1) \pmod{n}$. 
2. Hence $\displaystyle a^{\varphi(n)}\cdot \prod_{\substack{1\leq i <n \\ \gcd(i, n)=1}} i \equiv \prod_{\substack{1\leq i <n \\ \gcd(i, n)=1}} i$
3. Since the products only contain $i$ coprime to $n$ the whole product will share no prime factors to $n$ and so the whole product is coprime to $n$ and therefore can be cancelled.
4. Therefore $a^{\varphi(n)}\equiv 1 \pmod{n}$.

---
# Inverses
## Definition
Using the [[Modular Arithmetic#Reduced Residue System|Reduced Residue System]] $\text{mod n }$we can see that with $\gcd(a,n)=1$, $\forall b \in \mathbb{Z}^+ ,\ 0 < b < p, \ \exists! x \text{ s.t } ax \equiv b \pmod{n}$.
In particular if $b=1$ we get $ax \equiv 1 \pmod{n}$. This means that $a$ and $x$ are multiplicative inverses $\text{mod n}$. *(This comes from the fact that across the real numbers $a \cdot a^{-1} \equiv 1$*
You can find $x$ by using **[[Divisibility#Bézout's Identity|Bezout's Identity]]** $\gcd(a, n) = 1\Leftrightarrow \exists p, q \text{ s.t } ax + ny=1 \Rightarrow ax=1-ny \Rightarrow ax=1 \pmod{n}$
The existence allows division. 
## Existence
However inverses are ***NOT*** guaranteed to exist but they are $\text{mod p}$ if $a \not\equiv 0 \pmod{p}$. More generally $a^{-1} \pmod{n}$exists *if and only if* $\gcd(a, n)=1$.
**Proof**
1. Let $\gcd(a,n)=d$, then $ax\equiv 1\pmod{n}\implies n|ax-1\implies d|1\implies d=1$

## Uniqueness
Inverses are unique meaning only one solution exists to $ax \equiv 1 \pmod{p}$ *(meaning an element only has one inverse)*. It follows that no two elements have the same inverse due to the fact that $a^{-1}=b\implies b^{-1}=a$.
**Proof**
1. Assume that there are two inverses such that $ax\equiv ay\equiv 1 \pmod{n}$ $x,y<n$.
2. So we get that $a(x-y)\equiv 0 \pmod{n}\implies n|a(x-y)$. Since $\gcd(a,n)=1$ this must mean that $n|(x-y)$ but since $x,y<n\implies (x-y)<n$, $(x-y)=0\implies x=y$

## Fractional Behaviour
You can write inverses as a fraction like $a \cdot b^{-1} \equiv \frac{a}{b}$. They can be added and multiplied normally.
**Proof of Fractional Addition**
$\displaystyle bd(a\cdot b^{-1}+c\cdot d^{-1})=bd(a\cdot b^{-1})+bd(c\cdot d^{-1})\equiv ad+ bc \pmod{p} \Rightarrow \frac{a}{b}+\frac{c}{d}\equiv \frac{ad+bc}{bd} \pmod {p}$
**Proof of Fractional Multiplication**
$\displaystyle bd(a \cdot b^{-1})\cdot(c \cdot d^{-1}) =b(a \cdot b^{-1})\cdot d(c \cdot d^{-1})\equiv a \cdot c \pmod{p} \Rightarrow \frac{a}{b} \cdot \frac{c}{d} \equiv \frac{ac}{bd} \pmod{p}$
## Pairs of Inverses
Since $a^{-1} \equiv b \pmod{p} \Rightarrow a \equiv b^{-1} \pmod{p}$, inverses can be written in pairs $(a,b)$.
An element can be self inverse meaning $a^2\equiv 1 \pmod{p}$. This means $p|a^2-1=(a+1)(a-1) \Rightarrow p|(a+1) \text{ or } p|(a-1) \Rightarrow a \equiv 1 \text{ or } a \equiv -1$ *(This is the only case where $a$ is self inverse).*

---
# Wilson's Theorem
Start with $2 \cdot 3 \cdots (p-2)\pmod{p}$ using the fact that $\text{mod p}$ every element in $\{2, 3, \dots, (p-2)\}$ has a unique inverse, you can pair these elements up to get $1 \cdot 1 \cdots 1 \equiv 1 \pmod{p}$. Multiplying both sides by $(p-1)$ you obtain *Wilson's Theorem* 
$$
\text{p is prime } \Leftrightarrow(p-1)!\equiv -1 \pmod{p}
$$

*Proof of the reverse direction*
Assume $n$ is composite then $\exists p, q, \ 1 <p, q < n \text{ s.t } pq=n$ since $1 <p, q < n$ both $p, q$ must be contained in $(n-1)!$ so $(n-1)!=k(pq) = kn \Rightarrow n|(n-1)! \Rightarrow (n-1)! \equiv 0 \pmod{n}$. Therefore if $(n-1)! \not\equiv 0 \pmod{n}$, $n$ can't be composite and is therefore prime.

---
# Congruence Equations
Equations with modular arithmetic are given in terms called congruence equations and their answers are usually given in terms of least residues.
The set of least residues $k \pmod{m}$ is $\{0, 1, \ldots, m-1\}$

Since a solution $x \equiv n \pmod{m}$ represents an infinite number of solutions, you can write a general solution as: $\{n + km : k \in \mathbb{Z}\}$

## Congruence Equation Properties
Let $a, b, m \in \mathbb{Z}, m > 0$,  $\gcd(a,m) = d$
- $d \nmid b \Rightarrow$ the equation $ax \equiv b \pmod{m}$ has no solutions
- $d \mid b \Rightarrow$ the equation has $d$ solutions in the set of least residues
- $(ka \equiv kb \pmod{m}) \wedge (\gcd(k,m) = d) \Rightarrow a \equiv b \pmod{\frac{m}{d}}$

---
# Advance Properties and Results
## Results
1. $\displaystyle a^x \equiv a^y \equiv 1 \pmod{n} \Rightarrow a^{\gcd(x, y)} \equiv 1 \pmod{n}$
2. $\displaystyle ad \equiv bd \pmod{n} \Rightarrow a \equiv b \quad \left(\text{ mod} {\frac{n}{\gcd(n, d)}}\right)$
3. $(a+b)^{p^i} \equiv a^{p^i}+b^{p^i} \pmod{p} \quad i \in \mathbb{Z}^{+}$
4. $x^p-x \equiv x(x-1)(x-2)\cdots (x-(p-1)) \pmod{p} \quad \forall x$
5. For $p>3$, $\displaystyle  1+\frac{1}{2}+\frac{1}{3}+\cdots + \frac{1}{p-1} \equiv 0 \pmod{p^2}$  *(Wolstenholme's Theorem)*. This is also equivalent to saying $\displaystyle  1+\frac{1}{2}+\frac{1}{3}+\cdots + \frac{1}{p-1} \equiv \frac{m}{n} \land (\gcd(m, n) = 1) \Rightarrow p^2|m$.
6. $\displaystyle \binom{p-1}{k} \equiv (-1)^k \pmod{p}$
## Explanations
1. $\displaystyle a^x \equiv a^y \equiv 1 \pmod{n} \Rightarrow a^{\gcd(x, y)} \equiv 1 \pmod{n}$
	1. By Bezouts Theorem $mx+ny = \gcd(m, n)$.
	2. $a^{\gcd(m, n)} = a^{mx+ny}=a^{mx} \cdot a^{ny} = {(a^{m})}^{x} \cdot {(a^{n})}^{y} \equiv 1 \pmod{d}$
2. $\displaystyle ad \equiv bd \pmod{n} \Rightarrow a \equiv b \quad \left(\text{ mod} {\frac{n}{\gcd(n, d)}}\right)$
	1. We have $n|d(a-b)$.
	2. $n=gn'$, $g=gd'$ with $g=\gcd(n,d)$
	3. So $n'|d'(a-b)$. So $n'|(a-b)$
	4. Therefore $\displaystyle a\equiv b \left(\text{ mod } n'= {\frac{n}{\gcd(n, d)}}\right)$
3. $(a+b)^{p^i} \equiv a^{p^i}+b^{p^i} \pmod{p} \quad i \in \mathbb{N}_0$
	1. Prove that $(a+b)^p \equiv a^p+b^p \pmod{p}$
		1. Expanding *LHS* obtains $(a+b)^p = a^p + \binom{p}{1} ba^{p-1} + \cdots + \binom{p}{p-1}b^{p-1}a + a^p$. 
		2. Since $p|\binom{p}{k} \quad (0<k<p)$, all terms except $a^p$ and $b^p$ are divisible by $p$
	2. Inductive proof.
		1. Base case: it is clear that $i=0$ satisfies the equation.
		2. Assume $(a+b)^{p^i} \equiv a^{p^i}+b^{p^i}$.
		3. $(a+b)^{p^{i+1}}=((a+b)^{(p^i)})^p$, by our assumption $\equiv (a^{p^i}+b^{p^i})^p \equiv (c+d)^p \equiv c^p+d^p \equiv (a^{(p^i)})^p + (b^{(p^i)})^p \equiv a^{p^{i+1}}+b^{p^{i+1}}$ 
4. $x^p-x \equiv x(x-1)(x-2)\cdots (x-(p-1)) \pmod{p} \quad \forall x\in\mathbb{Z}$
	1. By Fermat's Little Theorem *LHS*$=0$.
	2. One of $x, x-1 \dots,x-(p-1)$ is $0 \pmod{p}$.
5. For $p>3$, $\displaystyle  1+\frac{1}{2}+\frac{1}{3}+\cdots + \frac{1}{p-1} \equiv 0 \pmod{p^2}$  *(Wolstenholme's Theorem)*. This is also equivalent to saying $\displaystyle  1+\frac{1}{2}+\frac{1}{3}+\cdots + \frac{1}{p-1} \equiv \frac{m}{n} \land (\gcd(m, n) = 1) \Rightarrow p^2|m$.
	1. $\displaystyle \sum_{i=1}^{p-1} \frac{1}{i} =\sum_{i=1}^{\frac{p-1}{2}} \left(\frac{1}{i}+\frac{1}{p-i}\right) = p\sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)}$ 
	2. Since we have a factor of $p$ it is now sufficient to show that $\displaystyle \sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)} \equiv p \equiv 0 \pmod{p}$ for the original sum to be $\equiv 0 \pmod{p}$.
	3. Since $(p-i) \equiv -i \pmod{p}$ we can replace the denominators with $-i^2$ and we can multiply the sum by $2$ to restore the amount of terms back to $p-1$, the reason being that after $\frac{p-1}{2}$ the terms descend back symmetrically so term $i$ is equivalent to term $p-i$ as $\frac{1}{i(p-i)}= \frac{1}{(p-i)(p-(p-i))} = \frac{1}{(p-i)i}$ 
	4. So we get $\displaystyle 2\sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)} \equiv - \sum_{i=1}^{p-1} \frac{1}{i^2} \pmod{p}$.
	5. Since inverses are unique we get that $\{1^{-1}, 2^{-1}, \dots, (p-1)^{-1}\} \equiv \{1, 2, \dots, p-1\} \pmod{p}$ so each term corresponds to a unique residue. Therefore $\displaystyle \sum_{i=1}^{p-1} \frac{1}{i^2}  \equiv \sum_{i=1}^{p-1} i^2 = \frac{(p-1)p(2p-1)}{6} \pmod{p}$ . Since $p>3 \Rightarrow \gcd(p, 6) =0 , \ \frac{(p-1)p(2p-1)}{6} \equiv kp \equiv 0 \pmod{p}$ 
	6. Going back to step 4 we now get $\displaystyle 2\sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)} \equiv 0 \pmod{p} \Rightarrow p|\left(2\sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)}\right)$ but $\displaystyle \gcd(2, p)=1 \Rightarrow p|\left(\sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)}\right) \Rightarrow \sum_{i=1}^{\frac{p-1}{2}} \frac{1}{i(p-i)} \equiv 0 \pmod{p}$ which by step 2 is sufficient to prove the statement. 
6. $\displaystyle \binom{p-1}{k} \equiv (-1)^k \pmod{p}$
	1. $\displaystyle \binom{p-1}{k}=\frac{(p-1)!}{k!(p-1-k)!}=\frac{(p-k)!(p-k-1)!}{k!(p-k-1)!}=\frac{(p-k)!}{k!}$ 
	2. $\displaystyle \frac{(p-k)!}{k!}\equiv \frac{-1\times-2\times \cdots \times-k}{k!} \equiv \frac{(-1)^kk!}{k!}\equiv (-1)^k \pmod{p}$

---
# Euler's Totient Function
Euler's totient function is defined as 
$$
\varphi(n) = \text{the number of positive integers} \leq n, \text{ that are copprime to } n
$$

## Properties
1. $\varphi(n)$ is [[Arithmetic Functions#Multiplicative Functions|Multiplicative Function]]
2. $\varphi(p^k) = p^k-p^{k-1}$
3. Let $n = p_1^{\alpha_1}p_2^{\alpha_2}\cdots p_k^{\alpha_k}$ $\displaystyle\varphi(n) = n\left(1-\frac{1}{p_1}\right)\cdots\left(1-\frac{1}{p_k}\right)=p_1^{\alpha_1-1}p_2^{\alpha_2-1}\cdots p_k^{\alpha_k-1}\cdot (p_1-1)\cdots(p_k-1)$
4. $\displaystyle \sum_{d|n} \varphi(d) = n$
5. $\displaystyle\left(\frac{6}{\pi^2}\right)n^2 < \sigma(n)\varphi(n) < n^2$
### Explanations
1. $\varphi(n)$ is [[Arithmetic Functions#Multiplicative Functions|Multiplicative Function]]
	1. Consider $\varphi(mn)$. Then consider the set numbers $0<k< mn$.
	2. By [[Divisibility#Euclid's Division Lemma|Euclid's Division Lemma]] every such number can be written in the form $k = mr+c$ with $0 \leq r \leq n-1  ,\ 1 \leq a \leq m$. You can think of putting this in a grid with each $k$ being in row index $r$ and column index $c$.
	3. $\gcd(m, n) =1 \Rightarrow (\gcd(k, mn) =1 \Leftrightarrow \gcd(k, m)=1 \land \gcd(k, n)=1)$
	4. Let $k_{{row}_i}$ be the subset of $k$ that has coefficient $i$ for $m$ e.g. $k=mi+c$.
	5. Each $k_{{row}_i}$ forms a complete residue class $\text{mod m}$ as $k_{{row}_i} \equiv \{1, 2,\dots, m\} = \{0, 1, 2,\dots, m-1\}$ so for each $k_{{row}_i}$ there are $\varphi(m)$ elements coprime to $m$.
	6. Then let $k_{{col}_i}$ be the subset of $k$ with remainder $i$ e.g. $k = mr +i$
	7. Each $k_{{col}_i}$ forms a complete residue class $\text{mod n}$ as $k_{{col}_i} \equiv \{1, 2,\dots, n\} = \{0, 1, 2,\dots, n-1\}$ so for each $k_{{col}_i}$ there are $\varphi(n)$ elements coprime to $n$.
	8. So the total amount that is coprime to $mn$ is $\varphi(m)\varphi(n)$ - *You can think this as starting in the top row there are $\varphi(m)$ elements that are coprime to $m$ and each of them form a column in which there are $\varphi(n)$ that are also coprime to $n$. Only the columns where the first element is coprime to $m$ work as any element that has a common factor $d$ with $m$ will form a column in which all those elements share that common factor with $m$.* (This is due to the [[Divisibility|fact]] that $\gcd(a\pm km, m) = \gcd(a, m)$)
2. $\varphi(p^k) = p^k-p^{k-1}$
	1. Every number $\leq p^k$ other than a multiple of $p$ is coprime to $p^k$. There are $p^{k-1}$ multiples of $p\leq p^k$ and there are $p^k$ numbers $\leq p^k$ so combing them we get $\varphi(p^k) =p^k-p^{k-1}$
3. Let $n = p_1^{\alpha_1}p_2^{\alpha_2}\cdots p_k^{\alpha_k}$ $\displaystyle\varphi(n) = n\left(1-\frac{1}{p_1}\right)\cdots\left(1-\frac{1}{p_k}\right)=p_1^{\alpha_1-1}p_2^{\alpha_2-1}\cdots p_k^{\alpha_k-1}\cdot (p_1-1)\cdots(p_k-1)$
	1. Using *property 2*, $\displaystyle\varphi(p^k) = p^k-p^{k-1}=p^{k}\left(1-\frac{1}{p_k}\right)$
	2. Since $\varphi$ is multiplicative and primes are pairwise coprime. 
$$
\begin{aligned}\displaystyle \varphi(n) &= \varphi(p_1^{\alpha_1}p_2^{\alpha_2}\cdots p_k^{\alpha_k}) \\ &=  \varphi(p_1^{\alpha_1})\cdot\varphi(p_2^{\alpha_2})\cdots\varphi(p_k^{\alpha_k})\\&=p_1^{\alpha_1}\left(1-\frac{1}{p_1}\right)\cdot p_2^{\alpha_2}\left(1-\frac{1}{p_2}\right)\cdots p_k^{\alpha_k}\left(1-\frac{1}{p_k}\right)\\&=p_1^{\alpha_1}p_2^{\alpha_2}\cdots p_k^{\alpha_k}\left(1-\frac{1}{p_1}\right)\cdots\left(1-\frac{1}{p_k}\right)\end{aligned}
$$

4. $\displaystyle \sum_{d|n} \varphi(d) = n$. (This is *[[Arithmetic Functions#Multiplicative Functions|completely multiplicative]]* as $f(n)=n$ is - $f(mn) = mn = f(m)f(n) = (m)(n)$). 
	1. Let $n = p_1^{\alpha_1} \cdot p_2^{\alpha_2}\cdots p_k^{\alpha_k}$ 
	2. Every positive divisor $d = p_1^{\beta_1} \cdot p_2^{\beta_2} \cdots p_k^{\beta_k} \quad 0 \leq \beta_i \leq \alpha_i\ \forall i$.
	3. $\displaystyle \sum_{d|n} \varphi(d) = \sum_{0 \leq \beta_1 \leq \alpha_1} \sum_{0 \leq \beta_2 \leq \alpha_2} \dots \sum_{0 \leq \beta_k \leq \alpha_k} \varphi(p_1^{\beta_1} \cdot p_2^{\beta_2} \cdots p_k^{\beta_k})$
	4. Using the fact that $\varphi(n)$ is multiplicate we get $\displaystyle \sum_{d|n} \varphi(d) = \sum_{0 \leq \beta_1 \leq \alpha_1} \sum_{0 \leq \beta_2 \leq \alpha_2} \dots \sum_{0 \leq \beta_k \leq \alpha_k} \varphi(p_1^{\beta_1}) \varphi(p_2^{\beta_2}) \cdots \varphi(p_k^{\beta_k})$
	5. You can repeatedly factor out $\displaystyle\sum_{0\leq\beta_k\leq\alpha_k}\varphi(p_k^{\beta_k})$ from the summation with $0\leq\beta_{k-1}\leq\alpha_{k-1}$ as it is constant as you are changing all $\beta_k$ up to ***but not including*** $\beta_k$ so the summation is constant and can be factored out.
	6. This obtains $\displaystyle \left(\sum_{0\leq\beta_1\leq\alpha_1} \varphi(p_1^{\beta_1}) \right)\cdots \left(\sum_{0\leq\beta_k\leq\alpha_k} \varphi(p_k^{\beta_k}) \right)$ 
	7. For each term we get $\varphi(1)+\varphi(p)+\varphi(p^2)+\cdots+\varphi(p^\alpha)$ which using property 2 gets a telescoping sum of $1+(p-1)+(p^2-p)+\cdots+(p^{\alpha}-p^{\alpha-1})=p^{\alpha}$
	8. Replacing every sum we get $p_1^{\alpha_1} \cdot p_2^{\alpha_2}\cdots p_k^{\alpha_k} = n$
5.  $\displaystyle\left(\frac{6}{\pi^2}\right)n^2 < \sigma(n)\varphi(n) < n^2$
	1. INSERT PROOF
---
# Modular Contradictions
1. $a^2 \equiv\{0, 1\}\pmod{3}$
2. $a^2 \equiv\{0, 1\}\pmod{4}$
3. $a^2 \equiv\{0, \pm1\}\pmod{5}$
4. $(\text{odd})^2 \equiv\ 1\pmod{8}$
5. $a^3 \equiv\{0, \pm1\}\pmod{7}$
6. $a^3 \equiv\{0, \pm1\}\pmod{9}$
7. $\displaystyle a^{\textstyle \frac{p-1}{2}}\equiv \pm 1 \pmod{p}$, $\gcd(a,p)=1$ *by Fermat's Little Theorem*
8. $\displaystyle a^{\textstyle\frac{\varphi(n)-1}{2}}\equiv \pm 1 \pmod{n}$, $\gcd(a,n)=1$ *by Euler's Theorem*