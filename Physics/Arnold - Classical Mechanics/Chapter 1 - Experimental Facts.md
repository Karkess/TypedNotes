---
title: Chapter 1 - Experimental Facts

---

# Part I - Newtonian Mechanics
## Chapter 1 - Experimental Facts
### 1. The Principles of relativity and Determinacy 
This chapter covers experimental "facts" at the heart of classical mechanics. These for the most part are just approximately true and can be disproven by more exact experiments.

A. *Space and Time*
Our space is three-dimensional and Euclidean, and time is one-dimensional.

B. *Galileo's Principle of Relativity*
There exist coordinate systems (called inertial) possessing the following properties:
1. All the laws of nature at all moments in time are the same in all inertial coordinate systems.
2. All coordinate systems in uniform rectilinear motion with respect to an inertial one are themselves inertial. 

C. *Newton's Principle of Determinacy*
The initial state of a mechanical system uniquely determines all of its motion.

---
### 2. The Galilean Group and Newton's Equations

A. *Notation*
We denote the set of all real numbers by $\mathbb{R}$. We denote by $\mathbb{R}^n$ an n-dimensional real vector space. 

*Affine* n-dimensonal space $\mathbb{A}^n$ is distinguished from $\mathbb{R}^n$ in that there is "no fixed origin." The group $\mathbb{R}^n$ acts on $\mathbb{A}^n$ as a group of parallel displacements. $$a\rightarrow a+\vec{b},\quad a\in\mathbb{A}^n,\;\vec{b}\in\mathbb{R}^n,\;a+\vec{b}\in\mathbb{A}^n.$$ Note: The sum of two points in $\mathbb{A}^n$ is not defined, but their difference is defined and is a vector in $\mathbb{R}^n$. 

A *Euclidean structure* on the vector space $\mathbb{R}^n$ is a positive definite symmetric bilinear form called a *scalar product*, defining the distance: $$\rho(x,y)=\|x-y\|=\sqrt{(x-y,x-y)}$$ between the points in the *Affine* space. An affine space with this distance function is called a *Euclidean space* and is denoted $\mathbb{E}^n$. 

---
B. *Galilean Structure*
Galilean spacetime structure consists of three elements:
1. The universe is a four-dimension affine space $\mathbb{A}^4$. The points of $\mathbb{A}^4$ are called *world points* or *events*. The parallel displacements of the universe $\mathbb{A}^4$ constitute a vector space $\mathbb{R}^4$. 
2. Time is a linear mapping $t:\mathbb{R}^4\rightarrow\mathbb{R}$ from a vector space of parallel displacements of the universe to the real "time axis." The *time interval* from event $a\in\mathbb{A}^4$ is the number $t(b-a)$. If $t(b-a)=0$, then events $a$ and $b$ are called *simultaneous*. 
    The set of events simultaneous events $\mathbb{A}^3$ with a given event form a three dimensional affine subspace in $\mathbb{A}^4$. It is called a *space of simultaneous events $mathbb{A}^3$.
3. The *distance between simultaneous events* $$\rho(a,b)=\|a-b\|=\sqrt{(a-b,a-b)}\quad\,a,b\in\mathbb{A}^3$$ is given by a scalar product on the space $\mathbb{R}^3$. This distance makes every space of simultaneous event into the three-dimensional euclidean space $\mathbb{E}^3$.

---
C. *Motion, velocity acceleration*
A motion in $\mathbb{R}^n$ is a differential mapping $x:I\rightarrow\mathbb{R}^n$, where $I$ is an interval on a real axis. The derivative: $$\dot{\vec{x}}(t_0)=\frac{d\vec{x}}{dt}\bigg|_{t=t_0}=\lim_{h\rightarrow0}\frac{\vec{x}(t_0+h)-x(t_0)}{h}\in\mathbb{R}^n$$is called a *velocity vector* at the point $t_0\in I$.
The second derivative $$\ddot{x}(t_0)=\frac{d^2\vec{x}}{dt^2}\bigg|_{t=t_0}$$ is called the *acceleration vector* at the point $t_0$. 
The image of a mapping $x:I\rightarrow\mathbb{R}^N$ is called a *trajectory* or *curve* in $\mathbb{R}^N$. 

We now define a mechanical system of $n$ points moving in three-dimensional euclidean space. 
Let $\vec{x}:\mathbb{R}\rightarrow\mathbb{R}^3$ be a motion in $\mathbb{R}^3$. The graph of this mapping is a curve in $\mathbb{R}\times\mathbb{R}^3$.

A curve in galilean space space is called a *world line*. A motion of a system of $n$ points gives, in galilean space, $n$ world lines. 

A direct product of $n$ copies of $\mathbb{R}^3$ is called the *configuration space* of the system of $n$ points. Our $n$ mapping $\vec{x}_i:\mathbb{R}\rightarrow\mathbb{R}^3$ define one mapping of the motion of a system of $n$ points: $$\vec{x}:\mathbb{R}\rightarrow\mathbb{R}^N\quad n=3n$$

---
D. *Newton's Equations*
Newton's principle of determinacy - All motions of a ytem are uniquely determined by initial positions $(\vec{x}(t_0)\in\mathbb{R}^N)$ and initial velocities $(\vec{\dot{x}}(t_0)\in\mathbb{R}^n)$. 
Specifically, there is a function $\vec{F}:\mathbb{R}^N\times\mathbb{R}^N\times\mathbb{R}\rightarrow\mathbb{R}^N$ such that $$\vec{\ddot{x}}=\vec{F}(\vec{x},\vec{\dot{x}},t).$$ This is called Newton's Equation, as he used it as the basis of mechanics.

---
E. *Constraints imposed by the principle of relativity*
Galileo's Principle of relativity states that in physical space-time there is a selected galilean structure that if we subject the world lines of all points of any mechanical system to one and the same galilean transformation, we obtain world lines of the same system. 

**Example 1** Time translations. Invariance with respect to time translation means that "the laws of nature remain constant". This means if $\vec{x}=\vec{\phi}(t) is a solution to Newton's equation, then for any $s\in\mathbb{R},\vec{x}=\vec{\phi}(t+s)$ is also a solution. This shows that the right-hand side does not depend on time: $$\vec{\ddot{x}}=\vec{\phi}(\vec{x},\vec{\dot{x}}).$$

**Example 2** Translations in three-dimensional space are  galilean transformations. Invariance with respect to such translations means that *space* is *homogeneous* or "has the same properties at all points." This means that an inertial system of coordinates can depend on relative velocities. 

**Example 3** Among the galilean transformations are the rotations in three-dimensional space. Invariance with respect to these rotations means that *space is isotropic*.

Thus, if $\vec{\phi}_i:\mathbb{R}\rightarrow\mathbb{R}^3(i=1,\dots,n)$ is a motion of a system of particles satisfying Newton's equation and $G:\mathbb{R}^4\rightarrow\mathbb{R}^3$ is an orthogonal transformation, then the motion $G\vec{\phi}_i:\mathbb{R}\rightarrow\mathbb{R}^3(i,\dots,n)$ also satisfies newtons equations. In other words: $$\vec{F}(G\vec{x},G\vec{\dot{x}})=G\vec{F}(\vec{x},\vec{\dot{x}}).$$

---
### 3 Examples of mechanical systems
**Example 1**: *A stone falling to earth*
Experiments show that $$\ddot{x}=-g\quad g\approx9.8\mathrm{m/s}^2\,\text{(Galileo)},$$ where $x$ is the height of a stone above the surface of the Earth.
Introducing "potential energy" as $U=gx$, then $$\ddot{x}=-\frac{dU}{dx}.$$ If $U:\mathbb{E}^N\rightarrow\mathbb{R}$ is a differential function on euclidean space, then we will denote $\frac{\partial U}{\partial x}$ the gradient of the function $U$. 

---
**Example 2**: *Falling from a great height*
Newton discovered a more precise law of falling bodies: $$\ddot{x}=-g\frac{r^2_0}{r^2},$$ where $r=r_0+x.$

This can also be written as $$U=-\frac{k}{r}\quad =gr^2_0,$$ inversely proportional to the distance to the center of the earth. 

---
**Example 3**: *Motion of a weight along a line under the action of a spring*
Experiments show that under small extensions of the spring the equation of the motion of the weight will be $$\ddot{x}=-\alpha^2x.$$ 
The potential energy of this system can be represented by $$U=\frac{\alpha^2x^2}{2}.$$

---
**Example 4**: *Conservative Systems*
Let $\mathbb{E}^{3n}=\mathbb{E}^3\times\cdots\times\mathbb{E}^{3}$ be the configuration space of a system of $n$ points in the euclidean space $\mathbb{E}^3$. Let $U:\mathbb{E}^{3n}\rightarrow\mathbb{R}$ be a differentiable function and let $m_1,\dots,m_n$ be positive numbers.

**Definition.** The motion of $n$ points, of masses $m_1,\dots,m_n$, in the potential field with potential energy $u$ is given by the system of differential equations $$m_i\vec{\ddot{x}}_i=-\frac{\partial U}{\partial\vec{x}_i}\quad i=1,\dots n.$$
The equations of motion in Examples 1 to 3 have this form can be written in the same form. 

For example, the three-body problem of celestial mechanics in which $$U=-\frac{m_1m_2}{\|\vec{x}_1-\vec{x}_2\|}-\frac{m_2m_3}{\|\vec{x}_2-\vec{x}_3\|}-\frac{m_3m_1}{\|\vec{x}_3-\vec{x}_1\|}.$$