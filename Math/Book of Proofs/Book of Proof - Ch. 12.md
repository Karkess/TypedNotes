---
title: Book of Proof - Ch. 12

---

# 12.1 Functions

**Definition 12.1** Suppose $A$ and $B$ are sets. A **function** $f$ from $A$ to $B$ (denoted as $f:A\rightarrow B$) is a relation $f\subseteq A\times B$ from $A$ to $B$, satisfying the property that for each $a\in A$ the relation $f$ contains exactly one ordered pair of the form $(a,b)$. The statement $(a,b)\in f$ is abbreviated as $f(a)=b$.  

---

**Definition 12.2** For a function $f:A\rightarrow B$, the set $A$ is called the **domain** of $f$. (Think of the domain as the set of possible "input values" for $f$.) The set B is called the **codomain** of $f$. The **range** of $f$ is the set $\{f(a):a\in A\}={b:(a,b)\in f\}$. (Think of range as the set of all possible "output values" for $f$. Think of the codomain as a sort of "target" for the outputs.)  

---
# 12.2 Injective and Surjective Functions

**Definition 12.4** A function $f:A\rightarrow B$ is:
1. **Injective** (or *one-to-one*) if for all $a,a'\in A, a\neq a'\implies f(a)\neq f(a')$.  
2. **Surjective** (or *onto* $B$) if for every $b\in B$ there is an $a\in A$ with $f(a)b$.  
3. **Bijective** if $f$ is both injective and surjective.  

---
# 12.3 The Pigeonhole Principle Revisited
**The Pigeonhole Principle** (function version)  
Suppose $A$ and $B$ are finite sets and $f:A\rightarrow B$ is any function.  
1. If $|A|>|B|$ then $f$ is not injective.  
2. If $|A|<|B|$ then $f$ is not surjective.  

---
# 12.4 Composition
**Definition 12.5** Suppose $f:A\rightarrow B$ and $g:B\rightarrow C$ are functions with the property that the codomain of $f$ equals the domain of $g$. The **Composition** of $f$ with $g$ is another function, denoted $g\circ f$ and defined as follows: If $x\in A$, then $g\circ f(x)=g(f(x))$. Therefore $g\circ f$ sends elements of $A$ to elements of $C$, so $g\circ f:A\rightarrow C$. 

---
**Theorem 12.1** Compositions of functions is associative. That is if $f:A\rightarrow B, g:B\rightarrow C\text{, and }h:C\rightarrow D$, then $(h\circ g)\circ f=h\circ(g\circ f)$.  

**Theorem 12.2** Suppose $f:A\rightarrow B$ and $g:B\rightarrow C$. If both $f$ and $g$ are injective, then $g\circ f$ is injective. If both $f$ and $g$ are surjective, then $g\circ f$ is surjective.  

---
# 12.5 Inverse Functions

**Definition 12.6** For a set $A$, the **identity function** on $A$ is the function $i_A:A\rightarrow A$ defined as $i_A(x)=x\,\,\,\forall\, x\in A$.  

**Definition 12.7** Given a relation $R$ from $A$ to $B$, the **inverse relation** of $R$ is the relationship from $B$ to $A$ defined as $R^{-1}=\{(y,x):(x,y)\in R\}$. In other words, the inverse of $R$ is the relation $R^{-1}$ obtained by interchanging the elements in every ordered pair in $R$.

---
**Theorem 12.3** Let $f:A\rightarrow B$ be a function. Then $f$ is bijective if and only if the inverse function $f^-1$ is a function from $B$ to $A$.  

---
# 12.6 Image and Preimage

**Definition 12.9** Suppose $f:A\rightarrow B$ is a function.  
1. If $X\subseteq A$, the **image** of $X$ is the set $f(X)=\{f(x):x\in X\}\subseteq B$.  
2. If $Y\subseteq B$, the **preimage** of $Y$ is the set $f^{-1}(Y)-\{x\in A:f(x)\in Y\}\subseteq A$.  

---

