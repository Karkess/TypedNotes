# Chapter 35 - 3 Forms
---
## 35.1 - A 3-Form Requires Three Dimensions
---
Let us begin by recognizing that 3-forms require at least three dimensions in order to exist, consider a construction with 1-forms:
$$H=\varphi\tens\varphi\tens\varphi\rightarrow H(\v{v}_1,\v{v}_2,\v{v}_3)=\varphi(\v{v}_1)\varphi(\v{v}_2)\varphi(\v{v}_3).$$ This specific tensor is totally symmetric.

To create a 3-form, we require by definition that our tensor be *totally antisymmetric*, and this is impossible. Consider $\Xi$:
$$\Xi_{ijk}=\Xi(\hat{e}_i,\hat{e}_j,\hat{e}_k).$$
In $\R^2$ there are only two basis vectors, $\{\hat{e}_1,\hat{e}_2\}$, so that means that two slots would have the same vector and thus vanish entirely. Thus for us to have a $p$-form we must have at least $p$ dimensions.

---
## 35.2 - The Wedge Product of a 2-form and a 1-form

To do this, we have a cyclic permutation of the vectors: 
$$(\Psi\gp\sigma)(\v{v}_1,\v{v}_2,\v{v}_3)=\Psi(\v{v}_1,\v{v}_2)\sigma(\v{v}_3)+\Psi(\v{v}_3,\v{v}_1)\sigma(\v{v}_2)+\Psi(\v{v}_2,\v{v}_3)\sigma(\v{v}_1).$$

Although the wedge product is antisymmetric when it combines two 1-forms, it is symmetric when it combines a 2-form and a 1 form: 
$$\Psi\gp\sigma=\sigma\gp\Psi$$

Here is the general rule: 
*If $\Psi$ is a $p$-form and $\Omega$ is a $q$-form, then* 
$$\Psi\gp\Omega=(-1)^{pq}\,\Omega\wedge\Psi.$$

And of course
$$\Omega\gp\Omega=0.$$

---
## 35.3 The Volume 3-Form
Now let us take $\Psi=\ext x^1\gp\ext x^2$ and $\sigma=\ext x^3$, and define the *volume 3-form* to be 
$$\cal{V}\equiv(\ext x^1\gp\ext x^2)\gp\ext x^3.$$

This is the standard volume of a parallelepiped. The wedge products of 3 forms is associative, so they can be calculated in any order. (Not commutative).

---
## 35.4 The Volume 3-Form in Spherical Polar Coordinates
This is the same as before, we substitute in our coordinates, such as $x=r\sin\phi\cos\theta$, take the exterior derivative, and multiply them getting the same thing we'd expect: 
$$\ext x\gp\ext y\gp\ext z=r^2\sin\phi\;\ext r\gp\ext\phi\gp\ext\theta.$$

---
## 35.5 The Wedge Product of Three 1-Forms and of $p$ 1-Forms
