---
title: Book of Proof - Ch. 7

---

# Chapter 7 - Proving Non-Conditional Statements

# 7.1 If-and-Only-If Proof

Some propositions have the form $$P\text{ if and only if }Q.$$  

We call this a biconditional statement because it asserts both of the following conditional statements:
$$
\begin{aligned}
\text{If }P\text{, then }Q.\\
\text{If }Q\text{, then }P.
\end{aligned}
$$
So to prove biconditional statements we must prove **two** conditional statements.  

**Outline for If-and-Only-If Proof**  
**Proposition** If $P$ if and only if $Q$.

$Proof$.  
Prove $P\implies Q$ using direct, contrapositive, or contradiction proof.  
Prove $Q\implies P$ using direct, contrapositive, or contradiction proof.  

---
Let us see a simple example of a biconditional proof.

**Proposition** The integer $n$ is odd if and only if $n^2$ is odd.  

*Proof*. Suppose $n$ is odd. Then, by definition of an odd number, $n=2a+1$ for some integer $a$. Thus $n^2=(2a+1)^2=4a^2+4a+1=2(2a^2+2a)+1$. This expresses $n^2$ as twice an integer, plus 1, so $n^2$ is odd.  

Conversely, we need to prove that $n^2$ being odd implies that $n$ is odd. Suppose $n$ is not odd. Then $n$ is even, so $n=2a$ for some integer $a$ (by definition of an even number). Thus $n^2=(2a)^2=2(2a^2)$, so $n^2$ is even because it's twice an integer. Thus $n^2$ is not odd. We've now proved that if $n$ is not odd, then $n^2$ is not odd, and this is a contrapositive proof that if $n^2$ is odd then $n$ is odd.  

---
# 7.2 Equivalent Statements

Sometimes we use a list of statements where if any of them are deemed true or false, all of them are deemed true or false. An example from linear algebra:

**Theorem** Suppose $A$ is an $n\times n$ matrix. The following statements are equivalent:  
a. The matrix $A$ is invertible.  
b. The equation $Ax=b$ has a unique solution for every $b\in\mathbb{R}^N$.  
c. The equation $Ax=0$ has only the trivial solution.  
d. The reduced row echelon form of $A$ is $I_n$.  
e. $\det{A}\neq0.$  
f. The matrix $A$ does not have 0 as an eigenvalue.  

---
# 7.3 Existence Proofs; Existence and Uniqueness Proofs

Before we have been proving universally quantified statements, $$\forall x, P(x)\implies Q(x)$$
How would we prove an *existentially* quantified statement? $$\exists x,R(x)$$

As this statement asserts there exists some specific object $x$ for which $R(x)$ is true, all have to do is provide an example. 

These statements are called **existence statements**, and theorems of this form are called **existence theorems**. 

---
Some examples are quite simple.

**Proposition**. There exists an even prime number.

*Proof*. Observe that 2 is an even prime number.

---
Some examples require a little more legwork. 

**Proposition** There exists an integer that can be expressed as the sum of two perfect cubes in two different ways.

*Proof*. Consider the number 1729. Note that $1^3+12^3=1729$ and $9^3+10^3=1729$. Thus the number 1729 can be expressed as the sum of two perfect cubes in two different ways.

---

Existence statements can be embedded inside of conditional statements. Like the definition of gcd:

If $a,b\in\mathbb{N}$, then there exist integers $k$ and $\ell$ for which $\gcd{(a,b)}=ak+b\ell$. 

This is a conditional statement that has the form $$a,b\in\mathbb{N}\implies\exists k,\ell\in\mathbb{Z},\gcd(a,b)=ak+b\ell.$$

---
As an example:

**Proposition 7.1** If $a,b\in\mathbb{N}$, then there exist integers $k$ and $\ell$ for which $\gcd(a,b)=ak+b\ell$. 

*Proof.* (Direct) Suppose $a,b\in\mathbb{N}$ Consider the set $A=\{ax+by : x,y\in\mathbb{Z}\}$.  
This set contains both positive and negative integers, as well as 0.  
Let $d$ be the smallest *positive* element of $A$.  
Because $d$ is in $A$, it must have the form $d=ak+b\ell$ for some specific $k,\ell\in\mathbb{Z}$.  
We will now show that $d=\gcd(a,b)$. To see that $d\mid a$, use the division algorithm to write $a=qd+r$ for integers $q$ and $r$ with $0\le r<d$. The equation $a=qd+r$ yields
$$
\begin{aligned}
r&=a-qd\\
&=a-q(ak+b\ell)\\
&=a(1-qk)+b(-q\ell)
\end{aligned}
$$
Therefore $r$ has the form $r=ax+by$, and thus is in $A$. Because $0\le r<d$ and $d$ is the smallest positive number in $A$, $r$ can't be positive, thus $r=0$.  
Updating our equation $a=qd+r$, we arrive at $a=qd$, so $d\mid a$. Without loss of generality this argument can be applied to $b=qd+r$ and show that $d\mid b$. Thus $d$ is a common divisor of $a$ and $b$.  
As $\gcd(a,b)$ divides $a$ and $b$, we have $a=\gcd(a,b)\cdot m$ and $b=\gcd(a,b)\cdot n$ for some $m,n\in\mathbb{Z}$. So $d=ak+b\ell=\gcd(a,b)\cdot mk+\gcd(a,b)\cdot n\ell=\gcd(a,b)(mk+n\ell)$, thus $d$ is a multiple of $\gcd(a,b)$. Therefore $d\ge\gcd(a,b)$, but $d$ can't be a larger common divisor of $a$ and $b$ than $\gcd(a,b)$, so $d=\gcd(a,b)$. $\blacksquare$

---

There also exists a set of proofs called *uniqueness proofs*. These have the form "*There is a unique x for which P(x).*"  

To prove it, you must produce an example $x=d$ for which $P(d)$ is true, **and** you must show that $d$ is the only such example. 

---
# 7.4 Constructive Versus Non-Constructive Proofs

There are two categories of existence proofs: Constructive and non-constructive.  
Constructive proofs display an explicit example that proves the theorem.  
Nonconstructive proofs prove an example exists without actually giving it.  

---
**Non-Constructive** example:  
**Proposition** There exist irrational numbers $x,y$ for which $x^y$ is rational. 

*Proof*. Let $x=\sqrt{2}^{\sqrt{2}}$ and $y=\sqrt{2}$. We know that $y$ is irrational, but not whether x is rational or irrational. On one hand, if $x$ is irrational, then we have an irrational number to an irrational power that is rational: $$x^y=\left(\sqrt{2}^{\sqrt{2}}\right)^\sqrt{2}=\sqrt{2}^{\sqrt{2}\sqrt{2}}=\sqrt{2}^2=2.$$
On the other hand, if $x$ is rational, then $y^y=\sqrt{2}^{\sqrt{2}}=x$ is rational. Either way, we have an irrational number to an irrational power that is rational. $\blacksquare$

**Constructive** example:  
**Proposition** There exist irrational numbers $x,y$ for which $x^y$ is rational. 

*Proof*. Let $x=\sqrt{2}$ and $y=\log_29$. Then
$$x^y=\sqrt{2}^{\log_29}=\sqrt{2}^{2\log_23}=\left(\sqrt{2}^2\right)^{\log_23}=2^{\log_23}=3.$$
As 3 is rational, we have shown that $x^y$ is rational.  
Suppose for the sake of contradiction that $\log_29$ is rational, so there are positive integers $a$ and $b$ for which $\frac{a}{b}=\log_29$. This means
$$
\begin{aligned}
2^\frac{a}{b}&=9\\
\left(2^\frac{a}{b}\right)^b&=9^b\\
2^a&=9^b
\end{aligned}
$$
But $2^a$ is even while $9^b$ is odd. This is a contradiction; the proof is complete. $\blacksquare$

---
# Exercises for Chapter 7

Do 1, 3, 8, 12, 14, 28

---
**1.** Suppose $x\in\mathbb{Z}$. Then $x$ is even if and only if $3x+5$ is odd.  

*Proof*. (Direct) Suppose $x$ is even, then $3x+5$ is odd. If $x$ is even, then there exists some integer $a$ such that $x=2a$. Substituting this into $3x+5$ we achieve $3(2a)+5=6a+5=2(3a+2)+1$, which is odd by definition of odd numbers.  
(Contradiction) Suppose $3x+5$ is odd, for the sake of contradiction we assume that $x$ is odd. This means there exists an integer b for which $x=2b+1$.  
Substituting this value in we achieve $3x+5=3(2b+1)+5=6b+3+5=6b+8=2(2b+4)$.  
This is an even value, so $3x+5$ is both even and odd. This is a contradiction. $\blacksquare$

---
**3.** Given an integer $a$, then $a^3+a^2+a$ is even if and only if $a$ is even.  

*Proof*. (Direct) Suppose $a$ is even, then $a^3+a^2+a$ is even. If $a$ is even, then there exists some integer $x$ for which $a=2x$. Inserting this into our expression we see that $(2x)^3+(2x)^2+2x=8x^3+4x^2+2x=2(4x^3+4x^2+2x)$. Thus $a^3+a^2+a$ is even when $a$ is even.  
(Contradiction) Suppose $a^3+a^2+a$ is even. For the sake of contradiction then $a$ is odd. By definition of odd integers $a=2y+1$ where $y\in\mathbb{Z}$.  
Inserting this into $a^3+a^2+a$ leads to 
$$
\begin{aligned}
a^3+a^2+a&=(2y+1)^3+(2y+1)^2+(2y+1)\\
&=(4y^2+4y+1)(2y+1)+(4y^2+4y+1)+(2y+1)\\
&=(8y^3+8y^2+2y+4y^2+4y+1)+(4y^2+4y+1)+(2y+1)\\
&=(8y^3+12y^2+6y+1)+(4y^2+4y+1)+(2y+1)\\
&=8y^3+16y^2+12y+3\\
&=2(4y^3+8y^2+6y+2)+1
\end{aligned}
$$
Thus $a^3+a^2+a$ is odd when $a$ is odd. This shows $a^3+a^2+a$ is both even and odd. This is a contradiction. $\blacksquare$  

---
**8.** Suppose $a,b\in\mathbb{Z}$. Prove that $a\equiv b\pmod{10}$ if and only if $a\equiv b\pmod{2}\text{ and }a\equiv b\pmod{5}$.  

*Proof* (Direct) Suppose $a\equiv b\pmod{10}$, then $a\equiv b\pmod{2}\text{ and }a\equiv b\pmod{5}$.  
The definition of congruence modulo states that $a\equiv b\pmod{n}\implies n\mid(a-b)$.  
So we suppose $10\mid(a-b)$ and show that $5\mid(a-b)$ and $2\mid(a-b)$.  
We have proved that if $a\mid b$, and $b\mid c$, then $a\mid c$.  
Since we know $10\mid(a-b)$, we just have to show that $2\mid10$ and $5\mid10$.  
We know that $a\mid b$ if $b=ac$ for some $c\in\mathbb{Z}$.  
We see that $10=5\cdot2$ and $10=2\cdot5$, so $5\mid10$ and $2\mid10$ are true.  
From this, we see that $2\mid(a-b)$ and $5\mid(a-b)$.  

(Direct) Suppose that $a\equiv b\pmod{2}\text{ and }a\equiv b\pmod{5}$, then $a\equiv b\pmod{10}$.  
Since we know $a\equiv b\pmod{2}\text{ and }a\equiv b\pmod{5}$, we know that $2\mid(a-b)$ and $5\mid(a-b)$.  
This leads to $a-b=2c$ *and* $a-b=5d$ for some integers $c$ and $d$.  
For these both to hold we need to find the lcm of these two values. lcm$(2,5)=10$. From this, we know that $a-b=10e$ for all integers $e$. By definition of congruence this means that $a\equiv b\pmod{10}$. $\blacksquare$

---
**12.** There exists a positive real number $x$ for which $x^2<\sqrt{x}$.  

*Proof*. (Example) Take the real number 0.5:
$$
\begin{aligned}
x^2&\implies0.5^2=0.25\\
\sqrt{x}&\implies\sqrt{0.5}\approx0.707
\end{aligned}
$$
Thus there exists a positive real number $x$ for which $x^2<\sqrt{x}.$

---
**14.** Suppose $a\in\mathbb{Z}$. Then $a^2\mid a$ if and only if $a\in\{-1,0,1\}$.  

The first direction is very easy. Simply directly test that all three cases divide. The other direction you set up the definition of divisibility and see that you get something like $a=ka^2\implies1=ka$ with $k$ and $a$ being integers, so you can only satisfy that with $1\cdot 1$ and $-1 \cdot -1$. You have to treat 0 as a case for this one too, and you get 0 as the third solution for the biconditional.

---
**28.** Prove the division algorithm: If $a,b\in\mathbb{N}$, there exist *unique* integers $q,r$ for which $a=bq+r$, and $0\le r<b$.  

I added this one on myself as it seems important but I've run out of time to solve this problem and must move on to Ch. 8. I am pretty sure there was a proof of this when I read Hungerford years ago, and the existence proof is in this book, so the unique part is the distinct part of this, of which I did 0 problems. I will have to target some uniqueness problems in the next chapters, as existence and uniqueness proofs seem pretty important in the type of analysis engineers do. 