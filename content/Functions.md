---
tags:
  - Maths/Algebra
---
# Definition of a Function
Given two sets $A,B$ a function is any subset of $A\times B$ such that each $a\in A$ pairs with **exactly one** $b\in B$. It is denoted as $f:A\to B$.
It can also be described that a *function* is a mapping from any element in one set (the *domain* $A$) to exactly one element in another (the *range* $B$). 
## Codomain
The ***codomain*** is the set of all possible outputs as *declared,* not necessarily those actually produced. In notation $f: A\to B$, $B$ is the codomain. 
*This is an important distinction especially in functional equations where it might specify that $f: \mathbb{Z}\to \mathbb{Z}$. Every integer must be a valid input and produce an $f(a) \in \mathbb{Z}$ but not every integer has to be obtainable for example $f(a)=0$ is a valid $f:\mathbb{Z}\to \mathbb{Z}$ solution despite ever integer except $0$ being obtainable.*
## Range
The ***range*** is simply the set of all possible outputs denoted as $\text{range(f)}=\{f(a) \ |\ a\in A\}$. The range is always a subset of the *codomain*. $\text{range(f)} \subseteq \text{codomain}$. In notation $f: A\to B$, $A$ is the range. 
## Image
The *range* is also called the ***image*** of the function $f$. You can also say that the *image* of $a \in \text{domain(f)}$ is $f(a) \in \text{range(f)}$.
## Preimage
Let the ***preimage*** of an element $b$ is $f^{-1}(b)=\{{a\in A \ | \ f(a)=b}\}$. Similarly, the preimage of a set $S$ is $f^{-1}(S)=\{{a\in A \ | \ f(a)\in S}\}$. *(Note that the preimage is **always** a set).*
The *preimage* is defined for all values in the *codomain* for all functions but a function can have no preimage if it's not *surjective* (the preimage is just $\emptyset$) or multiple preimages is it's not injective.  

***
# Functional Properties
## Injective
A function is ***injective*** on domain $A$ if different inputs map to different outputs. Formally denoted as 

$$
\begin{gather}
\forall x_{1},x_{2} \in A \quad f(x_{1})=f(x_{2})\implies x_{1}=x_{2} \\
\text{or equivalently} \\
x_{1}\neq x_{2}\implies f(x_{1})\neq f(x_{2})
\end{gather}
$$

It can also be state that *no two elements in the domain share the same image*.
### Monic
A function is ***monic*** *iff* 

$$
\forall g, h, \  f \circ g = f \circ h \implies g = h
$$


**Theorem**
A function then $f$ is *monic* $\Leftrightarrow$ $f$ is *injective*\.

*Proof:*
**Forward direction**
Suppose $f: X\to Y$ is injective and $f \circ g = f \circ h$. Where $g, h: Z\to X$. Then $\forall z \in Z$ we have $f(g(z)) = f(h(z))$. By injectivity we get $g(z) = h(z)$ since this is $\forall z\in Z$, we get $g=h$

**Reverse direction**
Fix a one element set $1 = \{*\}$. Then $\forall x \in X$ define $g_{x}(*) = x$ where $g_{x}:1\to X$. Then $\forall x_{1}, x_{2}, \ f(x_{1}) = f({x_{2}}) \implies f\circ g_{x_{1}} = f\circ g_{x_{2}} \implies g_{x_{1}} = g_{x_{2}}\implies x_{1}=x_{2}$. Hence $f$ is injective\.
## Surjective
$f:A\to B$ is *surjective* if it covers the whole domain. Formally denoted as 
$$
\forall y \in B, \quad \exists x \in A \text{ s.t } f(x)=y
$$
 A function is always surjective if $\text{codomian}=\text{range}$.  
### Epic
A function is ***epic*** *iff* 

$$
\forall g, h, \ g\circ f = h\circ f\implies g =h
$$



**Theorem**
A function then $f$ is *epic* $\Leftrightarrow$ $f$ is *surjective*\.

*Proof:*
**Forward Direction**
Suppose $f: X\to Y$ is surjective and $g \circ f = h \circ f$. Where $g, h: Y\to Z$. Then by surjectivity, $\forall y \in Y, \ \exists x \in X \text{ s.t }f(x)=y$. So $\forall y\in Y$ we can find a suitable $x\text{ s.t } g(f(x)) = h(f(x)) \implies g(y) = h(y)$. Hence $g=h$.

**Reverse Direction** - *Proof by contrapositive*
Suppose $f: X\to Y$ is **not** surjective. Then $\exists y \in Y \text{ s.t }  \nexists x, \ f(x)=y$. Pick such a $y$ and call it $a$. Then fix a two element set $Z= \{1, 2\}$. Then define 

$$
g(x) = 1, \quad h(x) = \begin{cases}1 & y\neq a \\ 2 & y=a\end{cases}
$$

But $g \circ f = h \circ f$ as $\forall x \in X, \ f(x) \neq a$ so $g(f(x)) = h(f(x)) = 1$. But since $h \neq g$, $f$ is not epic\. 

## Bijective
$f:A\to B$ is bijective if it is both *injective* and *surjective*

***
# Parity
We call a function $f$ *even* $\Leftrightarrow f(-x)=f(x)$ and we call $f$ *odd* $\Leftrightarrow f(-x)=-x$. If neither holds than  has no parity.  This terminology comes from the function $x^{n}$ where if $n$ is even $(-x)^{n}=x^{n}$ and if $n$ is odd $(-x)^{n}=-x^{n}$. 
This concept still holds for many functions as if $f$ is equal to some power series then $f\text{ even}\implies$ the power series only contains even powers of $x$ likewise for odd functions.
**Proof**
1. Let $f(x)=\sum a_{n}x^{n}$ and assume for contradiction that $f$ is even. In it's radius of convergence $f$ is *absolutely* convergent.
2. Then split $f$ into it's even and odd sums. $f=\sum b_{m}x^{\text{even}}+\sum c_{k}x^{\text{odd}}$ 
3. Since $f$ is even then $f(x)-f(-x)=0\implies \sum b_{m}x^{\text{even}}+\sum c_{k}x^{\text{odd}}-\sum b_{m}(-x)^{\text{even}}-\sum c_{k}(-x)^{\text{odd}}$.
4. But $\sum b_{m}x^{\text{even}}=\sum b_{m}(-x)^{\text{even}}$ as every power is even. Similarly $\sum c_{k}(-x)^{\text{odd}}=-\sum c_{k}x^{\text{odd}}$
5. This leads us with $0 = \sum c_{k}(-x)^{\text{odd}}+\sum c_{k}(-x)^{\text{odd}}\implies\sum c_{k}(-x)^{\text{odd}} = 0 \quad \forall x$ hence $f$ contains no odd powers
6. Similar argument can be made for odd functions.

## Constructing Even and Odd Functions
Given a function $f$ which has no parity, we can create two special functions $f_{\text{odd}}, f_{\text{even}}$ which are even and odd functions respectively with the property that $f_{\text{odd}}+f_{\text{even}}=f$. We can think of this as taking the odd and even *"components"* of $f$. And if $f$ is a power series $f_{\text{odd}}, f_{\text{even}}$ are precisely the part of the power series with odd and even powers respectively. Making these functions is very easy. 
$$
f_{\text{odd}}=\frac{f(x)-f(-x)}{2},\quad f_{\text{even}}=\frac{f(x)+f(-x)}{2}
$$

It is trivial to check these functions are odd and even and that they have the property $f_{\text{odd}}+f_{\text{even}}=f(x)$.
***
# Indicator Function
Let $A \subseteq U$, the ***indicator function*** of $A$ denoted by $1_{A}$ is a function with domain $U$ and range $\{0,1\}$ defined as 
$$
1_{A}(x)=\begin{cases} 1, & x \in A \\0, & x \notin A \end{cases}
$$

*** 