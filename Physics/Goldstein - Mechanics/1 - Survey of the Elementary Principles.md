---
title: 1 - Survey of the Elementary Principles

---

# Chapter 1 - Survey of the Elementary Principles
## 1.1 - Mechanics of a Particle
First we shall formally define some familiar terms.

Let $\vec{r}$ be the radius vector of a particle from some given origin and $\vec{v}$ its vector velocity: $$\vec{v}=\frac{d\vec{r}}{dt}.$$

The *linear momentum* $\vec{p}$ of a particle is defined as a product of particle mass and velocity: $$\vec{p}=m\vec{v}.$$

As a consequence of interactions with external objects and fields the particles may experience various types of forces. The vector sum of these forces is $\vec{F}$ and is contained in newton's second law of motion which follows the differential equation: $$\vec{F}=\frac{d\vec{p}}{dt}\equiv\dot{\vec{p}}.$$

We may also write this as $$\vec{F}=\frac{d}{dt}(m\vec{v})$$ or when the mass is constant this reduces to $$\vec{F}=m\frac{d\vec{v}}{dt}=m\vec{a}$$ where $\vec{a}$ is the vector acceleration of the particle defined by $$\vec{a}\equiv\frac{d^2\vec{r}}{dt^2}.$$

A reference frame where the equations of force are valid are called *inertial* or *Galilean*. 

---
Many important conclusions of mechanics are expressed in the form of conservation theorems. For example,

*Conservation Theorem for the Linear Momentum of a Particle: If the total force $\vec{F}$, is zero, then $\dot{\vec{p}}=0$ and the linear momentum $\vec{p}$ is conserved.*

---

The angular momentum of a particle about point $O$, denoted by $\vec{L}$, is defined as: $$\vec{L}=\vec{r}\times\vec{p},$$where $\vec{r}$ is the radius vector from $O$ to the particle. 

We define the *moment of force* or *torque* about $O$ as $$\vec{N}=\vec{r}\times\vec{F}.$$ or analogously$$\vec{r}\times\vec{F}=\vec{N}=\vec{r}\times\frac{d}{dt}(m\vec{v}).$$ We can also write it by using the vector identity: $$\frac{d}{dt}(\vec{r}\times m\vec{v})=\vec{v}\times m\vec{v}+\vec{r}\times\frac{d}{dt}(m\vec{v}),$$ where $\vec{v}\times\vec{mv}$ obviously vanishes, leading us to $$\vec{N}=\frac{d}{dt}(\vec{r}\times m\vec{v})=\frac{d\vec{L}}{dt}\equiv\dot{\vec{L}}.$$

Which leads us to another conservation theorem: 

*Conservation Theorem for Angular Momentum: If the total torque, $\vec{N}$, is zero, then $\dot{\vec{L}}=0$ and the angular momentum $\vec{L}$ is conserved.*

---
Next we'll consider the work done by an external force $\vec{F}$ upon a particle going from point 1 to point 2, defined as: $$W_{12}=\int_1^2\vec{F}\cdot d\vec{s}.$$ and for constant mass (henceforth assumed):$$\int\vec{F}\cdot d\vec{s}=m\int\frac{d\vec{v}}{dt}\cdot\vec{v}dt=\frac{m}{2}\int\frac{d}{dt}(v^2)dt,$$ and therefore $$W_{12}=\frac{m}{2}(v^2_2-v^2_1).$$ 

The scalar quantity $\frac{mv^2}{2}$ is called the *kinetic energy* of the particle and is denoted by $T$, so that hte work does is equivalent to the change in the kinetic energy: $$W_{12}=T_2-T_1.$$

The work around a closed path is zero, id est, $$\oint\vec{F}\cdot d\vec{s}=0.$$

From the requirement that $W_{12}$ be independent of the path of integration, then $\vec{F}$ must be the gradient of some scalar function of the potential: $$\vec{F}=-\nabla V(\vec{r}),$$ where $V$ is called the *potential* or *potential energy*.

For a conervative system, the work done by the forces is $$W_{12}=V_1-V_2.$$ Combining this with with our work being a change in kinetic forces, we arrive at $$T_1+V_1=T_2+V_2.$$ This is the conservation of energy of a particle.

*The Energy Conservation Theorem for a Particle: If the forces acting on a particle are conservative, then the total mechanical energy of the particle, $T+V$, is conserved.* 

---
### As I understand it
This is just a simple review of basic physics 101-esque things. I do love the description of force as the gradient of the potential at the position of a particle, to me it demystifies force, but retains the mystery of energy. Still don't get that. I'm disturbed that I'm not really comfortable with the $\int\vec{F}\cdot d\vec{s}$. The dot with the differential is really bugging me. 

We hit conservation of linear momentum, angular momentum, and energy, so we wrapped up those conserved quantities of a mechanical process. 

## 1.2 Mechanics of a System of Particles
Generalizing from the last section to those of many particles we must distinguish *external forces* from *internal forces*, thus, we distinguish the $i$th particle as such: $$\sum_j\vec{F}_{ji}+\vec{F}_i^{(e)}=\dot{\vec{p}}_i\,,$$ where $\vec{F}_i^{(e)}$ is the external force on the $i$th particle, and $\vec{F}_{ji}$ is the internal force on the $i$th particle due to the $j$th particle ($F_{ii}=0$). Assuming (Which is not true for all forces), that the forces the particles exert on each other are equal and opposite (sometimes called the *weak law of action and reaction*)  summed over all particles takes the form $$\frac{d^2}{dt^2}\sum_im_ir_r=\sum_i\vec{F}_i^{(e)}+\sum_{i,j}F_{ji},\quad i\neq j$$

To reduce the left-hand side, we define a vector $\vec{R}$ as the average radii vectors of particles, weighted in proportion to their mass: $$\vec{R}-\frac{\sum m_ir_i}{\sum m_i}=\frac{\sum m_ir_i}{M}.$$

The vector $\vec{R}$ defines a point known as the *center of mass*, or more loosely, the *center of gravity*. 

This reduces our equation to: $$M\frac{d^2\vec{R}}{dt^2}=\sum_i\vec{F}_i^{(e)}\equiv\vec{F}^{(e)},$$ which means that the center of mass moves as if the total external force were acting on the entire mass of the system concentrated at the center of mass. 

We find the total linear momentum of the system to be: $$\vec{P}=\sum m_i\frac{d\vec{r}_i}{dt}=M\frac{d\vec{R}}{dt}.$$

*Conservation Theorem for the Linear Momentum of a System of Particles: If the total external force is zero, the total linear momentum is conserved.*

For angular momentum, if the internal forces between the two particles, in addition to being equal and opposite, also lie along a line joining the particles (called the *strong law of action and reaction*), then all cross products vanish and we arrive at $$\frac{d\vec{L}}{dt}=\vec{N}^{(e)}$$

*Conservation Theorem for Total Angular Momentum: $\vec{L}$ is constant in time if the applied (external) torque is zero.*

The rest of this section is just a shift of center of mass potential showing the additive nature of vector potentials. Standard stuff. Ends with showing that in a rigid body that internal fores do no work. 

## 1.3 Constraints