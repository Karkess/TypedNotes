---
title: Chapter 2 - Sequences and Series

---

# Chapter 2 - Sequences and Series
## 2.1 Discussion: Rearrangements of Infinite Series
Consider the infinite series $$\sum^\infty_{n=1}\frac{(-1)^{n+1}}{n}=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}+\cdots$$

We can begin by computing 'partial sums', or sums up to some $n$ to see where the successive values are and the odd ones decrease while the even ones increase seeing to reach a singular point. 

We will prove that they do zone in on a point around $S\approx0.69$. 

It is shown by a simple example that addition in an infinite sum is not commutative, which makes me feel better about the Ramanujan sum. 

This also shows a rearrangement of infinite sums around matrix components and show that double sums yield different answers when swapped in position. 

## 2.2 - The Limit of a Sequence
**Definition 2.2.1.** A *sequence* is a function whose domain is $\mathbb{N}$. 

**Definition 2.2.3 (Convergence of a Sequence).** A sequence $(a_n)$ *converges* to a real number *a* if, for every positive number $\epsilon$, there exists an $N\in\mathbb{N}$ such that whenever $n\ge N$ it follows that $|a_n-a|<\epsilon$. 

**Definition 2.2.4.** Given a real number $a\in\mathbb{R}$ and a positive number $\epsilon>0$, the set $$V_\epsilon(a)=\{x\in\mathbb{R}:|x-a|<\epsilon\}$$ is called the $\epsilon$-*neighborhood of* $a$. 

**Definition 2.2.3B (Convergence of a Sequence: Topological Version)** A sequence $(a_n)$ converges to $a$ if, given any $\epsilon$-neighborhood $V_\epsilon(a)$ of $a$, there exists a point in the sequence after which all of the terms are in $V_\epsilon(a)$. In other words, every $\epsilon$-neighborhood contains all but a finite number of points.

I agree this definition is much simpler and easier to follow. Essentially it's saying, is that if the rest of the sequence is in a finite distance from the current point, then the sequence converges. To me this sounds like saying "The sequence converges if it converges", but mathematicians love definitions like these.

**Example 2.2.5.** Consider the sequence $(a_n)$ where $a_n=\frac{1}{\sqrt{n}}$, we claim that $$\lim(\frac{1}{\sqrt{n}})=0.$$

*Proof*. Let $\epsilon>0$ be an arbitrary positive number. Choose a natural number $N$ satisfying $$N>\frac{1}{\epsilon^2}.$$ Let $n\ge N$, then $$n>\frac{1}{\epsilon^2}\text{ implies }\frac{1}{\sqrt{n}}<\epsilon\text{, and hence }|a_n-0|<\epsilon.\quad\blacksquare$$

---
### Quantifiers
The definition of convergence contains the use of several quantifiers, and it is instructive to see a basic outline of how proofs of convergence are done.
$$\text{Template for a proof that }(x_n)\rightarrow x:$$
- "Let $\epsilon>0$ be arbitrary"
- Demonstrate a choice for $N\in\mathbb{N}$. This step usually requires the most work, almost all of which is done prior to actually writing the formal proof.
- Now, show that $N$ actually works.
- "Assume $n\ge N$."
- With $N$ well chosen, it should be possible to derive the inequality $|x_n-x|<\epsilon$. 


**Theorem 2.2.7 (Uniqueness of Limits).** *The limit of a sequence when it exists, must be unique.*

---
### Divergence
**Definition 2.2.9.** A sequence that does not converge is said to *diverge*.

## 2.3 The Algebraic and Order Limit Theorems
**Definition 2.3.1.** A sequence $(x_n)$ is *bounded* if there exists a number $M>0$ such that $|x_n|\le M$ for all $n\in\mathbb{N}$. 

**Theorem 2.3.2.** *Every convergent sequence is bounded*.

**Theorem 2.3.3 (Algebraic Limit Theorem).** *Let $\lim{a_n}=a$, and $\lim{b_n}=b$, then,*
1. $\lim(ca_n)=ca\;\;\forall\;\;c\in\mathbb{R};$
2. $\lim(a_n+b_n)=a+b;$
3. $\lim(a_nb_n)=ab
4. $\lim(a_n/b_n)=a/b$, *provided* $b\neq0$. 

---
### Limits and Order