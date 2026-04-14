---
title: Chapter 4 - Lagrangian Mechanics on Manifolds
tags: [Part II - Lagrangian Mechanics]

---

# Part II - Lagrangian Mechanics
## Chapter 4 - Lagrangian Mechanics on Manifolds
In this chapter we introduce the concepts of a differentiable manifold and its tangent bundle. A Lagrangian function, given on the tangent bundle, defines a Lagrangian "holonomic system" on a manifold. Systems of point masses with holonomic constraints (exempli gratia, a pendulum or a rigid body) are special cases.

---
### 17. Holonomic constraints
**A.** *Example*
Let $\gamma$ be a smooth curve in the plane. If there is a very strong force field in a neighborhood of $\gamma$, directed towards the curve, then a moving point will always be close to $\gamma$. In the limit case of an infinite force field, the point must remain on the curve $\gamma$. In this case, we say that a constraint is put on the system. 
To formulate this precisely, we introduce curvilinear coordinates $q_1$ and $q_2$ on a neighborood of $\gamma;\,q_1$ is in the direction of $\gamma$ and $q_2$ is distance from the curve.
We consider a system with potential energy $$U_N=Nq^2_2+U_0(q_1,q_2),$$ depending on the parameter $n$ (which we will let tend to infinity). 
We consider the initial conditions on $\gamma$: $$q_1(0)=q_1^0\quad\dot{q}_1(0)=\dot{q}_1^0\quad q_2(0)=0\quad\dot{q}_2(0)=0.$$ 
Denote by $q_1=\varphi(t,N)$ the evolution of the coordinate $q_1$ under a motion with these initial conditions in the field $U_N$.

**Theorem**. *The following limit exists as $N\rightarrow\infty:$ $$\lim_{N\rightarrow\infty}\varphi(t,N)=\psi(t)$$ The limit $q_1=\psi(t)$ satisfies Lagrange's equation $$\frac{d}{dt}\left(\frac{\partial L_*}{\partial\dot{q}_1}\right)=\frac{\partial L_*}{\partial q_1},$$ where $L_*(q_1,\dot{q}_1)=T|_{q_2=\dot{q}_2=0}$ ($T$ is the kinetic energy of the motion along $\gamma$).*

Thus, as $N\rightarrow\infty$, Lagrange's equations for $q_1$ and $q_2$ induce Lagrange's equation for $q_1=\psi(t)$. 

---
**B.** *Definition of a system with constraints*
**Definition.** Let $\gamma$ be an $m$-dimensional surface in the $3n$-dimensional configuration space of the points $\vec{r}_1,\dots,\vec{r}_n$ with masses $m_1,\dots,m_n$. Let $\vec{q}=(q_1,\dots,q_m)$ be some coordinates on $\gamma:\vec{r}_i=\vec{r}_i(q)$. The system is described by the equations $$\frac{d}{dt}\frac{\partial L}{\partial\dot{\vec{q}}}=\frac{\partial L}{\partial\vec{q}}\quad L=\frac{1}{2}\sum m_i\dot{r}_i^2+U(\vec{q})$$ is called a system of $n$ points with $3n-m$ ideal *holonomic constraints*. The surface $\gamma$ is called the *configuration space of the system with constraints*.
If the surface $\gamma$ is given by $k=3n-m$ functionally independent equations $f_1(\vec{r})=0,\dots,f_k(\vec{r})=0$, then we say that the system is constrained by the relations $f_1=0,\dots,f_k=0.$

Holonomic constraints also could have been defined as the limiting case of a system with a large potential energy. The meaning of these constraints in mechanics lies in the experimentally determined fact that many mechanical systems belong to this class more or less exactly. 

---
### 18. Differential Manifolds
**A.** *Definition of a differential manifold*
A set $M$ is gien the structure of a differentiable manifold if $M$ is provided with a finite or countable collection of *charts*, so that every point is represented in at least one chart.
A chart is an open set $U$ in the euclidean coordinate space $\vec{q}=(q_1,\dots,q_n)$, together with a one-to-one mapping $\varphi$ of $U$ onto some subset of $M,\,\varphi:U\rightarrow\varphi\,U\subset M.$

We assume that if points $\vec{p}$ and $\vec{p}\,'$ in two charts $U$ and $U'$ have the same image in $M$, then $\vec{p}$ and $\vec{p}\,'$ have neighborhoods $V\subset U$ and $V'\subset U'$ with the same image in $M$. In this way we get a mapping $\varphi'\,^{-1}\varphi:V\rightarrow V'$. 

This is a mapping of the region $V$ of the euclidean space $\vec{q}$ onto the region $V'$ of the euclidean space $\vec{q}\,'$, and it is given by $n$ functions of $n$ variables, $\vec{q}\,'=\vec{q}\,'(\vec{q}),\,\,(\vec{q}=\vec{q}(\vec{q}\,')).$ The charts $U$ and $U'$ are called *compatible* if these functions are differentiable. 
An *atlas* is a union of compatible charts. Two atlases are *equivalent* if their union is also an atlas. 
A differentiable manifold is a class of equivalent atlases. We will consider only *connected manifolds*. Then the number $n$ will be the same for all charts; it is called the *dimension* of the manifold. 
A *neighborhood* of a point on a manifold is the image under a mapping $\varphi:U\rightarrow M$ of a neighborhood of the representation of this point in a chart $U$. We assume that every two different points have non-intersecting neighborhoods. 

---
**B.** *Examples*
**Example 1.** Euclidean space $\mathbb{R}^n$ is a manifold, with an atlas consisting of one chart. 
**Example 2.** The sphere $S^2=\{(x,y,z):x^2+y^2+z^2=1\}$ has the structure of a manifold with atlas, for example, consisting of two charts $(U_i,\varphi_i,i=1,2)$

**Definition** The dimension of the configuration space is called the *number of degrees of freedom*.

---
**C.** *Tangent Space*
If $M$ is a $k$-dimensional manifold embedded in $\mathbb{E}^n$, then at every point $\vec{x}$ we have a $k$-dimensional tangent space $TM_x$ is the orthogonal complement to $\{\mathrm{grad}\,f_1,
\dots,\mathrm{grad}\,f_{n-k}\}$. The vectors of the tangent space $TM_x$ based at $x$ are called tangent vectors to $M$ at $x$. We can also define these vectors directly as velocity vectors of curves in $M$. $$\dot{\vec{x}}=\lim_{t\rightarrow0}\frac{\vec{\varphi}(t)-\vec{\varphi}(0)}{t}\text{ where }\vec{\varphi}(0)=\vec{x},\,\vec{\varphi}(t)\in M.$$ 
The definition of tangent vectors can be given in intrinsic terms independent of the embedding of $M$ into $\mathbb{E}^n$. 
We will call two curves, $\vec{x}=\vec{\varphi}(t)$ and $\vec{x}=\vec{\psi}(t)$ *equivalent* if $\vec{\varphi}(0)=\vec{\psi}(0)=\vec{x}$ and $\lim_{t\rightarrow0}(\vec{\varphi{t}}-\vec{\psi}(t))/t=0$ in some chart. Then this tangent relationship is true in any chart.

**Definition.** A *tangent vector* to a manifold $M$ at the point $\vec{x}$ is an equivalence class of curves $\vec{\varphi}(t),$ with $\vec{\varphi}(0)=\vec{x}$

The set of tangent vectors to $M$ at $\vec{x}$ forms a *vector space* $TM_x$. This space is also called the *tangent space* to $M$ at $\vec{x}$.

**Definition**. Let $U$ be a chart of an atlas for $M$ with coordinates $q_1,\dots,q_n$. Then the *components* of the tangent vector to the curve $\vec{q}=\vec{\varphi}(t)$ are the numbers $\xi_1,\dots,\xi_n$, where $\xi_i=(d\varphi_i/dt)|_{t=0}$

---
**D.** *The tangent bundle*
The union of the tangent spaces to $M$ at various points, $\bigcup_{\vec{x}\in M}\,TM_\vec{x}$ has a natural differentiable manifold structure, the dimension of which is twice the dimension of $M$. 
This manifold is called the *tangent bundle* of $M$ and is denoted by $TM$. A point of $TM$ is a vector $\vec{\xi}$, tangent to $M$ at some point $\vec{x}$.
Local coordinates on $TM$ are constructed as follows: 
Let $q_1,\dots,q_n$ be local coordinates on $M$, and $\xi_1,\dots,\xi_n$ components of a tangent vector in this coordinate system.
Then the $2n$ numbers $(q_1,\dots,q_n,\xi_1,\dots\xi_n)$ give a local coordinate system on $TM$. (Sometimes it is written $dq_i$ instead of $\xi_i$.)
The mapping $p:TM\rightarrow M$ which takes a tangent vector $\xi$ to the point $x\in M$ at which the vector is tangent to $M\,(\xi\in TM_\vec{X})$, is called the *natural projection*. The inverse image of a point $\vec{x}\in M$ under the natural projection, $p^{-1}(\vec{x})$ is the tangent space $TM_\vec{x}$. This space is called the *fiber of the tangent bundle over the point $\vec{x}$*.

---
**E.** *Riemannian Manifolds*
If $M$ is a manifold embedded in euclidean space, then the metric on euclidean space allows us to measure the lengths of curves, angles between vectors, volumes, et cetera. All of these quantities are expressed by means of the lengths of the tangent vectors, that is, by the positive-definite quadratic form given on every $TM_{\vec{x}}$ $$TM_\vec{x}\rightarrow\mathbb{R}\quad\vec{\xi}\rightarrow\langle\,\vec{\xi},\vec{\xi}\,\rangle.$$

(For example, the kength of a curve on a manifold is expressed using this form as $(\gamma)=\int^{x_1}_{x_0}\sqrt{\langle d\vec{x},d\vec{x}\rangle}$, or, if the curve is given parametrically, $\gamma:[t_0,t_1]\rightarrow M,t\rightarrow\vec{x}(t)\in M$, then $$l(\gamma)=\int_{t_0}^{t_1}\sqrt{\langle\,\dot{\vec{x}},\dot{\vec{x}}\,\rangle}\,dt.$$ 

**Definition.** A differentiable manifold with a fixed positive-definite quadratic form $\langle\,\vec{\xi},\vec{\xi}\,\rangle$ on every tangent space $TM_\vec{x}$ is called a *Riemannian manifold*. The quadratic form is called the *Riemannian metric*. 

*Remark*. Let $U$ be a chart of an atlas for $M$ with coordinates $q_1,\dots,q_n$. Then a Riemannian metric is given by the formula $$ds^2=\sum^n_{i,j=1}a_{ij}(q)\,dq_i\,dq_j\quad a_{ij}=a_{ji},$$ where $dq_i$ are the coordinates of the tangent vector.

---
**F.** *The derivative map*
Let $f:M\rightarrow N$ be a mapping of a manifold $M$ to a manifold $N$. $f$ is called *differentiable* if in local coordinates on $M$ and $N$ it is given by differentiable functions. 

**Definition** The *Derivative* of a differentiable mapping $f:M\rightarrow N$ at a point $\vec{x}\in M$ is the linear map of the tangent spaces $$f_{\star\vec{x}}:TM_\vec{x}\rightarrow TN_{f(\vec{x})}$$

---
### 19. Lagrangian Dynamical Systems
**A.** *Definition of a Lagrangian system*
Let $M$ be a differentiable manifold, $TM$ its tangent bundle, and $L:TM\rightarrow\mathbb{R}$ a differntiable function. A map $\gamma:\mathbb{R}\rightarrow M$ is called the *motion in the langrangian system with configuration manifold $M$ and lagrangian function $L$ if $\gamma$ is an extral of the functional* $$\vec{\Phi}(\vec{\gamma})=\int^{t_1}_{t_0}L(\dot{\vec{\gamma}})\,dt,$$ where $\dot{\vec{\gamma}}$ is the velocity vector $\dot{\vec{\gamma}}\in TM_{\gamma(t)}$. 

**Theorem.** *The evolution of the local coordinates $\vec{q}=(q_1,\dots,q_n)$ of a point $\vec{\gamma}(t)$ under motion in a Lagrangian system on a manifold satisfies the Lagrange equations* $$\frac{d}{dt}\frac{\partial L}{\partial\dot{\vec{q}}}=\frac{\partial L}{\partial\vec{q}},$$ *where $L(\vec{q},\dot{\vec{q}})$ is the expression for the function $L:TM\rightarrow\mathbb{R}$ in the coordinates $\vec{q}$ and $\dot{\vec{q}}$ on $TM.$*

---
**B.** *Natural Systems*
Let $M$ be a Riemannian manifold. The quadratic form on each tangent space, $$T=\frac{1}{2}\langle\,\vec{v},\vec{v}\,\rangle\quad\vec{v}\in TM_\vec{x},$$ is called the *kinetic energy*. A differentiable function $U:M\rightarrow\mathbb{R}$ is called *potential energy*. 

**Definition.** A Lagrangian system on a Riemannian manifold is called *natural* if the Lagrangian function is equal to the difference between the kinetic and potential energies: $L=T-U$. 

**Example**. Consider two mass points $m_1$ and $m_2$ joined by a line segment of length $l$ in the $(x,y)$-plane. Then a configuration space of three dimensions $$M=\mathbb{R}^2\times S^1\subset\mathbb{R}^2\times\mathbb{R}^2$$ is defined on the four dimensional configuration space $\mathbb{R}^2\times\mathbb{R}^2$ of two free points $(x_1,y_1)$ and $(x_2,y_2)$ by the condition $\sqrt{(x_1-x_2)^2+(y_1-y_2)^2}=l$. 
There is a quadratic form on the tangent space to the four-dimensional space $(x_1,x_2,y_1,y_2)$: $$m_1(\dot{x}_1^2+\dot{y}_1^2)+m_2(\dot{x}_2^2+\dot{y}_2^2).$$
Our three dimensional manifold, as it is embedded in the four dimensional one, is provided with a Riemannian metric. The holonomic system thus obtained is called in mechanics a line segment of fixed length in the $(x,y)$-plane. The kinetic energy is given by the formula $$T=m_1\frac{\dot{x}_1^2+\dot{y}_1^2}{2}+m_2\frac{\dot{x}_2^2+\dot{y}_2^2}{2}.$$

---
**C.** *Systems with holonomic constraints*
Consider configuration manifold $M$ of a system with constraints as embedded in the $3n$-dimensional configuration space of a system of free pints. The metric on the $3n$-dimensional space is given by the quadratic form $\sum^n_{i=1}m_i\dot{\vec{r}}\,_i^2$. The embedded Riemannian manifold $M$ with potential energy $U$ coincides with the limiting case of the system with potential $U+N\vec{q}_2^2,\,N\rightarrow\infty$, which rapidly grows outside of $M$. 

---
**D.** *Procedure for solving problems with constraints*
1. Determine the configuration manifold and introduce coordinates $q_1,\dots,q_k$ (in a neighborhood of each of its points).
2. Express the kinetic energy $T=\sum\frac{1}{2}m_i\dot{\vec{r}}_i^2$ as a quadratic form in the generalized velocities $$T=\frac{1}{2}\sum a_{ij}\,(\vec{q})\,\dot{q}_i\,\dot{q}_j.$$
3. Construct the Lagrangian function $L=T-U(\vec{q})$ and solve Lagrange's equations.

**Example.** We consider the motion of a point mass of mass $1$ on a surface of revolution in three-dimensional space. It can be shown that the orbits are geodesics on the surface. In cylindrical coordinates $r,\varphi,z$ the surface is given (locally) in the form $r=r(z)$ or $z=z(r)$. The kinetic energy has the form $$T=\frac{1}{2}(\dot{x}^2+\dot{y}^2+\dot{z}^2)=\frac{1}{2}[(1+r_z'^2)\dot{z}^2+r^2(z)\dot{\varphi}^2]$$ in coordinate $\phi$ and $z$, and $$T=\frac{1}{2}(\dot{x}^2+\dot{y}^2+\dot{z}^2=\frac{1}{2}[(1+z_r'^2)\dot{r}^2+r^2\dot{\varphi}^2]$$ in coordinates $r$ and $\varphi$. 
The Lagrangian function $L$ is equal to $T$. In both coordinate systems $\varphi$ is a cyclic coordinate. The corresponding momentum is preserved: $p_\varphi=r^2\dot{\varphi}$ is nothing other than the $z$-component of angular momentum. 
Since the system has two degrees of freedom, knowing the cyclic coordinate $\varphi$ is sufficient for integrating the problem completely. 
We can obtain a clear picture of the orbits by reasoning slightly differently. Denote by $\alpha$ the angle of the orbit with the meridian. We have $r\dot{\varphi}=|v|\sin{x}$, where |v| is the magnitude of the velocity vector.
By law of the conservation of energy, $H=L=T$ is preserved. Therefore, $|v|$= constant, so the conservation law for $p_\varphi$ takes the form $$r\sin\alpha=\text{constant}$$("Clairaut's theorem").
This relationship shows that the motion takes place in the region $|\sin{x}|\le1$, id est, $r\ge r_0\sin{x_0}$. Furthermore, the inclination of the orbit from the meridian increases as the radius $r$ decreases. When the radius reachest the smallest possible value, $r=r_0\sin{x_0}$, the orbit is reflected and returns to the region with larger r.

---
**E.** *Non-autonomous systems*
A Lagrangian non-atonomous system differs from the autonomous system which we have been studying until now, but the additional dependence of the lagrangian function on time: $$L:TM\times\mathbb{R}\rightarrow\mathbb{R}\quad L=L(\vec{q},\dot{\vec{q}},t).$$ In particular, but the kinetic and potential energies can depend on time in a non-autonomous natural system: $$T:TM\times\mathbb{R}\rightarrow\mathbb{R}\quad U:M\times\mathbb{R}\rightarrow\mathbb{R}\quad T=T(\vec{q},\dot{\vec{q}},t)\quad U=U(\vec{q},t).$$

A system of $n$ mass points, constrained by holonomic constraints dependent on time, is defined with the help of a time-dependent submanifold of the configuration space of a free system. Such a space is given by a mapping $$i:M\times\mathbb{R}\rightarrow\mathbb{E}^{3n}\quad i(\vec{q},t)=\vec{x},$$ which, for any fixed $t\in\mathbb{R}$, defines an embedding $M\rightarrow\mathbb{E}^{3n}$. The formula of section $D$ remains true for a non-autonomous system.

---
### 20. Emmy Noether's Theorem
Various laws of conservation (of momentum, angular momentum, et cetera) are particular cases of one general theorem: to every one-parameter group of diffeomorphisms of the configuration manifold of a Lagrangian system which preserves the Lagrangian function, there corresponds a first integral of the equations of motion.

---
**A.** *Formulation of the Theorem*
Let $M$ be a smooth manifold, $L:TM\rightarrow\mathbb{R}$ a smooth function on its tangent bundle $TM$. Let $h:M\rightarrow M$ be a smooth map.
**Definition**. *A Lagrangian system $(M,L)$ admits the mapping $h$ for any tangent vector $\vec{v}\in TM$,*$$L(h_*\vec{v})=L(\vec{v}).$$

**Noether's Theorem.** *If the system $(M,L)$ admits the one-parameter group of diffeomorphisms $h^s:M\rightarrow M,s\in\mathbb{R}$, then the Lagrangian system of equations corresponding to $L$ has a first integral $I: TM\rightarrow\mathbb{R}$.*
*In local coordinates $q$ on $M$ the integral $I$ is written in the form $$I(\vec{q},\dot{\vec{q}})=\frac{\partial L}{\partial\dot{\vec{q}}}\frac{dh^s(\vec{q})}{ds}\big|_{s_0}.$$

---
**B.** *Proof*
First, let $M=\mathbb{R}^n$ be coordinate space. Let $\vec{\varphi}:\mathbb{R}\rightarrow M,\vec{q}=\vec{\varphi}(t)$ to be a solution to Lagrange's equations. Since $h_*^s$ preserves $L$, the translation of asolution, $h^s\circ\vec{\varphi}:\mathbb{R}\rightarrow M$ also satisfies Lagrange's equations for any $s$.
We consider the mapping $\vec{\Phi}:\mathbb{R}\times\mathbb{R}\rightarrow\mathbb{R}^n$, given by $\vec{q}=\vec{\Phi}(s,t)=h^s(\vec{\phi}(t))$.
We will denote derivatives with respect to $t$ by dots and with respect to $s$ by primes. By hypothesis $$0=\frac{\partial(\vec{\Phi},\dot{\vec{\Phi}})}{\partial s}=\frac{\partial L}{\partial\vec{q}}\cdot\vec{\Phi}'+\frac{\partial L}{\partial\dot{\vec{q}}}\dot{\vec{\Phi}}',$$ where the partial derivatives of $L$ are taken at the point $\vec{q}=\vec{\Phi}(s,t),\,\,\dot{\vec{q}}=\dot{\vec{\Phi}}(s,t).$
As we stated above, the mapping $\vec{\Phi}|_{s=\text{constant}}:\mathbb{R}\rightarrow\mathbb{R}^n$ for any fixed $s$ satisfies Lagrange's equation $$\frac{\partial}{\partial t}\left[\frac{\partial L}{\partial\dot{\vec{q}}}(\vec{\Phi}(s,t),\,\dot{\vec{\Phi}}(s,t))\right]=\frac{\partial L}{\partial\vec{q}}(\vec{\Phi}(s,t),\,\dot{\vec{\Phi}}(s,t)).$$
We introduce the notation $\vec{F}(s,t)=(\partial L/\partial\dot{\vec{q}})(\vec{\Phi}(s,t),\,\dot{\vec{\Phi}}))$ and substitute $\partial\vec{F}/\partial t$ for $\partial L/\partial\vec{q}$ in the hypothesis. 
Writing $\dot{\vec{q}}'$ as $d\vec{q}'/dt$, we get $$0=\left(\frac{d}{dt}\frac{\partial L}{\partial\dot{\vec{q}}}\right)\vec{q}'+\frac{\partial L}{\partial\dot{\vec{q}}}\left(\frac{d}{dt}\vec{q}'\right)=\frac{d}{dt}\left(\frac{\partial L}{\partial\dot{\vec{q}}}\right)=\frac{dI}{dt}$$

---
**21.** *D'Alembert's principle*
We give here a new definition of a system of point masses with holonomic constraints and prove its equivalence to the definition given in 17. 

**A.** *Example*
Consider the holonomic system $(M,L)$, where $M$ is the surface in three-dimensional space $\{x\}$: $$L=\frac{1}{2}m\dot{\vec{x}}-U(\vec{x}).$$ In mechanical terms, 
the mass point $\vec{x}$ of mass $m$ must remain on the smooth surface $M$."
Consider a motion of the point, $\vec{x}(t)$. IF Newton's equations $m\ddot{\vec{x}}+(\partial U/\partial\vec{x})=0$ were satisfied, then in absence of external forces $U=0$ the trajectory would be a straight line and could not lie on the surface $M$. 
From the point of view of Newton, this indicates the presence of a new force "forcing the point to stay on the surface."

**Definition.** The quantity $$\vec{R}=m\ddot{\vec{x}}+\frac{\partial U}{\partial\vec{x}}$$ is called the *constraint force*. 

**B.** *Formulation of the D'Alembert-Lagrange principle*
In mechanics, tangent vectors to the configuration manifold are called *virtual variations*. The D'alembert-Lagrange principle states: $$\left(m\ddot{\vec{x}}+\frac{\partial U}{\partial\vec{x}},\vec{xi}\right)=0$$ *for any virtual variation $\xi$*, or stated differently, the *work of the constraint force on any virtual variation is zero*.
