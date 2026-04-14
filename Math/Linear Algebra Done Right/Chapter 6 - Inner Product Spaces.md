---
title: Chapter 6 - Inner Product Spaces

---

# Chapter 6 - Inner Product Spaces
**6.1 Notation** $\mathbb{F}, V$
- $\mathbb{F}$ denotes $\mathbb{R}$ or $\mathbb{C}$.
- $V$ denotes a vector space over $\mathbb{F}$. 

---
$$\text{Learning Objectives for this Chapter}$$
- Cauchy-Schwarz Inequality
- Gram-Schmidt Procedure
- Linear Functionals on Inner Product Spaces
- Calculating Minimum Distance to a Subspace

## 6.A Inner Product and Norms
### Inner Products

**6.2 Definition** *dot product*
For $x,y\in\mathbb{R}^n$, the *dot product* of $x$ and $y$, denoted $x\cdot y$, is defined by $$x\cdot y=x_1y_1+\cdot+x_ny_n\,,$$ where $x=(x_1,\dots,x_n)$ and $y=y_1,\dots,y_n\,$. 

**6.3 Definition** *inner product*
An *inner product* on $V$ is a function that takes each ordered pair $(u,v)$ of elements of $V$ to a number $\langle u,v\rangle\in\mathbb{F}$ and has the following properties:

**positivity** $$\langle u,v\rangle\ge0\;\forall\;v\in V;$$
**definiteness** $$\langle u,v\rangle=0\text{ if and only if }v=0;$$
**additiivty in the first slot** $$\langle u+v,w\rangle=\langle u,w\rangle+\langle v,w\rangle\;\forall\;u,v,w\in V;$$
**homogeneity in the first slot** $$\langle \lambda u,v\rangle=\lambda\langle u,v\rangle\;\forall\;\lambda\in\mathbb{F}\;\land\;u,v\in V;$$
**conjugate symmetry** $$\langle u,v\rangle=\overline{\langle v,u\rangle}\;\forall\;u,v\in V.$$

*note: Although most mathematicians definean inner product as above, many physicists (handsome guys) require homogeneity in the second slot instead of the first* 

---
**6.5 Definition** *inner product space*
An **inner product space** is a vector space $V$ along with an inner product on $V$.

**6.7 Basic properties of an inner product**
1. For each fixed $u\in V$, the function that takes $v$ to $\langle v,u\rangle$ is a linear map from $V$ to $\mathbb{F}$. 
2. $\langle 0,u\rangle=0$ for every $u\in V$.
3. $\langle u,0\rangle=0$ for every $u\in V$.
4. $\langle u,v+w\rangle=\langle u,v\rangle+\langle u,w\rangle\;\forall\;u,v,w\in V.$
5. $\langle u,\lambda v\rangle=\overline{\lambda}\langle u,v\rangle\;\forall\;\lambda\in\mathbb{F}\;\land\;u,v\in V$.

---
### Norms
**6.8 Definition** *norm,* $\|v\|$
For $v\in V$, the *norm* of $v$, denoted $\|v\|$, is defined by $$\|v\|=\sqrt{\langle v,v\rangle}.$$

**6.10 Basic properties of the norm**
Suppose $v\in V$.
1. $\|v\|=0$ if and only if $v=0.$
2. $\|\lambda v\|=|\lambda|\,\|v\|\;\forall\;\lambda\in\mathbb{F}.$

**6.11 Definition** *orthogonal*
Two vectors $u,v\in V$ are called *orthogonal* if $\langle u,v\rangle=0$.

**6.12 Orthogonality and $0$**
1. $0$ is orthogonal to every vector in $V$.
2. $0$ is the only vector in $V$ that is orthogonal to itself.

**6.13 Pythagorean Theorem**
Suppose $u$ and $v$ are orthogonal vectors in $V$, Then $$\|u+v\|^2=\|u\|^2+\|v\|^2.$$

**6.14 An orthogonal decomposition** 
Suppose $u,v\in V$, with $v\neq0$. Set $c=\frac{\langle u,v\rangle}{\|v\|^2}$ and $w=u-\frac{\langle u,v\rangle}{\|v^2\|}v,$ then, $$\langle w,v\rangle=0\quad\text{and}\quad u=cv+w.$$

**6.15 Cauchy-Schwarz Inequality**
Suppose $u,v\in V$. Then $$|\langle u,v\rangle|\le\|u\|\,\|v\|.$$ This inequality is an equality if and only if one of $u,v$ is a scalar multiple of the other. 

**6.18 Triangle Inequality**
Suppose $u,v\in V$, then $$\|u+v\|\le\|u\|+\|v\|.$$ This inequality is an equality if and only if one of $u,v$ is a non-negative multiple of the other.

**6.22 Parallelogram Equality**
Suppose $u,v\in V$, then $$\|u+v\|^2+\|u-v\|^2=2(\|u\|^2+\|v\|^2).$$

---
## 6.B Orthonormal Bases
**6.23 Definition** *orthonormal*
- A list of vectors is called **orthonormal** if each vector in the list has norm $1$ and is orthogonal to all the other vectors in the list.
- In other words, a list $e_1,\cdots,e_m$ of vectors in $V$ is orthonormal if $$\langle e_j,e_j\rangle=\begin{cases}1\quad\text{if }j=k.\\0\quad\text{if }j\neq k.\end{cases}$$

**6.25 The norm of an orthonormal linear combination**
If $e_1,\dots,e_m$ is an orthonormal list of vectors in $V$, then $$\|a_1e_1+\cdots+a_me_m\|^2=|a_1|^2+\cdots+|a_m|^2$$ for all $a_1,\dots,a_m\in\mathbb{F}$. 

**6.26 An orthonormal list is linearly independent**
Every orthonormal list of vectors is linearly independent. 

**6.27 Definition** *orthonormal basis*
An **orthonormal basis** of $V$ is an orthonormal list of vectors in $V$ that is also a basis of $V$. 

**6.28 An orthonormal list of the right length is an orthonormal basis**
Every orthonormal list of vectors in $V$ with length $\mathrm{dim}\,V$ is an orthonormal basis of $V$. 

**6.30 Writing a vector as linear combination of orthonormal basis** 
Suppose $e_1,\dots,e_n$ is an orthonormal basis of $V$ and $v\in V$, then $$v=\langle v,e_1\rangle e_1+\cdots+\langle v,e_n\rangle e_n$$ and $$\|v\|^2=|\langle v,e_1\rangle |^2+\cdots+|\langle v,e_n\rangle |^2.$$

**6.31 Gram-Schmidt Procedure**
Suppose $v_1,\cdots,v_m$ is a linearly independent list of vectors in $V$. Let $e_1=\frac{v_1}{\|v_1\|}$.For $j=2,\dots,m$ define $e_j$ inductively by $$e_j=\frac{v_j-\langle v_j,e_1\rangle e_1-\cdots-\langle v_j,e_{j-1}\rangle e_{j-1}}{\|v_j-\langle v_j,e_1\rangle e_1-\cdots-\langle v_j,e_{j-1}\rangle e_{j-1}\|}.$$ then, $e_1,\dots,e_m$ is an orthonormal list of vectors in $V$ such that $$\mathrm{span}(v_1,\dots,v_j)=\mathrm{span}(e_1,\dots,e_j)$$ for $j=1,\dots,m$. 

**6.34 Existence of an orthonormal basis**
Every finite-dimensional inner product space has an orthonormal basis.

**6.35 Orthonormal list extends to orthonormal basis**
Suppose $V$ is finite-dimensional, then every orthonormal list of vectors in $V$ can be extended to an orthonormal basis in $V$. 

**6.37 Upper-triangular matrix with respect to orthonormal basis**
Suppose  $T\in\mathcal{L}(V).$ if $T$ has an upper-triangular matrix with respect to some basis of $V$, then $T$ has an upper-triangular matrix with respect to some orthonormal basis of $V$. 

**6.38 Schur's Theorem**
Suppose $V$ is a finite-dimensional complex vector space and $T\in\mathcal{L}(V)$. Then $T$ has an upper-triangular matrix with respect to some orthonormal basis of $V$.

---
### Linear Functionals on Inner Product Spaces
**6.39 Definition** *linear functional* 
A **linear functional** on $V$ is a linear map from $V$ to $\mathbb{F}$. In other words, a linear functional is an element of $\mathcal{L}(V,\mathbb{F})$. 

**6.42 Riesz Representation Theorem**
Suppose $V$ is finite-dimensional and $\phi$ is the linear functional on $V$. Then there is a unique vector $u\in V$ such that $$\phi(v)=\langle v,u\rangle$$ for every $v\in V$. 

---
## 6.C Orthogonal Complements and Minimization Problem
**6.45 Definition** *orthogonal component*, $U^\perp$
If $U$ is a subset of $V$, then the *orthogonal complement* of $U$, denoted $U^\perp$, is the set of all vectors in $V$ that are orthogonal to every vector in $U$: $$U^\perp=\{v\in V:\langle v,u\rangle=0\text{ for every }u\in U\}.$$

**6.46 Basic properties of orthogonal complement**
1. If $U$ is a subset of $V$, then $U^\perp$ is a subspace of $V$. 
2. $\{0\}^\perp=V.$
3. $V^\perp=\{0\}.$
4. If $U$ is a subset of $V$, then $U\cap U^\perp\subset\{0\}$.
5. If $U$ and $W$ are subsets of $V$ and $U\subset W$, then $W^\perp\subset U^\perp$. 

**6.47 Direct sum of a subspace and its orthogonal complement**
Suppose $U$ is a finite-dimensional subspace of $V$, then $$V=U\oplus U^\perp.$$

**6.50 Dimension of the orthogonal complement**
Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$, then $$\mathrm{dim}\,U^\perp=\mathrm{dim}\,V-\mathrm{dim}\,U.$$

**6.51 The orthogonal complement of the orthogonal complement**
Suppose $U$ is a finite-dimensional subspace of $V$, then $$U=(U^\perp)^\perp.$$

**6.53 Definition** *orthogonal projection*, $P_U$
Suppose $U$ is a finite dimensional subspace of $V$. The *orthogonal projection* of $V$ onto $U$ is the operator $P_U\in\mathcal{L}(V)$ 

**6.55 Properties of the orthogonal projection $P_U$**
Suppose $U$ is a finite-dimensional subspace of $V$ and $v\in V$. Then
1. $P_U\in\mathcal{L}(V)$;
2. $P_Uu=u$ for every $u\in U$;
3. $P_Uw=0$ for every $w\in U^\perp$;
4. range $P_U=U$;
5. null $P_U=U^\perp$
6. $v-P_Uv\in U^\perp$
7. $P_U^2=P_U$;
8. $\|P_uv\|\le\|v\|;$
9. for every orthonormal basis $e_1,\dots,e_m$ of $U$, $$P_Uv=\langle v,e_1\rangle e_1+\cdots+\langle v,e_m\rangle e_m.$$

---
### Minimization Problems
**6.56 Minimizing the distance to a subspace**
Suppoe $U$ is a finite-dimensional subspace of $V, v\in V$, and $u\in U$, then $$\|v-P_Uv\|\le\|v-u\|.$$ Furthermore, the inequality above is an equality if and only if $u=P_Uv.$