# Axioms of Groups

* A binary operation on a set is a calculation that combines 2 elements of a set to produce another element of the same set
* An identity element of set $S$ under binary operation $\*$ is an element $e \in S$ such that $\forall a \in S$, $a * e = e * a = a$
  There can only be one identity element
* $\exists$ identity element $e \Rightarrow \exists a,b \in S$ such that $a * b = b * a = e \Rightarrow$ $a$ is the inverse of $b$ and vice versa
* A binary operation is associative if $\forall a,b,c \in S$
  $a * (b*c) = (a*b) * c$

A Group is a set together with a binary operation that follows the axioms:

* Closure: $\forall a,b \in G$, $a * b \in G$
* Identity: $\exists$ identity element $e$
* Inverse: $\forall a \in G$, $\exists a^{-1}$
* Associativity: $\*$ is associative $\forall a,b,c \in G$

# A-Level Further Pure 2

## Cayley Tables & Finite Groups

A Cayley Table fully describes a finite group by showing all possible products of elements in the group

When a group's elements are displayed in a Cayley Table:

* All entries are $\in G$
* Every entry appears exactly once in each row & column
* The position of $e$ is symmetric about the leading diagonal (diagonal from $(1,1) \cdots (n,n)$)

## Modular Arithmetic Groups

You can use modular arithmetic to define a finite group of integers.

The operation $\times_n$ is defined as $ab \pmod{n}$
The operation $+\_n$ is defined as $(a+b) \pmod{n}$

You can use $\equiv_n$ to show multiplication or addition modulo $n$:
$a * b \equiv_n c \qquad a,b,c \in G$

## Groups of Permutations

A group can be any set of objects with any operation as long as they follow the axioms.

A set could be the permutation of $n$ objects with operation $a \circ b$. $a,b \in S$ where $a \circ b$ is the operation of applying permutation $b$ then $a$ forms a group.

The symmetric group is a group on $n$ elements defined as the group of all possible permutations that can be performed on $n$ objects coupled with the operation of composition $(a \circ b)$.

You can use 2 row notation to describe permutations like:

$$
\\begin{pmatrix} 1 & ... & n \\ p_1 & ... & p_n \end{pmatrix}
$$

The top row shows the starting position and $p_i$ denotes what object will end up in the $i$th position and NOT what position the $i$th object will end up in.

### Composition:

To find $a \circ b = c$, $c$ will be $\begin{pmatrix} 1 \cdots n \\ c_1 \cdots c_2 \end{pmatrix}$ where $c_i$ is found by finding $b_i$ in $b$ (in the bottom row) then find $b_i$ in top row of $a$ and $c_i$ is the corresponding $a\_{(b_i)}$.

### Inverse:

To find the inverse swap top & bottom & set.

## Groups of Symmetries

You can construct a group by considering all symmetrical transformations of an n-sided polygon (There is n possible rotations and n possible reflections) coupled with the composition operation.

## Cyclic Groups

A cyclic group is a group that can be written where all elements can be written as $a^k$ where $a$ is the group generator and $k \in \mathbb{Z}^+$. $a^k$ denotes performing the group operation $k$ times.

$a^3 = a \circ a \circ a \qquad a^k = \underbrace{a \circ a \cdots \circ a}\_{k \text{ times}}$

## Order of Subgroups

* If a group $G$ has $n$ elements then the order (denoted as $|G|$) is $n$
* The order of an element $a$ in group $(G,\*)$ with identity $e$ is the smallest integer $k$ such that $a^k = e$
* If $|G|$ is finite then $|a| \mid |G|$
* $G$ is cyclic $\Leftrightarrow \exists a$ such that $|a| = |G|$
  Let $a \in G \Rightarrow$:
  $|a| \in \mathbb{N}^0 \Rightarrow (a^m = e \Leftrightarrow |a||m)$
  $|a| = \infty \Rightarrow (x \neq y \Rightarrow a^x \neq a^y)$
  $(a^x = a^y & x \neq y) \Rightarrow |a| \in \mathbb{N}^0$

## Subgroups and Isomorphisms

If some subset of the underlying set of a group adheres to the group axioms then it is a subgroup.

If $H$ is a subgroup of $G$ then:
$H \subset G \Rightarrow H$ is a proper subgroup of $G$
$H \subseteq G \Rightarrow H$ is a subgroup of $G$
$H < G \Rightarrow |H| < |G|$
$H \leq G \Rightarrow |H| \leq |G|$
Every group has at least 2 trivial subgroups ${e}, *$ and $(G,*)$ - itself.

You can find subgroups of finite groups quickly by using the following rule:

Let $G$ be a group and $H$ a finite subset of $G$ $\Rightarrow$ ($H$ is a subgroup if $H$ is closed under the operation of $G$)

* $|G| < \infty \Rightarrow \forall a \in G$ generates $H \subseteq G$ written as $\langle a \rangle$
* Lagrange's theorem states:
  $H \subseteq G$, $|G| < \infty \Rightarrow |H| \mid |G|$

## Isomorphisms

2 groups $(G,\*)$, $(H,\circ)$ are isomorphic $(G \cong H)$ if there exists a mapping $f: G \rightarrow H$ such that:

* $f$ maps all elements of $G$ to $H$
* $f$ is one to one
* $f$ preserves structure: $f(a\*b) = f(a) \circ f(b)$

If $G \cong H$ with identity elements $e_G$, $e_H$ and $f: G \rightarrow H$ is an isomorphism then $\forall a \in G$ and $\forall n \in \mathbb{Z}$:

* $f(e_G) = e_H$
* $f(a^{-1}) = \[f(a)\]^{-1}$
* $f(a^n) = \[f(a)\]^n$
* $|G| = |H|$
* If $G$ has $k$ elements of order $n$ then $H$ has $k$ elements of order $n$
* If $G$ has $k$ subgroups of order $n$, $H$ has $k$ subgroups of order $n$
* $J \subseteq G \Rightarrow \exists L \subseteq H$ such that $J \cong L$

Groups of order $\leq 8$ can be classified by the order of their elements.

