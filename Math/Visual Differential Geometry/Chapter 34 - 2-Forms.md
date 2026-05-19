# Chapter 34 - 2-Forms
## Personal Notes
Before working through the text book this time I worked a lot of practice examples and discussed with ChatGPT and had it make a summary of the key points of our conversation, this is where it landed: 

### 2-Forms, Tensors, and Geometric Intuition (Supplement)

---

**Core Idea: $(0,2)$ Tensors**

A tensor of valence $\begin{bmatrix}0\\2\end{bmatrix}$ is a multilinear map that takes two vectors and returns a scalar:
$$
T(u,v).
$$

Interpretation:
> A rule assigning a scalar to how two directions interact.

---

**Symmetric vs Antisymmetric**

**Symmetric Case**
$$
T(u,v) = T(v,u)
$$

- Measures: alignment, length, energy-like quantities  
- Defines a quadratic form:
$$
T(u,u)
$$

Interpretation:
> Measures how a direction interacts with itself (magnitude-like)

---

**Antisymmetric Case (2-Forms)**
$$
\omega(u,v) = -\omega(v,u)
$$

- Measures: oriented area  
- Properties:
$$
\omega(u,u)=0
$$

Interpretation:
> Measures the oriented area spanned by two directions

---

**Wedge Product**

For 1-forms $dx, dy$:
$$(dx \wedge dy)(u,v)=dx(u)\,dy(v) - dx(v)\,dy(u)$$

In coordinates:
$$
(dx \wedge dy)(u,v) = u_x v_y - v_x u_y
$$

Interpretation:
> Oriented area of the projection onto the $xy$-plane

---

**General 2-Forms in $\mathbb{R}^3$**

A general 2-form:
$$
\omega =
A\,dx \wedge dy
+
B\,dy \wedge dz
+
C\,dz \wedge dx
$$

Interpretation:
- Each term measures area in a coordinate plane  
- Total = weighted sum of projected areas  

---

**Vector Field $\rightarrow$ 2-Form (Flux Construction)**

Given a vector field:
$$
\vec{w} = (w_x, w_y, w_z),
$$

associate the 2-form:
$$
\omega =
w_x\,dy \wedge dz
+
w_y\,dz \wedge dx
+
w_z\,dx \wedge dy.
$$

Interpretation:
> Converts flow direction into flux through surfaces

---

**Example: Flow Through a Surface**

Let:
$$
\vec{w} = (0,0,z)
$$

Then:
$$
\omega = z\,dx \wedge dy.
$$

Evaluate on surface directions:
$$
u = (1,0,0), \quad v = (0,1,0)
$$

$$
\omega(u,v) = z.
$$

Interpretation:
- $dx \wedge dy$: surface (window)  
- $z$: flow through that surface  

---

**Component Representation**

The 2-form
$$
\omega = z\,dx \wedge dy
$$

corresponds to:
$$
(W_{\mu\nu}) =
\begin{pmatrix}
0 & z & 0 \\
-z & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}
$$

---

**Evaluation (Contraction)**

Given vectors $X,Y$:
$$
\omega(X,Y) = W_{\mu\nu} X^\mu Y^\nu.
$$

Interpretation:
> Plug vectors into the tensor to obtain a scalar

---

**Key Distinction**

| Object | Measures | Inputs |
|------|--------|--------|
| Symmetric tensor | length / alignment | 1 or 2 directions |
| 2-form | oriented area / flux | 2 directions |

---

**Recognition Rules**

Use a 2-form when:
- depends on a surface  
- depends on orientation  
- requires two independent directions  

Use a symmetric tensor when:
- depends on magnitude / energy  
- uses the same direction twice  

---

**Final Mental Models**

Metric:
$$
g(u,u)
$$
> “How large is this direction?”

2-form:
$$
\omega(u,v)
$$
> “How much passes through the area spanned by these directions?”

---

**Summary**

- Wedge product $\rightarrow$ oriented area  
- 2-form $\rightarrow$ weighted area / flux  
- Contraction $\rightarrow$ evaluation of tensor on vectors  
- Vector field $\rightarrow$ 2-form via flux construction  

---
## 34.1 Definition of a 2-Form and of a $p$-form
We defined several vitally important tensors of valence $\valence{0}{2}$ that are *symmetric*, the metric tensor, the Ricci tensor, the energy-momentum tensor, and the Einstein tensor. Now we focus on antisymmetry.

Starting with a general definition of a p-form: 
*A **$p$-form**, also called a differential form of **degree** $p$, is a **completely antisymmetric** tensor of valence $\valence{0}{p}$, meaning that swapping any two of the vector inputs swaps its sign*. 

Naturally, if $p=2$, we have a 2-form. Higher values of $p$ aren't too common, but arise in some important applications of Forms, such as ***Symplectic Manifolds*** that naturally arise in Hamiltonian mechanics.

---
## 34.2 Example: The Area 2-Form
In $\R^2$ let us define: $$\cal{A}(\vec{u},\vec{v})=\text{oriented area of a parallelogram with edges }\v{u}\text{ and }\v{v}$$ This $\cal{A}$ is a $2$-Form! 

Note that for an arbitrary 2-Form: $$\Psi(\v{u},\v{u})=0.$$

And by antisymmetry of course $\Psi(\v{y},\v{x})=-\Psi(\v{x},\v{y})$. 

---
## 34.3 The Wedge Product of Two 1-forms
Recall that any tensor of valence $\valence{0}{2}$ can be split into a sum of a symmetric tensor and antisymmetric tensor. If we apply this procedure to the tensor product of two arbitrary one forms we find that $$\phi\otimes\psi=\frac{1}{2}\left[\phi\otimes\psi+\psi\otimes\phi\right]+\frac{1}{2}\left[\phi\otimes\psi-\psi\otimes\phi\right].$$ 
The antisymmetric part of this is a 2-form two form obtained by multiplying two one forms,. This gives us a new kind of multiplication called the wedge product: $$\phi\wedge\psi\equiv\phi\otimes\psi-\psi\otimes\phi\tag{34.3}.$$

Swapping the input order of the two form reverses the sign $$\phi\wedge\psi=-\psi\wedge\phi$$

Which as is true for antisymmetry we have $$\psi\gp\psi=0.$$

We call this wedge product, the antisymmetric 2-Form, the *area 2-form* $$\cal{A}=\ext x\gp\ext y\tag{34.4}$$

The proof of 34.4 is done by components showing that this is equivalent to the determinant wedge product, so I'll show it. $$\begin{aligned}(\ext x\gp\ext y)(\v{u},\v{v})&=(\ext x\tens\ext y-\ext y\tens\ext x)(\bmat{u^1\\u^2},\bmat{v^1\\v^2})\\&=u^1v^2-u^2v^1\\&=\det\bmat{u^1&v^1\\u^2&v^2}\\&=\cal{A}(\v{u},\v{v})\end{aligned}$$

Now we come to the crucial idea: *Let us use numbers $\varphi(\v{v})$ and $\psi(\v{v})$ as the $x$ and $y$ coordinates of a point in $\R^2$*. The two 1-forms define a mapping $\cal{F}$ of vectors in $\R^3$ (or any $\R^n$) to vectors in $\R^2$: 
$$\vec{v}\rightarrow\cal{F}(\v{v})\equiv\bmat{\varphi(\v{v})\\\psi(\v{v})}.$$

Which leads to the *meaning* of the wedge product, as the edges are mapped to a parallelogram in $\R^2$ with edges $\cal{F}(\v{v}_1)$ and $\cal{F}(\v{v}_2)$: 

*When the wedge product $(\varphi\gp\psi)$ is applied to an arbitrary parallelogram in $\R^n$, it outputs the oriented area of the image parellelogram in $\R^2$ under the mapping $\cal{F}$*:
$$(\varphi\gp\psi)(\v{v}_1,\v{v}_2)=\cal{A}[\cal{F}(\v{v}_1),\cal{F}(\v{v}_2)].\tag{34.6}$$

---
## 34.4 The Area 2-Form in Polar Coordinates
When we do a double integral in $\R^2$, we write the element of area as $d\cal{A}=dx\,dy$, and we have previously explained how this is connected to the area 2-form: $\cal{A}=\ext x\gp\ext y$, but when we switch to polar coordinates we instead write the element of area as $r\,dr\,d\theta$, in this case, there is a simple geometric derivation of this formula. The corresponding 2-form is $$r\,\ext r\gp\ext\theta.$$

We can derive this from 2-forms as 
$$\begin{aligned}\ext x\gp\ext y&=\ext(r\cos\theta)\gp\ext(r\sin\theta)\\&=[(\ext r)\cos\theta)-r\sin{\theta}\,\ext\theta]\gp[(\ext r)\sin\theta+r\cos\theta\,\ext\theta]\\&=\cos^2\theta\,r\,\ext r\gp\ext\theta-\sin^2\theta\,r\,\ext\theta\gp\ext r\\&=r\,\ext r\gp\ext\theta.\end{aligned}$$

---
## 34.5 Basis 2-Forms and Projections
Recall that the set of tensors $\{\ext x^i\gp\ext x^j\}$ forms a basis for tensors of valence $\valence{0}{2}$. This applies to *all* such tensors, including the 2-forms, but in the case of 2-forms we go a step further and say 
$$\text{The set of 2-forms }\{\ext x^i\gp\ext x^j\}\text{, with }i<j\text{ is a basis for the 2-forms.}\tag{34.7}$$
and
$$\text{In }\R^n\text{, the set of 2-forms is a vector space of dimension }\frac{1}{2}n(n-1)\tag{34.8}.$$

Because $\bf{\Psi}$ is a 2-form, we have 
$$\bf{\Psi}=\Psi_{12}(\ext x\gp\ext y)=\Psi_{12}\,\cal{A}.$$

If we go up one dimension to $\R^3$ we have
$$\bf{\Psi}=\Psi_{23}(\ext y\gp\ext z)+\Psi_{31}(\ext z\gp\ext x)+\Psi_{12}(\ext x\gp\ext y)\tag{34.9}$$

**Important Note:** 
*If $(\ext x\gp \ext y)$ is applied to a parallelogram $\cal{P}$ in $\R^3$, the output is the oriented area $\cal{A}_z$ of the orthogonal projection (in the z-direction) of $\cal{P}$ onto the $(x,y)-$plane.*

---
## 34.6 Association 2-Forms with Vectors in $\R^3$: Flux
It is possible to do calculus with forms in any number of dimensions, but the vector calculus we learn as undergrads is only possible in three dimensions. 

Geometrically, 2-forms and vectors are distinctly different. Algebraically, the distinction is clear as well. In $n$ dimensions a vector as $n$ components, whereas a 2-form as $\frac{1}{2}n(n-1)$ components. However, in three dimensions, they have the same number of components! 

Historically, the physicists of the 1880s had no idea that under the hood were powerful 2-forms that made their tools so robust, but we can now see this as a sort of numerical coincidence! We actually had 2-forms masquerading as vectors! 

To begin to analyze this further, we will rewrite the components (34.9) of the general 2-form $\Psi$ with a single raised index, and immediately identity these with components of a corresponding *vector*, which we shall denote by the same symbol as the 2-form, but underlined: $\ul\Psi$, id est, $$\Psi=\Psi^1(\ext x^2\gp\ext x^3)+\Psi^2(\ext x^3\gp\ext x^1)+\Psi^3(\ext x^1\gp\ext x^2)\leftrightarrows\ul\Psi\bmat{\Psi^1\\\Psi^2\\\Psi^3}.\tag{34.10}$$

The most natural mathematical way to understand this correspondence is via the **Hodge star duality operator ($\hodge$)**, which is a purely mathematical operation that maps a $p$-form to an ($n-p$)-form (in $n$ dimensions.)

The compelling reason to associate a 2-form with a vector this way is to introduce the physicist's powerful concept of *flux*. 

Imagine a uniform flow of fluid through space with velocity $\ul\Psi$. Now, define $$\Phi(\v{v}_1,\v{v}_2)\equiv\text{ Amount of fluid crossing }\cal{P}\text{ per unit time}=\text{flux of }\ul\Psi\text{ through }\cal{P}.\tag{34.11}$$

We count the flux as *positive* if the orientation of $\cal{P}$ is *counterclockwise* around $\ul\Psi$. 

Now we ask: *How is this flux 2-form $\Phi$ related to the 2-form $\Psi$ associated with the flow velocity $\ul\Psi\,$*? $$\begin{aligned}\Phi(\v{v}_1,\v{v}_2)&=\Psi^1\cal{A}_1+\Psi^2\cal{A}_2+\Psi^3\cal{A}_3\\&=\Psi(\v{v}_1,\v{v}_2)\end{aligned}$$ Thus $\Phi=\Psi!$

Concluding: 
*If fluid flows through 3-dimensional space with velocity $\ul\Psi$, its flux 2-form is $\Psi$, and vice-versa.*

---
## 34.7 Relation of the Vector and Wedge products in $\R^3$. 
To relate Vector Calculus to Forms we take a second consideration; we associate 1-forms with vectors. We do this similarly to 2-forms. Given a 1-form $\varphi$, we denote the corresponding vector with the same symbol but underlined:
$$\varphi=\varphi_1\ext x^1+\varphi_2\ext x^2+\varphi_3\ext ^3\,\rightleftarrows\,\ul\varphi=\bmat{\varphi_1\\\varphi_2\\\varphi_3}.$$

The two fundamental kinds of multiplication in Vector Calculus are the *scalar product* and the *vector product*. 
The scalar product readily generalizes to any number of dimensions and is expressed as: 
$$\varphi(v)=\ul\varphi\cdot\v{v}$$

The *vector product* however, is specific to three dimensions. Given two vectors $\ul{\v{\varphi}}$ and $\ul{\v{\sigma}}$, with the angle from the first to the second being \theta, recall that we define the *vector product* to be orthogonal to both, and its direction given by the right hand rule, and it's length given by the area of the parallelogram they span: 
$$|\ul{\vec{\varphi}}\times\ul{\v{\sigma}}\equiv\cal{A}(\ul{\v{\varphi}},\ul{\v{\sigma}})=\norm{\ul{\v{\varphi}}}\norm{\ul{\v{\sigma}}}\sin\theta.$$

It's strange that the length of a vector is equal to an area, the reality is that the vector product is actually the wedge product of the corresponding one forms, as shown by previous explanation of ***Hodge Duality***: 
$$\ul{\v{\varphi}}\times\ul{\v{\sigma}}\quad\leftrightarrows\quad\varphi\gp\sigma.\tag{34.16}$$

Note that 3 dimensions is the *only* case where a 2-form can be identified as the flux 2 form of a vector flow. 

We have a standard formula for the volume of a  parallelpiped with edges $\v{u},\v{v}$ and $\v{\Omega}$: 
$$\begin{aligned}\text{Volume=flux=}\Omega(\vec{u},\vec{v})&=\bmat{\Omega^1\\\Omega^2\\\Omega^2}\cdot\bmat{u^2v^3-u^3v^2\\u^3v^1-u^1v^3\\u^1v^2-u^2v^1}\\&=\det\bmat{\Omega^1&u^1&v^1\\\Omega^2&u^2&v^2\\\Omega^3&u^3&v^3}\end{aligned}\tag{34.17}$$

---
## 34.8 The Faraday and Maxwell Electromagnetic 2-Forms
For this section we take the Minkowski metric to be 
$$ds^2=-dt^2+dx^2+dy^2+dz^2$$

There are several 2-forms in 4-dimensional spacetime that play fundamental roles in the laws of physics. 

The laws of electromagnetism were first discovered empirically in a long, symphonic sequence of utterly ingenious experiments conducted by self-educated Michael Faraday in the basement laboratory within the Royal Institution of London

By 1873 Maxwell had his twenty equations until in 1885 Oliver Heaviside reduced them to the four that we now know as Maxwell's Equations. 

These insights eventually lead to Einstein's discovery of special relativity, in a paper he titled "On the Electrodynamics of Moving Bodies". 

The classical description of these fields is as two 3-dimensional vector fields, with six components in all, each one being a function of space and of time:
$$\text{Electric Field}=\ul{\Efield}=\bmat{\cal{E}_x\\\cal{E}_y\\\cal{E}_z}\quad\text{and}\quad\text{Magnetic Field}=\ul{\Bfield}=\bmat{\cal{B}_x\\\cal{B}_y\\\cal{B}_z}$$

Each of these may be associated with a flux 2-form and with a 1 form: 
$$\Efield=\cal{E}_x(\ext y\gp\ext z)+\cal{E}_y(\ext z\gp\ext x)+\cal{E}_z(\ext x\gp\ext y)$$
and
$$\epsilon=\cal{E}_x\ext x+\cal{E}_y\ext y+\cal{E}_z\ext z.$$

And similarly for the magnetic fields. 

Einstein explained that *none* of these 2-forms and 1-forms has an absolute observer-independent existence. 

Very remarkably (and beautifully), *Nature informs us that the electric and magnetic 2-forms and 1-forms combine into a single electromagnetic 2-form that does have absolute meaning in spacetime*
It is called the **Faraday 2-form**, and is denoted $\cal{F}$:
$$\cal{F}=\text{Faraday}=\epsilon\wedge\ext t+\Bfield$$

---
Personal aside:
So we have a two-form here of $\epsilon\gp\ext t$, and so this is like one one-form is spatial and one is time, so this correlates to a world sheet. A particle moving through this is a force along a worldline, the geometry is a spacetime parallelogram. $\Bfield$ is the magnetic flux, I think is how all this works.

The intuition behind this: Say we want to measure the electric field, what do we typically do? We measure the acceleration of an electric particle, so it requires a spatial component and a time component, so imagine we accelerate a charge in a wire, a one dimensional motion mixed with time, so $\epsilon$ and $t$. The amount moved through time can be measured with $\ext t$. The relationship between these two is antisymmetric, if we swap the direction of movement we have an opposite charge, so antisymmetric combination of two one forms: $\epsilon\wedge\ext t$. The magnetic field is $\Bfield$ and measured by flux through a hoop, so just the flux of this is a two form and defined by a purely spatial two form. Again, we have opposite charge if we have direction change, so it's antisymmetric, so again this is a two-form confirmed. We know they contribute to one object of the electromagnetic field so we sum them, and we get the Faraday 2-form $\cal{F}$. 

---
Continuing Needham: 
If we insert a vector $\v{u}$ into the second slot of $\cal{F}$  we obtain $\cal{F}(\dots,\v{u})$, this is a one-form. 

Suppose we place a charge $q$ in the electromagnetic field described by $\cal{F}$ Let the particle's 4-velocity vector in spacetime be $\v{u}$, let its 4-momentum be described by the 1-form $\pi$, and let it's proper time be $\tau$. Then, $q\cal{F}(\dots,\v{u})$ *describes the electromagnetic force exerted on the particle: 
$$\frac{d\pi}{d\tau}=q\cal{F}(\dots,\v{u}).\tag{34.32}$$
This is a 1-form, awaiting the insertion of a vector, and the resulting number is the magnitude of the force acting in the direction of the inserted vector. 

Contrast this with the more complicated formula - the **Lorentz Force Law** - That one learns in introductory electrodynamics for the rate of change of the spatial vector momentum $\v{p}$  of a particle that has a spatial vector velocity $\v{v}$: $$\frac{d\v{p}}{dt}=q(\ul{\Efield}+\v{v}\times\ul{\Bfield}).$$

In this classical formulation, *different observers in relative motion will all disagree about the values of $\v{p},\ul{\Efield},\v{v},$ and $\ul{\Bfield}$! 

---
A quick reminder of Maxwell's equations:

Maxwell's Source-Free Equations:
$$\begin{aligned}\del\cdot\ul{\Bfield}&=0,\\\del\times\ul{\Efield}+\partial_t\ul{\Bfield}&=0.\end{aligned}\tag{34.24}$$

Maxwell's Source Equations: 
$$\begin{aligned}\del\cdot\ul{\Efield}&=4\pi\rho,\\\del\times\ul{\Bfield}-\partial_t\ul{\Efield}&=4\pi\ul{j}.\end{aligned}\tag{34.25}$$

---
This brings us to the Maxwell 2-form, closely related to $\cal{F}$ and denoted $\hodge\cal{F}$, which is *almost* (but not quite) the result of interchanging the roles of the electric and magnetic fields in the Faraday 2-form: 
$$\hodge\cal{F}=\text{Maxwell}=\beta\gp\ext t-\cal{E}.$$

The star operator ($\hodge$) is the Hodge Duality Operator. It maps a $p$-form to an $(n-p)$-form. Since we are in 4 dimensions, the operator maps a 2-form to another 2-form. Taking the dual of Maxwell, we recover Faraday (with a minus): $$\hodge\hodge\cal{F}=-\cal{F}$$ Somewhat beautiful that these two exist to be duals of each other. 