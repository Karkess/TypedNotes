---
title: Chapter 2 - Finite-Dimensional Vector Spaces

---

# Chapter 2 - Finite-Dimensional Vector Spaces
**2.1 Notation** $\mathbb{F}, V$
- $\mathbb{F}$ denotes $\mathbb{R}$ or $\mathbb{C}$.
- $V$ denotes a vector space over $\mathbb{F}$.

Last Chapter: Arbitrary Vector Spaces

Learning Objectives:
- Span
- Linear Independence
- Bases
- Dimension
## 2.A - Span and Linear Independence

**2.2 Notation** *list of vectors*
We usually write lists of vectors without surrounding parenthesis.

---
### Linear Combinations and Span

**2.3 Definition** *linear combination*
A *linear combination* of a list $v_1,\dots,v_m$ of vectors in $V$ is a vector of the form $$a_1v_1+\cdots+a_mv_m,$$ where $a_1,\dots,a_m\in\mathbb{F}$. 

**2.5 Definition** *span*
The set of all linear combinations of a list of vectors $v_1,\dots,v_m$ in $V$ is called the *span* of $v_1,\dots,v_m$ denoted $\mathrm{span}(v_1,\dots,v_m)$. In other words, $$\mathrm{span}(v_1,\dots,v_m)=\{a_1v_1+\cdots+a_mv_m:a_1,\dots,a_m\in\mathbb{F}\}.$$ The span of the empty list $(\:)$ is defined to be $\{0\}$. 

---
**2.7 Span is the smallest containing subspace**
The span of a list of vectors in $V$ is the smallest subspace of $V$ containing all vectors in the list.

This is interesting, because it challenges what I was thinking 'span' meant, technically. I was thinking any vectors that spanned a vector space just meant that that a linear combination that could create all of the elements in that space. Like I think of $\hat{x}$ and $\hat{y}$ spanning the $x,y$-plane, but I would think if you added a third vector it would still span the space, but this makes it sound like the vectors have to be linearly independent to be a part of a span. Either that or I'm not understanding subspace, still. 'Smallest containing subspace' is confusing to me. This requires more reading.

Okay so span doesn't require linear independence. I'm still not feeling strong on what a subspace is. It seems very simple I'm not sure why it's not clicking intuitively. 

To me it feels just like a subgroup.

Apparently this is accurate, so I have an understanding of what a subspace is alright, and what span is, I think. I think the issue is this is the opposite direction I usually think of. I mentally construct a span from a space and not a space from a span, and that's much more difficult for me. Well I guess in quantum I do, that makes perfect sense to me and seems even more abstract, in the sense that it's an infinite dimensional vector space spanned by an infinite number of orthogonal functions. Hmm. I'm so confused that I'm not even sure what I'm confused on. I guess technically I can construct this to make absolute sense and I can use it, but I don't *feel* like I *really understand*. 

I think the issue might be more semantic? I am treating "containing subspace" like a noun. Is it? That doesn't make much sense. 

Yes I think this is my confusion. I'm not sure why I thought out loud here. If I were to phrase it how I best understand, I'd say that the subspace constructed by the span of a set of vectors is the smallest subspace containing all linear combinations of those vectors. 

---
**2.8 Definition** *spans*
If $\mathrm{span}(v_1,\dots,v_m)$ equals $V$, we say that $v_1,\dots,v_m$ *spans* $V$. 

**2.10 Definition** *finite-dimensional vector space*
A vector space is called *finite-dimensional* if some list of vectors in it spans the space.

Well this is concerning with what I said above. I thought the infinite set of orthogonal functions in quantum spanned an infinite dimensional space. 

Oh wait, Axler specifically stated that lists are finite earlier, there is no issue with my understanding of span in Hilbert spaces. (Well to be fair, there is probably a lot I don't understand, but you can say that the Hilbert space is spanned by these quantum functions).

**2.11 Definition** *polynomial* $\mathcal{P}(\mathbb{F})$
- A function $p:\mathbb{F}\rightarrow\mathbb{F}$ is called a *polynomial* with coefficients in $\mathbb{F}$ if there exist $a_0,\dots,a_m\in\mathbb{F}$ such that $$p(z)=a_0+a_1z+a_2z^2+\cdots+a_mz^m$$ for all $z\in\mathbb{F}$
- $\mathcal{P}(\mathbb{F})$ is the set of all polynomials with coefficients in $\mathbb{F}$. 

$\mathcal{P}(\mathbb{F})$ is a vector space over $\mathbb{F}$ and is thus a subspace of $\mathbb{F}^\mathbb{F}$, the vector space of functions from $\mathbb{F}$ to $\mathbb{F}$. 

**2.12 Definition** *degree of a polynomial*, $\mathrm{deg}\,p$
- A polynomial $p\in\mathcal{P}(\mathbb{F})$ is said to have a *degree m* if there exist scalars $a_0,a_1,\dots,a_m\in\mathbb{F}$ with $a_m\neq0$ such that $$p(z)=a_0+a_1z+\cdots+a_mz^m$ for all $z\in\mathbb{F}$. if $p$ has degree $m$ , we write $\mathrm{deg}\:p=m$.
- The polynomial that is identically $0$ is said to have degree $-\infty$. 

**2.13** $\mathcal{P}_m(\mathbb{F})$
For $m$ a nonnegative integer, $\mathcal{P}_m(\mathbb{F}) denotes the set of all polynomials with coefficients in $\mathbb{F}$ and degree at most $m$. 

**2.15 Definition** *infinite-dimensional vector space*
A vector space is called *infinite dimensional* if it is not finite-dimensional.

---
### Linear Independence

**2.17 Definition** *linearly independent*
- A list $v_1,\dots,v_m$ of vectors in $V$ is called **linearly independent** if the only choice of $a_1,\dots,a_m\in\mathbb{F}$ that makes $a_1v_1+\cdots+a_mv_m$ equals $0$ is $a_1=\cdots=a_m=0$.
- The empty list $(\,\,)$ is also declared to be linearly independent.


**2.19 Definition** *linearly dependent* 
- A list of vectors $V$ is called *linearly dependent* if it is not linearly independent. 
- In other words, a list $v_1,\dots,v_m$ of vectors $V$ is linearly dependent if there exist $a_1,\dots,a_m\in\mathbb{F}$, not all $0$, such that $a_1v_1+\cdots+a_mv_m=0$. 

---
**2.21 Linear Dependence Lemma**
Suppose $v_1,\dots,v_m$ is linearly dependent list in $V$. Then there exists $j\in\{1,2,\dots,m\}$ such that the following hold:
1. $v_j\in\mathrm{span}(v_1,\dots,v_{j-1})$;
2. If the $j^{\text{th}}$ term is removed from $v_1,\dots,v_m$, the span of the remaining list equals $\mathrm{span}(v_1,\dots,v_m)$.


**2.23 Length of linearly independent list $\le$ length of the spanning list**
In a finite-dimensional vector space, the length of every linearly independent list of vectors is less than or equal to the length of every spanning length of vectors. 

**2.26 Finite-dimensional subspaces**
Every subspace of a finite-dimensional vector space is finite-dimensional. 


## 2.B Bases
**2.27 Definition** *basis*
A **basis** of $V$ is a list of vectors in $V$ that is linearly independent and spans $V$. 

**2.29 Criterion for basis**
A list $v_1,\dots,v_n$ of vectors in $V$ is a basis of $V$ if and only if every $v\in V$ can be written uniquely in the form $$v=a_1v_1+\cdots+a_nv_n,$$ where $a_1,\dots,a_n\in\mathbb{F}$. 

**2.31 Spanning list contains a basis**
Every spanning list in a vector space can be reduced to a basis of the vector space. 

**2.32 Basis of finite-dimensional vector space**
Every finite dimensional vector space has a basis. 

**2.33 Linearly independent list extends to a basis**
Every linearly independent list of vectors in a finite-dimensional vector space can be extended to a basis of the vector space. 

**2.34 Every subspace of $V$ is part of a direct sum equal to $V$**
Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then there is a subspace $W$ of $V$ such that $V=U\oplus W$. 

## 2.C Dimension

**2.35 Basis length does not depend on basis**
Any two bases of a finite-dimensional vector space have the same length.**

**2.36 Definition** *dimension*, $\mathrm{dim}\,V$. 
- The *dimension* of a finite-dimensional vector space is the length of any basis of the vector space.
- The dimension of $V$ (if $V$ is finite-dimensional) is denoted by $\mathrm{dim}\,V$. 

**2.38 Dimension of a subspace** 
If $V$ is finite-dimensional and $U$ is a subspace of $V$, then $\mathrm{dim}\,U\le\mathrm{dim}\,V$. 

**2.39 Linearly indepdendent list of the right length is a basis**
Suppose $V$ is finite-dimensional. Then every linearly independent list of vectors in $V$ with length $\mathrm{dim}\,V$ is a basis of $V$. 

**2.42 Spanning list of the right length is a basis**
Suppose $V$ is finite dimensional. Then every spanning list of vectors in $V$ with a length $\mathrm{dim}\,V$ is a basis of $V$. 

**2.43 Dimension of a sum**
If $U_1$ and $U_2$ are subspaces of a finite-dimension vector space, then $$\mathrm{dim}\,(U_1+ U_2)=\mathrm{dim}\,U_1+\mathrm{dim}\,U_2-\mathrm{dim}\,(U_1\cap U_2).$$