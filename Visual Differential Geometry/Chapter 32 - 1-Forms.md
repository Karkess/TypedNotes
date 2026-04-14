---
title: Chapter 32 - 1-Forms
tags: [Act V - Forms]

---

# Chapter 32 - 1-Forms
## 32.1 Introduction
Forms come from a type of calculus whose full name is sometimes called ***The Exterior Calculus of Differential Forms***. 

Forms were discovered by Cartan around the turn of the 20ths century. 

## 32.2 Definition of a 1-Form
**Definition.** *A **1-form** is a linear real valued function of a single vector input.*

Note, the '1-' is an indicator of the single vector input. 2-forms have two vector inputs, and k-forms have k vector inputs. 

Older works might call a 1-form a *covariant vector* or a **covector**. 

---
These 1-forms do normal vector space stuff: $$\omega\text{ is a 1-form }\quad\iff\quad\omega(k_1c_1+k_2v_2)=k_1\,\omega(v_1)+k_2\,\omega(v_2).$$ This is the natural way to check that a particular $\omega$ is a 1-form and can be split into two steps: $$\begin{cases}\omega(v_1+v_2)&=\omega(v_1)+\omega(v_2)\\\omega(kv)&=k\,\omega(v)\end{cases}$$

A 1-form is *Defined* by its action on vector. Two 1-forms are equal if and only if they have the same effect on all vectors.

## 32.3 Examples of 1-Forms
*Gravitational work*
Gravitational work can be described as the 1-form $$\omega(v)\equiv\text{ work done moving the mass along }v$$ because we input one vector and output a value. 

This is why we dot the differential when integrating for work $\vec{F}\cdot\,d\vec{r}$. Here, $\vec{F}$ would be the 1-form. 

We can represent this in tensorial notation and think of these as vectors and covectors, $\int_\gamma F_i\,dr^i$, giving us this path dependence. This notation makies it a bit clearer that 1-forms can be interpreted or represented by simple tensors. 

---
*Visualizing the Gravitational Work 1-form*
The function of these one forms can be thought of as taking a contour map and the vector pierces a number of these level planes, and the number of planes it pierces correlates to the value once evaluated. 
![image](https://hackmd.io/_uploads/Sklp59I2bg.png)
$$\omega(\vec{v})=\text{ number of surfaces of }\omega\text{ pieces by }\vec{v}.$$

---
*Row Vectors*
Row vectors can be thought of as 1-forms, if we think of work, the row vector would be $$\omega=\begin{pmatrix}0&0&F\end{pmatrix},\quad\text{because then}\quad\omega(\vec{v})=\begin{pmatrix}0&0&F\end{pmatrix}\begin{pmatrix}x\\y\\h\end{pmatrix}=Fh=\text{work}.$$

---
*Dirac's Bras*
Treating the kets in quantum mechanics as state vectors, then the bra is a 1 form, where we have $$\omega(v)\equiv\langle\omega |v\rangle.$$

## 32.4 Basis 1-Forms
At a point $p$ in an $n$-manifold, suppose that we have chosen a basis $\{\hat{e}_j\}$ for $T_p$, so that a general vector can be written using the Einstein summation convention as $$\vec{v}=v^j\hat{e}_j.$$We shall *not* assume that the basis is orthonormal.
Given this basis, there is a natural way to associate it with a *dual basis* $\{\omega^i\}$ for the space $T^*_p$ of 1-forms at $p:$
$$\omega^i\text{ picks out the i-th component of }v\quad\iff\quad\omega^i(\vec{v})=v^i.$$

While the *set* of basis 1-forms $\{\omega^1,\omega^2\}$ is dual to the *set* of basis vectors $\{\hat{e}_1,\hat{e}_2\}$, $\omega^1$ is not dual to $\hat{e}_1$. 

Equivalent definition of a basis $\{\omega^i\}$: $$\omega^i(\hat{e}_j)=\delta^i_j\quad\iff\quad\omega^i(\vec{v})=v^i.$$

## 32.5 Components of a 1-Form
Let the general 1-form $\varphi$ act on the general vector $\vec{v}$: $$\begin{aligned}\varphi(\vec{v})&=\varphi(v\,^j\,\hat{e}_j)\\&=v\,^j\varphi(\hat{e}_j)\\&=\omega\,^j(\vec{v})\,\varphi(\hat{e}_j).\end{aligned}$$
We now define the components of $\varphi_j$ of $\varphi$: $$\varphi_j\equiv\varphi(\hat{e}_j)$$

## 32.6 The Gradient as a 1-Form: df
*Review of the Gradiant as a vector: $\nabla f$*
Recall that the *Gradient* of a function $f$ is defined as $$\nabla f\equiv\begin{bmatrix}\partial_xf\\\partial_yf\end{bmatrix}.$$
The significance of the vector is that:
*$\nabla f$ points in the direction of the most rapid increase of $f$, and its magnitude $|\nabla f|$ equals the maximum rate of increase of $f$ with distance as we move in that direction.*

We now derive this from a more primitive fact. 
Let $\{\hat{e}_1,\hat{e}_2\}$ be the standard orthonormal basis along the $(x^1,x^2)=(x,y)$ axes, and let $\delta f$ be the small change in $f$ from moving along the short vector $$\vec{v}=\delta x^1\hat{e}_1+\delta x^2\hat{e}_2=\begin{bmatrix}\delta x\\\delta y\end{bmatrix}.$$By definition, $\partial_xf$ is the rate of change of $f$ as we move in the $x-direction$, so the change in $f$ resulting from moving $\delta x$ is ultimately equal to $(\partial_xf)\delta x;$ and likewise for $y$, therefore, $$\delta f=(\partial_xf)\delta x+(\partial_yf)\delta y=(\nabla f)\cdot\vec{v}.$$ IF we interpret this geometrically, and keep the length $|\vec{v}|\equiv\delta s$ fixed, then as $\vec{v}$ rotates around a circle, $$\delta f=|\nabla f|(\delta s\cos{\theta}),$$ where $\theta$ is the angle that $\vec{v}$ makes with the gradient $\nabla f$ so that $(\delta s\cos\theta)$ is simply the projection of $\vec{v}$ onto the direction of $\nabla f$. 
Let $\hat{v}=\frac{\vec{v}}{|\vec{v}|}$ be the unit vector in the direction of $\vec{v}$, we can express the result as $$|\nabla_\hat{v}f=\frac{df}{ds}=|\nabla f|\cos\theta.$$
This immediately confirms the interpretation of $\nabla f$ given when stating the significance. IT also shows that if we move in the direction orthogonal to $\nabla f$ then the rate of change of $f$ vanishes. This is the direction of the curve defined by $f=$ constant. 

---
I totally misunderstood the above section thinking I was missing where $\theta$ is sweeping to align with a direction that corresponds to $\nabla f$. Instead it's far simpler, it's using the standard dot product definition and showing that whenever you change direction of the vector away from $\nabla f$ that $\cos \theta$ is the scaling factor at which the magnitude decreases, and thus $\theta=0$ is the direction of maximal increase.

---
*The Gradient as a 1-Form: $\mathbf{d}f$*
The gradient is more naturally a 1-form, which before we explain we will first define as $$\bf{d}f(\vec{v})\equiv\vec{\nabla}_\vec{v}f.$$ The bold $\bf{d}$ operator is called the *exterior derivative*. 

---
*The Cartesian 1-Form Basis:* $\{\mathbf{d}x^j\}$
What is the meaning of 1-forms $\mathbf{d}x=\mathbf{d}x^1$ and $\mathbf{d}y=\mathbf{d}x^2$ in $\mathbb{R}^2$ ? 
We shall look at their effect on a general vector: $\vec{v}=\begin{bmatrix}v^1\\v^2\end{bmatrix}$. By definition: $$\begin{aligned}(\mathbf{d}x)\begin{bmatrix}v^1\\v^2\end{bmatrix}&=(\mathbf{d}x)\vec{v}\\&=\vec{\nabla}_\vec{v}x\\&=\vec{\nabla}_{v^1\hat{e}_1+v^2\hat{e}_2}x\\&=(v^1\vec{\nabla}_{\hat{e}_1}+v^2\nabla_{\hat{e}_2})x\\&=(v^1\partial_x+v^2\partial_y)x\\&=v^1.\end{aligned}$$ In words: $\bf{d}x$ is the 1-form that picks out the x-component of a vector. In general: $$(\bf{d}x^i)\hat{e}_j=\delta^i_j.$$It follows that a general 1-form $\varphi$ can be decomposed into components in this dual basis as $$\varphi=\varphi_j=\varphi(\hat{e}_j)\mathbf{d}x^j.$$

---
*The 1-Form Interpretation of* $df=(\partial_xf)dx+(\partial_yf)dy$. 
Taking the above $\varphi=\mathbf{d}f$  we have decomposed the gradient 1-form $\mathbf{D}f of a general function itno its Cartesian basis 1-form components, as follows: $$\mathbf{d}f=[(\mathbf{d}f)\hat{e}_j]\mathbf{d}x^j=[\partial_{x^j}f]\mathbf{d}x^j.$$ 

---
## 32.7 Adding 1-Forms Geometrically
What does the addition of 1-forms mean?
We superimpose the stacks representing 1-forms $\mathbf{d}x$ and $\mathbf{d}y$, and then join the resulting intersection points to make a new stack.