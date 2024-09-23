
# Axioms of Groups

- A binary operation on a set is a calculation that combines 2 elements of a set to produce another element of the same set
- An identity element of set $S$ under binary operation $*$ is an element $e \in S$ such that $\forall a \in S$, $a * e = e * a = a$
  There can only be one identity element
- $\exists$ identity element $e \Rightarrow \exists a,b \in S$ such that $a * b = b * a = e \Rightarrow$ $a$ is the inverse of $b$ and vice versa
- A binary operation is associative if $\forall a,b,c \in S$
  $a * (b*c) = (a*b) * c$

A Group is a set together with a binary operation that follows the axioms:
- Closure: $\forall a,b \in G$, $a * b \in G$
- Identity: $\exists$ identity element $e$
- Inverse: $\forall a \in G$, $\exists a^{-1}$
- Associativity: $*$ is associative $\forall a,b,c \in G$
# A-Level Further Pure 2
## Cayley Tables & Finite Groups

A Cayley Table fully describes a finite group by showing all possible products of elements in the group

When a group's elements are displayed in a Cayley Table:
- All entries are $\in G$
- Every entry appears exactly once in each row & column
- The position of $e$ is symmetric about the leading diagonal (diagonal from $(1,1) \cdots (n,n)$)
## Modular Arithmetic Groups

You can use modular arithmetic to define a finite group of integers.

The operation $\times_n$ is defined as $ab \pmod{n}$
The operation $+_n$ is defined as $(a+b) \pmod{n}$

You can use $\equiv_n$ to show multiplication or addition modulo $n$:
$a * b \equiv_n c \qquad a,b,c \in G$

## Groups of Permutations

A group can be any set of objects with any operation as long as they follow the axioms.

A set could be the permutation of $n$ objects with operation $a \circ b$. $a,b \in S$ where $a \circ b$ is the operation of applying permutation $b$ then $a$ forms a group.

The symmetric group is a group on $n$ elements defined as the group of all possible permutations that can be performed on $n$ objects coupled with the operation of composition $(a \circ b)$.

You can use 2 row notation to describe permutations like:

$$
\begin{pmatrix} 1 & \cdots & n \\ p_1 & \cdots & p_n \end{pmatrix}
$$

The top row shows the starting position and $p_i$ denotes what object will end up in the $i$th position and NOT what position the $i$th object will end up in.

### Composition:
To find $a \circ b = c$, $c$ will be $\begin{pmatrix} 1 \cdots n \\ c_1 \cdots c_2 \end{pmatrix}$ where $c_i$ is found by finding $b_i$ in $b$ (in the bottom row) then find $b_i$ in top row of $a$ and $c_i$ is the corresponding $a_{(b_i)}$.

### Inverse:
To find the inverse swap top & bottom & set.





## Groups of Symmetries

You can construct a group by considering all symmetrical transformations of an n-sided polygon (There is n possible rotations and n possible reflections) coupled with the composition operation.

## Cyclic Groups

A cyclic group is a group that can be written where all elements can be written as $a^k$ where $a$ is the group generator and $k \in \mathbb{Z}^+$. $a^k$ denotes performing the group operation $k$ times.

$a^3 = a \circ a \circ a \qquad a^k = \underbrace{a \circ a \cdots \circ a}_{k \text{ times}}$
## Order of Subgroups
- If a group $G$ has $n$ elements then the order (denoted as $|G|$) is $n$
- The order of an element $a$ in group $(G,*)$ with identity $e$ is the smallest integer $k$ such that $a^k = e$
- If $|G|$ is finite then $|a| \mid |G|$
- $G$ is cyclic $\Leftrightarrow \exists a$ such that $|a| = |G|$
Let $a \in G \Rightarrow$:
$|a| \in \mathbb{N}^0 \Rightarrow (a^m = e \Leftrightarrow |a||m)$
$|a| = \infty \Rightarrow (x \neq y \Rightarrow a^x \neq a^y)$
$(a^x = a^y \& x \neq y) \Rightarrow |a| \in \mathbb{N}^0$

## Subgroups and Isomorphisms
If some subset of the underlying set of a group adheres to the group axioms then it is a subgroup.

If $H$ is a subgroup of $G$ then:
$H \subset G \Rightarrow H$ is a proper subgroup of $G$
$H \subseteq G \Rightarrow H$ is a subgroup of $G$
$H < G \Rightarrow |H| < |G|$
$H \leq G \Rightarrow |H| \leq |G|$
Every group has at least 2 trivial subgroups $\{e\}, *$ and $(G,*)$ - itself.

You can find subgroups of finite groups quickly by using the following rule:

Let $G$ be a group and $H$ a finite subset of $G$ $\Rightarrow$ ($H$ is a subgroup if $H$ is closed under the operation of $G$)

- $|G| < \infty \Rightarrow \forall a \in G$ generates $H \subseteq G$ written as $\langle a \rangle$
- Lagrange's theorem states:
  $H \subseteq G$, $|G| < \infty \Rightarrow |H| \mid |G|$

## Isomorphisms

2 groups $(G,*)$, $(H,\circ)$ are isomorphic $(G \cong H)$ if there exists a mapping $f: G \rightarrow H$ such that:

- $f$ maps all elements of $G$ to $H$
- $f$ is one to one
- $f$ preserves structure: $f(a*b) = f(a) \circ f(b)$

If $G \cong H$ with identity elements $e_G$, $e_H$ and $f: G \rightarrow H$ is an isomorphism then $\forall a \in G$ and $\forall n \in \mathbb{Z}$:

- $f(e_G) = e_H$
- $f(a^{-1}) = [f(a)]^{-1}$
- $f(a^n) = [f(a)]^n$
- $|G| = |H|$
- If $G$ has $k$ elements of order $n$ then $H$ has $k$ elements of order $n$
- If $G$ has $k$ subgroups of order $n$, $H$ has $k$ subgroups of order $n$
- $J \subseteq G \Rightarrow \exists L \subseteq H$ such that $J \cong L$

Groups of order $\leq 8$ can be classified by the order of their elements.




## Flashcards
#Maths/Topics/Groups, #Maths/A-Level-Further-Pure/Groups

How can modular arithmetic be used to define a finite group of integers?
?
Modular arithmetic can be used to define finite groups of integers using two operations:
1. $\times_n$ defined as $ab \pmod{n}$
2. $+_n$ defined as $(a+b) \pmod{n}$
The notation $\equiv_n$ can be used to show multiplication or addition modulo $n$: $a * b \equiv_n c$ where $a,b,c \in G$ <!--SR:!2024-09-18,4,270-->

What is a group of permutations?
?
A group of permutations is a set of permutations of $n$ objects with the operation $a \circ b$, where $a,b \in S$ and $a \circ b$ is the operation of applying permutation **$b$ then $a$**. This set forms a group as long as it follows the group axioms. <!--SR:!2024-09-18,3,257-->

What is the **symmetric** group?
?
The symmetric group is a group on $n$ elements defined as the group of all possible permutations that can be performed on $n$ objects, coupled with the operation of composition $(a \circ b)$. <!--SR:!2024-09-16,1,237-->

How can permutations be represented using two-row notation?
?
Permutations can be represented using two-row notation as follows:
$$\begin{pmatrix}
1 & \cdots & n \\
p_1 & \cdots & p_n
\end{pmatrix}$$
The top row shows the starting position, and $p_i$ denotes what object will end up in the $i$th position (not what position the $i$th object will end up in). <!--SR:!2024-09-17,3,250-->

How is composition performed in permutation groups?
?
To find $a \circ b = c$, follow these steps:
1. Write $c$ as $\begin{pmatrix} 1 \cdots n \\ c_1 \cdots c_n \end{pmatrix}$
2. For each $i$, find $b_i$ in the bottom row of $b$
3. Find $b_i$ in the top row of $a$
4. $c_i$ is the corresponding element in the bottom row of $a$ <!--SR:!2024-09-19,4,277-->

How is the inverse of a permutation found?
?
To find the inverse of a permutation:
1. Swap the top and bottom rows
2. Rearrange the columns so that the new top row is in ascending order
---
What is a group of **symmetries**?
?
A group of symmetries is constructed by considering all symmetrical transformations of an n-sided polygon, including n possible rotations and n possible reflections, coupled with the composition operation. <!--SR:!2024-09-18,4,270-->

What is a cyclic group?
?
A cyclic group is a group where all elements can be written as $a^k$, where $a$ is the group generator and $k \in \mathbb{Z}^+$. $a^k$ denotes performing the group operation $k$ times. <!--SR:!2024-09-19,4,277-->

How is the order of a group defined?
?
The order of a group $G$, denoted as $|G|$, is the number of elements in the group. If a group $G$ has $n$ elements, then $|G| = n$. <!--SR:!2024-09-19,4,277-->

What is the order of an element in a group?
?
The order of an element $a$ in a group $(G,*)$ with identity $e$ is the smallest positive integer $k$ such that $a^k = e$. <!--SR:!2024-09-19,4,277-->

What is the relationship between the order of an element and the order of a finite group?
?
If $|G|$ is finite, then $\forall a \in G, \quad |a| \mid |G|$ <!--SR:!2024-09-18,4,270-->

What is the condition for a group to be cyclic?
?
A group $G$ is cyclic if and only if there exists an element $a$ in $G$ such that $|a| = |G|$. In other words, there must be an element whose order is equal to the order of the group. <!--SR:!2024-09-16,1,237-->

What are the properties of element orders in groups?
?
For an element $a$ in group $G$:
1. If $|a| \in \mathbb{N}$, then $a^m = e \Leftrightarrow |a||m$
2. If $|a| = \infty$, then $x \neq y \Rightarrow a^x \neq a^y$
3. If $a^x = a^y$ and $x \neq y$, then $|a| \in \mathbb{N}$ <!--SR:!2024-09-16,1,237-->

What is a subgroup?
?
A subgroup is a subset of the underlying set of a group that adheres to the group axioms. <!--SR:!2024-09-18,4,270-->

What are the notations for subgroups and their meanings?
?
1. $H \subset G$: $H$ is a proper subgroup of $G$
2. $H \subseteq G$: $H$ is a subgroup of $G$
3. $H < G$: $H$ is a proper subgroup of $G$ and $|H| < |G|$
4. $H \leq G$: $H$ is a subgroup of $G$ and $|H| \leq |G|$ <!--SR:!2024-09-18,3,257-->

What are the trivial subgroups of a group?
?
Every group has at least two trivial subgroups:
1. $\{e\}$, where $e$ is the identity element
2. $(G,*)$, the group itself <!--SR:!2024-09-19,4,277-->

---
What is a binary operation on a set?
?
A binary operation on a set is a calculation that combines two elements of a set to produce another element of the same set. <!--SR:!2024-09-19,4,277-->

What is an identity element in a set under a binary operation?
?
An identity element $e$ of set $S$ under binary operation $*$ is an element $e \in S$ such that $\forall a \in S$, $a * e = e * a = a$. There can only be one identity element. <!--SR:!2024-09-18,4,270-->

What is the inverse of an element in a group?
?
Given an identity element $e$ in a set $S$ with binary operation $*$, for elements $a,b \in S$, if $a * b = b * a = e$, then $a$ is the inverse of $b$ and vice versa. <!--SR:!2024-09-18,4,270-->

What is an associative binary operation?
?
A binary operation is associative if $\forall a,b,c \in S$, $a * (b*c) = (a*b) * c$. <!--SR:!2024-09-19,4,277-->

What are the four axioms that define a group?
?
A group is a set together with a binary operation that follows these four axioms:
1. Closure: $\forall a,b \in G$, $a * b \in G$
2. Identity: $\exists$ identity element $e$
3. Inverse: $\forall a \in G$, $\exists a^{-1}$
4. Associativity: $*$ is associative $\forall a,b,c \in G$ <!--SR:!2024-09-17,3,250-->

What is a Cayley Table and What are it’s properties?
?
When a group's elements are displayed in a Cayley Table:
1. All entries are elements of the group $G$
2. Every entry appears exactly once in each row & column
3. The position of the identity element $e$ is symmetric about the leading diagonal (diagonal from $(1,1)$ to $(n,n)$)
---
What is the rule for finding subgroups of finite groups?
?
Let $G$ be a group and $H$ a finite subset of $G$. $H$ is a subgroup if $H$ is closed under the operation of $G$. <!--SR:!2024-09-18,4,270-->

What does Lagrange's theorem state for finite groups?
?
For a finite group $G$ and its subgroup $H$, the order of $H$ divides the order of $G$. In mathematical notation: $H \subseteq G$, $|G| < \infty \Rightarrow |H| \mid |G|$ <!--SR:!2024-09-18,3,250-->

What conditions must be satisfied for two groups to be isomorphic?
?
Two groups $(G,*)$ and $(H,\circ)$ are isomorphic if there exists a mapping $f: G \rightarrow H$ such that:
1. $f$ maps all elements of $G$ to $H$
2. $f$ is one-to-one
3. $f$ preserves structure: $f(a*b) = f(a) \circ f(b)$ <!--SR:!2024-09-18,4,270-->

What properties are preserved under group isomorphisms?
?
For isomorphic groups $G$ and $H$ with isomorphism $f: G \rightarrow H$:
1. $f(e_G) = e_H$ (identity elements map to each other)
2. $f(a^{-1}) = [f(a)]^{-1}$ (inverses map to inverses)
3. $f(a^n) = [f(a)]^n$ for all $n \in \mathbb{Z}$
4. $|G| = |H|$ (groups have the same order)
5. Number of elements of each order is preserved
6. Number of subgroups of each order is preserved
7. Subgroup structure is preserved: $J \subseteq G \Rightarrow \exists L \subseteq H$ such that $J \cong L$ <!--SR:!2024-09-18,3,257-->

How can groups of order $\leq 8$ be classified?
?
Groups of order $\leq 8$ can be classified by the order of their elements. This means that the structure of these groups can be determined by examining the number and order of elements within each group. <!--SR:!2024-09-16,1,237-->


