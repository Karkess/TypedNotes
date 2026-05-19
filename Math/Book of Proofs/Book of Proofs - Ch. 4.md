---
title: Book of Proofs - Ch. 4

---

# 4.1 Theorems
*A theorem is a statement that is true and has been proved to be true.*

---
**Theorem**
Let $f$ be differentiable on an open interval $I$ and let $c \in I$. If $f(c)$ is the maximum or minimum value of $f$ on $I$, then $f'(c)=0$.

**Theorem**
If $\sum^\infty_{k=1}a_k$ converges, then $\lim_{k\to\infty}a_k=0$

**Theorem**
Suppose $f$ is continuous on the interval $[a,b]$. Then $f$ is integrable on $[a,b]$. 

**Theorem**
Every absolutely convergent series converges.

**Theorem**
If $n$ is a non-negative integer, then $\sum^{n}_{k=0}\binom{n}{k}^2=\binom{n}{k}$

---
These theorems roughly follow the form or can be put into the form *If P, then Q*.

---
Some theorems of a biconditional statement: $P\iff Q$.

Some theorems simply state facts.

**Theorem**
$$\text{The harmonic series } 1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\cdots\text{ diverges.}$$

---
A **Proposition** is a statement that is true but is not as significant.

A **Lemma** is a theorem whose main purpose is to help prove another theorem.

A **Corollary** is a result that is an immediate consequence of a theorem or proposition. 

---
# 4.2 Definitions

**Definition 4.1** An integer $n$ is **even** if $n=2a$ for some integer $a\in\mathbb{Z}$.

**Definition 4.2** An integer $n$ is **odd** if $n=2a+1$ for some integer $a\in\mathbb{Z}$.

**Definition 4.3** Two integers have the **same parity** if they are both even or they are both odd. Otherwise they have **opposite parity**.

---
**Definition 4.4** Suppose $a\text{ and }b$ are integers. We say that $a$ **divides** $b$, written $a\mid b \text{, if }b=ac\text{ for some }c\in\mathbb{Z}$. In this case we also say that $a$ is a **divisor** of $b$, and that $b$ is a **multiple** of $a$.

*Note*: Be careful with symbols: $8\mid16$ is **TRUE** and $8/16=0.5$, these have unique meanings.

---
**Definition 4.5** A number $n\in\mathbb{N}$ is **prime** if it has exactly two positive divisors, 1 and n. If N has more than two positive divisors, it is called **composite**. (Thus $n$ is composite if and only if $n=ab$ for $1<a,b<n.$)

**Definition 4.6** The **greatest common divisor** of integers $a$ and $b$, denoted $\gcd(a,b)$, is the largest integer that divides both $a$ and $b$.
The **least common multiple** of non-zero integers $a$ and $b$, denoted $\mathrm{lcm}(a,b)$, is the smallest integer in $\mathbb{N}$ that is a multiple of both $a$ and $b$. 

*Note*: $\gcd(0,0)=\infty$.

---

**Fact 4.1** If $a$ and $b$ are integers, then so are their sum, product, and difference. That is, if $a,b\in\mathbb{Z},\text{ then } a+b\in\mathbb{Z},\,a-b\in\mathbb{Z},\,\text{ and }ab\in\mathbb{Z}$.

**(The Divison Algorithm)** Given integers $a$ and $b$ with $b>0$, there exists unique integers $q$ and $r$ for which $a=qb+r\text{ and }0\le r<b.$

**Fact** Every natural number greater than 1 has a unique factorization into primes.

---
# 4.3 Direct Proof

**Outline for Direct Proof**  
**Proposition*   If $P$, then $A$  
*Proof*. Suppose $P$.  
$\,\,\,\,\,\,\,\vdots$  
Therefore $Q$. $\Box$

---

**Proposition** If $x$ is odd, then $x^2$ is odd.  
*Proof*. Suppose $x$ is odd. Then $x=2a+1$ for some $a\in\mathbb{Z}$, by definition of an odd number. Thus $x^2=\left(2a+1\right)^2=4a^2+4a+1=2\left(2a^2+2a\right)+1$ so $x^2=2b+1\text{ where } b=2a^2+2a\in\mathbb{Z}$. Therefore $x^2$ is odd, by definition of an odd number.

---
*Strategy*: Start with the first and last statement of the proof, and then work your way inward solving sometimes alternating from either side.

---
**Proposition** Let $a,b,\text{ and } c$ be integers.  
If $a\mid b\text{ and }b\mid c\text{, then }a\mid c$.  
*Proof*. Suppose $a\mid b\text{ and }b\mid c$  
*By Definition 4.4, we know $a\mid b$ means $b=ad$ for some $d\in\mathbb{Z}$.  
Likewise, $b\mid c$ means $c=be$ for some $e\in\mathbb{Z}$.  
Thus $c=be=(ad)e=a(de)$, so $c=ax$ for the integer $x=de.$*  
Therefore $a\mid c$.

---
**Proposition** If $x$ is an even integer, then $x^2-6x+5$ is odd.  
*Proof*. Suppose $x$ is an even integer.  
Then $x=2a$ for some $a\in\mathbb{Z}$, by definition of an even integer.  
So $x^2-6x+5=(2a)^2-6(2a)+5=4a^2-12a+4+1$$=2(a^2-6a+2)+1$.  
Therefore we have $x^2-6x+5=2b+1$, where $b=2a^2-6a+2\in\mathbb{Z}$.  
Consequently, $x^2-6x+5$ is odd, by definition of an odd number.

---

**Proposition** If $a,b,c\in\mathbb{N}$, then $\mathrm{lcm}(ca,cb)=c\cdot\mathrm{lcm}(a,b)$  
*Proof*. Assume $a,b,c\in\mathbb{N}$. Let $\mathrm{lcm}(ca,ab)\text{ and }n=c\cdot\mathrm{lcm}(a,b)$. We will show $m=n$. By definition, $\mathrm{lcm}(a,b)$ is a positive multiple of both $a\text{ and }b$, so $\mathrm{lcm}(a,b)=ax=by$ for some $x,y,\in\mathbb{N}$. From this we see that $n=c\cdot\mathrm{lcm}(a,b)=cax=cby$ is a positive multiple of both $ca$ and $cb$. Thus $m\le n$  
    On the other hand, as $m=\mathrm{lcm}(ca,cb)$ is a multiple of both $ca\text{ and }cb$, we have $m=cax=cby$ for some $x,y,\in\mathbb{Z}$. Then $\frac{1}{c}m=ax=by$ is a multiple of both $a$ and $b$. Therefore, $\mathrm{lcm}(a,b)\le\frac{1}{c}m$, so $c\cdot\mathrm{lcm}(a,b)\le m\text{, that is, }n\le m$.  
    We've shown that $m\le n\text{ and }n\le m\text{, so }m=n$. The proof is complete. $\Box$
    
---
**Proposition** Let $x$ and $y$ be positive numbers. If $x\le y$, then $\sqrt{x}\le\sqrt{y}$.  
*Proof*. Suppose $x\le y$. Subtracting $y$ from both sides gives $x-y\le 0$.  
This can be written as $\sqrt{x}^2-\sqrt{y}^2\le0$  
Factor this as a difference of two squares to get $(\sqrt{x}-\sqrt{y})(\sqrt{x}+\sqrt{y})\le0.$  
Dividing both sides by the positive number $\sqrt{x}+\sqrt{y}\text{ produces }\sqrt{x}-\sqrt{y}\le0.$  
Adding $\sqrt{y}$ to both sides gives $\sqrt{x}\le\sqrt{y}$.

---
**Proposition** If $x$ and $y$ are positive real numbers, then $2\sqrt{xy}\le x+y$.  
*Proof*. Suppose $x$ and $y$ are positive real numbers.  
Observe that $0\le(x-y)^2\text{, that is, }0\le x^2-2xy+y^2$  
Adding $4xy$ to both sides gives $4xy\le x^2+2xy+y^2$.  
Factoring yields $4xy\le(x+y)^2$.  
Previously we proved that such an inequality still holds that after taking the square root of both sides; doing so produces $2\sqrt{xy}\le x+y. \Box$

---
# 4.4 Using Cases

**Proposition** If $n\in\mathbb{N}\text{, then }1+(-1)^n(2n-1)\text{ is a multiple of }4.$  
*Proof*. Suppose $n\in\mathbb{N}$.  
Then $n$ is either even or odd. Let's consider these two cases separately.  

**Case 1.** Suppose $n$ is even. Then $n=2k$ for some $k\in\mathbb{Z}\text{ and }(-1)^n=1.$  
Thus $1+(-1)^n(2n-1)=1+(1)(2\cdot2k-1)=4k$, which is a multiple of 4.  

**Case 2.** Suppose $n$ is odd. Then $n=2k+1$ for some $k\in\mathbb{Z}\text{ and }(-1)^n=-1$.  
Thus $1+(-1)^n(2n-1)=1-(2(2k+1)-1)=-4k$, which is a multiple of 4.  

These cases show that $1+(-1)^n(2n-1)$ is always a multiple of 4.

---
**Proposition** Every multiple of 4 equals $1+(-1)^n(2n-1)\text{ for some }n\in\mathbb{N}$.  

$Proof$. In conditional form, the proposition is as follows: 
If $k$ is a multiple of 4, then there is an $n\in\mathbb{N}\text{ for which }1+(-1)^n(2n-1)=k$.  
What follows is a proof of this conditional statement.  
Suppose $k$ is a multiple of 4.  
This means $k=4a$ for some integer $a$.  
We must produce an $n\in\mathbb{N} \text{ for which } 1+(-1)^n(2n-1)=k$.  
This is done by cases, depending on whether a is zero, positive, or negative.  

**Case 1.** Suppose $a=0$. Let $n=1$. Then $1+(-1)^n(2n-1)=1+(-1)^1(2-1)=0=4\cdot0=4a=k$.  

**Case 2.** Suppose $a>0$. Let $n=2a$, which is in $\mathbb{N}$ because $a$ is positive. Also $n$ is even, so $(-1)^n=1$. Thus $1+(-1)^n(2n-1)=1+(2n-1)=2n=2(2a)=4a=k$.  

**Case 3.** Suppose $a<0$. Let $n=1-2a$, which is an element of $\mathbb{N}$ because $a$ is negative, making $1=2a$ positive. Also, $n$ is odd, so $(-1)^n=-1$. Thus $1+(-1)^n(2n-1)=1-(2n-1)=1-(2(1-2a)-1)=4a=k$.  

The above cases show us that no matter whether a multiple of $k=4a$ of 4 is zero, positive, or negative, $k=1+(-1)^n(2n-1)$ for some $n\in\mathbb{N}. \Box$

---
# 4.5 Treating Similar Cases

**Proposition** If two integers have opposite parity, then their sum is odd.  

*Proof*. Suppose $m$ and $n$ are two integers with opposite parity.  
We need to show that $m+n$ is odd. This is done in two cases, as follows.  

**Case 1** Suppose $m$ is even and $n$ is odd. Thus $m=2a\text{ and }n=2b+1$ for some integers $a$ and $b$. Therefore $m+n=2a+2b+1=2(a+b)+1$, which is odd (by Definition 4.2).  

**Case 2** Suppose $m$ is odd and $n$ is even. Thus $m=2a+1$ and $n=2b$ for some integers $a$ and $b$. Therefore $m+n=2a+2b+1=2(a+b)+1$, which is odd (by Definition 4.2).  

In either case, $m+n$ is odd. $\Box$  

---
A quicker way to summarize the above proof is to use the phrase "Without loss of generality" or "WLOG".  

**Proposition** Suppose $m$ and $n$ are two integers with opposite parity, then their sum is odd.  

*Proof*. Suppose $m\text{ and }n$ are two integers with opposite parity.  
We need to show that $m+n$ is odd.  
Without loss of generality, suppose $m$ is even and $n$ is odd.  
Thus $m=2a$ and $n=2b+1$ for some integers $a\text{ and }b$.  
Therefore $m+n=2a+2b=2(a+b)+1$, which is odd (by Definition 4.2). $\Box$

---
# Exercises for Chapter 4

Do: 1, 2, 4, 6, 7, 11, 16, 17

---
**1.** If $x$ is an even integer, then $x^2$ is even.  

*Proof*. Suppose $x$ is even.  
*Note*: an integer is even if $n=2a\text{ for }a\in\mathbb{Z}$  
If $x$ is even, then $x=2a\text{ for }a\in\mathbb{Z}$  
Thus $x^2 = (2a)^2=4a^2=2(2a\cdot a)$  
So $x^2=2b$ where $b$ is the integer $b=2a\cdot a$  
Thus $x^2=2b\text{ for }b\in\mathbb{Z}$  
Therefore, $x^2$ is even.

---
**2.** If x is an odd integer, then $x^3$ is odd.  

*Proof*. Suppose $x$ is odd.  
*Note*: an integer is odd if $n=2a+1\text{ for }a\in\mathbb{Z}$  
If $x$ is odd, then $x=2a+1\text { for }a\in\mathbb{Z}$  
Thus 
$$
\begin{aligned}
x^3&=(2a+1)^3\\
&=(2a+1)^2(2a+1)\\
&=(4a^2+4a+1)(2a+1)\\
&=(8a^3+8a^2+2a+4a^2+4a+1)\\
&=(8a^3+12a^2+6a+1)\\
&=(2(4a^3+6a^2+3a)+1)
\end{aligned}
$$  
So $x^3=2b+1\text{ where }b\text{ is the integer }4a^3+6a^2+3a$.  
Thus $x^3=2b+1\text{ for }b\in\mathbb{Z}$  
Therefore, $x^3$ is odd. $\Box$

---
**4.** Suppose $x,y\in\mathbb{Z}$. If $x$ and $y$ are odd, then $xy$ is odd.  

*Proof*. $x,y\in\{n\in\mathbb{Z}:n=2k+1\text{ for some }k\in\mathbb{Z}\}$  
*Note*: an integer is odd if $n=2a+1\text{ for }a\in\mathbb{Z}$  
Let $x=2a+1\text{ and }y=2b+1$.  
$$
\begin{aligned}
xy&=(2a+1)(2b+1)\\
&=4ab+2a+2b+1\\
&=2(ab+a+b)+1
\end{aligned}
$$
Thus $xy=2n+1\text{ where }n=(ab+a+b)\text{ for }a,b\in\mathbb{Z}$  
Therefore, $xy$ is odd when both $x$ and $y$ are odd. $\Box$

---
**6.** Suppose $a,b,c\in\mathbb{Z}$. If $a\mid b\text{ and }a\mid c\text{, then }a\mid(b+c)$  
*Proof*. $(a,b,c)\in\{(x,y,z)\in\mathbb{Z}:x\mid y\text{ and }x\mid z\}$  
*Definition 4.4*: $a\mid b\text{, if } b=ac\text{ for some }c\in\mathbb{Z}$  
By Definition 4.4, $a\mid b = ad\text{ for some }d\in\mathbb{Z}$  
Likewise $a\mid c = ae\text{ for some }e\in\mathbb{Z}$  
$a\mid(b+c) = a(d+e)\text{ for some }d,e\in\mathbb{Z}$  
Thus, $b+c=ax$ where $x=(d+e)\text{ for }d,e\in\mathbb{Z}$.  
Therefore, $a\mid(b+c)\text{ when }a\mid b\text{ and }a\mid c$.

---
**7.** Suppose $a,b
\in\mathbb{Z}\text{. If }a\mid b\text{, then }a^2\mid b^2.$  

*Proof*. Suppose $a\mid b$.  
*Definition 4.4*: $a\mid b\text{, if } b=ac\text{ for some }c\in\mathbb{Z}$  
By Definition 4.4, $a\mid b\text{, if }b=ac\text{ for some }c\in\mathbb{Z}$  
Take 
$$
\begin{aligned}
b^2&=(ac)^2\\
&=a^2c^2\\
&=a^2(c\cdot c)\\
&=a^2x
\end{aligned}
$$
where, $x=c^2$
So $b^2$ is a multiple of $a^2$ by a factor of $x\in\mathbb{Z}, x=c\cdot c$  
Therefore, $a^2\mid b^2$. $\Box$

---
**11.** Suppose $a,b,c,d\in\mathbb{Z}\text{. If }a\mid b\text{ and }c\mid d\text{, then }ac\mid bd$.  

*Proof*. Suppose $a\mid b\text{ and }c\mid d$  
*Definition 4.4*: $a\mid b\text{, if } b=ac\text{ for some }c\in\mathbb{Z}$  
$a\mid b=ae\text{ for }e\in\mathbb{Z}$  
$c\mid d=cf\text{ for }f\in\mathbb{Z}$  
$bd=aecf$  
$bd=ac(ef)$  
$bd=ac(x)\text{, where } x=ef, x\in\mathbb{Z}$  
Therefore, $ac\text{ divides }bd$.$\Box$

---
**16.** If two integers have the same parity, then their sum is even. (Try cases.)  

*Proof*. Suppose $m\text{ and }n$ are two integers with the same parity.  
*Note*: an integer is even if $n=2a\text{ for }a\in\mathbb{Z}$  

**Case 1** $m\text{ and }n\text{ are both even:} m=2a\text{ and }n=2b$.  
Therefore $m+n=2a+2b=2(a+b)=2x$  
where $x=a+b$.  
Therefore, when $m$ and $n$ are both even then their sum is even.  

**Case 2** $m\text{ and }n\text{ are both odd:} m=2a+1\text{ and }n=2b+1$.  
Therefore $m+n=(2a+1)+(2b+1)=(2a+2b+2)=2(a+b+1)=2x$  
where $x=a+b+1$  
Therefore, when $m$ and $n$ are both odd their sum is even.

In either case, m+n is even. $\Box$



---
**17.** If two integers have opposite parity, then their product is even.  

*Proof*. Suppose $m\text{ and }n$ are two integers with opposite parity.  
*Note*: an integer is even if $n=2a\text{ for }a\in\mathbb{Z}$  
Without loss of generality, suppose that m is even and n is odd.  
Thus, $m=2a\text{ and }n=2b+1\text{ for } a,b\in\mathbb{Z}$  
Therefore $mn=(2a)(2b+1)=(4ab+2a)=2(2ab+a)=2x$  
where $x=2ab+a$ and $x\in\mathbb{Z}$  
Therefore, mn=2x, which is even by Definition 4.1 $\Box$

---
**Bonus**  
**19.** Suppose $a,b\text{, and }c$ are integers. If $a^2\mid b\text{ and }b^3\mid c\text{, then }a^6\mid c$.  

*Proof.* Suppose $a,b\text{, and }c$ are integers and $a^2\mid b\text{ and }b^3\mid c$.  
*Definition 4.4*: $a\mid b\text{, if } b=ac\text{ for some }c\in\mathbb{Z}$  

If $a^2\mid b$ then $b=a^2d\text{, where }d\in\mathbb{Z}$  
If $b^3\mid c$ then $c=b^3e\text{, where }d\in\mathbb{Z}$  
Thus $c=(a^2d)^3e=a^6d^3e=a^6x$  
where $x=d^3e.\, x\in\mathbb{Z}$  
Therefore, if $a^2\mid b\text{ and }b^3\mid c\text{, then }a^6\mid c$. $\Box$