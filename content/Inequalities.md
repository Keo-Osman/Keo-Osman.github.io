#Maths/Algebra  
# Growth Rate of Functions
## [[Polynomials]]
$\text{degree(P)}>\text{degree(Q), leading coefficient > 0}\implies \exists a \text{ s.t } P(x)>Q(x) \quad \forall x>a$
$\text{degree(P)}>\text{degree(Q), leading coefficient < 0}\implies \exists a \text{ s.t } P(x)<Q(x) \quad \forall x>a$
## [[Exponential Functions]]
$a,b \in \mathbb{R}^+, \ b>1 \implies \exists c \text{ s.t } b^x>x^a \quad \forall x>c$
$a,b \in \mathbb{R}^+, \ b>1 \implies \exists c \text{ s.t } x^a>\log_{b}(x) \quad \forall x>c$
***
# Weighted F-Mean (Mean in an Arbitrary Function)
Given any function $f:I\to \mathbb{R}$ which is both [[Continuity|Continuous]] and [[Functions#Injective|Injective]] *(So that $f^{-1}$ is well defined)*, The *f-mean* of $x_{1},x_{2},\dots ,x_{n} \in I$ with weights $w_{1},w_{2},\dots ,w_{n} \in \mathbb{R}^{+}$ is defined as 

$$
M_{f}(x_{1},x_{2},\dots ,x_{n})=f^{-1}\left( \frac{\sum w_{i}f(x_{i})}{\sum w_{i}} \right)
$$


Since $f$ is both [[Continuity|Continuous]] and [[Functions#Injective|Injective]] it follows that $f$ is strictly *monotonic* so it follows that $x_{min} \leq \text{f-mean} \leq x_{max}$.
***
# Weighted Jensen's Inequality
Let $I$ be an interval on the reals $f:I\to \mathbb{R}$ be [[Concavity|Convex]] on $I$, with $x_{1},x_{2},\dots ,x_{n}\in I$ and real weights $w_{1},w_{2},\dots ,w_{n}> 0$ *(In many scenarios the weights will be normalised such that $\sum w_{i}=1$)*, Then 

$$
\frac{w_{1}f(x_{1})+w_{2}f(x_{2})\dots +w_{n}f(x_{n})}{\sum w_{i}}\geq f\left( \frac{w_{1}x_{1}+w_{2}x_{2}+\dots+w_{n}x_{n}}{\sum w_{i}} \right)
$$

If $f$ is concave then the inequality is flipped.
The equality holds if $x_{1}=x_{2}=\dots =x_{n}$ or $f$ is affine on the on a domain containing $x_{i}$.
**Proof**
1. W.L.O.G let $\displaystyle \sum^n w_{i}=1$.
2. Trivially for $n=1\implies w_{1}=1$ so $f(x_{1})=f(x_{1})$ and the (in)equality holds.
3. The definition of convexity means $\forall x_{1},x_{2} \quad f(w_{1}x_{1}+w_{2}x_{2}) \leq w_{1}f(x_{1})+w_{2}f(x_{2})$. *This is the $n=2$ case.*
4. Assume that Jensen's holds for $n=k$, then for $n=k+1$ with weights $w_{i}$ *(arbitrary, not necessarily the same as the $n=k$ case)* such that $\displaystyle \sum^{k+1}w_{i}=1$. If $w_{k+1}=1$ then all other terms are zero so the inequality trivially holds. If $w_{k+1}=0$ it is equivalent to the induction hypothesis so assume $w_{n} \in (0,1)$
5. Let $\displaystyle \mu_{i}=\frac{w_{i}}{1-w_{k+1}}, i=1,2,\dots,k ,\ \sum_{i=1}^{k}\mu_{i}=\frac{1}{1-w_{k+1}}\sum_{i=1}^k w_{i}=\frac{1}{1-w_{k+1}}(1-w_{k+1})=1$ 
6. So we can rewrite $\displaystyle w_{1}x_{1}+\dots+w_{k+1}x_{k+1}=(1-w_{k+1})\sum_{i=1}^{k} \mu_{i}x_{i}+w_{k+1}x_{k+1}$
7. $\displaystyle f\left( \sum_{i=1}^{k+1} w_{i}x_{i} \right)=f\left((1-w_{k+1})\sum_{i=1}^{k} \mu_{i}x_{i}+w_{k+1}x_{k+1}\right)$
8. By convexity *(same as $n=2$ case)*, $\displaystyle \leq (1-w_{k+1})f\left(\sum_{i=1}^{k} \mu_{i}x_{i}\right)+w_{k+1}f(x_{k+1})$
9. By our inductive hypothesis $\displaystyle (1-w_{k+1})f\left(\sum_{i=1}^{k} \mu_{i}x_{i}\right) \leq (1-w_{k+1})\left(\sum_{i=1}^k \mu_{i}f(x_{i})\right)=\left(\sum_{i=1}^k (1-w_{k+1})\mu_{i}f(x_{i})\right)$
10. So we get that $\displaystyle (1-w_{k+1})f\left(\sum_{i=1}^{k} \mu_{i}x_{i}\right)+w_{k+1}f(x_{k+1}) \leq \left(\sum_{i=1}^k (1-w_{k+1})\mu_{i}f(x_{i})\right) +w_{k+1}f(x_{n})= \sum_{i=1}^{k+1}w_{i}f(x_{k+1}) \quad \square$
11. The exact same argument follows for concave functions but the inequality of the $n=2$ case flips $\quad \square$.

*Intuition*: The way this proof works is that we view the last point separately and the rest as *one* convex combination. We then renormalise with $\mu$ to insure the weights sum to $1$ (ensuring that the *one* point a convex combination) so we can apply the two-point Jensen that states that $f(\alpha U+(1-\alpha)V)\leq \alpha f(U)+(1-\alpha) \forall \alpha \in[0,1]$ and we've just used $\displaystyle U=\sum_{i=1}^k \mu_{i}x_{i}, V=x_{k+1}, \ \alpha=1-w_{k+1}$. And then invoke our induction hypothesis on $f(U)$. *($U$ acts as a shortcut for all input as it forms a new point which lies in the interval as $x_{min}\leq U \leq x_{max}$)*
[Online Proof](https://brilliant.org/wiki/jensens-inequality/)
## Weighted Power Mean
The *weighted power mean* is the case of $f(x)=x^p$ and $I=\mathbb{R}^+$ of the *f-mean*.
**Proof**
1. $f(x)=x^p, \ f^{-1}(x)=x^{1/p}$
2. $\displaystyle M_{f}=f^{-1}\left(\frac{\sum w_{i}f(x_{i})}{\sum w_{i}} \right) =\left(\frac{\sum w_{i}x_{i}^{p}}{\sum w_{i}}\right)^{1/p} \quad \square$

Given $a_{1},a_{2},\dots ,a_{n} \in \mathbb{R}^+$ with weights $w_{1},w_{2},\dots ,w_{n} \in \mathbb{R}^{+}$ where$\text{ W.L.O.G, } \sum w_{i}=1$ and $p \in\mathbb{R}$, The weighted power mean is 

$$
\displaystyle M_{p}(a_{1},a_{2},\dots,a_{n})=\begin{cases}
\displaystyle  \left( \sum w_{i}a_{i}^p \right)^{1/p} &p\neq 0 \\
\displaystyle  \prod a_{i}^{w_{i}} &p=0
\end{cases}
$$


The weights $w_{i}$ serve to emphasises a certain element so if $a_{i}$ is more important then $w_{i}$ will be greater. In the case where $\displaystyle w_{1}=w_{2}=\dots =w_{n}=\frac{1}{n}$, we get an unweighted/regular version. 
Some special case for $p$ are: $p=-1\text{ :HM}, \ p=0\text{ :GM}, \ p=1\text{ :AM}, \ p=2\text{ :QM}$.
$a_{i}=0$ is valid for $p>0$.
### Weighted Power Mean Inequality


$$
r>s\implies M_{r}(a_{1},a_{2},\dots,a_{n})\geq M_{s}(a_{1},a_{2},\dots,a_{n})
$$


The equality holds if and only if $a_{1}=a_{2}=\dots=a_{n}$.
For the cases of $p \in\{-1,0,1,2\}$ we get the inequality $\text{QM}\geq\text{AM}\geq\text{GM}\geq\text{HM}$. Again the equality only holding when all elements are equal.
### Weighted Geometric Mean 
The *weighted geometric mean* is the case of the *f-mean* where $I=\mathbb{R}^{+}$ and $f(x)=\ln(x)$
**Proof** 
1. $\displaystyle M_{f}=f^{-1}\left( \frac{\sum w_{i}f(x_{i})}{\sum w_{i}} \right)=e^{ \displaystyle\frac{\sum w_{i}\ln(x_{i})}{\sum w_{i}} }$
2. Using logarithm laws we get that $\displaystyle\frac{\sum w_{i}\ln(x_{i})}{\sum w_{i}}=\ln\left(\left( \prod x_{i}^{w_{i}}\right)^{\displaystyle\frac{1}{\sum w_{i}}}\right)$
3. So $\exp\left( \ln\left(\left( \prod x_{i}^{w_{i}}\right)^{\displaystyle\frac{1}{\sum w_{i}}}\right) \right)=\left(\displaystyle \prod x_{i}^{w_{i}}\right)^{\displaystyle\frac{1}{\sum w_{i}}}$
4. W.L.O.G we can assume that $\sum w_{i}=1$ to get a cleaner version and obtain $M_{f}=\displaystyle \prod x_{i}^{w_{i}} \quad \square$

It is also the $\displaystyle \lim_{ p \to 0 }$ of the *power mean* $\displaystyle \lim_{ p \to 0 } M_{p}(a_{1},a_{2},\dots,a_{n})=\prod a_{i}^{w_{i}}$
**Proof**
1. $\text{ W.L.O.G } \sum w_{i}=1$
2. $\displaystyle M_{p}=\left( \sum w_{i}x_{i}^{p} \right)^{1/p}$
3. $\displaystyle \ln M_{p}=\frac{\ln \left(\sum w_{i}x_{i}^{p}\right)}{p}$
4. $\displaystyle \ \lim_{ p \to 0 } \ln M_{p}=\frac{0}{0}$ indeterminate form we can use [[L'Hopitals Rule]]
5. $\displaystyle \lim_{ p \to 0 } \ \ln M_{p}=\frac{\frac{d}{dp} \ln \left(\sum w_{i}x_{i}^{p}\right)}{\frac{d}{dp}p}=\frac{d}{dp}\ln \left(\sum w_{i}x_{i}^{p}\right)=\frac{\sum w_{i}x_{i}^{p}\ln x_{i}}{\sum w_{i}x_{i}^{p}} \bigg|_{p=0}=\frac{\sum w_{i}\ln x_{i}}{\sum w_{i}}$
6. Therefore $\displaystyle \lim_{ p \to 0 } \ M_{p}=\exp\left( \displaystyle\frac{\sum w_{i}\ln x_{i}}{\sum w_{i}}\right)=\prod x_{i}^{w_{i}} \quad \square$

***
# Muirhead's Inequality
Suppose we have two sequences $x_{1}\geq x_2 \geq \dots \geq x_{n}$ and $y_{1}\geq y_2 \geq \dots \geq y_{n}$ such that $x_{1}+x_{2}\dots +x_{n}=y_{1}+y_{2}\dots +y_{n}$ and $x_{1}+x_{2}\dots +x_{n-1}\geq y_{1}+y_{2}\dots +y_{n-1}$, we say that $(x_{n})\text{ majorises }y(n)$ also denoted as $(x_{n})\succ (y_{n})$.
*Muirhead's Inequality* states that 

$$
(x_{n})\succ (y_{n})\implies \sum_{sym}a_{1}^{x_{1}}a_{2}^{x_{2}}\cdots a_{n}^{x_{n}}\geq \sum_{sym}a_{1}^{y_{1}}a_{2}^{y_{2}}\cdots a_{n}^{y_{n}}
$$


INSERT PROOF
with Karamta's Inequality

***
# Holders Inequality
For sequences $\{a_{1_{1}},a_{1_{2}},\dots ,a_{1_{n}}\},\{a_{2_{1}},a_{2_{2}},\dots ,a_{2_{n}}\},\dots,\{a_{k_{1}},a_{k_{2}},\dots ,a_{k_{n}}\} \in \mathbb{R}_{>0}$ and weights $\lambda_{1},\lambda_{2},\dots ,\lambda_{k} \in \mathbb{R}_{\geq_{0}}\text{ s.t } \sum \lambda_{i}=1$, Holders states that 

$$
\sum_{j=1}^{n}\prod_{i=1}^{k}a_{i_{j}}^{\lambda_{i}}\leq \prod_{i=1}^{k}\left(\left( \sum_{j=1}^{n}a_{i_{j}} \right)^{\lambda_{i}}\right)
$$

With the equality holding if and only if the sequences are proportional to each other
INSERT PROOF
## Variants
### $k=2$ Case
Using Holders with two sequences $a_{i},b_{i}$ and weights $\lambda_{1}=\frac{p}{p+q}, \lambda_{2}=\frac{q}{p+q}$ for $p,q\in \mathbb{R}^{+}$
Let $a_{1},a_{2},\dots ,a_{n} \in \mathbb{R}\geq_{0}$ and $b_{1},b_{2},\dots ,b_{n} \in \mathbb{R}_{\geq_{0}}$ and $p,q \in \mathbb{R}^{+}$, Then 

$$
\displaystyle \left( \sum a_{i} \right)^{p}\left( \sum b_{i} \right)^{q}\geq\left( \sum (a_{i}^{p}b_{i}^{q})^{\frac{1}{p+q}} \right)^{p+q}
$$

With the equality only holding when the sequences are proportional to each other.
**Proof**
1. Plugging in conditions to Holders we get $\displaystyle \left( \sum a_{i} \right)^{\frac{p}{p+q}}\left( \sum b_{i} \right)^{\frac{q}{p+q}}\geq \left( \sum a^{\frac{p}{p+q}}b^{\frac{q}{p+q}} \right)$
2. Rearranging and raising both sides to the power of $p+q$ gets $\displaystyle \left( \sum a_{i} \right)^{p}\left( \sum b_{i} \right)^{q}\geq\left( \sum (a_{i}^{p}b_{i}^{q})^{\frac{1}{p+q}} \right)^{p+q}$ as desired $\quad \square$.

**Alternate Proof**
1. Since the inequality is homogeneous we can scale both $a_{i}$ and $b_{i}$ such that $\sum a_{i}=\sum b_{i}=1$
2. Then by **Weighted AM-GM** $\displaystyle \sum \sqrt[p+q]{a_{i}^{p}b_{i}^{q}} \leq \sum \frac{pa_{i}+qb_{i}}{p+q}=\frac{1}{p+q}\left( p\sum a_{i} +q\sum b_{i}\right)=1=\left( \sum a_{i} \right)^{p}\left( \sum b_{i} \right)^{q} \quad \square$

More concretely the scaling that is used is $a_{i}\to ta_{i} \text{ s.t }\sum ta_i=1$ and $b_{i}\to sb_{i} \text{ s.t } \sum sb_{i}$.
So we yield that $\displaystyle \left( \sum ta_{i} \right)^{p}\left( \sum sb_{i} \right)^{q}=t^{p}s^{q}\left( \sum a_{i} \right)^{p}\left( \sum b_{i} \right)^{q}$ and $\displaystyle \left( \sum ((ta_{i})^{p}(sb_{i})^{q})^{\frac{1}{p+q}} \right)^{p+q}=\left(t^{\frac{p}{p+q}}s^{\frac{q}{p+q}} \sum (a_{i}^{p}b_{i}^{q})^{\frac{1}{p+q}} \right)^{p+q}=t^{p}s^{q}\left( \sum (a_{i}^{p}b_{i}^{q})^{\frac{1}{p+q}} \right)^{p+q}$
So both sides scale by a positive factor of $t^{p}s^{q}$ so we can divide through and now we have $\sum a_{i}=\sum b_{i}=1$
### Classical Conjugate-Exponent Form
Using the $k=2$ case and making transformations $a_{i}\to a_{i}^{p}, \ b_{i}\to b_{i}^{q}$ and renaming exponents so that $\frac{p}{p+q}\to \frac{1}{p}, \ \frac{q}{p+q}\to \frac{1}{q}$ *(This adds the condition $p,q>1$)* we get 

$$
\sum a_{i}b_{i}\leq \left( \sum a_{i}^{p} \right)^{1/p}\left( \sum b_{i}^{q} \right)^{1/q}
$$


### Cauchy-Schwarz
Using the classical conjugate-exponent form and setting $p=q=\frac{1}{2}$ then squaring the whole inequality (Also equivalent to the full holders inequality with $\lambda_{1}=\lambda_{2}=\frac{1}{2}$ then transformations $a_{i}\to a_{i}^{2}, \ b_{i}\to b_{i}^{2}$)

$$
\left( \sum a_{i}^{2} \right)\left( \sum b_{i}^{2} \right)\geq \left( \sum a_{i}b_{i} \right)^{2}
$$


*Note that now we introduced the squares we have expanded the domain so now we get that* $a,b \in \mathbb{R}$
### Titu's Lemma
*Titu's Lemma* states that for $a_{1},a_{2},\dots ,a_{n}\in \mathbb{R}$ and $b_{1},b_{2},\dots ,b_{n}\in \mathbb{R}^{+}$ 

$$
\frac{a_{1}^{2}}{b_{1}}+\frac{a_{2}^{2}}{b_{2}}+\dots+\frac{a_{n}^{2}}{b_{n}}\geq \frac{(a_{1}+a_{2}+\dots+a_{n})^{2}}{b_{1}+b_{2}\dots +b_{n}}
$$


Note this is just *Cauchy-Schwarz* applied to the sequences $\displaystyle \left\{\frac{a_{n}}{\sqrt{b_{n}}}\right\}$ and $\{\sqrt{b_{n}}\}$ *hence the extra restrictions on $b_{i}\in \mathbb{R}^{+}$*.
This is a very useful version for eliminating fractions.
***
# Chebyshev's Sum Inequality
Let $a_{1},a_{2},\dots ,a_{n} \in \mathbb{R}$ and $b_{1},b_{2},\dots ,b_{n} \in \mathbb{R}$ such that they are both monotonic in the same direction, Then 

$$
\frac{1}{n}\sum a_{i}b_{i}\geq \left( \frac{1}{n} \sum a_{i}\right)\left( \frac{1}{n}\sum b_{i} \right)
$$

With equality only holding when at least on of the sequences is constant ***or*** they are proportional meaning $\exists c \text{ s.t } b_{i}=ca_{i} \quad\forall i$.
If they are monotonic but in opposite directions then the reverse inequality holds with the same conditions for equality.
INSERT PROOF
***
# Schur's Inequality 
Let $a,b,c \in \mathbb{R}_{\geq_{0}}, \ r\in \mathbb{R}^{+}$, Then *Schur's Inequality* States 

$$
\sum_{cyc}a^{r}(a^{2}+bc)\geq \sum_{cyc}a^{r+1}(b+c)
$$

With equality if and only if $a=b=c$ or $\{a,b,c\}=\{x,x,0\}$
The $r=1$ case is most common and is 

$$
a^{3}+b^{3}+c^{3}+3abc \leq \sum_{sym}a^{2}b
$$


INSERT PROOF
***
# Tangent Line Trick