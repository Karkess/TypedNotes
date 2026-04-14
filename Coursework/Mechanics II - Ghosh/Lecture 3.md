---
title: Lecture 3
tags: [Mechanics II]

---

# Lecture 3
### Quick review of last lecture:
General matrix formula: $A\vec{x}=B$
Solution form: $\vec{x}=A^{-1}B$
Inverse formula: $A^{-1}=\frac{\mathrm{adj}\,A}{\mathrm{det}\,A}$
Matrix elements:
- $a_{ij}$ - Element in row $i$ and column $j$
- $c_{ij}$ - Cofactor element of row $i$ and column $j$
- $m_{ij}$ - Minor element of row $i$ and column $j$

Adjoint matrix (Transpose of the cofactor matrix): $$\mathrm{adj}(A)=\begin{pmatrix}c_{11}&c_{21}&\cdots\\c_{12}&\ddots&\\\vdots&&c_{ji}\end{pmatrix}.$$

Transpose: $(A_{ij})^\text{T}=A_{ji}$ (Swapping rows and columns).

---
### Lecture starts
A brief review of coordinate systems, with four listed:
- $(x,y,z)$ - Cartesian
- $(r,\theta,\phi)$ - Spherical
- $(p,\phi,z)$ - Cylindrical
- $(q_1,q_2,q_3)$ - Generalized

![image](https://hackmd.io/_uploads/SJREwADBbg.png)
An example point in spherical coordinates.

---
Reviewed the interpretation of vectors as arrows:

![image](https://hackmd.io/_uploads/ByyFDAwBZg.png)

A review of vector magnitude: $$|A|=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2+(z_2-z_1)^2}$$

Dot product definition: $$\vec{A}\cdot\vec{B}=|A|\,|B|\cos{\theta}$$

Cross product definition: 
$$\vec{A}\times\vec{B}=|A|\,|B|\sin{\theta}\cdot\hat{n}$$ where $\hat{n}$ is a unit vector in the direction $\vec{n}$. 

Cross product by determinant review. 
Triple product $\vec{A}\cdot(\vec{B}\times\vec{C})$. This formula is actually the same as the cross product, a $3\times3$ determinant, but instead of directions $(\hat{x},\hat{y},\hat{z})$ as our row 1, we have our vector $\vec{A}$. 

---
### Operators
Talking about the $\nabla$ operator.
Gradient: $\nabla\vec{A}$, $$\nabla\vec{A}=\frac{d\vec{A}}{dx}\hat{x}+\frac{d\vec{A}}{dy}\hat{y}+\frac{d\vec{A}}{dz}\hat{z}.$$

Divergence: $\vec{\nabla}\cdot\vec{A}$ $$\vec{\nabla}\cdot\vec{A}=\frac{\partial A_x}{\partial x}+\frac{\partial A_y}{\partial y}+\frac{\partial A_z}{\partial z}$$


Curl: $\vec{\nabla}\times\vec{A}$