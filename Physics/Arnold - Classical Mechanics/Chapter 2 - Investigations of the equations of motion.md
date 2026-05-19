---
title: Chapter 2 - Inverstigations of the equations of motion
tags: [Part I - Newtonian Mechanics]

---

# Part I - Newtonian Mechanics
## Chapter 2 - Investigation of the equations of motion. 
In most cases, such as the three-body problem), we can neither solve the system of differential equations nor completely describe the behavior of the solutions. Here we consider a few simple problems which can be solved. 

---
### 4. Systems with one degree of freedom
**A**. *Definitions*
A system with one degree of freedom is a system described by one differential equation: $$\ddot{x}=f(x)\quad x\in\mathbb{R}.$$The kinetic energy is the quadratic form $$T=\frac{1}{2}\dot{x}^2.$$ The potential energy is the function $$U(x)=-\int^x_{x_0}f(\xi)\,d\xi.$$ The sign of the potential energy is chosen such that the potential energy of a stone is larger if the stone is higher off the ground.
The total energy is the sum $$E=T+U.$$ In general, the total energy is a function $E(x,\dot{X})$.

---
**Theorem** (The law of the conservation of energy) *The total energy of a system moving according to Newton's equation is conserved: $E(x(t),\dot{x}(t))$ is independent of $t$.*
**Proof**. $$\frac{d}{dt}(T+U)=\dot{x}\ddot{x}+\frac{dU}{dx}\dot{x}=\dot{x}(\ddot{x}-f(x))=0.$$

---
**B**. *Phase flow*
Newton's equation is equivalent to the system of two equations: $$\dot{x}=y\quad\dot{y}=f(x).$$We consider the plane with coordinates $x$ and $y$, which we call the *phase plane* of Newton's equation. The points of the phase plane are called *phase points*. The equation $\dot{y}=f(X)$ determines a vector field on the phase plane, called the *phase velocity of the field*. 

A solution to the system of equations is a motion $\vec{\phi}:\mathbb{R}\rightarrow\mathbb{R}^2$ of a phase point in the phase plane, such that the velocity of the moving point at each moment of time is equal to the phase velocity vector at a location of the phase point at that moment. 

The image of $\vec{\phi}$ is called the *phase curve*. Thus the phase curve is given by the parametric equations $$x=\phi(t)\quad y=\dot{\phi}(t).$$ A phase curve can consist of only one point, in which case the point is called an *equilibrium position*. The vector of the phase velocity at this point is zero. 

On each phase curve the total energy is constant, thus each phase curve lies entirely on the energy level set $E(x,y)=h.$

---
**C**. *Examples*
**Example 1.** The basic equation of the theory of oscillations is $$\ddot{x}=-x.$$ In this case, we have $$T=\frac{\dot{x}^2}{2}\quad U=\frac{x^2}{2}\quad E=\frac{\dot{x}^2}{2}+\frac{x^2}{2}.$$

The energy level sets are the concentric circles and the origin. The phase velocity at point $(x,y)$ has components $(y,-x)$. It is perpendicular to the radius vector and equal in magnitude, therefore the motion of the phase point in the phase plane is a uniform motion around $0$: $x=r_0\cos(\phi_0-t),\,y=r_0\sin(\phi_0-t).$

---
### 5. Systems with two degrees of freedom
**A**. *Definitions*
By a system with two degrees of freedom we mean a system defined by the differential equations $$\vec{\ddot{x}}=\vec{f}(\vec{x}),\quad\vec{x}\in\mathbb{E}^2,$$ where $\vec{f} is a vector field on the plane.
A system is said to be *conservative* if there exists a function $U:\mathbb{E}^2\rightarrow\mathbb{R}$ such that $\vec{f}=-\frac{\partial U}{\partial \vec{x}}$. The equation of motion of a conservative system then has the form $\vec{\ddot{x}}=-\frac{\partial U}{\partial\vec{x}}$. 

---
**B**. *The law of conservation of energy*
**Theorem**. *The total energy of a conservative system is conserved, i.e., $$\frac{dE}{dt}=0,\quad\text{where }E=\frac{1}{2}\vec{\dot{x}}^2+U(\vec{x}),\vec{\dot{x}}^2=(\vec{\dot{x}},\vec{\dot{x}}).$$*

**Proof**.$$\frac{dE}{dt}=(\vec{\dot{x}},\vec{\ddot{x}})+(\frac{\partial U}{\partial\vec{x}})=(\vec{\ddot{x}}+(\frac{\partial U}{\partial\vec{x}}),\vec{\dot{x}})=0.$$

**Corollary**. *If at the initial moment the total energy is equal to $E$, then all trajectories lie in the region where $U(x)\le E$, i.e., a point remains inside the potential well $U(x_1,x_2)\le E$ for all time.*
*Remark* In a system with one degree of freedom, it is always possible to introduce the potential energy $$U(x)=\int^x_{x_0}f(\xi)\,d\xi,$$ and in a system with two degrees of freedom this is not so. 

---
**C**. *Phase Space*
The equations of motion can be written as the system $$\begin{aligned}\dot{x}_1&=y_1\\\dot{x}_2&=y_2\\\dot{y}_1&=-\frac{\partial U}{\partial x_1}\\\dot{y}_2&=-\frac{\partial U}{\partial x_2}\end{aligned}$$ The phase space of a system with two degrees of freedom is the four dimension space with coordinates $x_1,x_2,y_1$ and $,y_2.$

All of phase space is partitioned into phase curves. Projecting the phase curves from four space into the $x_1,x_2$ plane gives the trajectories of our moving point in the $x_1,x_2$ plane. These trajectories are called orbits. Orbits can have points of intersection even when the phase curves do not intersect one another. 

The equation of the law of the conservation of energy: $$E=\frac{\vec{\dot{x}}^2}{2}+U(\vec{x})=\frac{y^2_1+y^2_2}{2}+U(x_1,x_2)$$ defined a three-dimensional hypersurface in four space: $E(x_1,x_2,y_1,y_@)=E_0:$, this surface, $\pi_{E_0}$ remains invariant under the phase flow $g^t\pi_{E_0}=\pi_{E_0}$. One could say that the phase flow flows along the energy level hypersurfaces. 

---
**Example** ("Lissajous figures") We look at small oscillations with two degrees of freedom defined by $$\ddot{x}_1=-x_1\quad\ddot{x}_2=-\omega^2x_2$$ The potential energy is $$U=\frac{1}{2}x^2_1+\frac{1}{2}\omega^2x^2_2.$$ From the law of the conservation of energy it follows that, if the initial moment of time the total energy is $$\frac{1}{2}(\dot{x}^2_1+\dot{x}^2_2)+U(x_1,x_2)=E,$$ then all motion takes place inside the ellipse $U(x_1,x_2)\le E.$ 
The solutions to this are harmonic oscillations which are independent on the vertical and horizontal axes. 

---
### 6. Conservative force fields
**A.** *Work of a force along a path*
The definition of work by a force $\vec{F}$ on a path $\vec{S}$ is the scalar product: $$A=(\vec{F},\vec{S})=|\vec{F}|\,|\vec{S}|\cdot\cos\phi.$$

**B.** *Conditions for a field to be conservative*
**Theorem.** *A vector field $\vec{F}$ is conservative if and only if its work along any path $M_1M_2$ depends only on the endpoints of the path, and not on the shape of the path.*

**C.** *Central fields*
**Definition.** A vector field in the plane $\mathbb{E}^2$ is called *central* with a center at $0$, if it is invariant with respect to the group of motions of the plane which fix $0$. 

**Theorem.** *Every central field is conservative, and its potential energy depends only on the distance to the center of the field,* $U=U(r).$

---
### 7. Angular Momentum
**Definition.** *The motion of a material point (with unit mass) in a central field on a plane* is defined by the equation $$\ddot{\vec{r}}=\vec{\Phi}(r)\hat{e}_r,$$ where $\vec{r}$ is the radius vector beginning at the center of the field $0,\,\,r$ is its length, and $\hat{e}_r$ is its direction.

**Definition.** The *angular momentum* of a material point of unit mass relative to the point $0$ is the vector product $$\vec{M}=[\vec{r},\dot{\vec{r}}].$$

**A.** *The law of conservation of angular momentum*
**Lemma.** Let $\vec{a}$ and $\vec{b}$ be two vectors changing with time in the oriented euclidean space $\mathbb{R}^3, then $$\frac{d}{dt}[\vec{a},\vec{b}]=[\dot{\vec{a}},\vec{b}]+[\vec{a},\dot{\vec{b}}].$$

**Theorem** (The law of conservation of angular momentum) *Under motion in a central field, the angular momentum $\vec{M}$ relative to the center of the field $0$ does not change with time.*

**B.** *Kepler's Law*
The law of conservation of angular momentum was first discovered by Kepler through observation of the motion of Mars. 
We consider at the point $\vec{r}$ with coordinate $(|\vec{r}|=r,\phi)$, two unit vectors $\hat{e}_r$, directed along the radius vector so that $$\vec{r}=r\hat{e}_r,$ and $\hat{e}_\phi$, perpendicular to it in the direction of increasing $\phi$. 

**Lemma.** *We have the relation* $$\dot{\vec{r}}=\dot{r}\hat{e}_r+r\dot\phi\hat{e}_\phi$$

Consequently, the angular momentum is $$\vec{M}=r^2\dot{\phi}[\hat{e}_r,\hat{e}_\phi]$$ 
thus, the quantity $\vec{M}=r^2\dot{\phi}$ is preserved.

Kepler called the rate of the change of the area $S(t)$ swept out by the radius the *sectorial velocity* $C$: $$C=\frac{dS}{dt}.$$

Kepler discovered through the observation of the motion of the planet that in equal times the radius vector sweeps out equal areas, so that the sectorial velocity is constant.

---
### 8. Investigation of motion in a central field 
**A.** *Reduction to a one-dimensional problem*
We look at the motion of a point (of mass 1) in a central field on the plane: $$\ddot{\vec{r}}=-\frac{\partial U}{\partial\vec{r}},\quad U=U(r).$$

**Theorem** *For the motion of a material point of unit mass in a central field, the distance from the center of the field varies in the same way as $r$ varies in the one-dimensional problem with potential energy* $$V(r)=U(r)+\frac{M^2}{2r^2}$$

*Remark* The total energy in the derived one-dimensional problem $$E_1=\frac{\dot{r}^2}{2}+V(r)$$ is the same as the total energy in the original problem. $$E=\frac{\dot{\vec{r}}^2}{2}+U(\vec{r},$$ since $$\frac{\dot{\vec{r}}^2}{2}=\frac{\dot{r}^2}{2}+\frac{r^2\dot{\phi}^2}{2}=\frac{\dot{r}^2}{2}+\frac{M^2}{2r^2}$$

**B.** *Integration of the equation of motion*
The total energy in the derived one-dimensional problem is conserved. Consequently, the dependence of $r$ on $t$ is defined by the quadrature $$\dot{r}=\sqrt{2(E-V(r))}\quad\int\,dt=\int\frac{dr}{\sqrt{2(E-V(r))}}.$$ Since $\dot{\phi}=M/r^2,d\phi/dr=(M/r^2)/\sqrt{2(E-V(r))},$ and the equation of the orbit in polar coordinates is found by quadrature, $$\phi=\int\frac{M/r^2\,dr}{\sqrt{2(E-V(r))}}.$$

**C.** *Investigation of the orbit*
Fixing the value of the angular momentum at $M$, we can visualize the variation of $r$ with time as the graph of potential energy. 

Let $E$ be the value of the total energy. All orbits corresponding to the given $E$ and $M$ lie in the region $V(r)\le E$. On the boundary of this region, $V=E$, i.e., $\dot{r}=0$. Therefore, the velocity of a moving point, in general, is not equal to zero since $\dot{\phi}\neq0$ for $M\neq0$. 

The inequality $V(r)\le E$ gives one or several annular regions in the plane: $$0\le r_{min}\le r\le r_{max}\le\infty.$$ 
If this is true, the motion is bounded and takes place in the ring between the circles of radius $r_{min}$ and $r_{max}$. 

In general, the orbit is not closed: the angle between the successive pericenters and the apocenters is given by the integral $$\vec{\Phi}=\int^{r_{max}}_{r_{min}}\frac{M/r^2\,dr}{\sqrt{2(E-V(r))}}.$$ The angle between two successive pericenters is twice as big. 

The orbit is closed if the angle $\Phi$ is commensurable with $2\pi$, i.e., if $\Phi=2\pi(\frac{m}{n})$. 

---
### 9. The motion of a point in three-space
**A.** *Conservative fields*
We consider a motion in the conservative field $$\ddot{\vec{r}}=-\frac{\partial U}{\partial\vec{r}},$$ where $U=U(\vec{r}),\,\vec{r}\in\mathbb{E}^3$. 
The law of conservation of energy holds: $$\frac{dE}{dt}=0, where $E=\frac{1}{2}\dot{\vec{r}}+U(\vec{r}).$$

---
**B.** *Central Fields*
For motion in a central field the vector $\vec{M}=[\vec{r},\dot{\vec{r}}]$ does not change: $d\vec{M}/dt=0$

Every central field is conservative and $$\frac{d\vec{M}}{dt}=[\dot{\vec{r}},\dot{\vec{r}}]+[\vec{r},\ddot{\vec{r}}]=0,$$ since $\ddot{\vec{r}}=-(\partial U/\partial\vec{r})$, and the vector $\partial U/\partial\vec{r}$ is collinear with $\vec{r}$ since the field is central.

**Corollary**. *For motion in a center field, every orbit is planar.*

---
**C.** *Axially symmetric fields*
**Definition**. A vector field in $\mathbb{E}^3$ has *axial symmetry* if it is invariant with respect to the group of rotations of space which fix every point of some axis.

**Definition**. The moment $\vec{M}_z$ relative to the $z$ axis of the vector $\mathbb{F}$ applied at the point $\vec{r}$ is the projection onto the $z$ axis of the moment of the vector $\vec{F}$ relative to some point on the axis: $$\vec{M}_z=(\hat{e}_z,[\vec{r},\vec{F}]).$$

**Theorem** *For a motion in a conservative field with axial symmetry around the $z$ axis, the moment of velocity relative to the $z$ axis is conserved.*

---
### 10. Motions of a system of $n$ points
**A.** *Internal and External forces*

We know all of this. Sum of internal particles and the group of particles can be treated as a single particle at the center of mass. 

---
