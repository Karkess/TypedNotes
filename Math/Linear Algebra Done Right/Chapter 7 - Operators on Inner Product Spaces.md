---
title: Chapter 7 - Operators on Inner Product Spaces

---

# Chapter 7 - Operators on Inner Product Spaces

**7.1 Notation** $\mathbb{F}, V$
- $\mathbb{F}$ denotes $\mathbb{R}$ or $\mathbb{C}$. 
- $V$ and $W$ denote finite-dimensional inner product spaces over $\mathbb{F}$/ 

---
$$\text{Learning Objectives For This Chapter}$$
- adjoint
- Spectral Theorem
- positive operators
- isometric
- Polar Decomposition
- Singular Value Decomposition

---
## 7.A Self-Adjoint and Normal Operators
### Adjoints
**7.2 Definition** *adjoint*, $T^*$
Suppose $T\in\mathcal{L}(V,W).$ The **adjoint** of $T$ is the function $T^*:W\rightarrow V$ such that $$\langle Tv,w\rangle=\langle v,T^*w\rangle$$ for every $v\in V$ and every $w\in W$. 

**7.5 The adjoint is a linear map**
If $T\in\mathcal{L}(V,W)$, then $T^*=\mathcal{L}(W,V)$. 

**7.6 Properties of the adjoint**
1. $(S+T)^*=S^*+T^*\quad\forall\quad S,T\in\mathcal{L}(V,W);$
2. $(\lambda T)^*=\overline{\lambda}T^*\quad\forall\quad\lambda\in\mathbb{F}\land T\in\mathcal{L}(V,W);$
3. $(T^*)^*=T\quad\forall\quad T\in\mathcal{L}(V,W);$
4. $I^*=I$ where $I$ is the identity operator on $V$;
5. $(ST)^*=T^*S^*\quad\forall\quad T\in\mathcal{L}(V,W)\land S\in\mathcal{L}(W,U)$ (here $U$ is an inner product space over $\mathbb{F}$)

**7.7 Nullspace and range of $T^*$
Suppose $T\in\mathcal{L}(V,W)$, then,
1. $\mathrm{null}\,T^*=(\mathrm{range}\,T)^\perp$;
2. $\mathrm{range}\,T^*=(\mathrm{null}\,T)^\perp$;
3. $\mathrm{null}\,T=(\mathrm{range}\,T^*)^\perp$;
4. $\mathrm{range}\,T=(\mathrm{null}\,T^*)^\perp$.

**7.8 Definition** *conjugate transpose*
The **conjugate transpose** of an $m$-by-$n$ matrix is the $n$-by-$m$ matrix obtained by interchanging rows and columns and taking the complex conjugate of each entry.


**7.10 The matrix of** $T^*$
Let $T\in\mathcal{L}(V,W)$. Suppose $e_1,\dots,e_n$ is an orthonormal basis of $V$ and $f_1,\dots,f_m$ is an orthonormal basis of $W$, then $$\mathcal{M}(T^*,(f_1,\dots,f_m),(e_1,\dots,e_n)).$$ is the conjugate transpose of $$\mathcal{M}(T,(e_1,\dots,e_n),(f_1,\dots,f_m)).$$

---
### Self-Adjoint Operators
**7.11 Definition** *self-adjoint*
An operator $T\in\mathcal{L}(V)$ is called **self-adjoint** if $T=T^*$. In other words, $T\in\mathcal{L}(V)$ is self-adjoint if and only if $$\langle Tv,w\rangle=\langle v,Tw\rangle$$ for all $v,w\in V$. 

**7.13 Eigenvalues of self-adjoint operators are real**
Every eigenvalue of a self-adjoint operator is real.

**7.14 Over $\mathbb{C},\,Tv$ is orthogonal to $v$ for all $v$ only for the $0$ operator**
Suppose $V$ is a complex inner product space and $T\in\mathcal{L}(V)$. Suppose $$\langle Tv,v\rangle=0$$ for all $v\in V$. Then $T=0$.

**7.15 Over $\mathbb{C},\langle Tv,v\rangle$ is real for all $v$ only for self-adjoint operators**
Suppose $V$ is a complex inner product space and $T\in\mathcal{L}(V)$. Then $T$ is self-adjoint if and only if $$\langle Tv,v\rangle\in\mathbb{R}$$ for every $v\in V$. 

**7.16 If $T=T^*$ and $\langle Tv,v\rangle=0$ for all $v$, then $T=0.$**
Suppose $T$ is a self-adjoint operator on $V$ such that $$\langle Tv,v\rangle=0$$ for all $v\in V$, then $T=0$. 

---
### Normal Operators
**7.18 Definition** *normal*
- An operator on an inner product space is called *normal* if it commutes with its adjoint.
- In other words, $T\in\mathcal{L}(V)$ is normal if $$TT^*=T^*T.$$

**7.20 $T$ is normal if and only if $\|Tv\|=\|T^*v\|\,\forall\,v$**
An operator $T\in\mathcal{L}(V)$ is normal if and only if $$\|Tv\|=\|T^*v\|$$ for all $v\in V$. 

**7.21 For $T$ normal, $T$ and $T^*$ have the same eigenvectors.**
Suppose $T\in\mathcal{L}(V)$ is normal and $v\in V$ is an eigenvector of $T$ with eigenvalue $\lambda$. Then $v$ is also an eigenvector of $T^*$ with eigenvalue $\overline{\lambda}$. 

**7.22 Orthogonal eigenvectors for normal operators**
Suppose $T\in\mathcal{L}(V)$ is normal, then eigenvectors of $T$ corresponding to distinct eigenvalues are orthogonal.

---
## 7.B The Spectral Theorem
### The Complex Spectral Theorem
**7.24 Complex Spectral Theorem**
Suppose $\mathbb{F}=\mathbb{C}$ and $T\in\mathcal{L}(V)$, then the following are equivalent: 
1. $T$ is normal.
2. $V$ has an orthonormal basis consisting of eigenvectors of $T$.
3. $T$ has a diagonal matrix with respect to some of the orthonormal basis of $V$. 

---
### The Real Spectral Theorem 
**7.26 Invertible Quadratic Expressions**
Suppose $T\in\mathcal{L}(V)$ is self-adjoint and $b,c\in\mathbb{R}$ are such that $b^2<4c$, then, $$T^2+bT+cI$$ is invertible.

**7.27 Self-adjoint operators have eigenvalues**
Suppose $V\neq\{0\}$ and $T\in\mathcal{L}(V)$ is a self-adjoint operator, then $T$ has an eigenvalue. 

**7.28 Self-adjoint operators and invariant subspaces**
Suppose $T\in\mathcal{L}(V)$ is self-adjoint and $U$ is a subspace of $V$ that is invariant under $T$, then, 
1. $U^\perp$ is invariant under $T$;
2. $T|_U\in\mathcal{L}(U)$ is self-adjoint;
3. $T|_{U^\perp}\in\mathcal{L}(U)$ is self-adjoint.

**7.29 Real Spectral Theorem**
Suppose $\mathbb{F}=\mathbb{R}$ and $T\in\mathcal{L}(V)$, then the following are equivalent:
1. $T$ is self-adjoint.
2. $V$ has an orthonormal basis consisting of the eigenvectors of $T$.
3. $T$ has a diagonal matrix with respect to some orthonormal basis of $V$. 

---
## 7.C Positive Operators and Isometries
### Positive Operators
**7.31 Definition** *positive operator*
An operator $T\in\mathcal{L}(V)$ is called *positive* if $T$ is self-adjoint and $$\langle Tv,v\rangle\ge0$$ for all $v\in V$. 

**7.33 Definition** *square root*
An operator $R$ is called a **square root** of an operator $T$ if $R^2=T.$

**7.35 Characterization of positive operators**
Let $T\in\mathcal{L}(V)$, then the following are equivalent:
1. $T$ is positive
2. $T$ is self-adjoint and all eigenvalues of $T$ are nonnegative
3. $T$ has a positive square root
4. 4t4 has a self adjoint square root
5. There exists an operator $R\in\mathcal{L}(V)$ such that $T=R^*R$. 

**7.36 Each positive operator has only one positive square root**
Every positive operator on $V$ has a unique positive square root.

---
### Isometries
**7.37 Definition** *isometry 
- An operator $S\in\mathcal{L}(V)$ is called an *isometry* if $$\|Sv\|=\|v\|$$ for all $v\in V$. 
- In other words, an operator is an isometry if it preserves norms. 

*Note: An isometry on a real inner product space is called **orthogonal**. An isometry on a complex inner product space is called a **unitary** operator. We use isometry so that results can apply to both real and complex inner product spaces. 

**7.42 Characterization of Isometries**
Suppose $S\in\mathcal{L}(V)$, then the following are equivalent:
1. $S$ is an isometry
2. $\langle Su,Sv\rangle=\langle u,v\rangle\quad\forall\quad u,v\in V$
3. $Se_1,\dots,Se_n$ is orthonormal for every orthonormal list of vectors $e_1,\dots,e_n$ in $V$
4. there exists an orthonormal basis $e_1,\dots,e_n$ of $V$ such that $Se_1,\dots,Se_n$ is orthonormal. 
5. $S^*S=I$
6. $SS^*=I$
7. $S^*$ is an isometry
8. $S$ is invertible and $S^{-1}=S^*$.

**7.43 Description of isometries when $\mathbb{F}=\mathbb{C}$**
Suppose $V$ is a complex inner product space and $S\in\mathcal{L}(V)$, then the following are equivalent: 
1. $S$ is an isometry.
2. There is an orthonormal basis $V$ consisting of eigenvectors of $S$ whose corresponding eigenvalues all have absolute value $1$. 

---
## 7.d Polar Decomposition and Singular Value Decomposition
**7.44 Notation** $\sqrt{T}$
If $T$ is a positive operator, then $\sqrt{T}$ denotes the unique positive square root of $T$. 

**7.45 Polar Decomposition**
Suppose $T\in\mathcal{L}(V)$, then there exists an isometry $S\in\mathcal{L}(V)$ such that $$S\sqrt{T^*T}.$$

---
### Singular Value Decomposition
**7.49 Definition** *singular values*
Suppose $T\in\mathcal{L}(V)$. The **singular values** of $T$ are the eigenvalues of $\sqrt{T^*T}$, with each eigenvalue $\lambda$ repeated $\mathrm{dim}\,E(\lambda,\sqrt{T^*T})$ times.

**7.51 Singular Value Decomposition**
Suppose $T\in\mathcal{L}(V)$ has singular values $s_1,\dots,s_n$, then, there exist orthonormal bases $e_1,\dots,e_n$ and $f_1,dots,f_n$ of $V$ such that $$Tv=s_1\langle v,e_1\rangle f_1+\cdots+s_n\langle v,e_n\rangle f_n$$ for every $v\in V$. 

**7.52 Singular values without taking the square root of an operator**
Suppose $T\in\mathcal{L}(V)$, then the singular values of $T$ are the nonnegative square roots of the eigenvalues of $T^*T$, with each eigenvalue $\lambda$ repeated $\mathrm{dim}\,E(\lambda,T^*T)$ times. 