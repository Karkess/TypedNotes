---
title: I. - The Equations of Motion

---

# Part I - The Equations of Motion
## Chapter 1 - Generalized co-ordinates
A *particle* is a body whose dimensions may be neglected in describing its motion. 

Described by the radius vector: $\vec{r}=\begin{pmatrix}x\\y\\z\end{pmatrix}$
The derivative $\vec{v}=\frac{d\vec{r}}{dt}=\dot{\vec{r}}$ of $\vec{r}$ with respect to $t$ describes the *velocity* of the particle.
The second derivative $\vec{a}=\frac{d\vec{v}}{dt}=\ddot{\vec{r}}$ of $\vec{r}$ with respect to $t$ is the *acceleration* of the particle. 

---
To define the position of $N$ particles in space, we need to specify $N$ radius vectors, i.e. $3N$ coordinates. The number of independent quantities needed to describe the position of any system is called the *degrees of freedom*. Any $s$ quantities $q_1,q_2,\dots,q_s$ which completely define the position of a system with $s$ degrees of freedom are called *generalized coordinates*

For any given state where the generalized coordinates are specified, the "mechanical state" is not completely known. Once all of the positions and velocities of all of the particles are known, the system is completely determined and can be calculated.

---
The relations between accelerations, velocities, and coordinates are called *equations of motion*.

---
### As I understand it, summary (Chapter 1).
This section is simply saying we can understand an isolated system mechanically as long as we understand the position and velocity of each particles, here denoted $(\vec{r},\vec{v}=\dot{\vec{r}})$ respectively. The 'dot' notation comes from Newton, and just means derivative with respect to time, so $\dot{x}=\frac{dx}{dt}$.

Generalized coordinates are just the known positions/relations (so these can be angles, for example) of all particles, and the degree of freedom is simply the minimum number of values needed to know all of the positions in whatever space you're working in (Here think like 2D versus 3D, but later this can be more abstract like a space of functions).

If you know the positions and velocities of all of the particles, then you know the current and future state of the systems from a classical mechanics perspective. We actually do simple simulations of materials from this standpoint! This is called Molecular Dynamics. 
## Chapter 2 - The principle of least action

The most general formulation of the law governing the motion of mechanical systems is the *principles of least action* or *Hamilton's priciple*, where the entire system can be characterized by $\mathcal{L}(q,\dot{q},t)$. 

---
If a system occupies positions defined by two coordinates at $t_1$ and $t_2$, the condition for hte motion of the system is that in which $$S=\int^{t_2}_{t_1}\mathcal{L}(q,\dot{q},t)\,dt$$ is minimized. Here, $\mathcal{L}$ is the *Lagrangian* of the system, and the integral is called the *action*. 

---
To minimize the value of our function, takes $q(t)$ to be the function of which $S$ is minimized, then, any function of the form $$q(t)+\delta q(t),$$ where $\delta q(t)$ is called the *variation* of the function. 
Since $q(t)$ is minimized, at $t_1$ and $t_2$ we have $$\delta q(t_1)=\delta q(t_2)=0.$$Which leads to a change in $S$ when we substitute $q=q+\delta q$ for $q$ we arrive at $$\int^{t_2}_{t_1}\mathcal{L}(q+\delta q,\dot{q}+\delta\dot{q},t)\,dt-\int^{t_2}_{t_1}\mathcal{L}(q,\dot{q},t)\,dt$$

The necessary condition for $S$ to be minimized by these terms is called the *first variation*, and requires that these leading terms of the first order should be zero. 

Thus, our ***principle of least action*** can be written as $$\delta S=\delta\int_{t_1}^{t_2}\mathcal{L}(q,\dot{q},t)\,dt=0,$$ or, effecting the variation (This step confused me, but it's not a calculation step from the above equation, instead, just think of it as finding the variation on the Lagrangian in the integral), $$\int_{t_1}^{t_2}\left(\frac{\partial\mathcal{L}}{\partial q}\delta q+\frac{\partial\mathcal{L}}{\partial\dot{q}}\delta\dot{q}\right)\,dt=0.$$ Since $\delta\dot{q}=\frac{d\delta q}{dt}$, we obtain (by integrating the second term by parts) $$\delta S=\left[\frac{\partial\mathcal{L}}{\partial{\dot{q}}}\,\delta q\right]^{t_2}_{t_1}+\int^{t_2}_{t_1}\left(\frac{\partial\mathcal{L}}{\partial q}-\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial \dot{q}}\right)\,\delta q\,dt=0.$$ and from $\delta q(t_1)=\delta q(t_2)=0$ we know that inside the integrand must be zero, thus, $$\frac{d}{dt} \left(\frac{\partial{\mathcal{L}}}{\partial \dot{q}}\right)-\frac{\partial\mathcal{L}}{\partial q}=0$$ When the function has more than one degree of freedom, the $s$ for different funtions must be varied independently, and we obtain $s$ equations of the form$$\frac{d}{dt}\left(\frac{\partial\mathcal{L}}{\partial\dot{q}_i}\right)-\frac{\partial\mathcal{L}}{\partial q_i}=0\quad\quad i\in\mathbb{N}.$$ These equations constitute a set of $s$ second-order equations for $s$ unknown functions $q_i(t)$.
The general solution would contain $2s$ arbitrary constants. These would be the initial conditions to specify what state the system was in at some instant.

If a mechanical system had two parts which non-interacting parts, the Lagrangian of the whole system is $$\mathcal{L}_{system}=\mathcal{L}_A+\mathcal{L}_B.$$

It is also evident that the the multiplication of the system by an arbitrary constant, say, $\lambda$, has no impact on the equations of motion.

One last remark, consider $\mathcal{L}'(q,\dot{q},t)$ and $\mathcal{L}(q,\dot{q},t)$, differing by the time derivative of some function $f(q,t)$: $$\mathcal{L}'(q,\dot{q},t)=\mathcal{L}(q,\dot{q},t)+\frac{d}{dt}\,f(q,t).$$ Integrating with our original conditions these two functions we arrive at $$S'=\int_{t_1}^{t_2}\mathcal{L}'(q,\dot{q},t)=\int_{t_1}^{t_2}\mathcal{L}(q,\dot{q},t)+\int_{t_1}^{t_2}\frac{df}{dt}\,dt=S+f(q^{(2)},t_2)-f(q^{(1)},t_1);$$ functions that differ by a quantity when varied is zeroed, thus $\delta S'=0$ and $\delta S=0$ are equivalent, and the equations of motion are unchanged. Thus the Lagrangian is defined only to within an additive total time derivative of any function of coordinates and time.

---
### As I understand it, summary (Chapter 2)
Right now, don't worry so much about the meaning of these equations physically, but more of the general structure of the solutions. These equations are saying that there is some function called the Lagrangian, which we label by $\mathcal{L}$, which has inputs of $(q,\dot{q},t)$. And we're saying there is something called an *action*, $S$, which we want to minimize, meaning that any variation (technically first-order change) vanishes. It's not necessarily that the action itself is minimized, but one that is stationary. A distinction that matters more when the Lagrangian is further generalized in later coursework. 

This requires a greater understanding of what integration really is, more than just area under a curve. If you think about integrating velocity, you get the total distance traveled. So in some sense, integration can be thought of as 'total amount of something that has occurred'. So here we want to minimize the total variation of something that has occured (eliminate variation), and that somethng is the Lagrangian. The Lagrangian in this case, a mechanical system, can be thought as a trade off in the energy between kinetic energy (the motion of the particle) and the potential energy (the position of the particle). The Lagrangian is frequently stated to be $\mathcal{L}=T\;(\text{Kinetic Energy})-V\;(\text{Potential Energy})$, where this is a little more obvious. 

So essentially minimizing the action is minimizing "trade off" in energy, like sometimes having more kinetic energy in one moment will reduce the potential energy needed later. It's a little tricky to wrap your brain around, but to summarize:$$\text{The action is the stationary under variation trade-off between}$$ $$\text{kinetic and potential energy of a mechanical system.}$$

The rest is just mathing our way through some derivations to get it into the form of the Euler-Lagrange equations (named after Euler in his derivation of the concept in calculus of variations, and Lagrange for application to physics).

The separation of Lagrangians where you can add them independently and multiply them by a number and leave them unchanged might seem arbitrary right now, and when I was an undergrad I would have been like "yeah okay whatever", but that's actually probably the most impactful bit of information in the entirety of the derivations above. These constraints might look familiar  from definitions in linear algebra, and it's crucial to know that these relationships hold when you revisit these topics later as an algebra or with tools of functional analysis. 

Some more fun facts involving the definitions we talked about above, you might have heard of Feynman's Path Integral interpretation of quantum mechanics. Essentially, we take the action above, but not just minimizing one path, but vary it for every single path based on what we call the 'phase' of the wave(function). This concept leads to an interpretation that 'particles' in quantum mechanics take every single path simultaneously and through a combination of constructive and destructive interference end up with the highest probability by far of taking the classical path above. 

Essentially, this seemingly innocuous mechanical derivation above using Lagrangian mechanics turns out to be an extremely powerful tool for analyzing our most advanced physics at the smallest scales in the universe, and if you continue your physics education you will see them again and again in quantum mechanics, quantum field theory, string theory, and more.

As a note: this is a kind of 'sloppy' presentation of the Lagrangian. The notion of it being purely mechanical actually undersells its value, and the action is more general than a minimization of this trade-off between mechanical energies. We want a 'stationary' action which has a much deeper meaning besides just a minimization of variation. Something that's worth thinking about, is that Planck's constant, $h$, has units of action. 

One last tiny note, is the value of the freedom from a coordinate system hinted at above. In general, we want our physics to hold no matter what coordinate system we use, if we're in 3D Cartesian, spherical, cylindrical, or any of countless others, the physics should work out to have the same physical phenomena. 
## Chapter 3 - Galileo's relativity principle

When considering mechanical phenomena we are generally required to choose a *frame of reference*, as the laws of motion appear in a different form from different frames of reference. 
In choosing a frame of reference, we want one where space is homogeneous and isotropic, and time is homogeneous. We call this special frame of reference an *inertial frame*. In particular, a frame in which a free body at rest remains at rest.

This has some implications for the Lagrangian. Since space and time are both homogeneous, the position and time of the particle cannot be explicitly used within the Lagrangian, meaning that it is a function of the magnitude of the velocity alone: $\mathcal{L}(v^2)$. *(Note: this is not always true, but it is true under assumptions that are implicit in this section of Landau and Lifshitz, so be careful about blind application. In particular, this assumes a free particle in an inertial frame with no external fields.)*

The independence from $\vec{r}$ means $\partial\mathcal{L}/\partial\vec{r}=0$, and thus the Euler-Lagrange equation is $$\frac{d}{dt}\left(\frac{\partial\mathcal{L}}{\partial\vec{v}}\right)=0,$$ when $\partial\mathcal{L}/\partial\vec{v}$ is a constant. As this is a function of only velocity, it follows that $\vec{v}=\text{constant}$. 

The result of all of this is that in an inertial frame, any free motion with a velocity has both a constant magnitude and direction, this is the *law of inertia*. 

If there is another frame moving in a straight line with regards to the inertial frame, the laws of free motion in the other frame will be the same as the original frame: In the sense that free motion takes place with constant velocity. Experiment shows that these frames are equivalent in all mechanical respects, and that there are an infinite number of inertial reference frames moving relative to one another. In every frame, the laws of mechanics, as well as space and time are the same. This is *Galileo's relativity principle*. 

The fact that there an infinite number of equivalent reference frames demonstrates that there is no singular preferred or "absolute" reference frame. 

The coordinates $\vec{r}$ and $\vec{r}\,'$ of a given point of two different frames of reference $K$ and $K'$ in which the first moves relative to the other by $\vec{V}$ relates the two by $$\vec{r}=\vec{r}\,'+\vec{V}t,$$ with time being the same in the two frames: $$t=t'.$$
The assumption that time is absolute is one of the foundations of classical mechanics.

The above isolated formula are referred to as *Galilean Transformations*. They can be formulated by asserting the invariance of the mechanical equations of motion under any such transformation. 

---
### As I understand it, summary (Chapter 3)
So we all have heard of and possibly even know Einstein's special relativity which says that Galilean relativity breaks as you approach speeds of light. 

A valuable descriptor that makes the above more intuitive is that inertial reference frames are once that aren't accelerating. The above definitions provided to them restrict inertial reference frames to ones that do not accelerate, but I feel like in our normal physics pedagogy it makes more sense to say that non-accelerating reference frames enforce the above relative motions. 

The intuition behind Galilean relativity if you've forgotten from your intro class is that it's basically the principle that says someone dropping a metal ball out of a moving car sees it drop straight down and someone watching it be dropped standing on the side of the road sees the ball move in the direction of the vehicle falling down. 

Here it talks a bit about homogeneous (same all throughout) and isotropic (same in all directions) space and time and how that impacts the Lagrangian. This again might seem strange, but again hints heavily at a freedom from coordinate system. You'll get deep in this when you begin introductions to gauge theory. 

## Chapter 4 - The Lagrangian for a free particle
Now we will determine the form of the Lagrangian in the simplest case, a free particle relative to an inertial frame of reference. 

From the last chapter, we know the Lagrangian must depend on the square of the velocity alone. To discover what the form of this dependence is, we make use of Galilean relativity:

Say we have an inertial reference frame $K$ moving with an infinitesimal velocity $\epsilon$ with respect to another reference frame $K'$, we then have $\vec{v}'=\vec{v}+\vec{\epsilon}$. 
Since the equations of motion have the same form in every frame, the Lagrangian ($\mathcal{L}(\vec{v}\,^2)$) must be converted by this transformation into a function $\mathcal{L}'$ which differs from $\mathcal{L}(\vec{v}\,^2)$ if at all, only by the total time derivative of a function of coordinates and time.

We have $\mathcal{L}'=\mathcal{L}(\vec{v}'\,^2)=\mathcal{L}(\vec{v}\,^2+2\vec{v}\cdot\vec{\epsilon}+\vec{\epsilon}\,^2)$. Expanding this expression in powers of $\epsilon$ and neglecting terms above the first order we have: (Note, this is a Taylor expansion and we just chop off $\vec{\epsilon}\,^2$ terms and higher exponents) $$\mathcal{L}(\vec{v}'\,^2)=\mathcal{L}(\vec{v}^2)+\frac{\partial\mathcal{L}}{\partial \vec{v}^2}\,2\vec{v}\cdot\vec{\epsilon}.$$ The second term of the right of this equation is a total time derivative only if it is a linear function of the velocity $\vec{v}$. Hence, $\frac{\partial\mathcal{L}}{\partial\vec{v}\,^2}$ is independent of velocity $\vec{v}$. This means the Lagrangian is proportional to the square of the velocity, which we write as $$\mathcal{L}=\frac{1}{2}mv^2.$$ 
Thus, for our $\mathcal{L}'$: $$\mathcal{L}'=\frac{1}{2}mv'\,^2=\frac{1}{2}m(\vec{v}+\vec{V})^2=\frac{1}{2}mv^2+m\vec{v}\cdot\vec{V}+\frac{1}{2}mV^2$$ or $$\mathcal{L}'=\mathcal{L}+d(m\vec{r}\cdot\vec{V}+\frac{1}{2}mV^2\,t)/dt$$ The second term is a total time derivative and may be omitted. 

Here, $m$ is the mass of the particle. The additive property of the Lagrangian for noninteracting particles discussed earlier means that $$\mathcal{L}=\sum\frac{1}{2}m_av_a^2.$$

Without the additive property above, the mass is meaningless, as the Lagrangian can be multiplied by any number without changing the equations of motion. It is only the ratios of the masses of particles that is meaningful. 

*There is a quick explanation why mass cannot be negative in classical mechanics here which I am omitting, but essentially minimizing a negative = no good.*

It is useful to notice that $$v^2=\left(\frac{dl}{dt}\right)^2=\frac{(dl)^2}{(dt)^2}$$ Hence, to obtain the Lagrangian, it is sufficient to find the square of the element of arc $dl$ in a given system of coordinates. 

Examples:
- Cartesian: $dl^2=dx^2+dy^2+dz^2$, so $$\mathcal{L}=\frac{1}{2}m(\dot{x}^2+\dot{y}^2+\dot{z}^2).$$
- Cylindrical: $dl^2=dr^2+r^2d\phi^2+dz^2$, so$$\mathcal{L}=\frac{1}{2}m(\dot{r}^2+r^2\dot{\phi}^2+\dot{z}^2).$$
- Spherical: $dl^2=dr^2+r^2d\theta^2+r^2\sin^2\theta \,d\phi$, so $$\mathcal{L}=\frac{1}{2}m(\dot{r}^2+r^2\dot{\theta}^2+r^2\dot{\phi}^2\sin^2\theta).$$

---
### As I understand it, summary (Chapter 4)
This chapter is a little more conceptually straightforward than others, just some math to describe the Lagrangian for a free particle, as the name suggests. The Taylor expansion I thought was a bit tricky so I actually explicitly defined that in the chapter notes themselves. 

One thing of note that's important is the definition of a total time derivative, which hasn't been discussed in the text thus far. It's just a result from the chain rule, so if you have for example $\frac{d}{dt}F(\vec{x},t)$ the total time derivative is $\frac{dF}{d\vec{x}}\cdot\vec{v}+\frac{dF}{dt}$. If we added some other order of $\vec{v}$, it would no longer represent a free particle in an inertial reference frame, by our definitions of inertial reference frame and free particle. 

Here, a free particle is one where there are no external forces and thus no accelerations. This is not stated outright because this framework is building up to a point where forces are not fundamental, but instead there are symmetries at play which determine the motion of a particle. Instead, try and think of a free particle more abstractly as simply a particle with a uniform velocity. 

## Chapter 5 - The Lagrangian for a system of particles
Now we'll look at a system of particles which interact with others in the system but not with any external bodies, i.e., a *closed system*. 

To do this we will add an interaction term for the particles, which we denote $U$: $$\mathcal{L}=\sum\frac{1}{2}m_av_a^2-U(r_1,r_2,\dots),$$ where $r_a$ is the radius of the $a^\text{th}$ particle. This is the general form of the Lagrangian for a closed system. Here, the sum $\sum\frac{1}{2}m_av_a^2$ is called the *kinetic energy* and $U$ is called the *potential energy*, for reasons discussed in Chapter 6. 

Notice that $U$ depends only on the positions of other particles, this shows that interactions are instantaneously propagated in this model, which is a restriction of Galilean relativity. 

An interesting note, as time is homogeneous, replacing $t$ by $-t$ results in valid unchanged equations of motion, and thus all motions obey the laws of classical mechanics in reverse as well.

Knowing the Lagrangian, we can derive the equations of motion: $$\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial\vec{v}_a}=\frac{\partial\mathcal{L}}{\partial\vec{r}_a}.$$Substituting in the first equation of this chapter arrives at: $$m_a\frac{d\vec{v}_a}{dt}=-\frac{\partial U}{\partial\vec{r}_a}$$In this form the equations of motion are called *Newton's Equations*, and the vector $$\vec{F}=-\frac{\partial U}{\partial\vec{r}_a}$$ is called the *force* on the $a^\text{th}$ particle. 

Generalizing our equations of motions outside of Cartesian coordinates we use instead $q_i$, leading us to the new Lagrangian $$\mathcal{L}=\frac{1}{2}\sum_{i,k}a_{i,k}(q)\dot{q}_i\dot{q}_k-U(q),$$ where $a_{i,k}$ are functions of coordinates only. 

When we swap to an open system, say, system $A$ with another interacting system $B$, we can treat the whole system $A+B$ as closed, and the difference in the Lagrangian comes down to: $$\mathcal{L}_A=T_A(q_A,\dot{q}_A)-U(q_A,q_B(t)),$$ so the potential energy may have an explicit time dependence. 

As an example, a when a single particle moves in an external field, the general form of the Lagrangian is: $$\mathcal{L}=\frac{1}{2}mv^2-U(\vec{r},t),$$ and the equation of motion is $$m\dot{\vec{v}}=-\frac{\partial U}{\partial \vec{r}}$$ A field that acts with the same force is called 'uniform', and thus would have the form $$U=-\vec{F}\cdot\vec{r}.$$

As a concluding remark, there may be various mechanical systems in which the interaction between different bodies takes the form of *constraints*, i.e. restrictions on their relative position. In general, this introduces a new factor into the problem in that the bodies result in friction at their points of contact and cease to be problems of pure mechanics. If this friction is so small it can be neglected, we can simply reduce the number of degrees of freedom of the system to a value less than $3N$ and once again use the Lagrangian. 

### As I understand it, summary. (Chapter 5)
This chapter introduces one of my favorite derivations with the introduction of Lagrangians, and that is that in this special case it can be reduced to the form of Newton's famous law and takes the role of Newtonian mechanics. You will discover later on that it becomes much more. 

As a fun conceptual side note, this also shows where the idea of 'force' comes from. We treat it as somewhat fundamental in introductory physics, but in fact it is just a convenient way to describe how the potential changes with the position of the particle. If you've ever wondered what 'force' is, as in like, a substance or something, now you instead have to ask what potential energy is and be equally if not more confused.

## Problems
Find the Lagrangian for all of the following problems assuming a gravitational field $g$.

---
![image](https://hackmd.io/_uploads/S1gvBfmHZg.png)
**Solution:** We take the angles $\phi_1$ and $\phi_2$ which rods $I_1$ and $I_2$ make with the assumed direction of $g$. Then, for particle $m_1$ we have $T_1=\frac{1}{2}\,m_1\,I_1^2\,\phi_1^2,\;U=-m_1\,g\,I_1\cos{\phi_1}$. 

For the kinetic energy of the second particle, we express the coordinates in terms of the angles: $$x_2=I_1\sin{\phi_1}+I_2\sin{\phi_2}\quad y_2=I_1\cos{\phi_1}+I_2\cos{\phi_2},$$ so $$\begin{aligned}T_2&=\frac{1}{2}m_2(\dot{x}_2\,^2+\dot{y}_2\,^2)\\&=\frac{1}{2}m_2\left[I_1\,^2\phi_1\,^2+I_2\,^2\phi_2\,^2+2I_1I_2\cos{(\phi_1-\phi_2)\phi_1\phi_2} \right]\end{aligned}$$
Which leads us to the beautiful and not at all way too long: 
$$\mathcal{L}=\frac{1}{2}(m_1+m_2)I_1\,^2\phi_1\,^2+\frac{1}{2}m_2I_2\,^2\phi_2\,^2+m_2I_1I_2\phi_1\phi_2\cos(\phi_1-\phi_2)$$$$+(m_1+m_2)gI_1\cos\phi_1+m2gI_2\cos\phi_2.$$
(No promises I typed that exactly correct).

---
