---
title: Lecture 4
tags: [Mechanics II]

---

# Lecture 4
### Brief overview of Lecture 3
Cartesian and other coordinate systems. 
Vector calculus: $$\vec{r}=x_1\hat{e}_1+\cdots+x_n+\hat{e}_n\quad\text{Position}$$ $$\vdots$$


$\phi(x,y,z)\quad\vec{A}(x,y,z)$ (Not sure what he said about these, maybe scalar versus vector quantities?)

Del operator: $$\nabla\equiv\frac{partial}{\partial x}\hat{x}+\frac{partial}{\partial y}\hat{y}+\frac{partial}{\partial z}\hat{z}.$$

Divergence, gradient, and curl covered again. 
-$\nabla\phi$ - Gradient
-$\nabla\cdot\vec{A}$ - Divergence
-$\nabla\times\vec{A}$ - Curl

Laplacian: $$\nabla^2\psi=\sum_i\frac{\partial^2\psi}{\partial_xi^2}.$$

---
## Lecture 4 Start

Example of Gradiant: 
$\nabla f(x,y,z)$, where $f(x,y,z)=e^x\sin{y}\ln{z}$: $$\nabla f(x,y,z)=\langle e^x\sin{y}\ln{z},\,e^x\cos{y}\ln{z},\,\frac{e^x\sin{y}}{z}\rangle.$$

Example of Divergence:
$\vec{\nabla}\cdot\vec{V}$, where $\vec{V}=\langle xy,2yz,3zx\rangle$. $$\begin{aligned}\vec{\nabla}\cdot\vec{V}&=\vec{\nabla}\cdot\langle xy,2yz,3zx\rangle\\&=y+2z+3x\end{aligned}$$

Example of Curl:
$\vec{\nabla}\times \vec{V}$ where $\vec{V}=\langle -y,x,0\rangle$: $$\vec{\nabla}\times\vec{V}$$

Example of Laplacian: $\vec{T}=x^2+2xy+3z+4$ and $\vec{V}=\langle x^2,\,3xz^2,\,-2xz\rangle$ $$\nabla^2\,T=\nabla(\nabla\,T)$$ $$\nabla^2\,\vec{V}=\nabla(\nabla\,\vec{V})$$

---
### Line Integral, Surface Integral, and Volume Integral
$$\int^\text{Line}\vec{A}\cdot d\vec{\ell}\rightarrow\text{Vector Quantity}$$
$$\int^\text{Surface}\vec{A}\cdot d\vec{a}\rightarrow\text{Vector Quantity}$$
$$\int^\text{Volume}\,d\tau\rightarrow\text{Scalar Quantity}$$

---
**Line integral Example**
Calculate the line integral of the function $\vec{v}=\langle y^2,2x(y+1)\rangle$ from the point $a=(1,1,0)$ to the point $b=(2,2,0)$, along the paths (1) and (2). What is $\oint\vec{v}\cdot d\vec{\ell}$ for hte loop that goes along $a\rightarrow b$ along (1) and then returns to $a$ along (2). (Too lazy to draw diagram)
$$\oint\vec{V}\cdot d\vec{\ell}\,_{(1)}=\int\vec{V} d\vec{\ell}_{{a\rightarrow b}\,_{(i)}}+\int\vec{V}\cdot d\vec{\ell}_{{b\rightarrow a}\,_{(ii)}}$$ $$\int\vec{V} d\vec{\ell}_{{a\rightarrow b}\,_{(i)}}=0+\int_1^21\,dx=1$$ $$\int\vec{V}\cdot d\vec{\ell}_{{b\rightarrow a}\,_{(ii)}}=0+\int_1^24(y+1)\,dy=10$$ $$\oint\vec{V}\cdot d\vec{\ell}\,_{(1)}=11$$

We seem to be out of time for the returning path, but the line 2 is simply $y=x\quad y\in[1,2]$.