---
title: Book of Proof - Ch. 6

---

# Chapter 6 - Proof by Contradiction

To do so, we assume the statement we are trying to assume is false, and that the conclusion is nonsense.

---
**Proposition** If $a,b\in\mathbb{Z}$, then $a^2-4b\neq2$  

*Proof*. Suppose this proposition is *false*.  
This conditional statement being false means there exist numbers $a$ and $b$ for which $a,b\in\mathbb{Z}$ is true, but $a^2-4b\neq2$ is false.  
In other words, there exists integers $a,b\in\mathbb{Z}$ for which $a^2-4b=2$.  
From this equation we get $a^2=4b+2=2(2b+1)$, so $a^2$ is even.  
Because $a^2$ is even, it follows that $a$ is even, so $a=2c$ for some integer $c$.  
Now plug $a=2c$ back into the boxed equation to get $(2c)^2-4b=2$, so $4c^2-4b=2$. Dividing by $2$, we get $2c^2-2b=1$.  
Therefore, $1=2(c^2-b)$, and because $c^2-b\in\mathbb{Z}$, it follows that $1$ is even.  
We know $1$ is **not** even, so something must be wrong.  
As the logic after the first like in the proof is correct, it must be the first line that was incorrect. Thus, the proposition is true.  

---
This proof logically follows $C\land\lnot C$, which is called a contradiction because there is no way for it to ever be true.

# 6.1 Proving Statements with Contradiction

**Outline for Proof by Contradiction**  
**Proposition** $P$.  

*Proof*. Suppose $\lnot P$.  
$\,\,\,\,\,\,\,\,\,\vdots$  
Therefore, $C\land\lnot C$. $\blacksquare$  

---
**Definition 6.1** A real number $x$ is **rational** if $x=\frac{a}{b}$ for some $a,b\in\mathbb{Z}$.  
Also, $x$ is **irrational** if it is not rational, this is if $x\neq\frac{a}{b}$ for every $a,b\in\mathbb{Z}$. 

---
**Proposition** The number $\sqrt{2}$ is irrational.  

*Proof*. Suppose for the sake of contradiction it is not true that $\sqrt{2}$ is irrational. Then $\sqrt{2}$ is rational, so there are integers for $a$ and $b$ for which $$\sqrt{2}=\frac{a}{b}.$$  
Let this fraction be fully reduced; in particular, this means that $a$ and $b$ and not both even.  
Squaring both sides of the equations gives $2=\frac{a^2}{b^2}$ and therefore $$a^2=2b^2.$$  
From this it follows that $a^2$ is even, and earlier we proved that $a^2$ being even means $a$ is even. Thus, as we know $a$ and $b$ aren ot both even, it follows that $b$ **is odd**.  
Now, since $a$ is even we know that $a$ can be represented by integer $2c$. Plugging this in gives $(2c)^2=2b^2$ and thus $b^2=2c^2$ which means $b^2$ is even.  
Thus we have a **contradiction** because these numbers both appear to be even.  

---
**Proposition** There are infinitely many prime numbers.  

*Proof*. For the sake of contradiction, suppose there are only finitely many prime numbers.  
We list all prime numbers as $p_1,p_2,p_3,\dots,p_n$  
Thus, $p_n$ is the $n$th and largeset prime number.  
Now consider the number $a=(p_1p_2p_3\dots p_n)+1$, that is, a product of all prime numbers plus 1.  
Now $a$ like any natural number greater than one has at least one prime divisor, and that means $p_k\mid a$ for at least one of our $n$ prime numbers $p_k$.  
Thus there is an integer $c$ for which $a=cp_k$ which is to say $$(p_1p_2p_3\dots p_{k-1}p_kp_{k+1}\dots p_n)+\frac{1}{p_k}=c,$$ so $$\frac{1}{p_k}=c-(p_1p_2p_3\dots p_{k-1}p_{k+1}\dots p_n).$$ The expression on teh right is an integer, while the expression on the left is not an integer. This is a contradiction. $\blacksquare$

---
**Proposition** For every real number $x\in[0,\pi/2]$, we have $\sin{x}+\cos{x}\ge1$  

*Proof*. Suppose, for the sake of contradiction that this is not true.  
Then there exists an $x\in[0,\pi/2]$ for which $\sin{x}+\cos{x}<1$  
Since $x\in[0,\pi/2]$, neither $\sin{x}$ nor $\cos{x}$ is negative, so $0\le\sin{x}+\cos{x}<1$.  
Thus $0^2\le(\sin(x)+\cos{x})^2<1$, which gives $0^2\le\sin^2{x}+2\sin{x}\cos{x}+\cos^2{x}<1^1$.  
As $\sin^2{x}+\cos^2{x}=1$, this means $2\sin{x}\cos{x}<0$.  
This contradicts the fact that neither $\sin{x}$ nor $\cos{x}$ is negative. $\blacksquare$

---
# 6.2 Proving Conditional Statements by Contradiction

**Outline for Proving a Conditional Statement with Contradiction**  

**Proposition** If $P$, then $Q$.  
*Proof*. Suppose $P$ and ~$Q$.  
$\,\,\,\,\,\,\,\,\vdots$
Therefore $C\land\lnot C$

---
**Proposition** Suppose $a\in\mathbb{Z}$. If $a^2$ is even, then $a$ is even.  

*Proof*. For the sake of contradiction, suppose $a^2$ is even and $a$ is not even.  
Then $a^2$ is even, and $a$ is odd.  
Since $a$ is odd, there is an integer $c$ for which $a=2c+1$.  
Then $a^2=(2c+1)^2=4c^2+4c+1=2(2c^2+2c)+1$, so $a^2$ is odd.  
Thus $a^2$ is even and $a^2$ is not even, a contradiction. $\blacksquare$  

---
**Proposition** If $a,b\in\mathbb{Z}\text{ and }a\ge2$, then $a\nmid b$ or $a\nmid(b+1)$.  

*Proof*. Suppose for the sake of contradiction there exist $a,b\in\mathbb{Z}\text{ with }a\ge2$, and for which it is not true that $a\nmid b\text{ or }a\nmid(b+1)$.  
By DeMorgan's law, we have $a\mid b\text{ and }a\mid(b+1)$.  
The definition of divisibility says there are $c,d\in\mathbb{Z}$ with $b=ac$ and $b+1=ad$.  
Subtracting one equation from the other gives $ad-ac=1\text{, so }a(d-c)=1$.  
Since $a$ is positive, $d-c$ is also positive (other wise $a(d-c)$ would be negative).  
Then $d-c$ is a positive integer and $a(d-c)=1\text{, so }a=1/(d-c)<2$.  
Thus we have $a\ge2$ and $a<2$, a contradiction $\blacksquare$. 

---
# 6.3 Combining Techniques

**Proposition** Every non-zero rational number can be expressed as a product of two irrational numbers.

*Proof*. This proposition can be reworded as follows: If *r* is a non-zero rational number, then *r* is a product of two irrational numbers. In what follows, we prove this with a direct proof.  
    Suppose *r* is a non-zero rational number. Then $r=\frac{a}{b}$ for all integers $a$ and $b$.  
Also, $r$ can be written as a product of two numbers as follows: $$r=\sqrt{2}\cdot\frac{r}{\sqrt{2}}.$$  
We know $\sqrt{2}$ is irrational, so to complete the proof we must show that $\frac{r}{\sqrt{2}}$ is also irrational. This means $$\frac{r}{sqrt{2}}=\frac{c}{d}$$ for integers $c$ and $d$, so $$\sqrt{2}=r\frac{d}{c}.$$ But we know that $r=\frac{a}{b}$, which combines with teh above equation to give $$\sqrt{2}=r\frac{d}{c}=\frac{a}{b}\frac{d}{c}=\frac{ad}{bc}.$$
This means $\sqrt{2}$ is rational, which is a contrdiction because we know it is irrational.   Therefore $\frac{r}{\sqrt{2}}$ is irrational.  
Hence, $r=\sqrt{2}\cdot\frac{r}{\sqrt{2}}$ is a product of two irrational numbers. $\blacksquare$

---
# 6.4 Some Words of Advice

Proof by contradiction is powerful but can hide even simpler contrapositive proofs, for example:  

**Proposition** Suppose $a\in\mathbb{Z}$. If $a^2-2a+7$ is even, then $a$ is odd.  

*Proof*. (Contradiction) Suppose $a^2-2a+7$ is even, then $a$ is not odd.  
That is, suppose $a^2-2a+7$ is even and $a$ is even.  
Since $a$ is even, there is an integer $c$ for which $a=2c$.  
Then $a^2-2a+7=(2c)^2-2(2c)+7=2(2c^2-2c+3)+1$, so $a^2-2a+7$ is odd.  
Thus $a^2-2a+7$ is both even and odd, a contradiction. $\blacksquare$  

*Proof*. (Contrapositive) Suppose $a$ is not odd.  
Then $a$ is even, so there is an integer $c$ for which $a=2c$.  
Then $a^2-2a+7=(2c)^2-2(2c)+7=2(2c^2-2c+3)+1$, so $a^2-2a+7$ is odd.  
Thus $a^2-2a+7$ is not even. $\blacksquare$

---
# Exercises for Chapter 6

Do 1 2 3 4 8 9 10

---
**1.** Suppose $n\in\mathbb{Z}$. If $n$ is odd, then $n^2$ is odd.  

*Proof*. (Contradiction) Suppose $n$ is odd, then $n^2$ is not odd.  
Since $n$ is odd, then there exists an integer $d$ where $n=2d+1$.  
Plugging this into $n^2$ we see
$$
\begin{aligned}
n^2&=(2d+1)^2\\
&=4d^2+4d+1\\
&=2(2d^2+2d)+1
\end{aligned}
$$
Thus $n^2$ is odd; $n^2$ is both odd and not odd. This is a contradiction. $\blacksquare$ 

---
**2.** Suppose $n\in\mathbb{Z}$. If $n^2$ is odd, then $n$ is odd.  

*Proof*. (Contradiction) Suppose $n^2$ is odd, then $n$ is not odd.  
Since $n$ is not odd, then there exists an integer $c$ for which $n=2c$.  
Plugging this into $n^2$ we see
$$
\begin{aligned}
n^2&=(2n)^2\\
&=4n^2\\
&=2(2n^2)
\end{aligned}
$$
Thus $n^2$ is even; $n^2$ is both odd and even. This is a contradiction. $\blacksquare$

---
**3.** Prove that $\sqrt[3]{2}$ is irrational.  

*Proof*. (Contradiction) Suppose $\sqrt[3]{2}$ is rational.  
This means that for some integers $a$ and $b$, $\sqrt[3]{2}=\frac{a}{b}$.  
Taking $a$ and $b$ to be fully reduced fractions we have: 
$$
\begin{aligned}
\sqrt[3]{2}&=\frac{a}{b}\\
2&=\frac{a^3}{b^3}\\
2b^3&=a^3\\
2(b^3)&=a^3
\end{aligned}
$$
From this we can see that $a^3$ is even. From an earlier proof we know that this means that $a$ is also even. We know now $a=2c\text{, for } c\in\mathbb{Z}$. Plugging this in we see
$$
\begin{aligned}
a^3&=(2c)^3\\
&=8c^3\\
&=2(4c^3)\\
2b^3&=2(4c^3)\\
b^3&=4c^3\\
b^3&=2(c^3)
\end{aligned}
$$
Which shows that $b^3$ is also even. From the earlier cited proof we know this also proves $b$ is even. When $a$ and $b$ are both even they can be reduced, but they are fully reduced. This is a contradiction. $\blacksquare$

---
**4.** Prove that $\sqrt{6}$ is irrational.  

This question should be the same as $\sqrt{2}$ multiplied by a factor of 3 inside the parenthesis  
Actually this generalizes really well. A much better question would have been that every non-perfect square is irrational.  
I'd prove that here but I'm lazy and want to start tackling harder proofs and will quickly move to other books and struggle more there instead of being smart and working hard here too.  

---
**8.** Suppose $a,b,c\in\mathbb{Z}$. If $a^2+b^2=c^2$, then $a$ or $b$ is even.  

*Proof*. (Contradiction) Suppose for the sake of contradiction if $a^2+b^2=c^2$ then $a$ and $b$ are both odd.  
This means that there exist integers $k$ and $l$ such that $a=2k+1$ and $b=2l+1$.  
$$
\begin{aligned}
c^2&=a^2+b^2\\
&=(2k+1)^2+(2l+1)^2\\
&=4k^2+4k+1+4l^2+4l+1\\
c^2&=4k^2+4l^2+4k+4l+2\\
c^2&=4(k^2+l^2+k+l)+2\\
c^2&=4m+2
\end{aligned}
$$
So we see that $c^2=4m+2$ where $m$ is the integer $k^2+l^2+k+l$.  
Now we will look at the squares modulo 4 in two cases.  

**Case 1** Suppose $n$ is an even integer and that $n^2\equiv0\pmod{4}$.  
By definition of even there exists an integer $j$ such that $n=2j$, which follows $n^2=(2j)^2=4j^2=4q$, where $q=j^2\in\mathbb{Z}$.  
By definition of congruence, $n^2\equiv0\pmod{4}$.

**Case 2** Suppose $n$ is an odd integer and that $n^2\equiv1\pmod{4}$.  
By definition of odd there exists an integer $m$ such that $n=2m+1$, which follows $n^2=(2m+1)^2=4m^2+4m+1=4(m^2+m)+1=4y+1$, where $y=m^2+m\in\mathbb{Z}$.  
By definition of congruence, $n^2\equiv1\pmod{4}$  

Because $c^2\mod{4}$ can never equal 2, it is not possible for $c^2$ to be both an integer and to equal $4m+2$ where m is an integer. This is a contradiction. $\blacksquare$ 

---
**9.** Suppose $a,b\in\mathbb{R}$. If $a$ is rational and $ab$ is irrational, then $b$ is irrational.  

Cutting for time. Presumably the strategy would be showing that a rational multiplied by a rational would still be rational. 

---
**10.** There exists no integers $a$ and $b$ for which $21a+30b=1$.  

Cutting for time. this feels structurally similar to the back half of 9 at a glance. 