---
title: Lecture 2
tags: [Mechanics II]

---

# Lecture 2

## Introduction to Matrices
Used for solving homogeneous linear equations.
Standard form for this $$A\vec{x}=B.$$ 
$$\begin{pmatrix}
A_{11}&\cdots&A_{1n}\\\vdots&\ddots&\vdots\\A_{n1}&\cdots&A_{nn}\end{pmatrix}\begin{pmatrix}x_1\\\vdots\\x_n\end{pmatrix}=\begin{pmatrix}b_1\\\vdots\\b_n\end{pmatrix}.$$

$A_{nn}$ represents a square matrix with $n$ rows and $n$ columns.

---
### Change of Basis (He used Rotation as exact example)
![image](https://hackmd.io/_uploads/SyyPVEHSWl.png)


---
I lost him he's talking about $\lambda_{11}$ but I don't think he's talking about eigenvalues.

Oh he just means matrix entries and he's talking about making systems of linear equation:$$\begin{aligned}x_1'&=\lambda_{11}x_1+\lambda_{12}x_2\\x_2'&=\lambda_{21}x_1+\lambda_{22}x_2\end{aligned}$$ can be represented as $$\begin{pmatrix}x_1'\\x_2'\end{pmatrix}=\begin{pmatrix}x_1\\x_2\end{pmatrix}\begin{pmatrix}\lambda_{11}&\lambda_{12}\\\lambda_{21}&\lambda_{22}\end{pmatrix}.$$

---
Matrix characteristics:
- $a_{ij}$ - element of row $i$ column $j$.
- $M_{ij}$ - Minor of element in row $i$ column $j$.
- $c_{ij}$ - Cofactor of row $i$ column $j$. 

For the Minor of say, row 1 column 1 ($M_{11}$), to use the minor we have the matrix remaining if we removed column 1 and row 1: 

The cofactor is the sign of the minor, given by $(-1)^{i+j}$.

![image](https://hackmd.io/_uploads/Skj_U4BBZg.png)

These can be used to calculate the determinant, which wasn't detailed at this point in the lecture. (Look up cofactor formula, as a smaller version of 'big formula'). 

---
### Matrix Inverse

$A^{-1}A\vec{x}=A^{-1}B$
$A^{-1}A=I$
$I$ is the identity matrix, which is all zeroes outside of the main diagonal which is all 1.

$A^{-1}=\frac{\mathrm{adj}(A)}{\mathrm{det}(A)}$.

$\mathrm{adj}(A)$ is the adjoint of the matrix. 
The adjoint is the transpose of the cofactor matrix.

Transpose is swapping rows with columns, $$\text{Transpose:}\quad(A_{ij})^T=A_{ji}$$

---
Example, maybe

$$x+y=5$$ $$2x+2y=10$$ and $$x+y=5$$ $$x-y=-1$$ When given a set of linear equations you can achieve: 
- No solution
- Many solutions
- Unique solution

He said the first one has many solutions and erased everything. (The reason for this geometrically is that they are two overlapping lines, so any point on either of the infinitely long lines is an intersection of both lines.)

---
Possibly an example again
$$2x+y+z=7$$ $$3x-2y+5z=14$$ $$0x+2y+z=7$$
Into a matrices: $$\begin{pmatrix}2&1&1\\3&-2&5\\0&2&1\end{pmatrix}\begin{pmatrix}x\\y\\z\end{pmatrix}=\begin{pmatrix}7\\16\\7\end{pmatrix}.$$
Doing the cofactor formula: $$|A|=c_{11}+c_{12}+c_{13}+\dots$$$$\mathrm{det}\begin{pmatrix}2&1&1\\3&-2&5\\0&2&1\end{pmatrix}=-21$$

And then finding the cofactor matrix: $$\mathrm{cofactor}\begin{pmatrix}2&1&1\\3&-2&5\\0&2&1\end{pmatrix}=\begin{pmatrix}-12&-3&6\\1&2&4\\7&7&-7\end{pmatrix}.$$ $$\mathrm{adjoint}\begin{pmatrix}2&1&1\\3&-2&5\\0&2&1\end{pmatrix}=\begin{pmatrix}-12&1&7\\-3&2&-7\\6&-4&-7\end{pmatrix}.$$$$\mathrm{inverse}\begin{pmatrix}2&1&1\\3&-2&5\\0&2&1\end{pmatrix}=\frac{1}{21}\begin{pmatrix}-12&1&7\\-3&2&-7\\6&-4&-7\end{pmatrix}.$$ Finally, $$\frac{1}{21}\begin{pmatrix}-12&1&7\\-3&2&-7\\6&-4&-7\end{pmatrix}\begin{pmatrix}7\\14\\7\end{pmatrix}=\begin{pmatrix}1\\2\\3\end{pmatrix}$$