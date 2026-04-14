---
title: Chapter 3 - Variational Principles
tags: [Part II - Lagrangian Mechanics]

---

# Part II - Lagrangian Mechanics
Lagrangian mechanics describes motion in a mechanical system by means of the configuration space. The configuration space of a mechanical system has the structure of a differentiable manifold, on which a group of diffeomorphisms acts. The basic ideas and theorems of Lagrangian mechanics are invariant under this group, even if formulated in terms of local coordinates.

A Lagrangian mecahnical system is given by a manifold ("configuration space") and a function on its tangent bundle ("the Lagrangian function").

Every one-parameter group of diffeomorphisms of configuration space which fixes the lagrangian function defines a conservation law. (id est, a first integral of the equations of motion). 

A Newtonian potential system is a particular case of a Lagrangian system (the configuration space in this case is Euclidean, and the Lagrangian function is the difference between the kinetic and potential energies).

A Lagrangian point of view allows us to solve completely a series of important mechanical problems, including problems in the theory of small oscillations and in the dynamics of a rigid body. 

## Chapter 3 - Variational Principles
In this chapter we show that the motion of a Newtonian potential system are extremals of a variational principle, "Hamilton's principle of least action."

---
### 12. Calculus of Variations
The calculus of variations is concerned with the extremals of functions whose domain is an infinite-dimensional space: the space of curves. Such functions are called *functionals*.
An example of a functional is the length of a curve in the euclidean plane: if $\gamma=\{(t,x):x(t)=x,\,t_0\le t\le t_1\},$ then $\Phi(\gamma)=\int_{t_0}^{t_1}\sqrt{1+x^2}\,dt$. 

We consider an "approximation" $\gamma'$ to $\gamma,\,\gamma'=\{(t,x):x=x(t)+h(t)\}.$ We will call it $\gamma'=\gamma+h$. 
Consider the increment of $\Phi,\,\Phi(\gamma+h)-\Phi(\gamma)$, 

---
**A.** *Variations*
**Definition.** A function $\Phi$ is called *differentiable* if $\Phi(\gamma+h)-\Phi(\gamma)=F+R$, where $F$ depends linearly on $h$ anf where $R(h,y)=\mathcal{O}(h^2)$. The linear part of the increment, $F(h)$, is called the *differential*. 

It can be shown that if $\Phi$ is differentiable, its differential is uniquely defined. The differential of a function is also called its *variation*, and $h$ is called a *variation of the curve*.

**Theorem.** *The functional $\Phi(\gamma)=\int^{t_1}_{t_0}L(x,\dot{x},t)\,dt$ is differntiable, and the derivative is given by the formula* $$F(h)=\int^{t_1}_{t_0}\left[\frac{\partial L}{\partial x}-\frac{d}{dt}\frac{\partial L}{\partial\dot{x}}\right]h\,dt+\left(\frac{\partial L}{\partial\dot{x}}h\right)\bigg|^{t_1}_{t_0}.$$

---
**B.** *Extremals*
**Definition**. An *extremal* of a differentiable function $\Phi(\gamma)$ is a curve $\gamma$ such that $F(h)=0$ for all $h$.

**Theorem.** *The curve $\gamma:x=x(t)$ is an extremal of the function $\Phi(\gamma)=\int^{t_1}_{t_0}L(x,\dot{x},t)\,dt$ on the space of curves passing through the points $x(t_0)=x_0$ and $x(t_1)=x_1$, if and only if*$$\frac{d}{dt}\left(\frac{\partial L}{\partial\dot{x}}\right)=0\,\,\textit{ along the curve }x(t).$$

**Lemma.** *If a continuous function $f(t),\,t_0\le t\le t_1$ satisfies $\int_{t_0}^{t_1}f(t)h(t)dt=0$ for any continuous function $h(t)$ with $h(t_0)=h(t_1)=0$, then $f(t)\equiv0$.

---
**C.** *The Euler-Lagrange Equation*
**Definition**. The equation $$\frac{d}{dt}\left(\frac{\partial L}{\partial\dot{x}}\right)-\frac{\partial L}{\partial x}=0$$ is called the *Euler-Lagrange equation* for the functional $$\Phi=\int^{t_1}_{t_0}L(x,\dot{x},t)\,dt.$$

**Theorem.** *The curve $\gamma$ is an extremal of the functional $\Phi(\gamma)=\int^{t_1}_{t_0}L(x,\dot{x},t)\,,dt$ on the space of curves joining $(t_0,x_0)$ and $(t_1,x_1)$, if and only if the Euler-Lagrange equation is satisfied along $\gamma$.

---
**D.** *An important remark*
The condition for a curve $\gamma$ to be an extremal of a function does not depend on the choice of coordinate system. 

---
### 13. Lagrange's Equations
Here we indicate the variation principle whose extremals are solutions of Newton's equations of motion in a potential system.
We compare Newton's equations of dynamics $$\frac{d}{dt}(m_i\dot{r}_i)+\frac{\partial U}{\partial r_i}=0$$ with the Euler-Lagrange equation $$\frac{d}{dt}\frac{\partial L}{\partial\dot{\vec{x}}}-\frac{\partial L}{\partial\vec{x}}=0.$$

---
**A.** *Hamilton's Principle of Least Action*
**Theorem.** *Motions of the mechanical system following Newton's equation of dynamics coincide with the extremals of the functional $$\Phi(\gamma)=\int_{t_0}^{t_1}L\,dt,\quad\textit{where }L=T-U$$ is the difference between the kinetic and potential energy.*

**Corollary.** *Let $(q_1,\dots,q_{3n})$ be any coordinates in the configuration space in a system of $n$ mass points. Then the evolution of $\vec{q}$ with time is subject to the Euler-Lagrange equations* $$\frac{d}{dt}\left(\frac{\partial L}{\partial\vec{q}}\right)-\frac{\partial L}{\partial\vec{q}}=0,\quad\textit{where }L=T-U.$$

**Definition.** In mechanics we use the following terminology: 
- $L(\vec{q},\dot{\vec{q}},t)=T-U$ is the *Lagrange function* or the *Lagrangian*, 
- $q_i$ are the *generalized coordinates*, 
- $\dot{q}_i$ are the *generalized velocities*, 
- $\partial L/\partial\dot{q}_i=p_i$ are the *generalized momenta*, 
- $\partial L/\partial q_i$ are the *generalized forces*, 
- $\int_{t_0}^{t_1}L(\vec{q},\dot{\vec{q}},t)\,dt$ is the *action*, 
- $(d(\partial L/\partial\dot{q}_i)dt)-(\partial L/\partial q_i)=0$ are *Lagrange's Equations*.

---
**B.** *The simplest examples*
Example 1. For a free mass point in $\mathbb{E}^3$, $$L=T=\frac{m\dot{\vec{r}}^2}{2};$$ in cartesian coordinates $q_i=r_i$ we find $$L=\frac{m}{2}(\dot{q}^2_1+\dot{q}^2_2+\dot{q}_3^2).$$ Here the generalized velocities are the components of the velocity vector, the generalized momenta $p_i=m\dot{q}_i$ are the components of the momentum vector, and Lagrange's equations coincide with Newton's equations $d\vec{p}/dt=0$. The extremals are straight lines. It follows from Hamilton's principles that the straight lines are not only the shortest (id est, extremals of the length), but also extremals of the action. 

**Example 2** We consider planar motion in a central field in polar coordinates $q_1=r,\,q_2=\varphi$. From the relation $\dot{\vec{r}}=\dot{r}\hat{e}_r+\dot{\varphi}r\hat{e}_\varphi$ we find the kinetic energy $T=\frac{1}{2}m\dot{\vec{r}}^2=\frac{1}{2}m(\dot{r}^2+r^2\dot{\varphi}^2)$ and the Lagrangian $L(\vec{q},\dot{\vec{q}})=T(\vec{q},\dot{\vec{q}})-U(\vec{q})$, where $U=U(q_1)$. 
The generalized momenta will be $\vec{p}=\partial L/\partial\dot{\vec{q}}$, id est, $$p_1=m\dot{r}\quad p_2=mr^2\dot{\varphi}.$$ The first Lagrange equation $\dot{p}_1=\partial L/\partial q_1$ takes the form $$m\ddot{r}=mr\dot{\varphi}^2-\frac{\partial U}{\partial r}.$$ As $q_2=\varphi$ does not enter into $L$, we have $\partial L/\partial q_2=0$. This is the conservation of angular momentum. 

In general, when the field is not central $(U=U(r,\varphi))$, we find $\dot{\vec{p}}_2=-\partial U/\partial\varphi.$
This equation can be written in the form $d(\vec{M},\hat{e}_z)/dt=N$, where $N=([\vec{r},\vec{F}],\hat{e}_z)$ and $\vec{F}=-\partial U/\partial\vec{r}$. (The rate of change in angular momentum relative to the $z$ axis is equal to the moment of the force $\vec{F}$ relative to the $z$ axis.)

We have $dU=(\partial U/\partial r)dr+(\partial U/\partial\varphi)d\varphi=-(\vec{F},d\vec{r})=-(\vec{F},\hat{e}_r)dr-r(\vec{F},\hat{e}_\varphi)d\varphi$; there $-\partial U/\partial\varphi=r(\vec{F},\hat{e}_\varphi=r([\hat{e}_r,\vec{F}],\hat{e}_z)=([\vec{r},\vec{F}],\hat{e}_z).$ 
This suggests the following generalization of the law of conservation of angular momentum: 

**Definition** A coordinate $q_i$ is called *cyclic* if it does not enter into the Lagrangian: $\partial L/\partial q_i=0.$

**Theorem** *The generalize momentum corresponding to a cyclic coordinate is conserved:* $p_i=$ *constant.*

---
### 14. Legendre Transformation
The Legendre transformation transforms functions on a vector space to functions on the dual space. They are related to projective duality and tangential coordinates in algebraic geometry and the construction of dual Banach spaces in analysis. 

**A.** *Definition*
Let $y=f(x)$ be a convex function, $f''(x)>0$
The *Legendre transformation* of the function $f$ is a new function $g$ of a new variable, $p$, which is constructed by drawing the graph of $f$ in the $x,y$ plane. 
Let $p$ be a given number. Consider the straight like $y=px$. We take the point $x=x(p)$ at which the curve is farthest from the straight line in the vertical direction: for each $p$ in the function $px-f(x)=F(p,x)$ has a maximum with respect to $x$ at the point $x(p)$ 
Now we define $g(p)=F(p,x(p)).$ 
The point $x(p)$ is defined by the extremal position $\partial\vec{F}/\partial x=0$, id est, $f'(x)=p$. As $f$ is convex, this point is unique. 

**B.** *Examples*
Example 1. Let $f(x)=x^2$, then $F(p,x)=px-x^2, x(p)=\frac{1}{2}p,\,g(p)=\frac{1}{4}p^2.$

Alright I think I'm getting this a bit more, now. I mean it's all defined above and I'll just describe it again. Hmm nope, never mind I don't have a good intuitive description. The figure shows the curve with a single $p$, but I think it's a function defining lots of these. 

Doing lots of extra reading. 
So for this first example, $$g(p)=\sup\{px-f(x)\}\rightarrow\sup\{px-x^2\}$$ Differentiate with respect to x to maximize according to x: $$\frac{d}{dx}(px-x^2)=p-2x.$$ Setting this to zero: $$p-2x=0\rightarrow x=\frac{p}{2}$$ Plug $x(p)=\frac{p}{2}$ back into $px-x^2$: $$g(p)=p(\frac{p}{2})-\left(\frac{p}{2}\right)^2=\frac{p^2}{2}-\frac{p^2}{4}=\frac{p^2}{4},$$ thus the Legendre transform of $f(x)=x^2$ is $$g(p)=\frac{p^2}{4}\,\forall\,p\in\mathbb{R}.$$

So this is covered in Taylor's undergrad mechanics, soon we'll run into performing this on manifolds which would bump it to graduate level, and I'll start writing and working problems there. 

---
**C.** *Involutivity*
Let us consider a function $f$ which is differentiable as many times as necessary, with $f''(x)>0$. It is easy to verify that the Lengendre takes convex functions to convex functions, therefore we can apply it twice.

**Theorem.** *The Legendre transformation is involutive, id est, its square is the identity: If under the Legendre transformation $f$ is taken to $g$, then the Legendre transform of $g$ will again be $f$.*

**Corollary**. *Consider a given family of straight lines $y=px-g(p)$. then its envelope has the equation $y=f(x)$, where $f$ is the Legendre transforms of $g$.*

**D.** *Young's Inequality*
**Definition**. Two functions, $f$ and $g$, which are the Legendre transforms of one another are called *dual in the sense of Young*.

By definition of the Legendre transform, $F(x,p)=px-f(x)$ is less than or equal to $g(p)$ for any $x$ and $p$. From this we have *Young's inequality* $$px\le f(x)+g(p).$$

**Example 1.** If $f(x)=\frac{1}{2}x^2$, then $g(p)=\frac{1}{2}p^2$ and we obtain the inequality $px\le \frac{1}{2}x^2+\frac{1}{2}p^2$ for all $x$ and $p$.

---
**E.** *The case of many variables*
Now let $f(x)$ be a convex function of the vector variable $\vec{x}=(x_1,\dots,x_n)$ (id est, the quadratic form $((\partial^2f/\partial\vec{x}^2)d\vec{x},d\vec{x}))$ is positive definite), then the Legendre transform is the function $g(\vec{p})$ of the vector variable $\vec{p}=(p_1,\dots,p_n)$, as defined by the inequalities $g(\vec{p})=F(\vec{p},\vec{x}(\vec{p}))=\max_\vec{x}\,F(\vec{p},\vec{x})$, where $F(\vec{p},\vec{x})=(\vec{p},\vec{x})-f(\vec{x})$ and $\vec{p}=\partial f/\partial\vec{x}.$

---
### 15. Hamilton's equations
By means of a Legendre transformation, a Lagrangian system of second-order differential equations is converted into a remarkably symmetrical system of $2n$ first-order equations called a Hamiltonian system of equations (or canonical equations).

---
**A.** *Equivalence of Lagrange's and Hamilton's equations*
We consider the system of Lagrange's equations $\dot{\vec{p}}=\partial L/\partial\vec{q}$, where $\vec{p}=\partial L/\partial\dot{\vec{q}}$, with a given Lagrangian function $L:\mathbb{R}^n\times\mathbb{R}^n\times\mathbb{R}\rightarrow\mathbb{R}$, which we wil assume to be convex with respect to the second argument $\dot{\vec{q}}$. 

**Theorem.** *The system of Lagrange's equations is equivalent to the system of $2n$ first-order equations (Hamilton's equations)*$$\begin{aligned}\dot{\vec{p}}&=-\frac{\partial H}{\partial\vec{q}}\\\dot{\vec{q}}&=\,\,\,\,\frac{\partial H}{\partial\vec{p}},\end{aligned}$$*where $H(\vec{p},\vec{q},t)=\vec{p}\dot{\vec{q}}-L(\vec{q},\dot{\vec{q}},t)$ is the Legendre transformation of the Lagrangian function viewed as a function of $\dot{\vec{q}}$.*

---
**B.** *Hamilton's function and energy*
**Example**. Suppose now that the equations are mechanical, so that the Lagrangian has the usual form $L=T-U$, where the kinetic energy $T$ is a quadratic form with respect to $\dot{\vec{q}}$: $$T=\frac{1}{2}\sum a_{ij}\dot{q}_i\dot{q}_j,\quad\text{where }a_{ij}=a_{ii}(\vec{q},t)\text{ and }U=U(\vec{q}).$$

**Theorem.** Under the given assumptions, the Hamiltonian $H$ is the total energy $H=T+U$

I'm still trying to fully wrap my mind around the Legendre transform where I grasp it intuitively instead of just being able to compute and knowing what it does. 

I'll actually go through this following proof, which is based on the lemma:
**Lemma.** *The values of a quadratic form $f(\vec{x})$ and of its Legendre transform $g(\vec{p})$ coincide at the corresponding points: $f(\vec{x})=g(\vec{p})$.*

**Example.** For the form $f(x)=x^2$, this is a well known property of a tangent to the parabola. For the form $f(x)=\frac{1}{2}mx^2$ we have $p=mx$ and $g(p)=p^2/2m=mx^2/2=f(x)$.

**Proof of the Lemma**. By Euler's theorem on a homogeneous functions $(\partial f/
\partial\vec{x})\vec{x}=2f$, therefore, $g(\vec{p}(\vec{x}))=\vec{p}\vec{x}-f(\vec{x})=(\partial f/\partial\vec{x})\vec{x}-f=2f(x)-f(x)=f(x).$

**Proof of the theorem**. Reasoning as in the lemme, we find that $H=\vec{p}\dot{\vec{q}}-L=2T-(T-U)=T+U.$

**Example.** For one-dimensional motion $$\ddot{q}=-\frac{\partial U}{\partial q}.$$ In this case, $T=\frac{1}{2}\dot{q}^2, U=U(q),p=\dot{q},H=\frac{1}{2}p^2+U(q)$ and Hamilton's equations take the form $$\begin{aligned}\dot{q}&=p\\\dot{p}&=-\frac{\partial U}{\partial q}.\end{aligned}$$

**Corallary 1.** $dH/dt=\partial H/\partial t$. *In particular, for a system where the Hamiltonian function does not depend explicitly on time $(\partial H/\partial t=0)$ , the law of the conservation of the hamiltonian function holds: $H(\vec{p}(t),\vec{q}(t))=$ constant*.

---
**C.** *Cyclic coordinates*
When considering central fields, we noticed that a problem could be reduced to a one-dimensional problem by the introduction of polar coordinates. It turns out that, given any symmetry of a problem allowing us to choose a system of coordinates $\vec{q}$ in such a way that the Hamiltonian function is independent of some of the coordinates, we can find some first integrals and thereby reduce a problem in a smaller number of coordinates. 

**Definition**. If a coordinate $q_1$ does not enter into the Hamiltonian function $H(p_1,p_2,\dots,p_n;q_1,\dots.q_n;t)$, id est, $\partial H/\partial q_1=0$, then it is called *cyclic*. 

Clearly the coordinate $q_1$is cyclic if and only if it does not enter into the Lagrangian function $(\partial L/\partial q_1=0)$. IT follows from the Hamiltonian form of the equations of motion that:

**Corollary 2.** *Let $q_1$ be a cyclic coordinate, then $p_1$ is a first integral. In this case, the variation of the remaining coordinates with time is the same as in a system with the $n-1$ independent coordinates $q_2,\dots,q_n$ and with the Hamiltonian function $$H(p_2,\dots,p_n,q_2,\dots,q_n,t,c),$$ depending on the parameter* $c=p_1.$

**Corollary 3.** *Every closed system with two degrees of freedom which has a cyclic coordinate is integrable*. 

---
### 16. Liouville's Theorem
The phase flow of Hamilton's equations preserve phase volume. It follows, for example, that a Hamiltonian system cannot be asymptotically stable. 

For this section we'll be looking at Hamiltonian functions independent of time.

---
**A.** *The phase flow*
**Definition.** The $2n$-dimensional space with coordinates $p_1,\dots,p_n;q_1,\dots,q_n$ is called *phase space*

**Example**. In the case $n=1$ this is the phase plane of the system $\ddot{x}=-\partial U/\partial x$. 

**Definition.** The *phase flow* is the one-parameter group of transformations of phase space $$g^t:(\vec{p}(0),\,\vec{q}(0))\mapsto(\vec{p}(t),\,\vec{q}(t)),$$ where $\vec{p}(t)$ and $\vec{q}(t)$ are solutions of Hamilton's systems of equations. 

---
**B.** *Liouville's theorem*
**Theorem 1.** *The phase flow preserves volume*.

**Theorem 2.** *If $div\,f\equiv0,$ then $g^t$ preserves volume: $v(t)=v(0)$*.

---
**C.** *Proof*
**Lemma 1.** $(dv/dt)|_{t=0}=\int_{D(0)}\mathrm{div}\vec{f}\,dx \,\,(dx=dx_1\cdots dx_n)$

**Lemma 2.** *For any matrix* $A=(a_{ij})$,$$\det(E+At)=1+t\,\mathrm{tr}\,A+\mathcal{O}(t^2),\quad t\rightarrow0.$$

Liouville's theorem allows one to apply methods of *ergodic theory* to the study of mechanics. We consider only the simplest example:

---
**D.** *Poincaré's recurrence theorem*
Let $g$ be a volume-preserving one-to-one mapping which maps a bounded region $D$ of euclidean space onto itself: $gD=D$. 
Then, in any neighborhood $U$ of any point $D$ there is a point $x\in U$ which returns to $U$, id est, $g^nx\in U$ for some $n>0$.

Aside: (The way the ball will move in an asymmetrical cup is unknown; however, Poincaré's theorem predicts it will return to a neighborhood of the original position)

This theorem applies, for example, to the phase flow $g^t$ of a two-dimensional system whose potential $U(x_1,x_2)$ goes to infinity as $(x_1,x_2)\rightarrow\infty$; in this case the invariant bounded region in phase space is given by the condition $$D=\{\vec{p},\vec{q}:T+U\le E\}.$$
Pointcaré's theorem can be strengthened, showing that almost every moving point returns repeatedly to the vicinity of its initial position. This is one of the few general conclusions which can be drawn about the character of motion. The details of motion are not known at all, even in the case $$\ddot{\vec{x}}=-\frac{\partial U}{\partial\vec{x}}\quad\text{where }\vec{x}=(x_1,x_2).$$ 

The following prediction is a parodxical conclusion from the theorem's of Poincaré and Liouville: if you open a partition separating a chamber containing gas and a chamber with vacuum, then after a while the gas molecules will again collect in the first chamber. 

---
**E.** *Applications of Poincaré's theorem*
**Example 1.** Let $D$ be a circle and $g$ rotation through an angle $\alpha$. If $\alpha=2\pi(m/n)$, then $g^n$ is the identity, and the theorem is obvious. If $\alpha$ is not commensurable with $2\pi$, then Poincaré's theorem gives $$\forall\,\delta>0\;\;\exists\;\; n:|g^nx-x|<\delta$$
It follows that:
**Theorem** *If $\alpha\neq2\pi(m/n)$, then the set of points $G^kx$ is dense on the circle.*

**Example 2.** Let $D$ be a two-dimension torus and $\varphi_1$ and $\varphi_2$ angular coordinates on it (longitude and latitude).
Consider the system of ordinary differential equations on the torus $$\dot{\varphi}_1=\alpha_1\quad\dot{\varphi}_2=\alpha_2.$$ Clearly, $\mathrm{div}\,\vec{f}=0$ and the corresponding motion $$g^t:(\varphi_1,\varphi_2)\rightarrow(\varphi_1+\alpha_1t,\varphi_2+\alpha_2t)$$ preserves the volume $d\phi_1\,\,d\phi_2$. From Poincaré's theorem it is easy to deduce: 
**Theorem**. *If $\alpha_1/\alpha_2$ is irrational, then the "winding line" on the torus $g^t(\phi_1,\phi_2)$ is dense on the torus.*