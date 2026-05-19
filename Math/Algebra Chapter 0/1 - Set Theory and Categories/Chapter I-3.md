---
title: Chapter I-3
tags: [1 - Set Theory and Categories]

---

# 3. Categories
Categories are affectionately called *abstract nonsense*, and can be considered the study of *things, and things that go from things to things*. 

Categories at a first glance look like sets, and have things that look like functions, called *functors*. 

## 3.1. Definition.
The definition of categories looks complicated at first, but can be summarized as a collection of 'objects' and of 'morphisms' between these objects, satisfying some natural conditions.  

---
**Definition 3.1.** A *category* $\mathcal{C}$ consists of  
- a class $\mathrm{Obj}(\mathcal{C})$ of *objects* of the category; and
- for every two objects $A,B$ of $\mathcal{C}$, a set $\mathrm{Hom}_\mathcal{C}(A,B)$ of *morphisms*, with the properties listed below:  
- For every object $A$ of $\mathcal{C}$, there exists (at least) one morphism $1_A\in\mathrm{Hom}_\mathcal{C}(A,A)$, the 'identity' on $A$. 
- One can compose morphisms: two morphisms $f\in\mathrm{Hom}_\mathcal{C}(A,B)$ and $g\in\mathrm{Hom}_\mathcal{C}(B,C)$ determine a morphism $gf\in\mathrm{Hom}_\mathcal{C}(A,C)$.That is, for every triplet of objects $A,B,C$ of $\mathcal{C}$ there is a function (of sets)$$\mathrm{Hom}_\mathcal{C}(A,B)\times\mathrm{Hom}_\mathcal{C}(B,C)\rightarrow\mathrm{Hom}_\mathcal{C}(A,C),$$and the image of the pair $(f,g)$ denoted $gf$. 
- This 'composition law' is associative: if $f\in\mathrm{Hom}_\mathcal{C}(A,B),g\in\mathrm{Hom}_\mathcal{C}(B,C)\text{, and }f\in\mathrm{Hom}_\mathcal{C}(C,D)$, then $$(hg)f=h(gf).$$
- The identity morphisms are identities with respect to composition: That is, for all $f\in\mathrm{Hom}_\mathcal{C}(A,B)$ we have $$f1_A=f,\quad1_Bf=f.$$

---
To remember all this, just think of functions of sets. There is an additional requirement that $$\mathrm{Hom}_\mathcal{C}(A,B),\quad\mathrm{Hom}_\mathcal{C}(C,D)$$ be *disjoint* unless $A=C,\:B=D$. 

A morphism of an object $A$ of a category $C$ to itself is called an *endomorphism*; $\mathrm{Hom}_\mathcal{C}(A,A)$ is denoted $\mathrm{End}_\mathcal{C}(A)$. 

## 3.2 Examples.

**Example 3.2.**  
We will take $\mathrm{Set}$ as an example of how to represent categories: 
- $\mathrm{Obj(Set)}=$ the class of all sets.
- for $A,B$ in $\mathrm{Obj(Set)}$ (That is, for $A,B$ sets) $\mathrm{Hom}_\mathrm{Set}(A,B)=B^A$.

---
**Example 3.3.** A different example  
Suppose $S$ is a set and $\sim$ is a relation on $S$ satisfying the reflexive and transitive properties. Then we can encode this data into a category:
- *objects*: the elements of $S$;
- *morphisms*: if $a,b$ are objects (that is, if $a,b\in S$), then let $\mathrm{Hom}(a,b)$ be the set containing the element $(a,b)\in S\times S$ if $a\sim b$, and let $\mathrm{Hom}(a,b)=\emptyset$ otherwise.

---
**Example 3.4.** Another small category  
Let $\mathrm{S}$ be a set. Define a category $\hat{\mathrm{S}}$ by setting
- $\mathrm{Obj(\hat{\mathrm{S}})}=\mathcal{P}(S)$, the power set $S$;
- for $A,B$ objects of $\hat{\mathrm{S}}$ (that is $A\subseteq B$ and $B\subseteq S$) let $\mathrm{Hom}_\hat{\mathrm{S}}(A,B)$ be the pair $(A,B)$ if $A\subseteq B$, and let $\mathrm{Hom}_\hat{\mathrm{S}}=\emptyset$ otherwise.

---
**Example 3.5.** An abstract but important example.  
Let $\mathrm{C}$ be a category, and let $A$ be an object of $\mathrm{C}$. We are going to define a category $\mathrm{C}_A$ whose objects are certain *morphisms* in $\mathrm{C}$, and whose morphisms are certain *diagrams* of $\mathrm{C}$. 
- $\mathrm{Obj}(\mathrm{C}_A)=$ all morphisms from any object of $\mathrm{C}$ to $A$; thus, an object of $\mathrm{C}_A$ is a morphism $f\in\mathrm{Hom}_\mathrm{C}(Z,A)$ for some object $Z$ of $C$. Pictorially, an object of $\mathrm{C}_A$ is an arrow $Z\xrightarrow{f}A$ in $\mathrm{C}$; these are often drop 'top-down'. 

---
**Example 3.6.** Applying 3.5's construction to 3.3.  
Say, for $S=\mathbb{Z}$ and $\sim$ the relation $\le$. Call $\mathrm{C}$ this category, and choose an object $A$ of $\mathrm{C}$-that is, an integer, for example $A=3$. Then the objects of $\mathrm{C}_A$ are morphisms in $\mathrm{C}$ with a target 3, that is, pairs $(n,3)\in\mathbb{Z}\times\mathbb{Z}$ with $n\le 3$. There is a morphism $$(m,3)\rightarrow(n,3)$$ if and only if $m\le n$. In this case, $\mathrm{C}_A$ may harmlessly be identified with the 'subcategory' of integers $\le3$, with 'the same' morphism as in $\mathrm{C}$. 

---
**Example 3.7.** This literally says to do an exercise. That's hardly an example, dick.

---
**Example 3.8.** An actual example of example 3.7.  
Let $\mathrm{C}=\mathrm{Set}$ and $A=$ a fixed singleton $\{*\}$. Call the resulting category $\mathrm{Set}^*$.   
An object in $\mathrm{Set}^*$ is then a morphism $f:\{*\}\rightarrow S$ in $\mathrm{Set}$, where $S$ is any set. The information in $\mathrm{Set}^*$ consists therefore of the choice of a nonempty set $S$ *and* of an element $s\in S$-that is, the element $f(*)$: this element determines, and is determined by, $f$.  
Thus, we may denote objects of $\mathrm{Set}^*$ as pairs $(S,s)$, where $S$ is any set and $s\in S$ is any element of $S$.  
A morphism between two such objects, $(S,s)\rightarrow(T,t)$, corresponds then to a set-function $\sigma:S\rightarrow T$ *such that* $\sigma(s)=t$  

Objects of $\mathrm{Set}^*$ are called 'pointed sets'. 

---
**Example 3.9.** Graphical (or maybe 'diagrammatical' would be more accurate?), which I am unable to reproduce here. It is quite a good example though. Worth looking at.  

---
**Example 3.10.** This seems like kind of a 'level-up' from 3.9, in terms of abstraction. Like, the objects of 3.10 are now the morphisms of 3.9, and morphisms for 3.10 now go between morphisms of 3.9, if that makes sense. It says this is how to check if you really understood, but I am not even sure what really understands means at this stage. To me it seems like an identical construction that only changes when we unpack objects. 

## Exercises
3.1 3.3 3.5 3.6 3.7 3.8 3.9 3.11

---