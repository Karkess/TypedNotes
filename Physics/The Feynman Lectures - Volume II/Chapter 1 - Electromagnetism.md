---
title: Chapter 1 - Electromagnetism

---

# Chapter 1 - Electromagnetism
## 1-1 Electrical Forces

The electrical force is one with positive and negative matter that has a strength that is about a *billion-billion-billion-billion* times stronger than gravity.
This force much like gravity varies predominantly by the inverse of the square of the distance.

If you were to stand at arms length with another person and each of you had *one percent* more electrons than protons, the repulsive force between you two would be so much that it could lift the "weight" of the entire Earth!

This raises the question of how the nucleus with its positive charges stays together, or how the electron doesn't crash into the nucleus, with their opposite charges. 
- The electron is held at a distance by considerations in quantum mechanics, such as the uncertainty principle with the momentum of the 'particle', among other considerations.
- The nucleus is held together by even stronger non-electrical nuclear forces, here, the aptly named 'Strong Force'. 
    - However, the strong nuclear force decays much faster than the electrical force, and in sufficiently large nuclei, such as uranium, the nuclear force helps nearest neighbors stay together, but electrical forces dominant to where clusters of protons are held together weakly, and thus decay can be induced by a slight introduction of energy, such as a slow neutron. 

The relationship of the force between charges is called *Coulomb's Law*. 

The electrical force is unified with the magnetic force as a single entity, which is why we refer to the subject as "Electromagnetism". 

---

We write the force $F$ on a charge $q$ moving with a velocity $v$ as $$F=q(E+v\times B).$$ Here, $E$ is the *electric field*, and B the *magnetic field*. 

We can determine the motion of the particle if we know the force acting on it, so here we can combine our force equations to determine uniquely the motion of the particles:$$\frac{d}{dt}\left[\frac{mv}{\sqrt{1-v^2/c^2}}\right]=F=q(E+v\times B).$$

The *principle of superposition of fields* states that if two fields are interacting at a single place at a single time, the field produced is simply the sum of the two fields: $$E=E_1+E_2.$$

Due to the unwieldy nature of determining forces that change with time and accelerations and motion, it turns out to be easier to determine the properties of electromagnetism in another formulation, by fields.

## 1-2 Electric and Magnetic Fields

In our determination of fields we change our understanding of $E$ and $B$ to be separate from simply the vectors $\vec{E}$ and $\vec{B}$ acting on a charge at a point at a time, but instead generalize to what *would* be felt by a charged particle if there were one there, without consideration of the charged particle itself. To do so, we parameterize the fields as follows: $$E(x,y,z,t)\quad\text{and}\quad B(x,y,z,t).$$ This determination has an understanding that placing a charge there did not disturb anything responsible for the generation of those fields. 

A "field" in physics is any physical quantity that takes on a different value at each point in space. 

## 1-3 Characteristics of Vector Fields

One property of fields we are interested in is the flux, which we can think of has how much of something flows through a surface, defined roughly as $$\text{Flux}=\text{(average normal component)}\cdot\text{(surface area)}.$$

For our electric field, this is an *electric flux*. We can think of flux through a closed surface, bounded surface, or any arbitrary region of space. 

Another element of fields we might find interesting is circulation, which we can imagine as whether or not something flows in one direction if we imagine freezing all of it except in a closed loop of tube, defined roughly as: $$\text{Circulation}=\text{(average tangential component)}\cdot\text{(distance around)}.$$

## 1-4 The Laws of Electromagnetism

The first law of electromagnetism describes the flux of the electric field: $$\text{The flux of }E\text{ through any closed surface}=\frac{\text{the net charge inside}}{\epsilon_0},$$ where $\epsilon_0$ is a convenient constant. 

If we accept that the field from a single charge is spherically symmetric, we can see this is the same as Coulomb's law. As the average value of a normal component of the field is just $E$ at that point. Since the field must be directed radially and have the same value at all points on the sphere, related to its area growing outward. From here we see we have an inverse square field. 

For an arbitrary stationary curve in space if we measure the circulation of the field around the curve, it is in general not $0$ (although it is for a Coulomb field). Rather, the second law states that $$\text{Circulation of }E\text{ around }C=\frac{d}{dt}(\text{flux of }B\text{ through }S),$$for any not closed surface $S$. 

Two more corresponding equations for the magnetic field $B$ complete our laws of the electromagnetic field: $$\text{Flux of }B\text{ through any closed surface}=0.$$
For a surface $S$ bounded by the curve $C$, $$c^2(\text{circulation of }B\text{ around }C)=\frac{d}{dt}(\text{flux of }E\text{ through }S)+\frac{\text{flux of electric current through }S}{\epsilon_0}\:.$$ The $c^2$ here is the square of the velocity of light. It appears because magnetism is actually a relativistic effect of electricity. 

If currents going through a loop reproduce magnets, are stationary magnets similar to moving charges? It turns out, yes. This is from the 'spin' of the electron. Now that's a complicated subject. May Tomonaga save me. 

From our equations we can see that the production of an electric field produces as well a magnetic field, and we see in the same vein that moving a magnetic field generates an electric field. In this sense, they propagate each other, and that is how these forces travel throughout space, and allow us such things as the ability to see! 

## 1.5 - What are the fields?
This section treats fields more abstractly, and asserts that the abstract way as accepting equations is the most efficacious route. A very Feynman pragmatic assertion, but interested when you consider his contributions to QFT, although those too were a precipitation of pragmatism. The section poses a thought experiment that has caught me back before I had accepted that I don't know shit, and that's what the magnetic field looks like if you move at the speed of the charge, which is why we call it a relativistic effect. It ends by stating that electromagnetic theory was already a relativistic theory at its foundation, and thus didn't need a correction the same way mechanics did. It was already tuned to $v^2/c^2$ precision. 
