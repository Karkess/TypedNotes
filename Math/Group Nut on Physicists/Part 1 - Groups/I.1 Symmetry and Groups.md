---
title: I.1 Symmetry and Groups
tags: ['Part I - Groups: Discrete or Continuous, Finite or Infinite']

---

# Part I - Groups: Discrete or Continuousm Finite or Infinite

"The notion of a group is defined and then illustrated with many examples. Finite groups are studied. The rotation group, as the canonical example of a continuous group, is approached in two different ways. The all-important concepts of Lie group and Lie algebra are introduced."

## I.1 Symmetry and Groups 
### Symmetry and Transformation 

A brief discussion of different types of symmetries in polygons.

### Symmetry in physics

No specific examples, just that we tend to find more symmetries in fundamental physics than one may have guessed. 

### Groups
A group $G$ is a set of entities $\{g_\alpha\}$ called group elements which are closed under the relation of the form $g_\alpha\cdot g_\beta=g_\gamma$, where all $g\in G$. So 'multiplying' or 'composing' two elements together stays in the group. This relation satisfies the following axioms:
1. Associativity: Composition is associative: $(g_\alpha\cdot g_\beta)\cdot g_\gamma=g_\alpha\cdot(g_\beta\cdot g_\gamma)$.
2. Existence of the identity: There exists a group element, known as the identity and denoted by $I$, such that $I\cdot g_\alpha=g_alpha$ and $g_\alpha\cdot I=g_\alpha\,$. 
3. Existence of the inverse: For every group element $g_\alpha$, there exists a unique group element, known as the inverse of $g_\alpha$ and denoted by $g_\alpha^{-1}$, such that $g_\alpha^{-1}\cdot g_\alpha=I$.

*Some comments*
1. Composition is not required to commute. 
    - Composition that does are called 'Abelian' groups, and that which does not are nonabelian. Strong, weak, and electromagnetic gauge symmetries are nonabelian. 
2. For groups, right and left inverses are the same.
3. Sometimes $I$ is denoted $g_0$. 
4. The label $\alpha$ that distinguishes the group element $g_\alpha$ may be discrete or continuous. 
5. The set of elements may be finite, in which case we have a finite group. 

---
### Examples of Groups
1. Rotations in 3-dimensional Euclidean space, referred to as $SO(3)$.
    - The determinant of the rotation matrix is $1$. 
2. Rotations in 2-dimensional Euclidean space, called $SO(2)$. 
3. The permutation group $S_4$ rearranges an ordered set of $4$ objects.
4. Even permutations of 4 objects form the group $A_4$. 
5. The two square roots of $1, \{1,-1\}$ form the group $Z_2$ under ordinary multiplication.
6. The three cube roots of $1$ form the group $Z_3=\{1,\omega,\omega^2\},$ where $\omega=e^{\frac{2\pi i}{3}}$. 
7. Complex numbers of magnitude 1, namely $e^{i\phi}$, form a group called $U(1)$
8. The addition of integers$\mod{N}$ generates a group. 
9. The addition of real numbers generates a group. 
10. Lorentz boosts form a group
11. $n$-by-$n$ matrices $M$ with determinants of 1 form a group under ordinary matrix multiplication. If the entries are real the group is known as $SL(n,\mathbb{R})$ and $SL(n,\mathbb{C})$. (SL = "Special Linear"). (S for special because they have determinant 1). 

---
### Concept of a subgroup 
Given a set of group elements $\{g_\alpha\}$ that form a group, if a subset of those elements $\{h_\alpha\}$ also forms a group, called $H$, then $H$ is a subgroup of $G$, and we write $H\subset G$. Examples:
1. $SO(2)\subset SO(3)$, follows logically, rotations in 2D are a subset of rotations in 3D.
2. $S_m\subset S_n$ for $m<n$. Permuting 3 objects is a subset of permuting 5 objects, and just keeping 2 the same. 
3. $A_n\subset S_n$
4. $Z_2\subset Z_4$, but $Z_2 \not\subset Z_5$.
5. $SO(3)\subset SL(3,\mathbb{R})$, no way this one comes up again, ;P.

--- 
### Cyclic subgroups
An group where the operation loops back on itself is a cyclic subgroup. If the number of elements in the subgroup is the same as the subgroup, then G is denoted $Z_k$. 

---
### Lagrange's Theorem
Lagrange proved the following theorem: Let a group $G$ with $n$ elements have a subgroup $H$ with $m$ elements. Then $m$ is a factor of $n$. In other words, $n/m$ is an integer. 

From this it follows that if $p$ is prime, then $Z_p$ does not have a nontrivial subgroup, hinting at the intimate link between group theory and number theory. 

---
### Direct product of groups
We can combine the elements of two groups $H\equiv F\otimes G$, which has an inverse of $(f,g)$ as $(f^{-1},g^{-1})$, and $F\otimes G$ has $mn$ elements. 

---
### Klein's Vierergruppe $V$

A simple example is $Z_2\otimes Z_2$, with four elements: $I=(1,1), A=(-1,1), B=(1,-1)\text{, and }C=(-1,-1)$. For example, we have $AB=(-1,-1)=C$. 

Note, the square of $Z_2\otimes Z_2$ (known as Vierergruppe (or "4-group" in German)) has any square element equal to $1$, whereas this is not true for $Z_4$. 

The elements of $F$ are written as $(f, I)$, and $G$  as $(I,g)$. These commute. 

It seems like an easy way to construct larger groups, but nature does the same. The theory of the strong, weak, and electromagnetic interaction is based on the group: $SU(3)\otimes SU(2) \otimes U(1)$. 

---
### A "teeny" bit of history.

Just a few quotes about founders of fields of math and the mention of a couple of names, with a tiny bit more detail on Galois. Fortunately I'm already a history of science nerd and am well acquainted with most of these characters, notable exceptions would be Abel and Ruffini. I don't really think I've ran into the name Ruffini much in my studies, Abel a trillion times through Abelian groups alone. 

I guess since I'm rambling already,  Zee mentioned the story of Galois being killed over the honor of a young woman, which is the popular story, but I think this is debated.

Wait, he said *or* his political beliefs. A key word. Never mind Zee is greater than my reading comprehension. I also love his attention to etymology. Really just a great guy all around, I think. Excellent author, so appreciative for him and very underrated. 

---
### Multiplication table: The "once and only once rule"

This section just goes in detail about  constructing Cayley tables (I think they're called this? Not sure what makes it a Cayley table, I guess) by going through and making sure that no element is repeated in each row or column and constructing it sequentially and then checking if the multiplications are self consistent. I actually love checking Cayley tables and constructing them. It remind me of the very early grades and has a familiar warmth to them, even when I had to manually verify some quaternion group that was a tiny bit tedious. 

---
### A quick way: Construct the cyclic subgroups
Using the idea that $\{g_n\}^k=I$ for some integer $k$, and Lagrange's Theorem, we can construct groups through looping these identities and then we get either $G=Z_n\otimes Z_n$ if an element times itself in $I$, or G the element times itself the number of elements in the group is itself, at least with groups of 4. 

---
### Presentations

Groups can be listed by their properties, or by their presentations (which list the elements (sometimes called generators)) from which all other elements can be obtained by group multiplication. As an example of the groups of 4 above: 
$$Z_4=\langle A|A^4=I\rangle$$$$Z_2\otimes Z_2:\langle A^2=B^2=I, AB=BA\rangle$$ It is clear from inspection these two groups are clearly distinct. 

---
### Homomorphism and Isomorphism
A map $f:G\rightarrow G'$ of a group $G$ onto the group $G'$ is called a homomorphism if it preserves the multiplicative structure of $G$, that is: $f(g_1)f(g_2)=f(g_1g_2)$.
The homomorphism is called an isomorphism if it is bijective.

*Note: The additive group of integers$\mod{N}$ is isomorphic to the multiplicative group $Z_n$, which is of value when discussing the relationship between the addition and multiplication of angular momenta in quantum mechanics.*

$Z_p\otimes Z_q$ and $Z_{pq}$ are isomorphic if $p$ and $q$ are prime or relatively prime. $SO(2)$ and $U(1)$ are also isomorphic$. 

---
## Exercises
**1. The center of a group $G$ (denoted by $Z$) is defined to the the set of elements $\{z_1,z_2,\dots\}$ that commute with all elements of $G$, that is, $z_ig=gz_i$ for all $g$. Show that $Z$ is an abelian subgroup of $G$.**

I don't really get this one. $z_ig=gz_i$ is abelian by definition. We construct a group specifically that commutes, which is the definition of abelian. Maybe I'm reading it wrong.

**2. Let $f(g)$ be a function of the elements in a finite group $G$, and consider the sum $\sum_{g\in G}f(g)$. Prove the identity--** No. I don't think I will. I see enough proofs in the math books I'm working through.

**3. Show that $Z_2\otimes Z_4\neq Z_8$.**
Let's do a progressive march solution, as Zee demonstrated, by adding (1,1) for each element:

$Z_2\otimes Z_4: (0,0)\xrightarrow1(1,1)\xrightarrow2(0,2)\xrightarrow3(1,3)\xrightarrow4(0,0)$. We have $4$ steps to loop, not $8$. 

**4. Find all groups of order $6$**. 

No part two. I'll google it though.

Damn there were only 2. My laziness betrayed me again. Anyways it's cyclic group of order 6 and permutation group of size 3. 