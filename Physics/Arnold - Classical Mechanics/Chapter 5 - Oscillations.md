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
Studying systems of the form given by the first equation in this chapter (1) can produce solutions close to the equilibrium position $x_0$. Then the first term of the Taylor series for $\vec{f}$ is linear: $$\vec{f}(\vec{x})=A\vec{x}+R_2(\vec{x}),\quad A=\frac{\partial\vec{f}}{\partial\vec{x}}\bigg|_0\text{ and }R_2=\mathcal{O}(\vec{x}^2),$$ where the linear operator $A$ is given in coordinates $x_1,\dots,x_n$ by the matrix $a_{ij}$:$$A(\vec{x})_i=\sum a_{ij}x_j:\quad a_{ij}=\frac{\partial f_i}{\partial x_j}.$$

This Matrix is the Jacobian, which tells you how little changes in input produce little changes in output, that's why we see it in tensor calc as well as linearization. 

---
### D. Linearization of a Lagrangian System
**Theorem.** *In order to linearize the Lagrangian system in a neighborhood of the equilibrium position $\vec{q}=0$, it is sufficient to replace the kinetic energy $$T=\frac{1}{2}a_{ij}(\vec{q})\dot{q}_i\dot{q}_j,\quad a_{ij}=a_{ij}(0)$$ and replace the potential energy $U(\vec{q})$ by its quadratic part $$U_2=\frac{1}{2}\sum b_{ij}q_iq_j,\quad b_{ij}=\frac{\partial^2U}{\partial q_i\partial q_j}\bigg|_{q=0}.$$*

**Note:** Here, $T_2$ and $U_2$ are notation for keeping the Taylor approximation up to the second term.

**Corollary.** *The period $\tau$ of oscillations close to the equilibrium position $\tau_0=\frac{2\pi}{\omega_0}$, (where $\omega^2_0=\frac{b}{a},\,b=\frac{\partial^2U}{\partial q^2}\bigg|_{q=q_0},\text{ and }a=a(q_0))$ as amplitudes of the oscillations decrease.*

This is just leading into our small oscillations, and just saying that most systems basically act almost entirely off of their second derivative of the potential energy near their local minima. 

---
### E. Small Oscillations
**Definition.** Motions in a linearized system $(L_2=T_2-U_2)$ are called *small oscillations* near an equilibrium $\vec{q}=\vec{q}_0$. In a one-dimensional problem the numbers $\tau_0$ and $\omega_0$ are called the *period* and the *frequency* of small oscillations. 

---
## 23. Small Oscillations
### A. A problem about pairs of forms

We will dig deeper into the problem of small oscillations by considering a system who's kinetic and potential energies are quadratic forms: $$T=\frac{1}{2}(A\dot{\vec{q}},\dot{\vec{q}})\quad U=\frac{1}{2}(B\vec{q},\vec{q})\quad\vec{q}\in\mathbb{R}^n,\dot{\vec{q}}\in\mathbb{R}^n.$$ The kinetic energy is a positive-definite form. 

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

A general solution for characteristic oscillations from Lagrange's equations can be found when $\lambda\neq0$ with the form $$\vec{q}(t)=\mathrm{Re}\sum^n_{k=1}C_ke^{i\omega_kt}\xi_k$$

---
## 24. Behavior of Characteristic Frequencies
This chapter will prove the Rayleigh-Courant-Fisher theorem on the behavior of characteristic frequencies of a system under increases in rigidity and under imposed constraints. 

### A. Behavior of characteristic frequencies under a change in rigidity
Consider a system performing small oscillations, with kinetic and potential energies 
$$T=\frac{1}{2}(A\dv{q},\dv{q})>0\text{   and   }U=\frac{1}{2}(B\v{q},\v{q})>0\quad\forall\;\;\;\v{q},\dv{q}\neq0.$$

**Definition.** A system with the same kinetic energy, and a new potential energy $U'$ is called *more rigid* if $U'=\frac{1}{2}(B'\v{q},\v{q})\ge\frac{1}{2}(B\v{q},\v{q})=U$ for all $\v{q}$. 

**Theorem 1** *Under an increase in rigidity, all the characteristic frequencies are increased, i.e., if $\omega_1\le\omega_2\le\dots\le\omega_n$ are the characteristic frequencies of a less rigid system, and $\omega'_1\le\omega'_2\le\dots\le\omega'_n$ are the characteristic frequencies of the more rigid system, then $\omega_1\le\omega'_1;\dots;\omega_n\le\omega'_n$.*

This theorem has a simple geometric meaning, WLOG we assume if A=E and a euclidean structure where $T=\frac{1}{2}(\dv{q},\dv{q})$, to each system we associate the ellipsoids $E:(B\v{q},\v{q})=1$ and $E':(B'\v{q},\v{q})=1.$, we see that

**Lemma 1.** *If the system $U'$ is more rigid than $U$, then the corresponding ellipsoid $E'$ lies inside $E$.*

We also see that 

**Lemma 2.** *The semi-major axes of the ellipsoid are the inverses of the characteristic frequencies $\omega_i:\omega_i=\frac{1}{a_i}$.*

**Theorem 2.** If the ellipsoid $E$ with a semi-axes $a_1\ge a_2\ge\cdots\ge a_n$ contains the ellipsoid $E'$ with semi-axes $a'_1\ge a'_2\ge\cdots\ge a'_n$, both ellipses having the same center, then the semi-axes inside the ellipsoid are smaller
$$a_1\ge a'_1,\cdots,a_n\ge a'_n.$$

---
### B. Behavior of characteristic frequencies under the imposition of a constraint

We return to a general system with $n$ degrees of freedom, and let $T=\frac{1}{2}(\dv{q},\dv{q})$ and $U=\frac{1}{2}(B\v{q},\v{q})(q\in\R^n)$ be the kinetic and potential energies of a system performing small oscillations. 

Let $\R^{n-1}\subset\R^n$ be an $(n-1)$-dimensional subspace in $\R^n$. Consider the system with $n-1$ degrees of freedom $(q\in\R^{n-1})$ whose kinetic and potential energies are the restrictions of $T$ and $U$ to $\R^{n-1}$. We say this system is obtained from the original by *imposition of a linear constraint*. 

Let $\omega_1\le\dots\le\omega_n$ be the $n$ characteristic frequencies of the original system, and $\omega'_1\le\dots\le\omega'_{n-1}$ the $(n-1)$ characteristic frequencies of the system with a constraint. 

**Theorem 3.** *The characteristic frequencies of the system with a constraint separate the characteristic frequencies of the original system* 
$$\omega_1\le\omega'_1\le\dots\le\omega_{n-1}\le\omega'_{n-1}\le\omega_n$$.

**Theorem 4.** *Consider the cross-section of the n-dimensional ellipsoid $E=\{\v{q}:(B\v{q},\v{q})=1\}$ with semi-axes $a_1\ge a_2\ge\dots\ge a_n$ by a hyperplane $\R^n-1$ through its center. Then the semi-axes of this $(n-1)$-dimensional ellipsoid-the cross section $E'$-separate the semi-axes of the ellipsoid $E$:*
$$a_1\ge a'_1\ge\cdots\ge a_{n-1}\ge a'_{n-1}\ge a_n.$$ 

---
### C. Extremal properties of eigenvalues
**Theorem 5.** *The smallest semi-axis of any cross section of the ellipsoid $E$ with semi-axes $a_1\ge a_2\ge\cdots\ge a_n$ by a subspace $\R^k$ is less than or equal to $a_k$*
$$a_k=\max_{\{\R^k\}}\min_{\v{x}\in\R^k\cap E}||\vec{x}||.$$ *(The upper bound is attained on the subspace spanned by the semi-axes $a_1\ge a_2\ge\cdots\ge a_k$).*