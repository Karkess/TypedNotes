---
title: Chapter 2 - Differential Calculus of Vector Fields

---

# Chapter 2 - Differential Calculus of Vector Fields
## 2.1 - Understanding Physics

It is useful, when solving the equations, that you learn what they mean. Reflect on the solution from the initial conditions and try to get a 'feel' for them. The differential equations are always sufficient, but having a feel for what they mean and what they do in different circumstances is a true understanding. 

Dirac said: "I understanding what an equation means if I have a way of figuring out the characteristics of its solution without actually solving it."

Much historical development is left out here, and is best worked backwards. 

I'll get around to those books eventually. I read part of one on Faraday that was very interesting, I'm not sure why I stopped, honestly. Perhaps sidetracked, I recall enjoying it. 

## 2.2 - Scalar and Vector feids - $T$ and $h$

A few vector algebra identities: $$\vec{A}\cdot\vec{B}=\text{scalar}=A_xB_x+A_yB_y+A_zB_z$$$$\vec{A}\times\vec{B}=\text{vector}=\begin{aligned}(\vec{A}\times\vec{B})_z&=A_xB_y-A_yB_x\\+\quad\:\:\:&\quad\quad\quad\:\:\:\,+\\(\vec{A}\times\vec{B})_x&=A_yB_z-A_zB_y\\+\quad\:\:\:&\quad\quad\quad\:\:\:\,+\\(\vec{A}\times\vec{B})_y&=A_zB_x-A_xB_z\end{aligned}$$$$\vec{A}\times\vec{A}=0$$$$\vec{A}\cdot(\vec{A}\times\vec{B})=0$$$$\vec{A}\cdot(\vec{B}\times\vec{C})=(\vec{A}\times\vec{B})\cdot\vec{C}$$$$\vec{A}(\vec{B}\times\vec{C})=\vec{B}(\vec{A}\cdot\vec{C})-\vec{C}(\vec{A}\cdot\vec{B})$$

---
And two calculus identities:
$$\Delta f(x,y,z)=\frac{\partial f}{\partial x}\Delta x+\frac{\partial f}{\partial y}\Delta y+\frac{\partial f}{\partial z}\Delta z$$$$\frac{\partial^2f}{\partial x\partial y}=\frac{\partial^2f}{\partial y\partial x}$$

The first of these two, of course, only true in the limit that $\Delta x,\Delta y,\Delta z\rightarrow 0.$

---
Scalar fields are simple fields with one value at each point in space. A vector field is a field with a vector at each value in space. 

The example given which gives rise to one variable in the title of this section is that of a gradiant of temperatures over an object being heated and cooled, and such the temperature at each point can be represented as a function of a scalar field: $T(x,y,z)$. 

The flow of heat, however, will be different in direction and magnitude dependent on the place, flowing more from hot to cold as a convention, for example, which we may call $h$, a vector field.

If $\Delta J$ is the thermal energy that passes per unit time through the surface element $\Delta a$, then $$h=\frac{\Delta J}{\Delta a}\hat{e}_f$$, where $$\hat{e}_f$ is a *unit vector* in the direction of flow.

This vector can also be represented in terms of its components. 

## 2.3 Derivatives of fields - The Gradient

To take a derivative of a field and find a vector, we are looking for the approximate form: $$\left(\frac{\partial T}{\partial x},\frac{\partial T}{\partial y},\frac{\partial T}{\partial z}\right).$$

We assign this the symbol $\nabla$, and refer to it as the gradient: $$\text{grad}\,T=\nabla T=\left(\frac{\partial T}{\partial x},\frac{\partial T}{\partial y},\frac{\partial T}{\partial z}\right).$$

## 2.4 The Operator $\nabla$

Taking the dot product with $\nabla$ in the order of $$\nabla\cdot\vec{h}=\frac{\partial h_x}{\partial x}+\frac{\partial h_y}{\partial y}+\frac{\partial h_z}{\partial z},$$ for example. This sum is invariant under coordinate transformation. 

This function is so important in physics, it has been given a special name, the *divergence*. 

Finally, we have the cross product with this operator: $$\nabla\times\vec{h}=\text{a vector}.$$

Summarizing, we have three major functions we care about: $$\begin{aligned}\nabla\, T&=\mathrm{grad}\,T=\text{a vector},\\\nabla\cdot\vec{h}&=\mathrm{div}\,h=\text{a scalar},\\\nabla\times\vec{h}&=\mathrm{curl}\,h=\text{a vector}.\end{aligned}$$

Which allows us to properly write those equations from chapter one: $$Maxwell's\:\:Equations$$$$(1)\quad\quad\nabla\cdot \vec{E}=\frac{\rho}{\epsilon_0}$$$$(2)\quad\quad\nabla\times\vec{E}=-\frac{\partial\vec{B}}{\partial t}$$$$(3)\quad\quad\nabla\cdot\vec{B}=0$$$$(4)\quad\quad c^2\,\nabla\times\vec{B}=\frac{\partial{\vec{E}}}{\partial t}+\frac{j}{\epsilon_0}$$

---
## 2.6 The differential Equation of Heat Flow
If  you have heat flowing through a simple slab, analyzing two faces with the same flat area $A$, temperature is propertional to this area, the temperature difference between the faces, and inversely proportional to the distance between them. This all with a constant dependent on the material. We write this $$J=\kappa(T_2-T_1)\frac{A}{d}.$$

We can then generalize this by shrinking it down and taking any two faces with a position parallel to the isothermals and we look at an arbitrarily small chunk to achieve $$dJ=\kappa\,dT\frac{dA}{dS}.$$

We can look at the heat flow in general and see that $dT/dS$ is just the rate of change of $T$ with position, and since the position change is perpendicular to the isotherms, this is the maximimum rate of change. The change in temperature of $\nabla T$ is opposite the direction of $\vec{h}$, so we can rewrite the above equation as $$\vec{h}=-\kappa\,\nabla T.$$

This is the differential equation of heat flow in bulk materials. Writing these differential equations as vector equations is powerful because it removes us from any need for a coordinate system. 

## 2.7 - Second Derivatives of Vector Fields

Two interesting theorems for physicists to know, which are inverses of each other:
If $\nabla\times\vec{A}=0$ there is a $\psi$ such that $A=\nabla\psi$. 
If $\nabla\cdot\vec{D}=0$ there is a $\vec{C}$ such that $\vec{D}=\nabla\times\vec{C}$.

There is another special second derivatives of which we give a special name, the *Laplacian*:$$\nabla^2=\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}+\frac{\partial^2}{\partial z^2},$$ which is a scalar operator. 

