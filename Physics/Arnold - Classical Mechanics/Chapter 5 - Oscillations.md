---
title: Chapter 5 - Oscillations

---

# Chapter 5 - Oscillations
## 22 - Linearization
### A. Equilibrium Positions

**Definition.** A point $x_0$ is called an *equilibrium position* of the system (1)$$\frac{d\vec{x}}{dt}=\vec{f}(\vec{x}),\quad\vec{x}\in\mathbb{R}^n$$ if $\vec{x}(t)\equiv x_0$ is a solution of this system. In other words, $\vec{f}(\vec{x}_0)=0$, id est, the vector field $\vec{f}(\vec{x})$ is zero at $x_0$. 

**Theorem.** *The point $\vec{q}=\vec{q}_0, \dot{\vec{q}}=\dot{\vec{q}}_0$ will be an equilibrium position if and only if $\dot{\vec{q}}_0=0$ and $\vec{q}_0$ is a critical point of the potential energy, id est, $$\frac{\partial U}{\partial\vec{q}}\bigg|_{\vec{q}_0}=0$$*

---
### B. Stability of Equilibrium Positions
**Theorem.** *If the point $\vec{q}_0$ is a strict local minimum of the potential energy $U$, then the equilibrium position $\vec{q}=\vec{q}_0$ is stable in the sense of Liapunov.*

---
### C. Linearization of a Differential Equation
Studying systems of the form given by the first equation in this chapter (1) can produce solutions close to the equilibrium position $x_0$. Then the first term of the Taylor series for $\vec{f}$ is linear: $$\vec{f}(\vec{x})=A\vec{x}+R_2(\vec{x}),\quad A=\frac{\partial\vec{f}}{\partial\vec{x}}\bigg|_0\text{ and }R_2=\mathcal{O}(\vec{x}^2),$$ wheret he linear operator $A$ is given in coordinates $x_1,\dots,x_n$ by the matrix $a_{ij}$:$$A(\vec{x})_i=\sum a_{ij}x_j:\quad a_{ij}=\frac{\partial f_i}{\partial x_j}.$$

This Matrix is the Jacobian, which tells you how little changes in input produce little changes in output, that's why we see it in tensor calc as well as linearization. 

---
### D. Linearization of a Lagrangian System
**Theorem.** *In order to linearize the Lagrangian system in a neighbohood of the equilibrium position $\vec{q}=0$, it is sufficient to replace the kinetic energy $$T=\frac{1}{2}a_{ij}(\vec{q})\dot{q}_i\dot{q}_j,\quad a_{ij}=a_{ij}(0)$$ and replace the potential energy $U(\vec{q})$ by its quadratic part $$U_2=\frac{1}{2}\sum b_{ij}q_iq_j,\quad b_{ij}=\frac{\partial^2U}{\partial q_i\partial q_j}\bigg|_{q=0}.$$*

**Note:** Here, $T_2$ and $U_2$ are notation for keeping the Taylor approximation up to the second term.

**Corollary.** *The period $\tau$ of oscillations close to the equilibrium position $\tau_0=\frac{2\pi}{\omega_0}$, (where $\omega^2_0=\frac{b}{a},\,b=\frac{\partial^2U}{\partial q^2}\bigg|_{q=q_0},\text{ and }a=a(q_0))$ as amplitudes of the oscillations decrease.*

This is just leading into our small oscillations, and just saying that most systems basically act almost entirely off of their second derivative of the potential energy near their local minima. 

---
### E. Small Oscillations
**Definition.** Motions in a linearized system $(L_2=T_2-U_2)$ are called *small oscillations* near an equilibrium $\vec{q}=\vec{q}_0$. In a one-dimensional problem the numbers $\tau_0$ and $\omega_0$ are called the *period* and the *frequency* of small oscillations. 

---
## 23. Small Oscillations
### A. A problem about pairs of forms

We will dig deeper into the problem of small oscillations by consdering a system who's kinetic and potential energies are quadratic forms: $$T=\frac{1}{2}(A\dot{\vec{q}},\dot{\vec{q}})\quad U=\frac{1}{2}(B\vec{q},\vec{q})\quad\vec{q}\in\mathbb{R}^n,\dot{\vec{q}}\in\mathbb{R}^n.$$ The kinetic energy is a positive-definite form. 

A pair of quadratic forms, $(A\vec{q},\vec{q}),(B\vec{q},\vec{q})$, the first of which is positive definite, can be reduced to principle axes by a linear change of coordinates: $$\vec{Q}=C\vec{q}\quad\vec{Q}=(Q_1,\dots,Q_n).$$ In addition, the coordinates $\vec{Q}$ can be chosen so that the form $(A\vec{q},\vec{q})$ decomposes into the sum of squares $(\vec{Q},\vec{Q})$. Let $\vec{Q}$ be such coordinates, then since $\dot{\vec{Q}}=C\dot{\vec{q}}$ we have $$T=\frac{1}{2}\sum^n_{i=1}\dot{Q}_i^2\quad U=\frac{1}{2}\sum^n_{i=1}\lambda_iQ_i^2.$$ The numbers $\lambda_i$ are called the *eigenvalues of the form $B$ with respect to $A$.*

---
Okay so I hardly understood this section but it turns out it's just saying we basically diagonalize the system $A^{-1}B$ which gives us independent oscillators and their frequency is $\lambda_i$. These quadratic forms generate sets of level curves, and we try and rotate the coordinate system such that the resultant coordinates eliminate cross terms (For 2D level curves that are quadratic forms this essentially is deforming an ellipse into a circle). 

Quadratic forms in general are just a way to measure how much of some geometric object, and when it's positive definite this is the magnitude. 

---
### B. Characteristic Oscillations
In the coordinates $\vec{Q}$ the Lagrangian system decomposes into $n$ independent equations $$\ddot{Q}=-\lambda_iQ_i.$$

Thus we have proved:
**Theorem.** *A system performing small oscillations is the direct product of $n$ one-dimensional systems performing small oscillations*. 

---
**Corollary.** *Suppose one of the eigenvalues is positive: $\lambda=\omega^2>0$. Then the system can perform small oscillations of the form $$\vec{q}(t)=(C_1\cos\omega t+C_2\sin\omega t)\xi,$$ where $\xi$ is an eigenvector corresponding to $\lambda$.*

**Definition.** This periodic motion is called a *characteristic oscillation* of the system, and the number $\omega$ is called the *characteristic frequency*.

---
### C. Decomposition into characteristic oscillations
**Corollary.** *Every small oscillation is a sum of characteristic oscillations.*

A general solution for characteristic oscillations from LAgrange's equations can be found when $\lambda\neq0$ with the form $$\vec{q}(t)=\mathrm{Re}\sum^n_{k=1}C_ke^{i\omega_kt}\xi_k$$

## 24. Behavior of Characteristic Frequencies