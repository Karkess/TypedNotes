---
title: Chapter 33 - Tensors

---

# Chapter 33 - Tensors
## 33.1 Definition of a Tensor: Valence

A fully general tensor is a multilinear function of vectors and 1-forms, and the *valence* tells us how many of each are present. 

*A **tensor $H$ of valence** $\begin{bmatrix}f\\v\end{bmatrix}$ at a point $p$ is a multilinear, real-valued function of $f$ 1-forms and $v$ vectors, such that the value of $H$ at $p$ depends only on the values of 1-forms and vectors at $p$.*

Thus a 1-form is a tensor of valence $\begin{bmatrix}0\\1\end{bmatrix}$ is a 1-form because it accepts a single vector to generate an output.

Likewise, a vector is a tensor of valence $\begin{bmatrix}1\\0\end{bmatrix}$ because it accepts a single 1-form to generate an output. 

---
In the general case we may divide the 'input' slots of $H$ into two groups: $$H(\varphi_1,\dots,\varphi_f||v_1,\dots,v_b).$$ For the general case, the order of input matters.

---
Let's re-examine the Riemann tensor $R$ from this definition.

Previously this was defined as a *vector*-valued multilinear function of three vector inputs: $\vec{w}$ is the vector that is parallel-transported around the parallelogram with edges defined by $\vec{u}$ and $\vec{w}$, and the output is the vector holonomy $\delta\vec{w}$: 
$$\delta\vec{w}=R(u,v;w)=\left([\vec{\nabla}_\vec{u},\vec{\nabla}_\vec{v}]-\vec{\nabla}_{[\vec{u},\vec{v}]}\right)\vec{w}.$$
To make this a real tensor, it must output a number, which means we must *contract* $\delta\vec{w}$ iwth a one form, meaning that the standard definition of the Riemann tensor is a tensor of valence $\begin{bmatrix}1\\3\end{bmatrix}$:$$R(\varphi||\vec{u},\vec{v},\vec{w})\equiv\langle\varphi,\delta\vec{w}\rangle=\varphi(\delta\vec{w}).$$

## 33.2 Example: Linear Algebra

Tensors contain much of the subject of linear algebra, consider $L(\dots||\vec{v})$ (were the 1-form slot is empty to yield a vector). $$\begin{aligned}L(k_1v_1+k_2v_2)&=L(\dots||k_1v_1+k_2v_2)\\&=k_1L(\dots||v_1)+k_2L(\dots||v_2)\\&=k_1L(v_1)+k_2L(v_2).\end{aligned}$$ Therefore, $L$ is a *linear transformation*. This sends vectors to vectors, and we can do the same with 1-forms.

## 33.3 New Tensors from Old
**Addition**
We cannot meaningfully add two tensors with different valences, but for tensors with the same valence (here for example, $\begin{bmatrix}2\\1\end{bmatrix}$):$$(H+J)(\varphi,\psi||v)\equiv H(\varphi,\psi||v)+J(\varphi,\psi||v).$$

---
**Multiplication: The Tensor Product**
Given two 1-forms, $\varphi$ and $\psi$, each of which acts on a single vector, it is natural to efine the *tensor product*, acting on *two* vectors, and therefore of valence $\begin{bmatrix}0\\2\end{bmatrix}$, as follows: 
$$ (\varphi\otimes\psi)(\vec{v},\vec{w})\equiv\varphi(\vec{v})\psi(\vec{w}).$$
*Note, order matters: $\varphi\otimes\psi\neq\psi\otimes\varphi.$*

**Terminology:** The tensor product is commonly called the *direct product* or the *outer product*. 

Note, under tensor multiplication, valences add like vectors: $$\begin{bmatrix}1\\3\end{bmatrix}+\begin{bmatrix}2\\2\end{bmatrix}=\begin{bmatrix}3\\5\end{bmatrix}.$$

As multiplication by a scalar does not change the valence, the valence of a scalar must be taken to be $\begin{bmatrix}0\\0\end{bmatrix}$.

## 33.4 Components
First, let $$T=T_{ij}(dx^i\otimes dx^j)$$ So we see that *the set of tensors $\{dx^i\otimes dx^j\}$ forms a **basis** for tensors of valence $\begin{bmatrix}0\\2\end{bmatrix}$.*

Likewise, a general tensor of $K(\varphi,\psi)$ of valence $\begin{bmatrix}2\\0\end{bmatrix}$ can be decomposed into basis tensors as: $$K=K^{ij}(e_i\otimes e_j).$$

## 33.5 Relation of the Metric Tensor to the Classical Line Element
The modern metric tensor is related to the classical, infinitesimal-based, line element $ds$ of Gauss. 

Gauss considered infinitesimal changes $du$ and $dv$ in the coordinates of a point on the surface, resulting in an infinitesimal line element $ds$ within the surface, then in Gauss's notation: $$ds^2=E\,du^2+2F\,du\,dv+G\,dv^2$$
Now, let $$x^1=,\quad x^2=v$$ and $$g_{11}=E, g_{12}=F, g_{22}=G$$ Then, the metric tensor can be expressed as: $$g=g_{ij}(dx^i\otimes dx^j)=E(du\otimes du)+F(du\otimes dv)+G(dv\otimes dv).$$

## 33.6 Example: Linear Algebra (Again)

Take our tensor $L(\varphi||v)$ to have components $$L^i\,_j=L(\vec{d}x^i||\hat{e}_j)$$
We can represent vector basis by column vectors: $$(\hat{e}_1,\hat{e}_2)=\left(\begin{bmatrix}1\\0\end{bmatrix},\begin{bmatrix}0\\1\end{bmatrix}\right)$$ and the dual 1-form basis as row vectors: $$(dx^1,dx^2)=\left(\begin{bmatrix}1&0\end{bmatrix},\begin{bmatrix}0&1\end{bmatrix}\right)$$ Thus, $$dx^1(\vec{v})=\begin{bmatrix}1&0\end{bmatrix}\begin{bmatrix}v^1\\v^2\end{bmatrix}=v^1.$$

In two dimensions, it follows that $L$ is represented by a familiar 2x2 matrix: $$L=L^i\,j\hat{e}_i\otimes\vec{d}x^j=\begin{bmatrix}L^1\,_1&L^1\,_2\\L^2\,_1&L^2\,_2\end{bmatrix}$$

And as a linear transformation: $$\begin{bmatrix}v^1\\v^2\end{bmatrix}\rightarrow\begin{bmatrix}L^1\,_1&L^1\,_2\\L^2\,_1&L^2\,_2\end{bmatrix}\begin{bmatrix}v^1\\v^2\end{bmatrix}=\begin{bmatrix}L^1\,_1v^1+L^1\,_2v^2\\L^2\,_1v^1+L^2\,_2v^2\end{bmatrix}=\begin{bmatrix}L^1\,_jv^j\\L^2_{\;j}\,v^j\end{bmatrix}.$$

Okay I understand how to write the subscripts now: $L^i_{\;j}$, not $L^i\,_j$. 

## 33.7 Contraction
Consider the contraction of a 1-form and a vector from the point of view of components: $$\varphi(\vec{v})=(\varphi_idx^i)(v^j\hat{e}_j)=(\varphi_iv^j)dx^i(\hat{e}_j)=(\varphi_iv^j)\delta^i_j=\varphi_jv^j$$

The contraction is a *geometrical* operation, and the answer is independent of the specific components of $\varphi$ and $\psi$. 

We now define the *Contraction* of the tensor with components $L^i_{\;j}$ to be $$L^j_{\;j}=L(\vec{x}^j||\hat{e}_j)=L^1_{\;1}+L^2_{\;2}=\mathrm{Tr}\begin{bmatrix}L^1_{\;1}&L^1_{\;2}\\L^2_{\;1}&L^2_{\;2}\end{bmatrix}.$$

The idea of contraction can be applied to any tensor whose inputs include at least 1-form and at least one vector: We sum over one upper index and one lower index.
A natural example of a contraction is the Riemann tensor yielding the Ricci tensor: $$R_{mij}^{\;\;\;\;m}=R_{ij}$$

Suppose we form $A\otimes B$, with valences $A=\begin{bmatrix}2\\0\end{bmatrix}$ and $B=\begin{bmatrix}0\\2\end{bmatrix}$: $$A^{ij}B_{jk}\equiv C^i_{\;k}.$$

## 33.8 Changing Valence with the Metric Tensor
We already know that the metric tensor $g$ of valence $\begin{bmatrix}0\\2\end{bmatrix}$ is *the* fundamental structure of a manifold. It gives us the geodesics, parallel transport, and the curvature. However, $g$ plays another role, *it allows us to change the valence of a tensor*. 

For example, if we take $$\text{vector }n\rightarrow\text{1-form }\nu,\quad\text{ where }\nu(\vec{w})\equiv g(\vec{w},\vec{n}).$$
we can relate the components of the 1-form $\nu$ to the original vector $n$ by taking $\nu=n_idx^i$ and thus $$n_i=g_{ij}n^j.$$

For example, if $n=n^j\,\hat{e}_j$ is a vector in Minkowski spacetime, with metric $$ds^2=dt^2-(dx^2+dy^2+dz^2)=[dx^0]^{^2}-\left([dx^1]^{^2}+[dx^2]^{^2}+[dx^3]^{^2}\right),$$ the corresponding 1-form is $$\vec{\nu}=n_idx^i=n^0dt-n^1dx-n^2dy-n^3dz.$$

We can take $$R_{ijkl}=R_{ijk}^{\;\;\;m}g_{ml}$$ which we naturally call index lowering, and in the reverse direction would be index raising. 

For this we use a tensor analogous to the metric tensor, $\tilde{g}$, which has valence $\begin{bmatrix}2\\0\end{bmatrix}$. 

Naturally, these are related as such $$\tilde{g}^{ik}g_{kj}=\delta^i_j.$$

## 33.9 Symmetry and Antisymmetry
Recall even and odd functions, which here we shall call symmetric and antisymmetric functions. If an arbitrary function is capable of being split into a sum of symmetric and antisymmetric functions: $$f(x)=f^+(x)+f^-(x),$$ then by definition $$f(-x)=f^+(x)-f^-(x),$$ and if a split is possible then it is explicitly defined by $$f^+(x)=\left[\frac{f(x)+f(-x)}{2}\right]\quad\text{and}\quad f^-(x)=\left[\frac{f(x)-f(-x)}{2}\right].$$

For example, if we take $f(x)=e^x$ then this split naturally leads to the hyperbolic functions. The symmetric part of $e^x$ is $f^+(x)=\cosh(x)$ and the antisymmetric part is $f^-(x)=\sinh(x)$.

It turns out we can do an analogous operation on tensors of valence $\begin{bmatrix}0\\2\end{bmatrix}$ obtaining (where round brackets denote symmetrization and square brackets denote antisymmetrization): $$E_{(ij)}\equiv E^+_{ij}=\frac{1}{2}[E_{ij}+E_{ji}]\quad\text{and}\quad E_{[ij]}\equiv E^-_{ij}=\frac{1}{2}[E_{ij}-E_{ji}]$$ thus $$E_{ij}=E_{(ij)}+E_{[ij]}.$$
