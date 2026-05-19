---
title: Chapter I-2
tags: [1 - Set Theory and Categories]

---

# 2. Functions between sets

## 2.1. Definition.
Sets interact with each other through *functions*.  
All that can be known about a function can be captured by: *Which element $b$ of $B$ is the image of any given element $a$ of $A$.* $$\Gamma_f:=\{(a,b)\in A\times B\mid b=f(a)\}\subseteq A\times B$$ This set $\Gamma_f$ *together with* information of source $A$ and target $B$ is the **graph** of $f$.  
For this subset to be defined as a graph/function it must follow the following rule:$$(\forall a\in A)(\exists!b\in B)\quad(a,b)\in\Gamma_f$$
Note that this definition excludes multivalued functions, such as $\pm\sqrt{x}$.  
Labeling a variable as a function one can write $f: A\rightarrow B$, or $$A\xrightarrow{\quad f\quad}B.$$ The action of a function $f:A\rightarrow B$ on an element $a\in A$, can be represented as $a\mapsto f(a)$.  
Every set has an identity graph which is diagonal in $A\times A$:$$\mathrm{id}_A:A\rightarrow A$$ defined as $(\forall a\in A)\,\mathrm{id}_A(a)=a$.  
The collection of all functions from set $A$ to set $B$ is itself a set, denoted $B^A$.  

The inclusion of any subset $S$ of a set $A$ determines a function $S\rightarrow A$, simply by send every element $s$ of $S$ to 'itself' in $A$, denoted $$f(S):=\{b\in B\mid(\exists a\in S)b=f(a)\}.$$ That is, f(S) is the subset of $b$ consisting of all elements that are images of elements of $S$ by the function $f$.  
The largest such subset, f(A), is called the *image of* $f$, denoted '$\mathrm{im}\,f$'.  
Also, $f\mid_S$ denotes the 'restriction' of $f$ to the subset $S$: This is the function $S\rightarrow B$ defined by $$\forall s\in S):f\mid_S(s)=f(s).$$

## 2.2. Examples: Multisets, indexed sets.

Multisets can be seen as a mapping $m:A\rightarrow\mathbb{N}^*$, with $m(a)$ representing how many times the element appears in the set. 

Indexing of sets, such as $a_1, a_2,\dots, a_n$ is also a function. It says "consider a function $a:\{1,2,\dots,n\}\rightarrow\mathbb{Z}$, where it is understood that $a_i$ is simply shorthand.  

## 2.3. Composition of functions.
Functions may be *composed*: if $f: A\rightarrow B$ and $g:B\rightarrow C$, then the operation $g\circ f$ is defined by $$(\forall a\in A)\quad(g\circ f)(a):=g(f(a)).$$
Composition is associative, that is, if $f:A\rightarrow B, g:B\rightarrow C\text{, and }h:C\rightarrow D$ are function, then $h\circ(g\circ f)=(h\circ g)\circ f$.

## 2.4. Injections, surjections, bijections.
- A function $f:A\rightarrow B$ is *injective* if $$(\forall a'\in A)(\forall a''\in A) a'\neq a''\implies f(a')\neq f(a'').$$
- A function $f:A\rightarrow B$ is *surjective* if$$(\forall b\in B)(\exists a \in A)\quad b=f(a).$$
- If $f$ is *both* injective **and** surjective, we call it *bijective*.

Injective is often written as $\rightarrowtail$ and surjective is often written as $\twoheadrightarrow$. Bijective is frequently shown as $\xrightarrow{\sim}$, and we call the two sets 'isomorphic' sets, or say *an isomorphism* of sets.

Using this new definition the 'copies' A' and B' of A and B we discussed in 1.3 are *isomorphic* sets to A and B.
## 2.5. Injections, surjections, bijections: Second viewpoint.
If a function is bijective, we can define an inverse.
Additionally, if a function has an inverse, it has a bijection. More precisely:

**Proposition 2.1.** *Assume $A\neq\emptyset$, and let $f:A\rightarrow B$ be a function. Then  
(1) $f$ has a left inverse if and only if it is injective.  
(2) $f$ has a right inverse if and only if it is surjective.  

---
**Proof** For (1).  
$(\implies)$ If $f:A\rightarrow B$ has a left inverse, then there exists a $g: B\rightarrow A$ such that $g\circ f=\mathrm{id}_A$. Now assume that $a'\neq a''$ are arbitrary different elements in $A$, then $$g(f(a'))=\mathrm{id}_A(a')=a'\neq a''=\mathrm{id}_A(a'')=g(f(a''));$$ that is, $g$ sends $f(a')$ and $f(a'')$ to different elements. This forces $f(a')$ and $f(a'')$ to be different, showing that $f$ is injective. 

$(\impliedby)$ Now assume that $f:A\rightarrow B$ is injective. In order to construct a function $g:B\rightarrow A$, we have to assign a unique value $g(b)\in A$ for each element $b\in B$. For this, choose any fixed element $s\in A$ (which we can do because $A\neq\emptyset$), then set 
$$
g(b) :=
\begin{cases}
a & \text{if }b=f(a)\text{ for some }a\in A,\\
s & \text{if }b\in\mathrm{im}f.
\end{cases}
$$
In words, if $b$ is the image of an element $a$ of $A$, send it back to $a$; otherwise, send it to your fixed element $s$.  

The given assignment defined a function, precisely because $f$ is injective: indeed, this guarantees that every $b$ that is the image of some $a\in A$ by $f$ is the image of a *unique* $a$ (two distinct elements of $A$ cannot be simultaneously sent to $b$ by $f$, since $f$ is injective). Thus, every $b\in B$ is sent to a unique well-defined element of $A$, as is required of functions.  

Finally, the function $g:B\rightarrow A$ is a left-inverse of $f$. Indeed, if $a\in A$, then $b=f(a)$ is of the first type, so it is sent back to $a$ by $g$; that is, $g\circ f(a)=a=\mathrm{id}_A(a)$ for all $a\in A$, as needed.  

--- 
**Corollary 2.2** A *function* $f:A\rightarrow B$ is a *bijection if and only if it has a (two sided) inverse.*

---
The standard notation for *the* inverse of a bijection $f$ is $f^-1$, but can also be used in a slightly different context. Here, $$f^-1(T)=\{a\in A\mid f(a)\in T\}.$$

---
## 2.6. Monomorphisms and epimorphisms.
A function is a *monomorphism* (or *monic*) if the following holds:$$\text{for all sets }Z\text{ and all functions }\alpha',\alpha'':Z\rightarrow A$$ $$f\circ \alpha'=f\circ \alpha''\implies \alpha'=\alpha''$$

---
**Proposition 2.3.** A function is *injective* if and only if it is a *monomorphism*. 

**Proof**. ($\implies$) By Proposition 2.1, if a function $f:A\rightarrow B$ is injective, then it has a left-inverse $g:B\rightarrow A$. Now assume that $\alpha',\alpha''$ are arbitrary functions from another set $Z$ to $A$ and that $$f\circ\alpha'=f\circ\alpha'';$$ compose on the left by $g$, and use the associativity of composition: $$(g\circ f)\circ\alpha'=g\circ(f\circ\alpha')=g\circ(f\circ\alpha'')=(g\circ f)\circ\alpha''$$ since $g$ is the left inverse of $f$, this says $$\mathrm{id}_A\circ\alpha'=\mathrm {id}_A\circ\alpha''$$ and therefore $$\alpha'=\alpha''.$$ as needed to conclude that $f$ is a monomorphism.  

($\impliedby$) Now assume that $f$ is a monomorphism. This says something about arbitrary sets $Z$ and arbitrary functions $Z\rightarrow A$; we are going to use a microscopic portion of this information, choosing $Z$ to be any singleton $\{p\}$. Then assigning functions $\alpha',\alpha'':Z\rightarrow A$ amounts to choosing which elements $a'=\alpha'(p),a''=\alpha''(p)$ we should send the single element $p$ of $Z$. For this particular choice of $Z$, the property defining monomorphisms, $f\circ\alpha'=f\circ\alpha''\implies\alpha'=\alpha''$, becomes $$f\circ\alpha'(p)=f\circ\alpha''(p)\implies\alpha'=\alpha'',$$that is, $$f(a')=f(a'')\implies\alpha'=\alpha''.$$
Now two functions from $Z=\{p\}$ to $A$ are equal if and only if they send $p$ to the same element, so this says $$f(a')=f(a'')\implies a'=a''.$$ This has to be all true for all $\alpha',\alpha''$, that is, for all choices of distinct $a',a''$ in $A$. In other words, $f$ has to be injective, as was to be shown. $\blacksquare$

---
The similar definition to *monomorphism* and proof for surjective functions is left as an exercise to the reader and is called an *epimorphism*. 

## 2.7. Basic Examples.
**Example 2.4.** Let $A,B$ be sets. Then there are *natural projections* $\pi_A,\pi_B$.$$A\times B\xrightarrow{\pi_A}A,$$ $$A\times B\xrightarrow{\pi_B}B.$$ defined by $$\pi_A((a,b)):=a,\quad\pi_B((a,b)):=b$$ for all $(a,b)\in A\times B$. Both of these maps are (clearly) surjective.

---
**Example 2.5.** Similarly there are natural injections from $A$ and $B$ to the disjoint union $$A\hookrightarrow A\coprod B$$ $$B\hookrightarrow A\coprod B$$ obtained by sending $a\in A$ and $b\in B$ to the corresponding element in the isomorphic copy $A'$ of $A$ and $B'$ of $B$ in $A\coprod B$.

---
**Example 2.6.**
If $\sim$ is an equivalence relation on set $A$, then there is a (clearly surjective) canonical projection$$A\twoheadrightarrow A/\sim$$ obtained by sending every $a\in A$ to its equivalence class $[a]_\sim$ .

## 2.8 Canonical decomposition
The significance of injective and surjective maps is that they are the structures that any functions can be constructed from.  

Observe that if every function $f:A\rightarrow B$ determines an equivalence relation $\sim$ on $A$: for all $a',a''\in A$, $$a'\sim a''\iff f(a')=f(a'').$$

---
**Theorem 2.7.** *Let $f:A\rightarrow B$ be any function, and define $\sim$ as above. Then $f$ decomposes as follows:* $$A\xrightarrow{f} B$$ $$A\twoheadrightarrow(A/\sim)\xrightarrow{\sim}_f\mathrm{im}f\hookrightarrow B$$ *where the first function is the canonical projection $A\rightarrow A/\sim$ (as in Example 2.6), and third function is the inclusion $\mathrm{im}\,f\subseteq B$, and the bijection $\tilde{f}$ in the middle is defined by* $$\tilde{f}([a]_\sim):=f(a)$$ *for all* $a\in A$.  

To verify we need to prove
-that formula *does* define a function;
-that function is in fact a bijection.  

---
**Proof.** Spelling out the first item discussed above, we have to verify that, for all $a',a''$ in $A$, $$[a']_\sim=[a'']_\sim\implies f(a')=f(a'').$$ Now $[a']_\sim=[a'']_\sim$ , means that $a'\sim a''$, and the definition of $\sim$ has been engineered precisely so that this would mean $f(a')=f(a'')$ as required here. So $\tilde{f}$ is indeed well-defined.  

To verify the second item, that is, that $\tilde{f}:A/\sim\rightarrow\mathrm{im}\,f$ is a bijection, we check explicitly that $\tilde{f}$ is injective and surjective.  
*Injective*: If $\tilde{f}([a']_\sim)=\tilde{f}([a'']_\sim)$, then $f(a')=f(a'')$ by definition of $\tilde{f}$; hence $a'\sim a''$ by the definition of $\sim$, and then $[a']_\sim=[a'']_\sim$ . Therefore $$\tilde{f}([a']_\sim)=\tilde{f}([a'']_\sim)\implies[a']_\sim=[a'']_\sim$$ proving injectivity. 
*Surjective*: Given any $b\in\mathrm{im}\,f$, there is an element $a\in A$ such that $f(a)=b$, Then $$\tilde{f}([a]_\sim)=f(a)=b$$ by definition of $\tilde{f}$. Since $b$ was arbitrary in $\mathrm{im}\,f$, this shows that $\tilde{f}$ is surjective, as needed. $\blacksquare$

## 2.9. Clarification
When considering disjoint unions $A\coprod B$ there are many choices for acceptable candidates for what could constitute this set, so instead we take it as a not well defined set and say that it is well-defined up to an isomorphism of $A,B$. 

## Exercises
Do: 2.1 2.2 2.4 2.5 2.9 2.10 2.11

---
2.1