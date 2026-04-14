---
title: I.2 - Finite Groups
tags: ['Part I - Groups: Discrete or Continuous, Finite or Infinite']

---

# I.2 Finite Groups
"Let me first give you an overview or road map to this introduction to the theory of finite groups. We discuss various important notions, including equivalence classes, invariant subgroups, simple groups, cosets, and quotient groups. These notions are illustrated mostly with the permutation groups, which are the easiest to graph and yet have enough structure for them to be highly nontrivial. We also introduce the dihedral groups and the quarternionic group."

---
### Permutation groups and Cayley's theorem

Cayley's theorem states that any finite group $G$ with $n$ elements is isomorphic to the permutation group $S_n$. 

---
### Cycles and Transpositions
For the convention in this book, $(142)$ denotes a cyclic permutation $1\rightarrow4\rightarrow2\rightarrow1.$ and $(35)$ denotes $3\rightarrow5\rightarrow3$. 

---
### Rules for multiplying permutations
**Theorem:** Any permutation can be written as a product of two-cycles. Simply agreeing with intuition that permutations can be performed one swap at a time. 

Some rules for applying 2-cycles:
1. If the two 2-cycles do not have a "number" in common, for example, $(12)$ and $(34)$, then they commute and have nothing more to say. 
2. $(12)(23)=(123).$ Note, since $(32)=(23)$, we can adopt the convention when multiplying 2-cycles, to match the head of one 2-cycle to the tail of the other 2-cycle.
3. We need hardly mention that (12)(21)=$I$.
4. $(12)(23)(34)=(12)(234)=\begin{pmatrix}1&2&3&4\\1&3&4&2\\2&3&4&1\end{pmatrix}=(1234)$.
5. $(123)(345)=(12)(23)(34)(45)=(12)(234(45)=(12345)$

A permutation is even or odd if it decomposes into an even or odd number of 2-cycles. 

---
## Square root of the identity
**Theorem** There is at least one element $g$, which is not the identity $I$, that also squares to the identity, $g^2=I$. (This element is called an *involution*)

---
### Equivalence Classes
An equivalence class very loosely defined are group elements that are "essentially the same".

Consider an example of rotations in $SO(3)$. Rotations of $17^\circ$ and $71^\circ$ are certainly not the same, but a $17^\circ$ rotation around $\hat{x}$ and $\hat{z}$ are very similar, but we wouldn't say $\hat{x}=\hat{z}$. 

Two elements, $g$ and $g'$ in group $G$ are said to be equivalent if there exists another element $f$ such that $$g'=f^{-1}gf.$$

Equivalence is transitive, $g\sim g'\,\land\,g'\sim g''\implies g\sim g''.$

---
### Three facts about classes
1. In an abelian world, everybody is in a class by himself or herself.
2. In any group, the identity is always proudly in its own private class of one.
3. Consider a class $c$ consisting of $\{g_1,\dots,g_{n_c}\}$, then the inverse of these $n_c$ elements, namely, $\{g_1^{-1},\dots,g_{n_c}^{-1}\}$, also forms a class, which we denote by $\overline{c}$

---
### The dihedral group $D_n$
The dihedral group $D_n$ is a set of transformations that leave an $n$-sided regular polygon invariant. 

We say that $D_n$ is presented by: $$D_n=\langle R,r\mid R^n=I,\,r^2=I,\,Rr=rR^{-1}\rangle.$$

---
### The quarternionic group $Q$
The quarternionic group $Q$ consists of the eight elements $\{1,-1,i,-i,j,-j,k,-k\}$ with group multiplication formed by Hamilton's rules: $$i^2=j^2=k^2=-1\quad\land\quad ij=-ji=k,\;jk=-kj=i,\;ki=-ik=j.$$

---
### Coxeter groups
A coxeter group is presented by: $$\langle a_1,a_2,\cdots,a_k\mid(a_i)^2=I,\;(a_ia_j)^{n_{ij}}=I,\;n_{ij}\ge2,\text{ with }i,j=1,2,\dots,k.$$

*Note: Not having an invariant subgroup makes a group **simple.***

Let $f$ be a homomorphic map of group $G$ into itself; in other words, the map is such that $f(g_1)f(g_2)=f(g_1g_2)$. Show that the kernel of $f$, that is, the set of elements that are mapped to the identity, is an invariant subgroup of $G$. 

---
### Invariant subgroup, cosets, and the quotient group
Let $G\rhd H$ (Reminder: This means that all elements equivalent to the elements in the subgroup $H$ are also in $H$.)

Having an invariant subgroup empowers us to form objects called cosets and construct the quotient group.

For an element $g$ consider the elements $\{gh_1,gh_2,\dots\}$ which we will denote by $gH$. This gives a bunch of sets $g_aH,\,g_bH,\dots$

$gH$ is a "*left coset*", which close under multiplication. 

We can mutiply these groups together by multiplying each group element in the set $g_aH$

The left cosets form a group. 

Thus, if a group $G$ has an invariant subgroup $H$, then we can construct another group consisting of left cosets $gH$, a group known as the quotient group written as $Q=G/H$.