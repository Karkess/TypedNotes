---
title: Chapter I-5
tags: [1 - Set Theory and Categories]

---

# 5. Universal Properties

## 5.1 Initial and final objects.
**Definition 5.1.** Let $\mathrm{C}$ be a category. We say that object $I$ of $\mathrm{C}$ is *initial* in $\mathrm{C}$ if for every object $A$ of $\mathrm{C}$ exists *exactly one* morphism $I\rightarrow A$ in $\mathrm{C}$: $$\forall A\in\mathrm{Obj}(\mathrm{C}):\mathrm{Hom}_\mathrm{C}(I,A)\text{ is a singleton.}$$

---
A category need not have an initial or final object. For example, the category obtained by endowing $\mathbb{Z}$ with the relation $\le$. For this to have an initial object, it would need to be smaller than every other integer, and similarly a largest integer for a final object. 

---
**Proposition 5.4.** Let $\mathrm{C}$ be a category.
- *If $I_1, I_2$ are both initial objects in $\mathrm{C}$, then $I_1\cong I_2$.*
- *If $F_1, F_2$ are both final objects in $\mathrm{C}$, then $F_1\cong F_2$.*
*Furthermore, these isomorphisms are uniquely determined.*

## 5.2. Universal properties.

This is a working explanation given without an understanding of functors, which aren't covered until chapter 8. 

We say that a construction *satisfies a universal property* when it may be viewed as a terminal object of a category. 

## 5.3. Quotients.
Let $\sim$ be an equivalence relation defined on set $A$. Let's parse the assertion:
"*The quotient $A/\sim$ is universal with respect to the property of mapping $A$ to a set in such a way that equivalent elements have the same image.*"
The assertion is talking about functions $$A\xrightarrow{\quad\phi\quad}Z.$$ With $Z$ any set, satisfying the property $$a'\sim a''\implies\phi(a')=\phi(a'').$$

## 5.4. Products.
This section gives an example of a product as a universal property through a commutative diagram of $A\times B$, but provides another example where a category that has products, such as those $a,b\in\mathbb{Z}$ for the relation $\le$, where the product can be seen as $z\le a\times b$, which can also be represented as $\mathrm{min}(a,b)\,\,\forall a,b$, which shows a connection between the Cartesian products between sets and the minimum of two integers. They both satisfy 'the same' universal property.

## 5.5. Coproducts.
The prefix *co-* usually indicates the 'reversing all arrows'. 
*Coproducts* are the *initial* objects in the categories $\mathrm{C}^{A,B}$ of morphisms with common *target*, whose *sources* are $A$ and $B$.
This section goes on to show a commutative diagram with reversed arrows from the Products diagram with a $A\coprod B$ instead of $A\times B$. 

**Proposition 5.6** *The $\text{disjoint union}$ is a coproduct in $\mathrm{Set}$.

The coproduct of $A\times B$ with the relation $\le$ on $\mathbb{Z}$ is the $\mathrm{max}(a,b)$.