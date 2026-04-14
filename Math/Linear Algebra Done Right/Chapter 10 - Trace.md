---
title: Chapter 10 - Trace

---

# Chapter 10 - Trace and Determinant
**Notation** $\mathbb{F},V$
- $\mathbb{F}$ denotes $\mathbb{R}$ or $\mathbb{C}$. 
- $V$ denotes a finite-dimensional nonzero vector space over $\mathbb{F}$. 

---
$$\text{Learning Objectives of this Chapter}$$
- Change of basis and its effect upon the matrix of an operator
- trace of an operator and of a matrix
- determinant of an operator and of a matrix
- determinants and volume

## 10.A Trace
### Change of Basis
**10.2 Definition** *identity matrix*, $I$
Suppose $n$ is a positive integer. The $n$-by-$n$ diagonal matrix $$\begin{pmatrix}1&&0\\&\ddots&\\0&&1\end{pmatrix}$$ is called the **identity matrix** and is denoted $I$. 

**10.3 Definition** *invertible, inverse*, $A^{-1}$
A square matrix $A$ is called invertible if there is a square matrix $V$ of the same size such that $AB=BA=I$; we call $B$ the **inverse** of $A$ and denote it by $A^{-1}$. 

**10.4 The matrix of the product of linear maps**
Suppose $u_1,\dots,u_n$ and $v_1,\dots,v_n$ and $w_1,\dots,w_n$ are all bases of $V$. Suppose $S,T\in\mathcal{L}(V)$, then $$\mathcal{M}(ST,u_1,\dots,u_n),(w_1,\dots,w_n))=$$ $$\mathcal{M}(S,(v_1,\dots,v_n),(w_1,\dots,w_n))\mathcal{M}(T,(u_1,\dots,u_n),(v_1,\dots,v_n))$$

I don't think there is much in this chapter to improve upon my current knowledge, I'd much prefer some more calculation type questions around these, so I think I'll call the book here.
