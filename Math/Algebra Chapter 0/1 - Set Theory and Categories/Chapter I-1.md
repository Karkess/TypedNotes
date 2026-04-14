---
title: Chapter I-1
tags: [1 - Set Theory and Categories]

---

# Preliminaries: Set Theory and Categories

# 1. Naive set theory

## 1.1. Sets. 

Defines sets as collections of elements.  

Multisets are sets in which elements are allowed to have multiplicity.  

---
A few famous sets:  
- $\emptyset$: The empty set, containing *no* elements;
- $\mathbb{N}$: The set of *natural numbers*;
- $\mathbb{Z}$: The set of *integers*;
- $\mathbb{Q}$: The set of *rational numbers*;
- $\mathbb{R}$: The set of *real numbers*;
- $\mathbb{C}$: The set of *complex numbers*.

---
A few quantifiers:
- $\exists$ means *there exists*... (Existential quantifier)
- $\forall$ means *for all*... (Universal quantifier)
- $\exists!$ means *there exists a unique*...

---
Mathematical statements can be written such as 
$$E=\{a\in\mathbb{Z}\mid(\exists n\in\mathbb{Z})a=2n\}$$can be read as "all integers $a$ such that there exists an integer $n$ for which $a=2n$."  
And can be written in shorthand as $$E=\{2n\mid n\in\mathbb{Z}\}.$$

---
## 1.2 Inclusion of sets

We say that set $S$ is a *subset* of set $T$ if every element of $S$ is an element of $T$, represented as $$S\subseteq T.$$ Logically stated this translates to $$s\in S\implies s\in T.$$
If we have $$S\subseteq T \land T\subseteq S\text{, then }S=T.$$
The cardinality of sets is written as $\lvert S\rvert$, and thus we have the relation if $S$ and $T$ are finite that $$S\subseteq T\implies\lvert S\rvert\le\lvert T\rvert.$$

---
## 1.3 Operations between sets
A list of a few operations between sets
-$\cup$: the *union*;  
-$\cap$: the *intersection*;  
-$\setminus$: the *difference*;  
-$\coprod$: the *disjoint union*;  
-$\times$: the (Cartesian) *product*.  

Two sets are *disjoint* if $S\cap T=\emptyset$.  
The complement of a subset $T$ in a set $S$ is the difference $S\setminus T$.

---
## 1.4 Disjoint unions, products
Roughly speaking, the *disjoint union* of two sets $S\text{ and }T$ is a set $S\coprod T$ obtained by first producing 'copies' $S'\text{ and }T'$ of the sets $S$ and $T$, wit hthe property that $S'\cap T'=\emptyset$.  

*Products* are defined as $$S\times T:=\{(s,t)\mid s\in S,t\in T\}.$$
If $S$ and $T$ are finite sets we have the property $$\lvert S\times T\rvert=\lvert S\rvert\lvert T\rvert.$$
We can extend operations to families, such as $$\bigcap^n_{i=1}S_i=S_1\cap S_2\cap\dots\cap S_n.$$

---
## 1.5 Equvalence relations, partitions, and quotients, oh my!
A relation on a set is defined as a subset $R$ of the product $S\times S$. If $(a,b)\in R$, we say that $a$ and $b$ are related by R, and write $$aRb.$$  

Take for example the building of '=', which corresponds to the 'diagonal' $$\{(a,b)\in S\times S\mid a=b\}=\{(a,a)\mid a\in S\}\subseteq S\times S.$$ Three properties of this relation are very important (For a moment, allow $\sim$ to denote equality):  

-*reflexivity*: $(\forall a\in S)a\sim a$  
-*symmetry*: $(\forall a\in S)(\forall b\in S)a\sim b\implies b\sim a$.  
-*transitivity*: $(\forall a\in S)(\forall b\in S)(\forall c\in S),(a\sim b\text{ and }b\sim c)\implies a\sim c.$  

---
**Definition 1.1** An *equivalence relation* on a set $S$ is any relation $\sim$ satisfying these three properties. (Reflexivity, symmetry, and transitivity)

**Definition 1.2** The *quotient* of the set $S$ *with respect to* the equivalence relation $\sim$ is the set $$S/\sim:=\mathcal{P}\sim$$ of equivalence classes of elements $S$ with respect to $\sim$. 

---
## Exercises

**1.2** Prove that if $\sim$ is an equivalence relation on set $S$, then the corresponding family $\mathcal{P}_\sim$ defined in 1.5 is indeed a partition of $S$: that is, its elements are nonempty, disjoint, and their union is $S$.  

*Proof*. Suppose $\sim$ is an equivalence relation on set $S$. We have equivalence classes $\forall a\in S: [a]_\sim=\{b\in S\mid b\sim a\}$. Our set $\mathcal{P}_\sim=\{[a]_\sim\mid a\in S\}$.  
Nonempty: By definition of reflexivity we have $(\forall a\in S)a\sim a$. This means that $a\in[a]$ and thus all sets are not empty.  
Disjoint: Suppose for the sake of contradiction that $[a]_\sim\cap[b]_\sim\neq\emptyset$. This means that there is an element $x$ for which $x\in[a]$ and $x\in[b]$. This means that $x\sim a$ and $x\sim b$. By transitivity we have $a\sim b$ and by symmetry we have $b\sim a$, so by the definition of equivalence classes we have $[a]=[b]$, meaning all seperate equivalence classes are disjoint.  
Union: $\forall a\in S, a\in[a]_\sim\implies\bigcup\mathcal{P}_\sim=S$.

Had a lot of trouble with Disjoint and needed help there. 

---
**1.3** Given a partition $\mathcal{P}$ on a set $S$, show how to define the relation $\sim$ on $S$ such that $\mathcal{P}$ is the corresponding partition.

A partition on $S$ is a family of *disjoint nonempty* subsets of $S$, *whose union is* $S$. Because our subsets are nonempty, we must have a relation such that $aRa$, for example, $\forall a\in S, a\sim a$. Because the subsets are disjoint, we need similar elements to be defined as a part of the same subset. So if an element $x\in a$ is similar to an element $x\in b$, we should find $a\sim b$ and similarly $b\sim a.$ Since these are related by $x$, we need that if $x\sim a$ and $x\sim b$ that $a \sim b$. Categorizing the relations as $\forall a\in S$ ensures that the union of all subsets in $\mathcal{P}$ is equivalent to $S$. 

My small physics brain read define to mean the same thing as describe. While conceptually solid my work is not a formal definition. The desired solution is just a simple definition of the equivalence of two elements in a single set. Below is the intended solution:
$$a\sim b\iff\{(\exists A\subseteq P)\mid(a\in A)\land(b\in A)\}$$

---
**1.6** Define a relation $\sim$ on the set $\mathbb{R}$ of real numbers by setting $a\sim b\iff b-a\in\mathbb{Z}$. Prove that this is an equivalence relation, and find a 'compelling' description for $\mathbb{R}/\sim$. Do the same for the relation $\approx$ on the plane $\mathbb{R}\times\mathbb{R}$ defined by declaring $(a_1,a_2)\approx(b_1,b_2)\iff b_1-a_1\in\mathbb{Z}$ and $b_2-a_2\in\mathbb{Z}.$

*Proof*. Suppose $\sim$ is a relation on set $\mathbb{R}$. We have the relationship $a\sim b:=b-a\in\mathbb{Z}$. To determine this we analyze the properties of *reflexivity, symmetry, and transitivity*.  
-*Reflexivity*: For any $a\in\mathbb{R}$ we have $a\sim a$ giving $a-a=0\in\mathbb{Z}$, so we have reflexivity.
-*Symmetry*: We have $a\sim b\implies b-a$, so $b\sim a\implies a-b=-(b-a)$. Because $\mathbb{Z}$ is closed under multiplication we have symmetry.  
-*Transitivity*: Let $c\in\mathbb{R}$, then we have $b\sim c=c-b$. Now take $a\sim b= b-a$. Taking $(c-b)+(b-a)=c-a\implies a\sim c$, so we have transitivity as well.
This satisfies all three requirements for $\sim$ to be considered an equivalence relation.
Looking at $\mathbb{R}/\sim$ this leads to a looping as you increase the real numbers from 0 to 1, essentially this is the real numbers mod 1. Geometrically this would be defined as a 'circle'.

The logic is identical for the second relation so I won't bother proving it, but $\mathbb{R}/\approx$ would be $\mathbb{R}^2$ mod 1, which would be like a torus geometrically. 