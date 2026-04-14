---
title: II. - Conservation Laws

---

# Chapter 2 - Conservation laws
## 6. Energy
There are functions that remain constant during motion and depend only on initial conditions. We call these *integrals of motion*. 

Then umber of independent integrals of motion for a closed mechanical system with $s$ degrees of freedom is $2s-1$. 

Since the equations of motion for a closed system do not involve the time explicitly, the choice for origin of time is entirely arbitrary. 

Not all integrals of motion are of equal importance in mechanics. Those whose constancy are derived from the fundamental homogeneity and isotropy of space and time are of profound significance because their quantities are ***conserved***. 

These additionally have an important common property of being additive, i.e., their interaction is negligible and thus the values for the system are equal to the sums of the values of the individual parts.

---
Let us first consider the conservation law resulting from the *homogeneity of time*. 

Due to this homogeneity, the Lagrangian of a closed system does not depend explicitly on time, and thus can be written as $$\begin{aligned}\frac{d\ell}{dt}&=\sum_i\frac{\partial \mathcal{L}}{\partial q_i}\dot{q}_i+\sum_i\frac{\partial \mathcal{L}}{\partial\dot{q}_i}\ddot{q}_i\\&=\sum_i\frac{d}{dt}\left(\dot{q}_i\frac{\partial \mathcal{L}}{\partial\dot{q}_i}\right)\end{aligned}$$or$$\frac{d}{dt}\left(\sum_i\dot{q}_i\frac{\partial \mathcal{L}}{\partial\dot{q}_i}-\mathcal{L}\right)=0$$Hence we get a constant energy of the system during the motion:$$E\equiv\sum_I\dot{q}_i\frac{\partial \mathcal{L}}{\partial\dot{q}_i}-\mathcal{L}.$$ Due to this additivity of the energy, we see that it is a linear function of the Lagrangian. 

This law for the conservation of energy not only holds for closed systems, but also those in constant external fields. 

As we saw, The Lagrangian of a closed system is of the form $\mathcal{L}=T(q,\dot{q})-U(q)$, where $T$ is a quadratic function of the velocities. Using Euler's Theorem on homogenous functions, we have: $$\sum_i\dot{q}_i\frac{\partial\mathcal{L}}{\partial\dot{q}_i}=\sum_i\dot{q}_i\frac{\partial T}{\partial\dot{q}_i}=2T.$$ Substituting in our energy: $$E=T(q,\dot{q})+U(q);$$, which in Cartesian coordinates are $$E=\sum_am_av_a^2+U(\vec{r}_1,\vec{r}_2,\dots).$$ 

Thus, the energy of the system can be written as the sum of the kinetic energy, which depends on the velocities, and the potential energy, which depends on the coordinates of the particles. 

---
### As I understand it
This is an interesting section in the sense that it states that the conservation of energy of mechanical systems are a result of the isotropy of space and time. 

Simply by allowing time to be an axis to be translated on with no change to be a system, we find that energy must be conserved. This 'translation' should be understood to be a symmetry. So the conservation of energy is due to the symmetry of time.

## 7. Momentum
A second conservation law follows from the *homogeneity of space*. From this, the mechanical properties are unchanged by a parallel displacement of the entire system in space. 

Let us therefore consider an infinitesimal displacement $\vec{\epsilon}$, and obtain the condition for the Lagrangian to remain unchanged.

A parallel displacement is a transformation in which every particle in the system is moved by the same amount, the radius $\vec{r}$ becoming $\vec{r}+\vec{\epsilon}$. The change in $\mathcal{L}$ resulting from an infinitesimal change in the coordinates, leaving the particle velocities fixed $$\delta\mathcal{L}=\sum_a\frac{\partial\mathcal{L}}{\partial\vec{r}_a}\cdot\delta\vec{r}_a=\vec{\epsilon}\cdot\sum_a\frac{\partial\mathcal{L}}{\partial\vec{r}_a},$$ where this gives an equivalent condition for $\delta\mathcal{L}=0$ which is $$\sum_a\frac{\partial\mathcal{L}}{\partial\vec{r}_a}=0.$$leading to$$\sum_a\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial\vec{v}_a}=\frac{d}{dt}\sum_a\frac{\partial\mathcal{L}}{\partial\vec{v}_a}=0$$Finally concluding that in a closed mechanical system our vector $$\vec{P}\equiv\sum_a\frac{\partial\mathcal{L}}{\partial\vec{v}_a}$$ and we call this the ***momentum*** of the system. 

If we follow through and differentiate the Lagrangian we arrive at $$\vec{P}=\sum_am_av_a.$$

Unlike energies, the sum of the values of momentum is equal to the sum of the values for individual particles, whether or not their interactions are neglected. 

Note the similar form to $$\frac{\partial\mathcal{L}}{\partial\vec{r}_a}=-\frac{\partial U}{\partial\vec{r}_a}.$$ This leads to the conclusion that $$\sum_a\vec{F}_a=0.$$

In particular, for a system of two particles, $\vec{F}_1+\vec{F}_2=0$: the force exerted by the first particle on the second is equal in magnitude, and opposite in direction, to that exerted by the second particle of the first. This is Newton's third law. 

---
$$\text{PROBLEM}$$A particle of mass $m$ is moving with a velocity $v_1$ leaves a half-space in which its potential energy is a constant $U_1$ and enters another in which its potential energy is a different constant $U_2$. Determine the change in the direction of the motion of the particle. 

**Solution.** The potential energy is independent of the coordinates whose axes are parallel to the plane separating the half-spaces. The component of momentum in that plane is therefore conserved. Denoting $\theta_1$ and $\theta_2$ the angles between the normal to the plane and the velocities $\vec{v}_1$ and $\vec{v}_2$ of the particle before and after passing the plane, we have $\vec{v}_1\sin{\theta_1}=\vec{v}_2\sin{\theta_2}$. The relationship between $\vec{v}_1$ and $\vec{v}_2$ is given by the law of conservation of energy, and the result is $$\frac{\sin\theta_1}{\sin\theta_2}=\sqrt{1+\frac{2}{m\vec{v}_1^2}(U_1-U_2)}.$$

## 8. Center of Mass
The momentum of a closed mechanical system has different values in different (inertial) frames of reference. If a frame $K'$ moves with a velocity $\vec{V}$ relative to another frame $K$, then the velocities $\vec{v}_a'$ and $\vec{v}_a$ of the particles relative to the two frames are such that $\vec{v}_a=\vec{v}_a'+\vec{V}$. The momenta of $\vec{P}$ and $\vec{P}'$ in the two frames are therefore related by $$\vec{P}=\sum_am_av_a=\sum_am_a\vec{v}_a'+\vec{V}\sum_am_a,$$ or concisely $$\vec{P}=\vec{P}'+\vec{V}\sum_am_a.$$

In particular, there is always a frame of reference $K'$ in which the total momentum is zero. We can find the velocity of this frame by finding where $\vec{P}'=0$: $$\vec{V}=\vec{P}/\sum m_a=\frac{\sum m_av_a}{\sum m_a}.$$

Id the total momentum of the mechanical system is zero in a given frame of reference, we say it is ***at rest*** relative to the frame. 

Seeing that the relationship between momentum and velocity for a system is the same as the momentum and velocity of a single particle, can be regarded as expressing the *additivity of mass*. 

We can take the velocity of the system as a whole is the rate of motion of a point whose radial vector is $$\vec{R}\equiv\frac{\sum m_ar_a}{\sum m_a}.$$ We call this point the *center of mass* of the system. 

The energy of a mechanical system which is at rest as a whole is usually called the *internal energy $E_i$*. This includes the kinetic energy of the relative motion of particles in the system and the potential energy of their interactions. Thus, the total energy of a system moving as a whole with velocity $\vec{V}$ can be expressed as $$E=\frac{1}{2}\mu\vec{V}^2+E_i.$$

---
$$\text{PROBLEM}$$
Find the law of transformation of the action $S$ from one inertial frame to another. 

**Solution.** The lagrangian is equal to the difference of the kinetic and potential energies, and is evidently transformed in accordance with: $$\mathcal{L}=\mathcal{L}'+\vec{V}\cdot\vec{P}'+\frac{1}{2}\mu\vec{V}^2.$$ Integrating this with respect to time, we obtain the required law of transformation of the action: $$S=S'+\mu\vec{V}\cdot\vec{R}'+\frac{1}{2}\mu\vec{V}^2t,$$ where $\vec{R}'$ is the radius vector of the center of mass in the frame $K'$.

## 9. Angular Momentum
Let us now derive the conversation law which comes from the *isotropy of space*. This isotropy means that the mechanical properties of a closed system do not vary when it is rotated as a whole in any manner of space. Let us therefore consider an infinitesimal rotation of the system, and obtain the condition for the Lagrangian to be unchanged. 

The vector $\delta\vec{\phi}$ will be used for the infinitesimal rotation. The direction of rotation will follow the right hand rule. The linear displacement of the ned of the radius vector is related to the angle by $|\delta\vec{r}|=r\sin(\theta)\,\delta\phi$. The direction of $\delta\vec{r}$ is perpendicular to the plane of $\vec{r}$ and $\delta\vec{\phi}$, thus: $$\delta\vec{r}=\delta\vec{\phi}\times\vec{r}.$$The velocity increment relative to the fixed system is given by $\delta\vec{v}=\delta\vec{\phi}\times\vec{v}$. 

If these expressions are used with the condition the Lagrangian remains unchanged by rotation we arrive at: $$\delta\mathcal{L}=\sum_a\left(\frac{\partial\mathcal{L}}{\partial\vec{r}_a}\cdot\delta\vec{r}_a+\frac{\partial\mathcal{L}}{\partial\vec{v}_a}\cdot\delta\vec{v}_a\right)=0$$ and our derivative $\partial\mathcal{L}/\partial\vec{v}_a$ replaced by $\vec{p}_a$, and $\partial\mathcal{L}/\partial\vec{r}_a$ by $\dot{\vec{p}}_a$, resuling in: $$\sum_a\left(\dot{\vec{p}}_a\cdot\delta\vec{\phi}\times\vec{r}_a+\vec{p}_a\cdot\delta\vec{\phi}\times\vec{v}_a\right)=0$$ Rearranging, $$\delta\vec{\phi}\sum_a\left(\vec{r}_a\times\dot{\vec{p}}_a+\vec{v}_a\times\vec{p}_a\right)=\delta\vec{\phi}\cdot\frac{d}{dt}\sum_a\vec{r}_a\times\vec{p}_a=0.$$

Due to $\delta\vec{\phi}$ being arbitrary, we know that hte condition $\frac{d}{dt}\sum\vec{r}_a\times\vec{p}_a=0$, and ultimately we conclude: $$\vec{M}\equiv\sum_a\vec{r}_a\times\vec{p}_a,$$ which we call the *angular momentum* or *moment of momentum*, which is conserved in the motion of a closed system. Similar to linear momentum, it is conserved regardless of interaction terms inside of the system. 

---
<center>
    
There are no other additive integrals of the motion. Thus, every closed system has seven such integrals: *Energy, three components of momentum, and three components of angular momentum*. 
    
</center>

---

Looking at the angular momentum from a different frame of reference we see that $$\vec{M}=\vec{M}'+\vec{R}\times\vec{P}.$$ In this, the angular momentum $\vec{M}$ consists of its 'intrinsic angular momentum', in a frame which it's at rest, and the angular momentum $\vec{R}\times\vec{P}$ due to its motion as a whole. 

From the cross product we can see that the law of conservation of angular momentum may hold when subject to a field which is symmetrical along an axis, if the angular momentum is defined relative to an origin lying on that axis. 

An important special case is that of a *centrally symmetric field* or *central field*, id est, a potential field dependent only on distance from the center. The angular momentum is conserved in along any axis passing through the center of the field. 

The component of angular momentum along any axis ca be found by differentiating the Lagrangian: $$M_{e_n}=\sum_a\frac{\partial\mathcal{L}}{\partial\phi_a},$$ where the coordinate $\phi$ is the angle of rotation about the axis $e_n$. 

## 10. Mechanical Similarity
