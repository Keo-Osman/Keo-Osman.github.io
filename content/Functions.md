#Maths/Algebra 
# Definition of a Function
Given two sets $A,B$ a function is any subset of $A\times B$ such that each $a\in A$ pairs with **exactly one** $b\in B$. It is denoted as $f:A\to B$.
It can also be described that a *function* is a mapping from any element in one set (the *domain* $A$) to exactly one element in another (the *range* $B$). 
## Codomain
The ***codomain*** is the set of all possible outputs as *declared,* not necessarily those actually produced.
In notation $f: A\to B$, $B$ is the codomain. 
This is an important distinction especially in functional equations where it might specify that $f: \mathbb{Z}\to \mathbb{Z}$. Every integer must be a valid input and produce an $f(a) \in \mathbb{Z}$ but not every integer has to be obtainable for example $f(a)=0$ is a valid $f:\mathbb{Z}\to \mathbb{Z}$ solution despite ever integer except $0$ being obtainable.
## Range
The ***range*** is simply the set of all possible outputs denoted as $\text{range(f)}=\{f(a) \ |\ a\in A\}$. 
The range is always a subset of the *codomain*. $\text{range(f)} \subseteq \text{codomain}$. 
In notation $f: A\to B$, $A$ is the range. 
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
## Surjective
$f:A\to B$ is *surjective* if it covers the whole domain. Formally denoted as 
$$
\forall y \in B, \quad \exists x \in A \text{ s.t } f(x)=y
$$
 A function is always surjective if $\text{codomian}=\text{range}$.  
## Bijective
$f:A\to B$ is bijective if it is both *injective and *surjective*
***
# Indicator Function
Let $A \subseteq U$, the ***indicator function*** of $A$ denoted by $1_{A}$ is a function with domain $U$ and range $\{0,1\}$ defined as 
$$
1_{A}(x)=\begin{cases} 1, & x \in A \\0, & x \notin A \end{cases}
$$

***