---
title: Book of Proof - Ch. 9

---

# Chapter 9 - Disproof

Proving a statement false is called a **disproof**. 

---
Three types of statements:  

---
**Known to be true**  
(Theorems & Propositions)  
Examples:  
- Pythagorean Theorem
- Fermat's Last Theorem
- The square of an odd number is odd
- The series $\sum^\infty_{k=1}\frac{1}{k}$ diverges

---
**Truth Unknown**  
(Conjectures)  
Examples:  
- All perfect numbers are even.
- Any even number greater than 2 is the sum of two primes. (Goldbach's Conjecture)
- There are infinitely many prime numbers of the form $2^n-1$, with $n\in\mathbb{N}$

---
**Known to be False**  
Examples:  
- All prime numbers are odd
- Some quadratic equations have three solutions
- 0=1
- There exist natural numbers $a, b\text{, and }c$ for which $a^3+b^3=c^3$

---

**How to disprove** $P$: Prove ~$P$. 

---
# 9.1 Disproving Universal Statements: Counterexamples

Since many theorems (and hence many conjectures) are universally qualified statements, it serves that we try to disprove a universally qualified statement such as $$\forall x\in S, P(X).$$
To disprove this statement, we prove the negation $$~(\forall x\in S,P(x)) = \exists x\in S,\lnot P(x).$$
The name for examples that disprove statements are called **counterexamples**.

---
**How to disprove** $\forall x\in S, P(x)$.  
Produce an example of an $x\in S$ that makes $P(x)$ false. 

---
**How to disprove** $P(x)\implies Q(x)$.  
Produce an example of $x$ that makes $P(x)$ true and $Q(x)$ false.

---
Example 9.1  
**Conjecture** For every $n\in\mathbb{Z}$, the integer $f(n)=n^2-n+11$ is prime.  
*Disproof*. The statement "For every $n\in\mathbb{Z}$, the integer $f(n)=n^2-n+11$ is prime," is **false**. As a counterexample, note that for $n=11$, the integer $f(11)=121=11\cdot11$ is not prime.  

---
# 9.2 Disproving Existence Statements

To disprove existence statements such as $$\exists x\in S,P(X)$$ we prove its negation $$\lnot(\exists x\in S,P(X))=\forall x\in S,\lnot P(x).$$

---
**Examples 9.3** Either prove or disprove the following conjecture.  
**Conjecture** There is a real number $x$ for which $x^4<x<x^2$.  

The negation is: *For every real number $x$, it is not the case that $x^4<x<x^2$
*Proof*. (Negation, Contradiction). Suppose for the sake of contradiction that there **is** an $x$ for which $x^4<x<x^2$. Then $x$ must be positive since it's greater than the non-negative number $x^4$  
Reasoning through some algebra we see
$$
\begin{aligned}
x^4 &< x < x^2\\
x^3 &< 1 < x\\
x^3-1 &< 0 < x-1\\
(x-1)(x^2+x+1) &< 0 < (x-1)\\
x^2+x+1&<0<1
\end{aligned}
$$
Here we see that $x^2+x+1<0$, but this cannot be true because $x$ is forced to be positive. Thus we have a contradiction.  
There is a real number $x$ for which $x^4<x<x^2$ is **false** because we have proved its negation "For every real number $x$ it is not the case that $x^4<x<x^2$".  

---
# 9.3 Disproof by contradiction

**How to disprove $P$ with contradiction**:  
Assume $P$ is true, and deduce a contradiction.  

---
The exercises for this chapter are cumulative. While I feel these would be good for practice, at the moment in this dash through this book wouldn't provide greater understanding. The goal is to immediately move from this book to Dummit and Foote or Lang for algebra, where I plan to focus on proof exercises. Thus my goal is to rush through to Induction and move on to the next book. 