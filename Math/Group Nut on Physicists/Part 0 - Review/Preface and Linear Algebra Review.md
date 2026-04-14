---
title: Preface and Linear Algebra Review
tags: [Part 0 - Review]

---

# Preface

This book essentially seems to be intended to cover about a semester's worth of content (although quite verbose, by design).  It's rather thick and informal, much like the mom of anyone who wastes their time reading my notes, which are written only for the sake of writing something. Intentionally these notes are no better than the book. They are mostly a reduced copy with occasional thoughts, which possess no value to any reader (including myself). 

# A Brief Review of Linear Algebra

Zee mentions a run in with a chicken and a rabbit problem as a kid. As I am rather tired and bored, lets work it out. $x$ chickens, $y$ rabbits. 7 heads and 22 legs, so... 
$$\begin{aligned}
x+y&=7\\
2x+4y&=22\\ \\
x&=7-y\\
2(7-y)+4y&=22\\ \\
14+4y-2y&=22\\
2y&=22-14\\ \\
y&=4 \\
x&=3 \\ \\
3\text{ chickens }&\text{& }4\text{ rabbits}
\end{aligned}$$

I  hope we all had fun (smile).
Damn on the next page he makes fun of us for solving like that. I revoke my prior smile.

---
Zee generalizes it to $M\vec{x}=\vec{u}$ as $$\begin{pmatrix}a&b\\c&d\end{pmatrix}\binom{x}{y}=\binom{u}{v}$$ in matrix form, from the abstracted equations $ax+by=u$ and $ac+dy=v$. 

There are some more general examples to refresh matrix actions on column vectors, although the row dot column method works fine for me. Here he demonstrates $$\begin{pmatrix}a&b\\c&d\end{pmatrix}\binom{x}{y}=\binom{ax+by}{cx+dy}.$$ Without the use of macros, \binom{x}{y} is a good way to make quick two entry column vectors. 

---
Trying 'espanso' here with a key command to quickly write the outline for pmatrices. $\begin{pmatrix}3\\4\\5\end{pmatrix}$ cool it works.

---
Apparently "Matrix" comes from the Latin word for 'womb', which itself is derivative of 'mater'. I should go do my Latin study more often. 

---
We denote entries of matrices as $M_{ij}$, the $i$th row and $j$th column. I have a shockingly difficult time remembering this, which I quite dislike. 

A short exercise. $M_{31}=g\quad M_{23}=f$. 

---
Generalizing multiplying n-dimensional vectors by n-dimension square matrices we achieve: $$u_i=\sum^n_{j=1}M_{ij}x_j.$$ and then we multiply matrices: $$p_i=\sum^n_{j=1}N_{ij}u_j=\sum^n_{j=1}\sum^n_{k=1}N_{ij}M_{jk}x_k=\sum^n_{k=1}P_{ik}x_k.$$

We defined the identity matrix by the classic Kronecker delta $\delta_{ij}$:$$\delta_{ij}=\begin{cases}1\quad\text{if }i=j\\0\quad\text{if }i\neq j\end{cases}\:\:.$$

---
### A few exercises
Zee instructed to do 1 through 5 if you're shaky with multiplying matrices, and I guess I could use more practice.

1. Let $E=\begin{pmatrix}0&1\\1&0\end{pmatrix}$ and $M$ be a $2\times2$ matrix. I'll make a generic one $M=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, show that $E$ is a row exchange.

**Solution:** 
$$\begin{aligned}EM&=\begin{pmatrix}0&1\\1&0\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}\\\begin{pmatrix}0&1\\1&0\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}&=\begin{pmatrix}\begin{pmatrix}0&1\end{pmatrix}\cdot\begin{pmatrix}a\\c\end{pmatrix}&\begin{pmatrix}0&1\end{pmatrix}\cdot\begin{pmatrix}b\\d\end{pmatrix}\\\begin{pmatrix}1&0\end{pmatrix}\cdot\begin{pmatrix}a\\c\end{pmatrix}&\begin{pmatrix}1&0\end{pmatrix}\cdot\begin{pmatrix}b\\d\end{pmatrix}\end{pmatrix}\\&=\begin{pmatrix}0a+1c&0b+1d\\1a+0c&1b+0d\end{pmatrix}\\\\\\EM&=\begin{pmatrix}c&d\\a&b\end{pmatrix}\end{aligned}$$

2. Now $E=\begin{pmatrix}s_1&0\\0&s_2\end{pmatrix}$, find $EM$.

**Solution:** $$EM=\begin{pmatrix}s_1a&s_1b\\s_2c&s_2d\end{pmatrix}$$

3. Now $E_1=\begin{pmatrix}1&0\\s&1\end{pmatrix}$, find EM. Then again for $E_2=\begin{pmatrix}1&s\\0&1\end{pmatrix}$
**Solution**: $$E_1M=\begin{pmatrix}a&b\\as+c&bs+d\end{pmatrix}$$$$E_2M=\begin{pmatrix}a+cs&b+ds\\c&d\end{pmatrix}$$

4. What is this even asking.
5. The LaTeX for this would make me cry if I did it like 1. 

Back to reading.

---
### Einstein's Repeated Index Summation
Whenever there is a summation symbol, the index being summed over is repeated, so Einstein came up with the idea to omit the summation symbol when the index is repeated, like some kind of Einstein. This book uses that notation, so we'd rewrite the earlier equation as $$P_{ik}=N_{ij}M_{jk}.$$

---
### A variety of sections that I'll collapse here
**Not commutative, but associative**
Matrix multiplication is not commutative, in general, $NM\neq MN$, but it is associative $(AB)C=A(BC)$. Then Zee encourages us to explore this with the Pauli matrices, though he doesn't call them that. (Presumably later)

**Transpose**
The superscript $T$ means to exchange rows and columns: $$(M_{ij})^T=M_{ji}.$$ The transpose of the product is the product of the transposes in reverse order: $$(NM)^T=M^TN^T.$$

**Trace** 
The trace of a matrix is the sum of its diagonal elements: $$\mathrm{tr}\,M=\sum_iM_{ii}=M_{ii}.$$
An interesting trace property: $\mathrm{tr}\,AB=\mathrm{tr}\,BA$, despite the products not being equal. 

**The Inverse**
This section just shows the inverse of a $2\times 2$ matrix via determinant formula: $$M^{-1}=\frac{1}{\mathcal{D}}\begin{pmatrix}d&-b\\-c&a\end{pmatrix},$$ where $\mathcal{D}\equiv ad-bc$.

Gives the long equation for $3\times3$ which is frankly just horrible hopefully everyone took linear algebra. 


**The determinant and the Laplace expansion**
This and the next section show how to do the compressed long formula version where you do sub-determinants. The co-something equation, I think.

Several more sections on various determinant things. I may come back to this summary starting at Cramer's Formula on another day. 