---
title: Chapter 1 - Vector Spaces.

---

# Chapter 1 - Vector Spaces
## 1.A $\mathbb{R}^n$ and $\mathbb{C}^n$
### Complex Numbers
**Definition 1.1** *Complex Numbers*
- A *complex number* is an ordered pair (a,b), where $a,b\in\mathbb{R}$, such that they represent $a+bi$. 
- The set of all complex numbers is denoted by $\mathbb{C}$:$$\mathbb{C}=\{a+bi:a,b\in\mathbb{R}\}.$$
- Addition and multiplication are defined on $\mathbb{C}$ as: $$(a+bi)+(c+di)=(a+c)+(b+d)i,$$ $$(a+bi)(c+di)=(ac-bd)+(ad+bc)i,$$ where $a,b,c,d\in\mathbb{R}$. 

---
***1.3 Properties of Complex Arithmetic***
**Commutativity** $$\alpha+\beta=\beta+\alpha\text{ and }\alpha\beta=\beta\alpha\text{ for all }\alpha\beta\in\mathbb{C};$$
**Associativity** $$(\alpha+\beta)=+\lambda=\alpha+(\beta+\lambda)\text{ and }(\alpha\beta)\lambda=\alpha(\beta\lambda)\text{ for all }\alpha,\beta,\lambda\in\mathbb{C};$$
**Identities** $$\lambda+0=\lambda\text{ and }\lambda 1=\lambda\text{ for all }\lambda\in\mathbb{C};$$
**Additive Inverse** $$\text{for every }a\in\mathbb{C}\text{, there exists a unique }\beta\in\mathbb{C}\text{ such that }\alpha+\beta=0;$$
**Multiplicative Inverse**$$\text{for every }a\in\mathbb{C}\text{ with }\alpha\neq0\text{, there exists a unique }\beta\in\mathbb{C}\text{ such that }\alpha\beta=1;$$
**Distributive Property**$$\lambda(\alpha+\beta)=\lambda\alpha+\lambda\beta\text{ for all }\lambda,\alpha,\beta\in\mathbb{C}.$$

---
**1.5 Definition** *$-\alpha,$ subtraction, $1/\alpha,$ division*
*Let $\alpha,\beta\in\mathbb{C}$*
- Let $-\alpha$ denote the additive inverse of $\alpha$. Thus, $-\alpha$ is the unique complex number such that $$\alpha+(-\alpha)=0.$$
- **Subtraction** on $\mathbb{C}$ is defined by $$\beta-\alpha=\beta+(-\alpha).$$
- For $\alpha\neq0$, let $1/\alpha$ denote the multiplicative inverse of $\alpha$. Thus $1/\alpha$ is the unique complex number such that $$\alpha(1/\alpha)=1.$$
- **Division** on $\mathbb{C}$ is defined by $$\beta/\alpha=\beta(1/\alpha).$$

---
**1.6 Notation** $\mathbb{F}$
We will use $\mathbb{F}$ to stand for either $\mathbb{R}$ or $\mathbb{C}$.

This notation comes from the fact that both $\mathbb{R} and $\mathbb{C}$ are *Fields*, denoted by $\mathbb{F}$. 

---
### Lists

**1.7 Example** $\mathbb{R}^2$ and $\mathbb{R}^3$.
- The set $\mathbb{R}^2$, which you can thinko f as a plane, is the set of all ordered pairs of real numbers: $$\mathbb{R}^2=\{(x,y):x,y\in\mathbb{R}\}.$$
- The set $\mathbb{R}^3$, which you can think of as ordinary space, is the set of all ordered triples of real numbers: $$\mathbb{R}^3=\{(x,y,z):x,y,z\in\mathbb{R}\}.$$

---
**1.8 Definition** *list, length*
Suppose $n$ is a nonnegative integer. A ***list*** of ***length*** $n$ is an ordered collection of $n$ elements seperated by commas and surrounded by parentheses. A list of length $n$ looks like: $$(x_1,\dots,x_n).$$ Two lists are equal if and only if they have the same length and elements in the same order.

*many mathematicians call a list of length $n$ an $n$-tuple.* 

---
### $\mathbb{F}^n$

**1.10 Definition** $\mathbb{F}^n$
$\mathbb{F}^n$ is the set of all lists of length $n$ of elements of $\mathbb{F}$: $$\mathbb{F}^n=\{(x_1,\dots,x_n):x_j\in\mathbb{F}\text{ for }j=1,\dots,n\}.$$ For $(x_1,\dots,x_n)\in\mathbb{F}^n$ and $j\in\{1,\dots,n\}$, we say that $x_j$ is the $j^\text{th}$ *coordinate* of $(x_1,\dots,x_n)$.

---
**1.12 Definition** *addition in $\mathbb{F}^n$.*
*Addition* in $\mathbb{F}^n$ is defined by adding corresponding coordinates: $$(x_1,\dots,x_n)+(y_1,\dots,y_n)=(x_1+y_1,\dots,x_n+y_n).$$

If $x,y\in\mathbb{F}^n$, then $x+y=y+x$. 

---
**1.14 Definition** $0$
Let $0$ denote a list of length $n$ whose coordinatesare all $0$:$$0=(0,\dots,0).$$

---
**1.16 Definition** *additive inverse in* $\mathbb{F}^n$. 
For all $x\in\mathbb{F}^n$, the *additive inverse* of $x$, denoted $-x$, is the vector $-x\in\mathbb{F}^n$ such that $$x+(-x)=0.$$ In other words, if $x=(x_1,\dots,x_n), then $-x=(-x_1,\dots,-x_n).$

---
**1.17 Definition** *scalar multiplication in* $\mathbb{F}^n$. 
The *product* of a number $\lambda$ and a vector in $\mathbb{F}^n$ is computed by multiplying each coordinate of the vector by $\lambda$: $$\lambda(x_1,
dots,x_n)=(\lambda x_1,\dots,\lambda x_n);$$here $\lambda\in\mathbb{F}$ and $(x_1,\dots,x_n)\in\mathbb{F}^n$. 

---
### Digression on Fields
A *Field* is a set containing at least two distinct elements called 0 and 1 along with all properties listed in 1.3. We will primarily deal with $\mathbb{R}$ and $\mathbb{C}$ here, but in general most theorems covered hold for all arbitrary fields.

---
### Exercises 1.A
Many exercises in this book will be done on paper, but I will knock out some here. 

1. Suppose $a$ and $b$ are real numbers, not both $0$. Find real numbers $c$ and $d$ such that $$1/(a+bi)=c+di.$$
**Solution:**
$$\begin{aligned}
\frac{1}{a+bi}&=c+di\\
\frac{1}{a+bi}\cdot\frac{a-bi}{a-bi}&=
\frac{a-bi}{a^2+b^2}\\
&=\frac{a}{a^2+b^2}-\frac{bi}{a^2+b^2}\\
\frac{1}{a+bi}&=\frac{a}{a^2+b^2}-\frac{bi}{a^2+b^2}\\
\text{Therefore,}\\
c&=\frac{a}{a^2+b^2}\\
d&=\frac{b}{a^2+b^2}
\end{aligned}$$
---
2. Show that $$\frac{-1+\sqrt{3}i}{2}$$ is the cube root of 1.
**Solution:**
$$\begin{aligned}\frac{-1+\sqrt{3}i}{2}\frac{-1+\sqrt{3}i}{2}&=\frac{(-1+\sqrt{3}i)(-1+\sqrt{3}i)}{4}\\&=\frac{1+3i^2-2\sqrt{3}i}{4}\\&=\frac{-(2+2\sqrt{3}i)}{4}\\&=\frac{-1-\sqrt{3}i}{2}\\\frac{-1-\sqrt{3}i}{2}\frac{-1+\sqrt{3}i}{2}&=\frac{(-1-\sqrt{3}i)(-1+\sqrt{3}i)}{4}\\&=\frac{1-3i^2+\sqrt{3}i-\sqrt{3}i}{4}\\&=\frac{1-3i^2}{4}\\&=\frac{1+3}{4}\\\left(\frac{-1+\sqrt{3}i}{2}\right)^3&=\frac{4}{4}\\\left(\frac{-1+\sqrt{3}i}{2}\right)^3&=1\quad\blacksquare \end{aligned}$$

---
## 1.B Definition of Vector Space

**1.18 Definition** *addition, scalar multiplication*
- An *addition* on a set $V$ is a function that assigns an element $u+v\in V$ to each pair of elements $u,v\in V$. 
- A *scalar multiplication* on a set $V$ is a function that assigns an element $\lambda v\in V$ to each $\lambda\in\mathbb{F}$ and each $v\in V$. 

---
**1.19 Definition** *vector space*
A *vector space* is a set $V$ along with an addition on $V$ and scalar multiplication on $V$ such that the following properties hold:

**commutativity** $$u+v=v+u\text{ for all }u,v\in V;$$
**associativity** $$(u+v)+w=u+(v+w)\text{ and }(ab)v=a(bv)\text{ for all }u,v,w\in V\text{ and all }a,b,\in\mathbb{F};$$
**additive identity** $$\text{there exists an element }0\in V\text{ such that }v+0=v\text{ for all }v\in V;$$
**additive inverse** $$\text{for every }v\in V\text{, there exists }w\in V\text{ such that }v+w=0;$$
**multiplicative identity** $$1v=v\text{ for all }v\in V;$$
**distributive properties**$$a(u+v)=au+av\text{ and }(a+b)v=av+bv\text{ for all }a,b\in\mathbb{F}\text{ and all }u,v\in V.$$

---
**1.20 Definition** *vector, point*
Elements of a vector space are called *vectors* or *points*. 

---
**1.22 Definition** *real vector space, complex vector space*
- A vector space over $\mathbb{R}$ is called a *real vector space*. 
- A vector space over $\mathbb{C}$ is called a *complex vector space*. 

---
**1.23 Notation** $\mathbb{F}^S$
- If $S$ is a set, then $\mathbb{F}^S$ denotes the set of functions from $S$ to $\mathbb{F}$. 
- For $f,g\in\mathbb{F}^S$, the *sum* $f+g\in\mathbb{F}^S$ is the function defined by $$(f+g)(x)=f(x)+g(x)$$ for all $x\in S$.
- For $\lambda\in\mathbb{F}$ and $f\in\mathbb{F}^S^, the *product* $\lambda f\in\mathbb{F}^S% is the function defined by $$(\lambda f)(x)=\lambda f(x)$$ for all $x\in S$. 

---
**1.25 Unique Additive Identity** 
A vector space has a unique additive identity.

*Proof*: Suppose $0$ and $0'$ are both additive identities for some vector space $V$, then $$0'=0'+0=0+0'=0,$$ where the first equality holds because $0$ is the additive identity, the second equality comes from commutativity, and the third equality holds because $0'$ is an additive identity. Thus $0'=0$, proving that $V$$ has only one additive identity. $\quad\blacksquare$

---
**1.26 Unique Additive Inverse**
Every element in a vector space has a unique additive inverse. 

*Proof*: Suppose $V$ is a vector space. Let $v\in V$. Suppose $w$ and $w'$ are additive inverse of $v$, then, $$w=w+0=w+(v+w')=(w+v)+w'=0+w'=w'.$$ Thus $w=w'$, as desired. $\quad\blacksquare$

---
**1.27 Notation** $-v,w-v$
Let $v,w\in V$, then,
- $-v$ denotes the additive inverse of $v$;
- $w-v$ is defined to be $w+(-v)$. 

**1.28 Notation** $V$
For the rest of the book, $V$ denotes a vector space over $\mathbb{F}$. 

---
### Exercises 1.B
1. Prove that $-(-v)=v$ for every $v\in V$. 

**Solution:**
*Proof*: For $v\in V$, we have: $(-v)$ defined as the additive inverse: $(-v)+v=0$, by definition, $-(-v)$ must be the additive inverse of $-v$, ie, $-(-v)+(-v) = 0$. From uniqueness in the vector space $V$ we see that $-(-v)$ is $v.\quad\blacksquare$

## 1.C Subspaces
**1.32 Definition** *subspace*
A subset $U$ of $V$ is called a *subspace* of $V$ if $U$ is also a vector space (using the same addition and scalar).

**1.34** Conditions for a subspace
A subset $U$ of $V$ is a subspace if and only if $U$ satisfies the following three conditions:

**additive identity** $$0\in U$$ **closed under addition** $$u,w\in U\text{ implies }u+w\in U;$$ **closed under scalar multiplication** $$a\in\mathbb{F}\text{ and }u\in U\text{ implies }au\in U.$$

---
### Sums of Subspaces
**1.36 Definition** *sum of subsets*
Suppose $U_1,\dots,U_m$ are subsets of $V$. The **sum** of $U_1,\dots,U_m$, denoted $U_1+\cdots+U_m=\{u_1+\cdots+u_m:u_1\in U_1,\dots,u_m\in U_m\}.$

[I like this box so I'm including it]
*Sums of subspaces in the theory of vector spaces are analogous to unions of subsets in set theory. Given two subspaces of a vector space, the smallest subspace containing them is their sum. Analogously, given two subsets of a set, the smallest subset containing them is their union*. 

---
### Direct Sums

**1.40 Definition** *direct sum*
Suppose $U_1,\dots,U_m$ are subspaces of $V$.
- The sum $U_1+\cdots+U_m$ is called a *direct sum* if each element of $U_1+\cdots+U_m$ can be written in only one way as a sum of $u_1+\cdots+u_m$, where each $u_j$ is in $U_j$. 
- If $U_1+\cdots+U_m$ is a direct sum, then $U_1\oplus\cdots\oplus U_m$ denotes $U_1+\cdots+U_m$, with the $\oplus$ notation serving as an indication that this is a direct sum. 

---
**1.44 Condition for a direct sum**
Suppose $U_1,\dots,U_m$ are subspaces of $V$. Then $U_1+\cdots+U_m$ is a direct sum if and only if the only way to write $0$ as a sum $u_1+\cdots+u_m$, where each $u_j$ is in $U_j$, is by taking each $u_j$ equal to $0$.

These definitions all feel somewhat obfuscating to me, although I suppose that is necessary for technical precision. Essentially to me it seems that the direct sum is only possible when no coordinates are shared aside from 0. So no (x,0) and (x,y), but (0,y) and (x,0) are fine. 

**Direct sum of two subspaces**
Suppose $U$ and $W$ are subspaces of $V$. Then $U+W$ is a direct sum if and only if $U\cap W=\{0\}$.

Alright I'm sorry Axler, this is a fantastic definition and I should have read one more paragraph before being critical. Although this did change my understanding, as I thought the empty set was an acceptable intersection from the prior definitions, but this is restricted by the definition of spaces that direct sums operate on. 

---
### Exercises 1.C
1. For each of the following subsets of $\mathbb{F}^3$, determine whether or not it is a subspace of $\mathbb{F}^3$. 

a) $\{(x_1,x_2,x_3)\in\mathbb{F}^3:x_1+2x_2+3x_3=0\};$ Yes
b) $\{(x_1,x_2,x_3)\in\mathbb{F}^3:x_1+2x_2+3x_3=4\};$ No, $(0,0,0)\neq0$
c) $\{(x_1,x_2,x_3)\in\mathbb{F}^3:x_1x_2x_3=0\};$ No, fails to be closed under addition.
d) $\{(x_1,x_2,x_3)\in\mathbb{F}^3:x_1=5x_3\};$ Yes

5. Is $\mathbb{R}^2$ a subspace of $\mathbb{C}^2$. 

I got this one wrong, my gut said yes. However, $i$ is a scalar in $\mathbb{C}^2$ and thus $\mathbb{R}^2$ isn't closed under scalar multiplication. My second gut reaction was that this isn't closed under scalar addition either, but this isn't geometric algebra. Scalar addition to vectors is not a thing in vector spaces. 

20. Suppose $$U=\{(x,x,y,y)\in\mathbb{F}^4:x,y\in\mathbb{F}\}$$ Find a subspace $W$ of $\mathbb{F}^4$ such that $\mathbb{F}^4=U\oplus W$. 

As long as $W$ does not contain any non-zero vectors of the form {(a,a,b,0)} or {(a,0,b,b)} and $W$ is of dimension $2$. 

24. Says to prove that even functions $U_e$ and odd functions $U_o$ form the space: $U_e\oplus U_o=\mathbb{R}^\mathbb{R}$. 

I'm not sure how exactly to do this and I probably could with time, but I don't have time to linger. However, the very concept was so interesting I thought it was worth writing down. $\mathbb{R}^\mathbb{R}$ is hard for me to wrap my mind around. Is this like the Hilbert spaces we work in, in quantum mechanics in a way? Where we construct an infinite dimensional vector space out of complex values functions? Would that be $\mathbb{C}^\mathbb{C}$? Or some infinite chain? How would I write that... $\mathbb{C}^{\mathbb{C}^\ddots}$ Apparently udots isn't default. 

Apparently I am wrong (According to all-knowing chatGPT), so the Hilbert space is a subset of $\mathbb{C}^\mathbb{R}$, it's not a tiered thing. This is infinite dimensional, which I guess is obvious if I think about it in the form of like $\mathbb{C}^2$ being four dimensional (a+bi) and (c+di), 4 variables. Got lost in the sauce trying to conceptualize R^R. 

This is still hard for me to conceptualize. Does C^Cmean anything? I guess so, complex to complex mappings? does $C^{C^C}?\: C^{C^\text{udots}}?$

Apparetly I should think of $C^{C^C}$ as a mapping of a complex function to complex functions with complex function as inputs. 
For sets $A,B: B^A:=\{f\mid f:A\rightarrow B\}$, and we can think of $\mathbb{R}^2$ for example as $2:={1,2}$ and $\mathbb{R}^2=\mathbb{R}^{\{1,2\}}$, and thus $\mathbb{R}^2=\{f:\{1,2\}\rightarrow\mathbb{R}\}$., where here 1,2 are just two subsets, so like $(x,y)$