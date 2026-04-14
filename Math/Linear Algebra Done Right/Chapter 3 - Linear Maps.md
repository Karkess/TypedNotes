---
title: Chapter 3 - Linear Maps

---

# Chapter 3 - Linear Maps

**3,1 Notation** $\mathbb{F}, V, W$
- $\mathbb{F}$ denotes $\mathbb{R}$ or $\mathbb{C}$. 
- $V$ and $W$ denote vector spaces over $\mathbb{F}$. 

**Learning Objectives for this Chapter**
- Fundamental Theorem of Linear Maps
- The matrix of al inear map with respect to given bases
- Isomorphic Vector Spaces
- Product Spaces
- Quotient Spaces
- The dual space of a vector space and the dual of a linear map

## 3.A The Vector Space of Linear Maps

**3.2 Definition** *linear map*
A **linear map** from $V$ to $W$ is a function $T:V\rightarrow W$ with the following properties:
**additiity** $$T(u+v)=Tu+Tv\:\forall\:u,v\in V;$$
**homogeneity** $$T(\lambda v)=\lambda(Tv)\:\forall\:\lambda\in\mathbb{F}\:\land\:\forall\:v\in V.$$

**3.3 Notation** $\mathcal{L}(V,W)$
The set of all linear maps from $V$ to $W$ is denoted $\mathcal{L}(V,W)$. 

---
I don't usually do examples, but I quite like this one.

**3.4 Example** *linear maps*
**Zero**
As ana dditional use, we let the symbol $0$ denote the function tha takes each element of some vector space to the additive identity of another vector space, that is, $0\in\mathcal{L}(V,W)$, defined by $$0v=0.$$ The $0$ on the left side is a function from $V$ to $W$, and the $0$ on the right side is the is the additive identity in $W$.

**Identity**
The *identity map*, denoted *I*, is the function on some vector space that takes each element to itself, that is, $I\in\mathcal{L}(V,V)$, defined by $$Iv=v.$$

**Differentiation**
Define $D\in\mathcal{L}(\mathcal{P}(R),\mathcal{P}(R))$ by $$Dp=p'.$$ This is indeed a linear map because $(f+g)'=f'+g'\:\land\: (\lambda f)'=\lambda f'$. 

**Integration**
Define $T\in\mathcal{L}(\mathcal{P}(R),R)$ by $$Tp=\int^1_0p(x)\,dx.$$ Again this is linear because the integration of two added functions is the addition of both integrals, and similarly a scalar multiple can be pulled out and put in. 

**Multiplication by** $x^2$
Define $T\in\mathcal{L}(\mathcal{P}(R),\mathcal{P}(R))$ by $$(Tp)(x)=x^2p(x)$$ for $x\in\mathbb{R}.$

**Backward Shift**
Recall that $\mathbb{F}^\infty$ denotes the vector space of all sequences of elements of $\mathbb{F}$. 
Define $T\in\mathcal{L}(\mathbb{F}^\infty,\mathbb{F}^\infty)$ by $$T(x_1,x_2,x_3,\dots)=(x_2,x_3,
dots)$$ from $\mathbb{R}^3\rightarrow\mathbb{R}^2$
Define $T\in\mathcal{L}(\mathbb{R}^3,\mathbb{R}^2)$ by $$T(x,y,z)=(2x-y+3z,7x+5y-6z).$$ from $\mathbb{F}^n\rightarrow\mathbb{F}^m$, where $m\land n\in\mathbb{N}$, $A_{j,k}\in\mathbb{F}$ for $j=1,\dots,m\,\land\, k=1,\dots,n$, and define $T\in\mathcal{L}(\mathbb{F}^n,\mathbb{F}^m)$ by $$T(x_1,dots,x_n)=(A_{1,1}x_1+\cdots+A_{1,n}x_n,\dots A_{m,1}x_1+\cdots+A_{m,n}x_n)$$.

---
**3.5 Linear maps and basis of domain**
Suppose $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_n\in W$. Then there exists a unique linear map $T:V\rightarrow W$ such that $$Tv_j=w_j$$ for each $j=1,\dots,n.$

---
### Algebraic Operations on $\mathcal{L}(V,W)$
**3.6 Definition** *addition and scalar multiplication on $\mathcal{L}(V,W)$*
Suppose $S,T\in\mathcal{L}(V,W)\,\land\,\lambda\in\mathbb{F}$. The *sum* $S+T$ and the *product* $\lambda T$ are the linear maps from $V\rightarrow W$ defined by $$(S+T)(v)=Sv+Tv\quad\text{and}\quad(\lambda T)(v)=\lambda(Tv),$$ for all $v\in V$

**3.7 $\mathcal{L}(V,W)$ is a vector space**
With the operations of addition and scalar multiplication as defined above, $\mathcal{L}(V,W)$ is a vector space.

**3.8 Definition** *Product of Linear Maps*
If $T\in\mathcal{L}(U,V)\text{ and }S\in\mathcal{L}(V,W)$, then the *product* $ST\in\mathcal{L}(U,W)$ is defined by $$(ST)(u)=S(Tu)$$ for $u\in U$. 

**3.9 Algebaic properties of products of linear maps**
**associativity**
$$(T_1T_2)T_3=T_1(T_2)(T_3)$$ whenever $T_1,T_2\text{, and }T_3$ are linaer maps such that the products make sense. 

**identity**
$$TI=IT=T$$whenever $T\in\mathcal{L}(V,W)$. (The first $I$ is the identity map on $V$, and the second is the identity map on $W$.)

**distributive properties** 
$$(S_1+S_2)T=S_1T+S_2T\text{ and }S(T_1+T_2)=ST_1+ST_2$$ whenever $T,T_1,T_2\in\mathcal{L}(U,V)$ and $S,S_1,S_2\in\mathcal{L}(V,W).$

**3.11 Linear maps takes $0$ to $0$**
Suppose $T$ is a linear map from $V$ to $W$; then, $T(0)=0$. 

## 3.B Null Spaces and Ranges

**3.12 Definition** *null space*, null $T$
For $T\in\mathcal{L}(V,W)$, the *null space* of $T$, denoted $\mathrm{null}\,T$, is the subset of $V$ consisting of those vectors that $T$ maps to $0$:$$\mathrm{null}\,T=\{v\in V:Tv=0\}.$$

*Note:* Some mathematicians use the term **kernel** instead of "null space". This is interesting, I never knew that's what kernel meant. 

**3.14 The null space is a subspace**
Suppose $T\in\mathcal{L}(V,W)$; then, $\mathrm{null}\,T$ is a subpsace of $V$. 

**3.15 Definition** *injective*
A function $T:V\rightarrow W$ is called *injective* if $Tu=Tv$ implies $u=v$. 

**3.16 Injectivity is equivalent to null space equals $\{0\}$**
Let $T\in\mathcal{L}(V,W)$; then, $T$ is injective if only if $\mathrm{null}\,T=\{0\}$. 

---
### Range and Surjectivity
**3.17 Definition** *range*
For $T$ a function from $V$ to $W$, the *range* of $T$ is the subset of $W$ consisting of those vectors that are of the form $T_v$ for some $v\in V$:$$\mathrm{range}\,T=\{T_v:v\in V\}.$$

In other words, range is the set of outputs of a function. 

**3.19 The range is a subspace**
If $T\in\mathcal{L}(V,W)$, then range $T$ is a subspace of $W$.

**3.20 Definition** *surjective*
A function $T:V\rightarrow W$ is aclled *surjective* if its range equals $W$. 

*note*: Many mathematicians use the term **onto**, which means the same as surjective. 

---
### Fundamental Theorem of Linear Maps
**3.22 Fundamental Theorem of Linear Maps**
Suppose $V$ is finite-dimensional and $T\in\mathcal{L}(V,W)$. Then range $T$ is finite-dimensional and $$\mathrm{dim}\,V=\mathrm{dim}\,\mathrm{null}\,T+\mathrm{dim}\,\mathrm{range}\,T.$$

**3.23 A map to a smaller dimensional space is not injective**
Suppose $V$ and $W$ are finite-dimensional vector spaces such that $\mathrm{dim}\,V>\mathrm{dim}\,W$. Then no linear map is injective.

**3.24 A map to a larger dimensional space is not surjective**
Suppose $V$ and $W$ are finite-dimensional vector spaces such that $\mathrm{dim}\,V<\mathrm{dim}\,W$. Then no linear map from $V$ to $W$ is surjective. 

**3.26 Homogenous system of linear equations**
A homogenous system of linear equations with more variables than equations has nonzero solutions. 

**3.29 Inhomogenous system of linear equations**
An inhomogenous system of linear equations with more equations than variables has no solution for some choice of the constant terms. 

## 3.C Matrices
### Representing a Linear Map by a Matrix
**3.30 Definition** *matrix*, $A_{j,k}$
Let $m$ and $n$ denote positive integers. An $m$-by-$n$ *matrix* $A$ is a rectangular array of elements of $\mathbb{F}$ with $m$ rows and $n$ columns: $$A=\begin{pmatrix}A_{1,1}&\cdots&A_{1,n}\\\vdots&&\vdots\\A_{m,1}&\cdots&A_{m,n}.\end{pmatrix}$$ 
The notation $A_{j,k}$denotes the entry in row $j$ and column $k$ of $A$. In other words, the first index refers to the row number and the second index refers to the column number.

**3.32 Definition** *Matrix of a linear map*, $\mathcal{M}(T)$.
Suppose $T\in\mathcal{L}(V,W)$ and $v_1,\dots,v_n$ is a basis of $W$. The *matrix of* $T$ with respect to these bases is the $m$-by-$n$ matrix $\mathcal{M}(T)$ whose entries $A_{j,k}$ are defined by $$T_{v_k}=A_{1,k}w_1+\cdots+A_{m,k}w_m.$$ If the bases are not clear from context, then the notation $\mathcal{M}(T,(v_1,\dots,v_n),(w_1,\dots,w_m))$ is used.

***Note: If $T$ maps an $n$-dimensional vector space to an $m$ dimensional vector space, then $\mathcal{M}(T)$ is an $m$-by-$n$ matrix***
Not sure how I never noticed this one, but this is a very interesting fact. It also makes my commonly seeing square matrices make a lot of sense.
I additionally found the below example illuminating:

**3.33 Example** Suppose $T\in\mathcal{L}(\mathbb{F}^2,\mathbb{F}^3)$ is defined by $$T(x,y)=(x+3y,2x+5y,7x+9y).$$ Find the matrix of $T$ with respect to the standard bases of $\mathbb{F}^2$ and $\mathbb{F}^3$. 
**Solution:** Because $T(1,0)=(1,2,7)$ and $T(0,1)=(3,5,9)$, the matrix of $T$ with respect to the standard bases is the $3$-by-$2$ matrix below: $$\mathcal{M}(T)=\begin{pmatrix}1&3\\2&5\\7&9\end{pmatrix}.$$

---
### Addition and Scalar Multiplication of Matrices
**3.35 Definition** *matrix addition* 
The sum of two matrices of the same size is the matrix obtained by adding corresponding entries in the matrices: $(A+C)_{j,k}=A_{j,k}+C_{j,k}$. 

**3.36 The matrix of the sum of linear maps**
Suppose $S,T\in\mathcal{L}(V,W).$ Then $\mathcal{M}(S+T)=\mathcal{M}(S)+\mathcal{M}(T)$. 

**3.37 Definition** *scalar multiplication of a matrix*
The product of a scalar and a amtrix is a matrix obtained by multiplying each entry in the matrix by the scalar: $(\lambda A)_{j,k}=\lambda A_{j,k}$. 

**3.38 The matrix of a scalar times a linear map**
Suppose $\lambda\in\mathbb{F}$ and $R\in\mathcal{L}(V,W)$. Then $\mathcal{M}(\lambda T)=\lambda\mathcal{M}(T)$.

**3.39 Notation** $\mathbb{F}^{m,n}$
For $m$ and $n$ positive integers, the set of all $m$-by-$n$ matrices with entries in $\mathbb{F}$ is denoted by $\mathbb{F}^{m,n}$. 

**3.40** $\mathrm{dim}\,\mathbb{F}^{m,n}=mn$.
Suppose $m$ and $n$ are positive integers. With addition and scalar multiplication defined as above, $\mathbb{F}^{m,n}$ is a vector space with dimension $mn$. 

---
### Matrix Multiplication
**3.41 Definition** *matrix multiplication*
Suppose $A$ is an $m$-by-$n$ matrix and $C$ is an $n$-by-$p$ matrix, then $AC$ is defined to bt the $m$-by-$p$ matrix whose entry in row $j$, column $k$, is given by the following equation: $$(AC)_{j,k}=\sum^n_{r=1}A_{j,r}C_{r,k}.$$ In other words, the entry in row $j$, column $k$ of $AC$ is computed by taking row $j$ of $A$ and column $k$ of $C$, multiplying together corresponding entries, and then summing. 

**3.43 The matrix of the product of linear maps**
If $T\in\mathcal{L}(U,V)$ and $S\in\mathcal{L}(V,W)$, then $\mathcal{M}(ST)=\mathcal{M}(S)\mathcal{M}(T)$. 

**3.44 notation** $A_{j,\cdot},A_{\cdot,k}$
This is just using $\cdot$ as a dummy index. 

**3.47** Entry of a matrix product equals a row times column. 
Suppose $A$ is an $m$-by-$n$ matrix and $C$ is an $n$-by-$p$ matrix; then, $$(AC)_{j,k}=A_{j,\cdot}C_{\cdot,k}$$ for $1\le j\le m$ and $1\le k\le p$. 

This is just the dot product thing row $\cdot$ column said more formally. 

**3.49 Column of a matrix product equals matrix times column**
Suppose $A$ is an $m$-by-$n$ matrix and $C$ is an $n$-by-$p$ matrix; then, $$(AC)_{\cdot,k}=AC_{\cdot,k}$$ for $1\le k\le p$. 

**3.52 Linear combination of columns**
Suppose $A$ is an $m$-by-$n$ matrix and $c=\begin{pmatrix}c_1\\\vdots\\c_n\end{pmatrix}$ is an $n$-by-$1$ matrix, then $$Ac=c_1A_{\cdot,1}+\cdots+c_nA_{\cdot,n}.$$ In other words, $AC$ is a linear combinations of colimns of $A$, with the scalars that multiply the columns coming from $c$. 

---
## 3.D Invertibility and Isomorphic Vector Spaces
### Invertible Linear Maps
**3.53 Definition** *invertible, inverse*
- A linear map $T\in\mathcal{L}(V,W)$ is called *invertible* if there exists a linear map $S\in\mathcal{L}(W,V)$ such that $ST$ equals the identity map on $V$ and $TS$ equals the identity map on $W$
- A linear map $S\in\mathcal{L}(W,V)$ satisfying $ST=I$ and $TS=I$ is called an *inverse* of $T$. 

**3.54 Inverse is Unique**
An invertible linear map has a unique inverse.

**3.55 Notation** $T^{-1}$
If $T$ is invertible, then its inverse is denoted by $T^{-1}$. In other words, if $T\in\mathcal{L}(V,W)$ is invertible, then $T^{-1}$ is the unique element of $\mathcal{L}(V,W)$ such that $T^{-1}T=TT^{-1}=I$.

**3.56 Invertibility is equivalent to injectivity and surjectivity**
A linear map is invertible if and only if it is injective and surjective. 

---
### Isomorphic Vector Spaces
**3.58 Definition** *isomorphism, isomorphic*
- An *isomorphism* is an invertible linear map.
- Two vector spaces are called *isomorphic* if there is an isomorphism from one vector space onto the other one. 

*Note: The Greek word **isos** means equal; the Greek word **morph** means shape, thus, **isomorphic** literally means equal shape.*

**3.59 Dimension shows whether vector spaces are isomorphic**
Two finite-dimensional vector spaces over $\mathbb{F}$ are isomorphic if and only if they have the same dimension. 

**3.60 $\mathcal{L}(V,W)$ and $\mathbb{F}^{m,n}$ are isomorphic**
Suppose $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_m$ is a basis of $W$. Then $\mathcal{M} is an isomorphism between $\mathcal{L}(V,W)$ and $\mathbb{F}^{m,n}$.

**3.61 $\mathrm{dim}\,\mathcal{L}(V,W)=(\dim{V})(\dim{W})$**
Suppose $V$ and $W$ are finite-dimensional. Then $\mathcal{L}(V,W)$ is finite-dimensional and $$\dim\mathcal{L}(V,W)=(\dim{V})(\dim{W}).$$

---
### Linear Maps Thought of as Matrix Multiplication
**3.62 Definition** *matrix of a vector,* $\mathcal{M}(v)$
Suppose $v\in V$ and $v_1,\dots,v_n$ is a basis of $V$. The *matrix of* $v$ with respect to this basis is the $n$-by-$1$ matrix $$\mathcal{M}(v)=\begin{pmatrix}c_1\\\vdots\\c_n\end{pmatrix},$$ where $c_1,\dots,c_n$ are scalars such that $$v=c_1v_1+\cdots+c_nv_n.$$

**3.64** $\mathcal{M}(T)_{\cdot,k}=\mathcal{M}(v_k).$ 
Suppose $T\in\mathcal{L}(V,W)$ and $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_m$ is a basis of $W$. Let $1\le k\le n$. Then the $k^\text{th}$ column of $\mathcal{M}(T)$, which is denoted by $\mathcal{M}(T)_{\cdot,k}$, equals $\mathcal{M}(v_k).$

**3.65 Linear maps act like matrix multiplication**
Suppose $T\in\mathcal{L}(V,W)$ and $v\in V$. Suppose $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_m$ is a basis of $W$, then, $$\mathcal{M}(Tv)=\mathcal{M}(T)\mathcal{M}(v).$$

---
### Operators
**3.67 Definition** *operator*, $\mathcal{L}(V)$
- A linear map from a vector space to itself is called an *operator*.
- The notation $\mathcal{L}(V)$ denotes the set of all operators on $V$. In other words, $\mathcal{L}(V)=\mathcal{L}(V,V)$.

**3.69 Injectivity is equivalent to surjectivity in finite dimensions** 
Suppose $V$ is finite-dimensional and $T\in\mathcal{L}(V)$. Then the following are equivalent:
1. $T$ is invertible;
2. $T$ is injective;
3. $T$ is surjective.

## 3.E Products and Quotients of Vector Spaces
### Products of Vector Spaces

**3.71 Definition** *product of vector spaces*
Suppose $V_1,\dots,V_m$ are vector spaces over $\mathbb{F}$.
- The *product* $V_1\times\cdots\times V_m$ is defined by $$V_1\times\dots\times V_m=\{(v_1,\dots,v_m):v_1\in V_1,\dots,v_m\in V_m\}$$
- Addition on $V_1\times\dots\times V_m$ is defined by $$(u_1,\dots,u_m)+(v_1,\dots,v_m)=(u_1+v_1,\dots,u_m+v_m).$$
- Scalar multiplication on $V_1\times\cdots\times V_m$ is defined by $$\lambda(v_1,\dots,v_m)=(\lambda v_1,\dots,\lambda v_m).$$

**3.73 Product of vector spaces is a vector space**
Suppose $V_1,\dots,V_m$ are vector spaces over $\mathbb{F}$. Then $V_1\times\cdots\times V_m$ is a vector space over $\mathbb{F}$. 

**3.76 Dimension of a product is the sum of dimensions**
Suppose $V_1,\dots,V_m$ are finite-dimensional vector spaces. Then $V_1\times\dots\times V_m$ is finite-dimensional and $$\dim(V_1\times\cdots\times V_m)=\dim V_1+\cdots+\dim V_m.$$

---
### Products and Direct Sums
**3.77 Products and direct sums**
Suppose that $U_1,\dots,U_m$ are subspaces of $V$. Define a linear map $\Gamma: U_1\times\cdots\times U_m\rightarrow U_1+\cdots+U_m$ by $$\Gamma(u_1,\dots,u_m)=u_1+\cdots+u_m.$$ Then $U_1+\cdots+U_m$ is a direct sum if and only if $\Gamma$ is injective.

**3.78 A sum is a direct sum if and only if dimensions add up**
Suppose $V$ is a finite-dimensional and $U_1,\dots,U_m$ are subspaces of $V$. Then $U_1+\cdots+U_m$ is a direct sum if and only if $$\dim(U_1+\cdots+U_m)=\dim\,U_1+\cdots+\dim\,U_m.$$

---
### Quotients of Vector Spaces

**3.79 Definition** $v+U$
Suppose $v\in V$ and $U$ is a subspace of $V$. Then $v+U$ is a subset of $V$ defined by $$v+U=\{v+u:u\in U\}.$$

**3.81 Definition** *affine subset, parallel*
- An *affine subset* of $V$ is a subset of $V$ of the form $v+U$ for some $v\in V$ and some subspace $U$ of $V$.
- For $v\in V$ and $U$ a subspace of $V$, the affine subset $v+U$ is said to be *parallel* to $U$. 

**3.83 Definition** *quotient spaces*
Suppose $U$ is a subspace of $V$, Then the *quotient space* $V/U$ is the set of all affine subsets of $V$ parallel to $U$. In othe words, $$V/U=\{v+U:v\in V\}.$$

**3.85 Two affine subsets parallel to $U$ are equal or disjoint**
Suppose $U$ is a subspace of $V$ and $v,w\in V$. Then the following are equivalent: 
1. $v-w\in U;$
2. $v+U=w+U;$
3. $(v+U)\cap(w+U)\neq\emptyset$

**3.86 Definition** *addition and scalar multiplication on* $V/U$ 
Suppose $U$ is a subspace of $V$. Then *addition* and *scalar multiplication* are defined on $V/U$ by $$(v+U)+(w+U)=(v+w)+U$$$$\lambda(v+U)=(\lambda v)+U$$ for all $v,w\in V$ and $\lambda\in\mathbb{F}$.

**3.87 Quotient Space is a vector space**
Suppose $U$ is a subspace of $V$. Then $V/U$, with the operations of addition and scalar multiplication as defined above, is a vector space.

**3.88 Definition** *quotient map*, $\pi$
Suppose $U$ is a subspace of $V$. The *quotient map* $\pi$ is the linear map $\pi:V\rightarrow V/U$ defined by $$\pi(v)=v+U$$ for $v\in V$.

**3.89 Dimension of a quotient space** 
Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then $$\dim V/U=\dim V-\dim U.$$

**3.90 Definition** $\tilde{T}$
Suppose $T\in\mathcal{L}(V,W)$. Define $\tilde{T}:V/(\mathrm{null}\,{T})\rightarrow W$ by $$\tilde{T}(v+\mathrm{null}\,T)=Tv.$$

**3.91 Null space and range of $\tilde{T}$**
Suppose $T\in\mathcal{L}(V,W), then,
1. $\tilde{T} is a linear map from $V/(\mathrm{null}\,T)\rightarrow W$;
2. $\tilde{T} is injective;
3. range $\tilde{T}$=range $T$;
4. $V/(\mathrm{null}\,T)$ is isomorphic to range $T$. 

## 3.F Duality
### The Dual Spaec and the Dual Map
**3.92 Definition** *linear functional*
A *linear functional* on $V$ is a linear map $V$ to $\mathbb{F}$. In other words, a linear functional is an element of $\mathcal{L}(V,\mathbb{F})$. 

**3.94 Definition** *dual space*, $V'$
The *dual space* of $V$, denoted $V'$, is the vector space of all linear functionals on $V$. In other words, $V'=\mathcal{L}(V,\mathbb{F})$. 

**3.95** $\dim V'=\dim V$
Suppose $V$ is finite-dimensional. Then $V'$ is also finite-dimensional and $\dim V'=\dim V$. 

**3.96 Definition** *dual basis*
If $v_1,\dots,v_n$ is a basis of $V$, then the *dual basis* of $v_1,\dots,v_n$ is the list $\phi_1,\dots,\phi_n$ of elements of $V'$, where each $\phi_j$ is the linear functional on $V$ such that $$\phi_j(v_k)=\begin{cases}1\quad\text{if}\,k=j\\0\quad\text{if}\,j\neq j\end{cases}$$

**3.98 Dual basis is a basis of the dual space**
Suppes $V$ is finite-dimensional. Then the dual basis of a basis of $V$ is a basis of $V'$. 

**3.99 Definition** *dual map*, $T'$
If $T\in\mathcal{L}(V,W)$, then the *dual map* of $T$ is the linear map $T'\in\mathcal{L}(W',V')$ defined by $T'(\phi)=\phi\circ T$ for $\phi\in W'$. 

**3.101 Algebraic properties of dual maps**
- $(S+T)'=S'+T'\,\forall\,S,T\in\mathcal{L}(V,W).$
- $(\lambda T)'=\lambda T'\:\forall\,\lambda\in\mathbb{F}\,\land\,T\in\mathcal{L}(V,W)$.
- $(ST)'=T'S'\:\forall\:T\in\mathcal{L}(U,V)\:\land\:S\in\mathcal{L}(V,W)$.

---
### The Null Space and Range of the Dual of a Linear Map

**3.102 Definition** *annihilator*; $U^0$
For $U\subset V$, the **annihilator** of $U$, denoted $U^0$, is defined by $$U^0=\{\phi\in V':\phi(u)=0\quad\forall\:u\in U\}.$$

**3.105 The annihilator is a subspace**
Suppose $U\subset V$. Then $U^0$ is a subspace of $V'$.

**3.106 Dimension of the annihilator**
Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$, then $$\dim{U}+\dim{U^0}=\dim{V}.$$

**3.107 The null space of $T'$**
Suppose $V$ and $W$ are finite-dimensional and $T\in\mathcal{L}(V,W)$, then, 
1. $\mathrm{null}\,T'=(\mathrm{range}\,T)^0;$
2. $\mathrm{dim}\:\mathrm{null}\:T'=\mathrm{dim}\:\mathrm{null}\:T+\mathrm{dim}\:W-\mathrm{dim}\:V.$

**3.108 $T$ is surjective is equivalent to $T'$ injective**
Suppose $V$ and $W$ are finite-dimensional and $T\in\mathcal{L}(V,W)$. Then $T$ is surjective if and only if $T'$ is injective. 

**3.109 The range of $T'$**
Suppose $V$ and $W$ are finite-dimensional and $T\in\mathcal{L}(V,W)$, then,
1. $\mathrm{dim}\;\mathrm{range}\:T'=\mathrm{dim}\;\mathrm{range}\:T;$
2. $\mathrm{range}\;T'=(\mathrm{null}\;T)^0$.

**3.110 $T$ injective is equivalent to $T'$ surjective**
Suppose $V$ and $W$ are finite-dimensional and $T\in\mathcal{L}(V,W)$. Then $T$ is injective if and only if $T'$ is surjective. 

---
### The Matrix of the Dual of a Linear Map
**3.111 Definition** *transpose,* $A^t$
The **transpose** of a matrix $A$, denoted $A^t$, is the matrix obtained from $A$ by interchanging the rows and columns. More specifically, if $A$ is an $m$-by-$n$ matrix, then $A^t$ is the $n$-by-$m$ matrix whose entriess are given by the equation $$(A^t)_{k,j}=A_{j,k}.$$

**3.113 The transpose of the product of matrices**
If $A$ is an $m$-by-$n$ matrix and $C$ is an $n$-by-$p$ matrix, then $(AC)^t=C^tA^t$. 

**3.114 The matrix of $T'$ is the transpose of the matrix of $T$.**
Suppose $T\in\mathcal{L}(V,W).$ Then $\mathcal{M}(T')=(\mathcal{M}(T))^t$.

---
### The Rank of a Matrix
**3.115 Definition** *row rank, column rank*
Suppose $A$ is an $m$-by-$n$ matrix with entries $\mathbb{F}$.
- The *row rank* of $A$ is the dimension of the span of the rows of $A$ in $\mathbb{F}^{1,n}.$
- The *column rank* of $A$ is the dimension of the span of the columns of $A$ in $\mathbb{F}^{m,1}$.

**3.117 Dimension of $\mathrm{range}\:T$ equals column rank of $\mathcal{M}(T)$**
Suppose $V$ and $W$ are finite-dimensional and $T\in\mathcal{L}(V,W)$, then, $\mathrm{dim}\:\mathrm{range}\:T$ equals the column rank of $\mathcal{M}(T)$.

**3.118 Row rank equals column rank**
Suppose $A\in\mathbb{F}^{m,n}$, then, the row rank of $A$ equals the column rank of $A$. 

**3.119 Definition** *rank*
The *rank* of a matrix $A\in\mathbb{F}^{m,n}$ is the column rank of $A$. 
