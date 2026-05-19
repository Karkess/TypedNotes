---
title: Chapter 1 - The Real Numbers

---

# Chapter 1 - The Real Numbers
## 1.1 - Discussion: The Irrationality of $\sqrt{2}$
A brief discussion of G.H. Hardy and *A Mathematician's Apology*. 

Unfortunately my very heavy-handed approach to mathematics would probably not be appreciated by him as art. I see it as a beautiful geometry, but I am far from eloquently discussing mathematics with proofs that are so beautiful as the irrationality of $\sqrt{2}$. 

**Theorem 1.1.1.** *There is no rational number whose square is $2.$*
This is the standard proof that if $p$ and $q$ are integers, then there is never a situation where $\left(\frac{p}{q}\right)^2=2.$ 

We define the *Natural Numbers* $$\mathbb{N}=\{1,2,3,4,5,\dots\}.$$Which we extend to *Integers* $$\mathbb{Z}=\{\dots,-2,-1,0,1,2,\dots\}.$$ And then the *Rational Numbers*$$\mathbb{Q}=\{\text{all fractions }\frac{p}{q}\text{ where }p\text{ and }q\text{ are integers with }q\neq0\}.$$
$\mathbb{Q}$ possesses qualities which make it a field, in contrast to $\mathbb{Z}$ and $\mathbb{N}$. However, the finite set $\{0,1,2,3,4\}$ with the modulo 5 do compose a field.

## 1.2 Some preliminaries
### Sets
A *set* is a collection of objects. 
Covers set builder notation, intersections, unions, empty set (uses $\emptyset$). 

### Functions
Talks about Dirichlet giving a definition of functions, essentially our classic $f:A\rightarrow B$. 

A fun function from Dirichlet: $$g(x)=\begin{cases}1\quad\text{if }x\in\mathbb{Q}\\0\quad\text{if }x\not\in\mathbb{Q}.\end{cases}$$

A quick overview of the triangle inequality.

### Logic and Proofs
The author here threatens me by saying he will make me write proofs ahead.

There is now a proof that seems very analysis-ey, probably because of the use of $\epsilon$. (also it feels like a limit)

**Theorem 1.2.6** *Two real numbers $a$ and $b$ are equal if and only if for every real number $\epsilon$ it follows that $|a-b|<\epsilon\,$.*

Discussion of conditional statements/biconditional statements. 

### Induction
Scary, this is like the dominos but in math books. 

A good inclusion of exercises in this book. Additionally exercise 1.2.5 is De Morgan's Laws and if I was smart I'd do them. I'm not though. I will simply forget and need them later. 

## 1.3 The Axiom of Completeness
We dive into a definition of a real number. We say the set of real numbers $\mathbb{R}$ is an extension of the rational numbers $\mathbb{Q}$ in which there are no holes or gaps. We want every length along the number line to correspond to a real number. 

### An Initial Definition for $\mathbb{R}$
First: $\mathbb{R}$ is a set containing $\mathbb{Q}$. 
The operation of addition and multiplication on $\mathbb{Q}$ extend to all of $\mathbb{R}$ in a way such that every element of $\mathbb{R}$ has an additive inverse. 

$\mathbb{R}$ is an *ordered field* that contains $\mathbb{Q}$ as a subfield. 

---
**The Axiom of Completeness**:
*Every nonempty set of real numbers that is bounded above has a least upper bound*. 

---
### Least Upper Bounds and Greatest Lower Bounds
**Definition 1.3.1.** A set $A\subseteq\mathbb{R}$ is *bounded above* if there exists a number $b\in\mathbb{R}$ such that $a\le b\;\;\forall\;\; a\in A$.
Similarly for *bounded below*, if there exists a lower bound $l\in\mathbb{R}$ satisfying $l\le a\;\;\forall\;\; a\in A$.

**Definition 1.3.2.** A real number $s$ is the *least upper bound* for a set $A\subseteq\mathbb{R}$ if it meets the following two criteria: 
1. $s$ is upper bound for $A$;
2. if $b$ is any upper bound for $A$, then $s\le b$. 

The least upper bound is also frequently called the *supremum* of the set. 

## 1.4 Consequences of Completeness
**Theorem 1.4.1 (Nested Interval Property)**
*For each $n\in\mathbb{N}$, assume we are given a closed interval $I_n=[a_n,b_n]=\{x\in\mathbb{R}\,:\,a_n\le x\le b_n\}.$ Assume also that each $I_n$ contains $I_{n+1}$. Then, the resulting sequence of closed intervals $$I_1\supseteq I_2\supseteq I_3\supseteq I_4\supseteq\cdots$$ has a nonempty intersection; that is, $\cap^\infty_{n=1}I_n\neq\emptyset$.*

---
### The Density of $\mathbb{Q}$ in $\mathbb{R}$
**Theorem 1.4.2 (Archimidean Property)** *(i) Given any number $x\in\mathbb{R}$, there exists an $n\in\mathbb{N}$ satisfying $n>x$.*
(ii) Given any real number $y>0$, there exists an $n\in\mathbb{N}$ satisfying $1/n<y$. 

**Theorem 1.4.3 (Density of $\mathbb{Q}$ in $\mathbb{R}$)** *For every two real numbers $a$ and $b$ with $a<b$, there exists a rational number $r$ satisfying $a<r<b$.*

**Corollary 1.4.4** *Given any two real numbers $a<b$, there exists an irrational number $t$ satisfying $a<t<b$. 

---
### The Existence of Square Roots
**Theorem 1.4.5.** *There exists a real number $\alpha\in\mathbb{R}$ satisfying $\alpha^2=2$.*

## 1.5 Cardinality
### 1-1 Correspondence
The term *Cardinality* is used in mathematics to refer to the size of a set. 

One way to determine the comparative size of two sets is to try and relate one element of one set with another, and seeing which set has empty slots left over. This method is interesting because it works on sets of infinite size.

**Definition 1.5.1.** A function $f:A\rightarrow B$ is *one-to-one* (1-1) if $a_1\neq a_2$ in $A$ implies that $f(a_1)\neq f(a_2)$ in $B$. The function $f$ is *onto* if, given any $b\in B$, it is possible to find an element for $a\in A$ for which $f(a)=b$. 

**Definition 1.5.2.** A set $A$ *has the same cardinality as* $B$ if there exists $f:A\rightarrow B$ that is 1-1 and onto. In this case, we write $A\sim B$. 

*Note: $(a,b)\sim\mathbb{R}$ for any interval $(a,b)$*. 

---
### Countable Sets
**Definition 1.5.5.** A set $A$ is *countable* if $\mathbb{N}\sim A$. An infinite set that is not countable is called an *uncountable* set.

**Theorem 1.5.6.** (i) *The set $\mathbb{Q}$ is countable*. (ii) *The set $\mathbb{R}$ is uncountable.*

(The proof of this was actually pretty interesting, and a good use of proof by contradiction that isn't too tough to follow.)

Informally this means that $\mathbb{R}$ is a bigger kind of infinity, and also that *countable* infinities are the smallest kind of infinity. 

**Theorem 1.5.7.** *If $A\subseteq B$ and $B$ is countable, then $A$ is either countable or finite.*

**Theorem 1.5.8.** (i) *If $A_1,A_2,\dots A_m$ are each countable sets, then the union $A_1\cup A_2\cup\cdots\cup A_m$ is countable.* (ii) If $A_n$ is a countable set for each $n\in\mathbb{N}$, then $\bigcup^\infty_{n=1}A_n$ is countable. 

---
## 1.6 Cantor's Theorem
This section is largely focused on Cantor's famous diagonalization method to show that $\mathbb{R}$ is uncountable, which I will not be typing in KaTeX here. 

### Cantor's Diagonalization Method 
**Theorem 1.6.1.** *The open interval $(0,1)=\{x\in\mathbb{R}:0<x<1\}$ is uncountable.*

### Power Sets and Cantor's Theorem
**Theorem 1.6.2 (Cantor's Theorem)** *Given any set $A$, there does not exist a function $f:A\rightarrow\mathcal{P}(A)$ that is onto.*

---
## 1.7 Epilogue
This starts with the conclusion that I came to immediately, that if $\mathcal{P}(A)$ is a cardinality larger than $A$, then $\mathcal{P}(\mathcal{P}(A))$ would be, and this could go on indefinitely.

It then talks about ordering of the cardinality of sets, and a universal set. Essentially that sets can be ordered like real numbers by cardinality, and that a restriction has to be put on a universal set because a set containing all things could have a power set of itself which introduces a paradox. 

This also introduces the notation $\aleph_0$ as a representation of the $\mathrm{card}\,\mathbb{N}$. 

The designation $c=\mathrm{card}\,\mathbb{R}=\mathrm{card}\,(0,1)$ is also introduced.

Cantor wondered if there were any cardinal numbers between the two. He also wondered if they were able to be ordered in a continuum, 

In 1940, Gödel proved that using only the agreed-upon set of axioms of set theory, the continuum hypothesis could not be disproved.

In 1963, Paul Cohen proved that it is impossible to prove this conjecture. 

I personally hate this. 

It can be accepted or rejected as a statement about the nature of infinite sets, and in neither case will any logical contradictions arise. That's fucked up. 

