---
title: Chapter I-4
tags: [1 - Set Theory and Categories]

---

# 4. Morphisms

## 4.1. Isomorphisms.
Let $\mathrm{C}$ be a category.  

**Definition 4.1.** A morphism $f\in\mathrm{Hom}_\mathrm{C}(A,B)$ is an *isomorphism* if it has a (two-sided) inverse under composition: that is, if $\exists g\in\mathrm{Hom}_\mathrm{C}(B,A)$ such that $$gf=1_A,\quad fg=1_B.$$

---
**Proposition 4.2.** *The inverse of an isomorphism is unique*.  

**Proof.** We have to verify that if both $g_1$ and $g_2:B\rightarrow A$ act as inverses of a given ismorphism $f:A\rightarrow B$, then $g_1=g_2$.  
The standard trick for this kind of verification is to compose $f$ on the left by one of the morphisms, and on the right by the other one; then apply associativity. The whole argument can be compressed into one line: $$g_1=g_11_B=g_1(fg_2)=(g_1f)g_2=1_Ag_2=g_2$$ as needed.  
Note that this argument really proves that if $f$ is a morhpism with a left-inverse $g_1$ and a right inverse $g_2$, then necessarily $f$ is an isomorphism, $g_1=g_2$, and this morphism is the (unique) inverse of $f$.  
Since the inverse of $f$ is uniquely defined by $f$, there is no ambiguity in denoting it by $f^{-1}$. 

---
**Proposition 4.3.** *With notation as above:*  
- *Each identity $1_A$ is an isomorphism and its own inverse*. 
- *If $f$ is an isomorphism, then $f^{-1}$ is an isomorphism and further $(f^{-1})^{-1}=f$.*
- *If $f\in\mathrm{Hom}_\mathrm{C}(A,B),g\in\mathrm{Hom}_\mathrm{C}(B,C)$ are isomorphisms, then the composition $gf$ is an isomorphism and $(gf)^{-1}=f^{-1}g^{-1}$*.

**Proof.** These all 'prove themselves'. For example, it is immediate to verify that $f^{-1}g^{-1}$ is a left-inverse of $gf$: indeed, $$(f^{-1}g^{-1})(gf)=f^{-1}((g^{-1}g)f)=f^{-1}(1_Bf)=f^{-1}f=1_A.$$ The verification that $f^{-1}g^{-1}$ is a right-inverse of gf is anologous.  

---
**Example 4.6.** There are categories in which *every* morphism is an isomorphism, such categories are called *groupoids*.

An *automorphism* of an object $A$ of a category $\mathrm{C}$ is an isomorphism from $A$ to itself. The set of automorphisms of $A$ is denoted $\mathrm{Aut}_\mathrm{C}(A)$; it is a subset of $\mathrm{End}_\mathrm{C}(A)$. Composition cenfers on $\mathrm{Aut}_\mathrm{C}(A)$ a remarkable structure:
- the composition of two elements $f,g\in\mathrm{Aut}_\mathrm{C}(A)$ is an element $gf\in\mathrm{Aut}_\mathrm{C}(A)$;
- composition is associative;
- $\mathrm{Aut}_\mathrm{C}(A)$ contains the element $1_A$, which is an identity for composition (that is, $f1_A=1_Af=f$);
- every element $f\in\mathrm{Aut}_\mathrm{C}(A)$ has an inverse $f^{-1}\in\mathrm{Aut}_\mathrm{C}(A)$. 

In other words, $\mathrm{Aut}_\mathrm{C}(A)$ is a *group*, for all objects $A$ and all categories $\mathrm{C}$.

## 4.2. Monomorphisms and epimorphisms

**Definition 4.7.** Let $\mathrm{C}$ be a category. A morphism $f\in\mathrm{Hom}_\mathrm{C}(Z,A)$ is a *monomorphism* if the following holds:  

*For all objects $Z$ of $\mathrm{C}$ and all morphisms $\alpha',\alpha''\in\mathrm{Hom}_\mathrm{C}(Z,A),f\circ\alpha'=f\circ\alpha''\implies\alpha'=\alpha''.$*

**Definition 4.8.** Let $\mathrm{C}$ be a category. A morphism $f\in\mathrm{Hom}_\mathrm{C}(B,Z)$ is a *monomorphism* if the following holds:  

*For all objects $Z$ of $\mathrm{C}$ and all morphisms $\alpha',\alpha''\in\mathrm{Hom}_\mathrm{C}(B,Z),\beta'\circ f=beta''\circ f\implies\beta'=\beta''.$*

---
## Exercises
4.1 4.2