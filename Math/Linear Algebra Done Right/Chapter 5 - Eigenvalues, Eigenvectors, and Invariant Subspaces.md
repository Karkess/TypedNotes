---
title: 'Chapter 5 - Eigenvalues, Eigenvectors, and Invariant Subspaces'

---

# Chapter 5 - Eigenvalues, Eigenvectors, and Invariant Subspaces

In this chapter we'll focus on an investigation of a linear map from a finite-dimensional vector space to itself.

---
**5.1 Notation** $\mathbb{F},V$
- $\mathbb{F}$ denotes $\mathbb{R}$ or $\mathbb{C}$. 
- $V$ denotes a vector space over $\mathbb{F}$. 

---
$$\text{Learning Objectives For This Chapter}$$
- Invariant subspaces
- Eigenvalues, eigenvectors, and eigenspaces
- each operator on a finite-dimensional complex vector space has an eigenvalue and an upper-triangular matrix with respect to some basis.
---
## 5.A Invariant Subspaces

**5.2 Definition** *invariant subspace*
Suppose $T\in\mathcal{L}(V).$ A subspace $U$ of $V$ iscalled **invariant** under $T$ if $u\in U$ implies $Tu\in U$
    - In other words, $U$ is invariant under $T$ if $T|_U$ is an operator on $U$. 
    - Note: $T|_U$ here denotes a restriction of $T$ to a smaller domain $U$. 

---
### Eigenvalues and Eigenvectors
We will here treat the simplest possible nontrivial invariant subspaces, invariant subspaces with dimension 1. 
Take any $v\in V$ with $v\neq0$ and let $U$ equal the set of all scalar multiples of $v:$ $$U=\{\lambda v:\lambda\in\mathbb{F}\}=\mathrm{span}(v).$$
Then $U$ is a $1$-dimensional subspace of $V$. If $U$ is invariant under an operator $T\in\mathcal{L}(V)$, then $Tv\in U$, and hence there is a scalar $\lambda\in\mathbb{F}$ such that $$Tv=\lambda v.$$ Conversely, if $Tv=\lambda v$ for some $\lambda\in\mathbb{F}$, then $\mathrm{span}(v)$ is a 1-dimensional subspace of $V$ invariant under $T$. 

**5.5 Definition** *eigenvalue*
Suppose $T\in\mathcal{L}(V)$. A number $\lambda\in\mathbb{F}$ is called an *eigenvalue* of $T$ if there exists $v\in V$ such that $v\neq0$ and $Tv=\lambda v$. 

*Note: The word **eigenvalue** is half-German, half-English. The German adjective **eigen** means "own" in the sense of characterizing an intrinsic property. Some mathematicians use the term **characteristic value** instead of eigenvalue*. 

**5.6 Equivalent Conditions to be an Eigenvalue**
Suppose $V$ is finite-dimensional, $T\in\mathcal{L}(V)$, and $\lambda\in\mathbb{F}$. Then the following are equivalent:
1. $\lambda$ is an eigenvalue of $T$;
2. $T-\lambda I$ is not injective;
3. $T-\lambda I$ is not surjective;
4. $T-\lambda I$ is not invertible.

*Recall that $I\in\mathcal{L}(V)$ is the identity operator defined by $Iv=v$ for all $v\in V$.*

**5.7 Definition** *eigenvector*
Suppose $T\in\mathcal{L}(V)$ and $\lambda\in\mathbb{F}$ is an eigenvalue of $T$. A vector $v\in V$ is called an *eigenvector* of $T$ corresponding to $\lambda$ is $v\neq0$ and $Tv=\lambda v$

**5.10 Linearly independent eigenvectors**
Let $T\in\mathcal{L}(V).$ Suppose $\lambda_1,\dots,\lambda_m$ are distinct eigenvalues of $T$ and $v_1,\dots,v_m$ are corresponding eigenvectors. Then $v_1,\dots,v_m$ is linearly independent.

**5.13 Number of Eigenvalues**
Suppose $V$ is finite-dimensional. Then each operator on $V$ has at most $\mathrm{dim}\,V$ distinct eigenvalues.

---
### Restriction and Quotient Operators

**5.14 Definition $T|_U$ and $T/U$**
Suppose $T\in\mathcal{L}(V)$ and $U$ is a subspace of $V$ invariant under $T$.
- The *restriction operator* $T|_U\in\mathcal{L}(U)$ is defined by $$T|_U(u)=Tu$$ for all $u\in U.$
- The *quotient operator* $T/U\in\mathcal{L}(V/U)$ is defined by $$(T/U)(v+U)=Tv+U$$ for $v\in V$. 

## 5.B Eigenvalues and Upper-Triangular Matrices
### Polynomials Applied to Operators

**5.16 Definition** $T^m$
Suppose $T\in\mathcal{L}(V)$ and $m$ is a positive integer.
- $T^m$ is defined by $$T^m=T\cdots T\:(m\text{ times})$$
- $T^0$ is defined to be the identity operator $I$ on $V$. 
- If $T$ is invertible with inverse $T^{-1}$, then $T^-m$ is defined by $$T^{-m}=(T^{-1})^m.$$


**5.17 Definition** $p(T)$
Suppose $T\in\mathcal{L}(V)$ and $p\in\mathcal{P}(\mathbb{F})$ is a polynomial given by $$p(z)=a_1+a_1z+a_2z^2+\cdots+a_mz^m$$ for $z\in\mathbb{F}$. Then $$p(T)=a_0I+a_1T+a_2T^2+\cdots+a_mT^m.$$

**5.19 Definition** *product of polynomials*
If $p,q\in\mathcal{P}(\mathbb{F})$, then $pq\in\mathcal{P}(\mathbb{F})$ is the polynomial defined by $$(pq)(z)=p(z)q(z)$$ for $z\in\mathbb{F}$.

**5.20 Multiplicative properties**
Suppose $p,q\in\mathcal{P}(\mathbb{F})$ and $T\in\mathcal{L}(V)$. Then
1. $(pq)(T)=p(T)q(T)$
2. $p(T)q(T)=q(T)p(T)$.

---
### Existence of Eigenvalues
**5.21 Operators on complex vector spaces have an eigenvalue**
Every operator on a finite-dimensional, nonzero, complex vector space has an eigenvalue. 

---
### Upper-Triangular Matrices
**5.22 Definition** *matrix of an operator* $\mathcal{M}(T)$
Suppose $T\in\mathcal{L}(V)$, and $v_1,\dots,v_n$ is a basis of $V$. The *matrix of* $T$ with respect to this basis is the $n$-by-$n$ matrix $$\mathcal{M}(T)=\begin{pmatrix}A_{1,1}&\cdots&A_{1,n}\\\vdots&&\vdots\\A_{n,1}&\cdots&A_{n,n}\end{pmatrix}$$whose entries $A_{j,k}$ are defined by $$T_{v_k}=A_{1,k}v_1+\cdots+A_{n,k}v_n.$$ If the basis is not clear from the context, then the notation $\mathcal{M}(T,(v_1,\dots,v_n))$ is used. 

---
*Note: The matrices of operators are square arrays*

**5.23 Example** Define $T\in\mathcal{L}(\mathbb{F}^3)$ by $T(x,y,z)=(2x+y,5y+3z,8z)$, then $$\mathcal{M}(T)=\begin{pmatrix}2&1&0\\0&5&4\\0&0&8\end{pmatrix}.$$

---
**5.24 Definition** *diagonal of a matrix*
The *diagonal* of a square matrix consists of the entries along the line from the upper left corner to the bottom right corner.

**5.25 Definition** *upper-triangular matrix*
A matrix is called *upper triangular* if all of the entries below the diagonal equals 0. 

**5.26 Conditions for upper-triangular matrix**
Suppose $T\in\mathcal{L}(V)$ and $v_1,\dots,v_n$ is a basis of $V$. Then the following is equivalent:
1. the matrix of $T$ with respect to $v_1,\dots,v_n$ is upper triangular;
2. $T_{v_j}\in\mathrm{span}\,(v_1,\dots,v_n)\text{ for each }j=1,\dots,n$;
3. $\mathrm{span}\,(v_1,\dots,v_j)$ is invariant under $T$ for each $j=1,\dots,n.$

**5.27 Over $\mathbb{C}$, every operator has an upper-triangular matrix
Suppose $V$ is a finite-dimensional complex vector space and $T\in\mathcal{L}(V)$. Then $T$ has an upper-triangular matrix with respect to some basis of $V$. 

**5.30 Determination of invertibility from upper-triangular matrix**
Suppose $T\in\mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$, then $T$ is invertible if and only if all entries of the diagonal are nonzero.

**5.32 Determination of eigenvalues from upper-triangular matrix**
Suppose $T\in\mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then the eigenvalues of $T$ are precisely the entries on the diagonal of that upper-triangular matrix.

---
## 5.C Eigenspaces and Diagonal Matrices
**5.34 Definition** *diagonal matrix*
A **diagonal matrix** is a square matrix that is 0 everywhere except possibly along the diagonal. 

**5.36 Definition** *eigenspace* $E(\lambda,T)$
Suppose $T\in\mathcal{L}(V)$ and $\lambda\in\mathbb{F}$. The *eigenspace* of $T$ corresponding to $\lambda$, denoted $E(\lambda,T)$, is defined by $$E(\lambda,T)=\mathrm{null}(T-\lambda I).$$ In other words, $E(\lambda,T)$ is the set of all eigenvectors of $T$ corresponding to $\lambda$, along with the $\vec{0}$ vector.

**5.38 Sum of eigenspaces is a direct sum**
Suppose $V$ is finite-dimensional and $T\in\mathcal{L}(V)$. Suppose also that $\lambda_1,\dots,\lambda_m$ are distinct eigenvalues of $T$, then, $$E(\lambda_1,T)+\cdots+E(\lambda_m,T)$$ is a direct sum, furthermore, $$\mathrm{dim}\,E(\lambda_1,T)+\cdots+\mathrm{dim}\,E(\lambda_m,T)\le\mathrm{dim}\,V.$$

**5.39 Definition** *diagonalizable*
An operator $T\in\mathcal{L}(V)$ is called *diagonalizable* if the operator has a diagonal matrix with respect to some basis of $V$.

**5.41 Conditionals equivalent to diagonalizability**
Suppose $V$ is a finite-dimensional and $T\in\mathcal{L}(V)$. Let $\lambda_1,\dots,\lambda_m$ denote the distinct eigenvalues of $T$. Then the following are equivalent: 
1. $T$ is diagonalizable;
2. $V$ has a basis consisting of eigenvectors of $T$;
3. There exist 1-dimensional subspaces $U_1,\dots,U_n$ of $V$, each invariant under $T$, such that $$V=U_1\oplus\cdots\oplus U_n;$$
4. $V=E(\lambda_1,T)\oplus\cdots\oplus E(\lambda_m,T);$
5. $\mathrm{dim}\,V=\mathrm{dim}\,E(\lambda_1,T)+\cdots+\mathrm{dim}\,E(\lambda_m,T)$

**5.44 Enough eigenvalues implies diagonalizability**
If $T\in\mathcal{L}(V)$ has $\mathrm{dim}\,V$ distinct eigenvalues, then $T$ is diagonalizable. 