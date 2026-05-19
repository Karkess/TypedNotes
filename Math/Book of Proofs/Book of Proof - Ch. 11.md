---
title: Book of Proof - Ch. 11

---

# 11.1 - Relations
**Definition 11.1** A **relation** on set $A$ is a subset $R\subseteq A\times A$. We often abbreviate the statement $(x,y)\in R$ as $xRy$. The statement $(x,y)\not\in R$ is abbreviated $x\not Ry$.  

---
# 11.2 - Properties of Relations

**Definition 11.2** Suppose $R$ is a relation on set $A$.  
1. Relation $R$ is **reflexive** if $xRx$ for every $x\in A$. That is, $R$ is reflexive if $\forall x\in A, xRx$.  
2. Relation $R$ is **symmetric** if $\forall x,y\in A, xRy\implies yRx$.  
3. Relation $R$ is **transitive** if $\forall x,y,z\in A,((xRy)\land(yRz))\implies xRz$  

---
# 11.3 - Equivalence Relations

**Definition 11.3** A relation $R$ on a set $A$ is an **equivalence relation** if it is reflexive, symmetric, and transitive.  

---
**Definition 11.4** Suppose $R$ is an equivalence relation on set $A$. Given any element $a\in A$, the equivalence class containing $a$ is the subset $\{x\in A:xRa\}$ of $A$ consisting of all elements of $A$ that relate to $a$. This set is denoted as $[a]$ Thus the equivalence class containing $a$ is the set $[a]=\{x\in A:xRa\}$.  

---
# 11.4 Equivalence Classes and Partitions

**Theorem 11.1** Suppose $R$ is an equivalence relation on set $A$. Suppose also that $a,b\in A$. Then $[a]=[b]$ only if $aRb$.  

---
**Definition 11.5** A **partition** of set $A$ is a set of non-empty subsets of $A$, such that the union of all subsets equals $A$, and the intersection of any two different subsets is $\varnothing$  

---
# 11.5 The integers Modulo n
ooh Cayley tables

**Definition 11.6** Let $n\in\mathbb{N}$. The equivalence classes of the equivalence relation $\equiv\pmod{n}$ are $[0],[1],[2],\dots,[n-1]$.  
The **integers modulo n** is the set $\mathbb{Z}_n=\{[0],[1],[2],\dots,[n-1]\}$. Elements of $\mathbb{Z}_n$ can be added by the rule $[a]+[b]=[a+b]$ and multiplied by the rule $[a]\cdot[b]=[ab]$.  

---
# 11.6 Relations Between Sets

**Definition 11.7** A **relation** from set $A$ to set $B$ is a subset $R\subseteq A\times B$.  

---
