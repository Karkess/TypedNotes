---
title: Book of Proof - Ch. 10

---

# Chapter 10 - Mathematical Induction

# 10.1 Proof by Induction
**Outline for Proof by Induction**

**Proposition** The statements $S_1,S_2,S_3,S_4,\dots$ are all true.  

*Proof*. (Induction)  
(1) Prove that the first statement $S_1$ is true.  
(2) Given any integer $k\ge1$, prove that the statement $S_k\implies S_{k+1}$ is true.  
It follows by mathematical induction that every $S_n$ is true.  

---
The first step (1) is called the **basis step**  
The second step (2) is called the **inductive step**  
The assumption that $S_k$ is true is called the **inductive hypothesis**.  

---
**Proposition** If $n\in\mathbb{N}$, then $1+3+5+7+\dots+(2n-1)=n^2$.  

*Proof*. (Mathematical induction).  
(1) Observe that if $n=1$, this statement is $1=1^2$, which is obviously true.  
(2) We must now prove $S_k\implies S_{k+1}$ for any $k\ge1$.  
We will use a direct proof. Suppose $1+3+5+7+\dots+(2k-1)=k^2$. Then
$$
\begin{aligned}
1+3+5+7+\dots\dots\dots\dots+(2(k+1)-1)&=\\
1+3+5+7+\dots+(2k-1)+(2(k+1)-1)&=\\
(1+3+5+7+\dots+(2k-1))+(2(k+1)-1)&=\\
k^2+(2(k+1)-1)&=k^2+2k+1\\
&=(k+1)^2.
\end{aligned}
$$
Thus $1+3+5+7+\dots+(2(k+1)-1)=(k+1)^2$. This proves that $S_k\implies S_{k+1}$.  
It follows by induction that $1+3+5+7+\dots+(2n-1)=n^2$ for every $n\in\mathbb{N}.\blacksquare$

---
# 10.2 Proof by Strong Induction

**Outline for Proof by Strong Induction**  
**Proposition** The statements $S_1,S_2,S_3,S_4,\dots$ are all true.  
*Proof*. (Strong Induction)  
(1) Prove the first statement $S_1$. (Or the first several $S_n$, if needed.)  
(2) Given any integer $k\ge1$, prove $(S_1\land S_2\land S_3\land\dots\land S_k)\implies S_{k+1}.\blacksquare$

---
**Proposition** Any postage of 8 cents or more is possible using 3 cents and 5 cents stamps.  

*Proof*. We will use strong induction.  
(1) This holds for postages of 8,9, and 10 cents. For 8 cents, use one 3 cents stamp and one 5 cent stamp. For 9 cents use three 3 cents stamps. For 10 cents use two 5 cents stamps.  
(2) Let $k\ge10$, and for each $8\le m\le k$, assume a postage of $m$ cents can be obtained exactly with 3 cents and 5 cents stamps.  
We must show that $S_{k+1}$ is true, that is, (k+1)-cents postage can be achieved with 3 cents and five cents stamps.  
By assumption, $S_{k-2}$ is true. Thus we can get (k-2)-cent postage with 3 cents and 5 cents stamps. Now we just add one more 3 cents stamp, and we have $(k-2)+3=k+1$ cents postage with 3 cents and 5 cents stamps.  

---
# 10.3 Proof by Smallest Counterexample

**Outline for Proof by Smallest Counterexample**  
**Proposition** The statements $S_1,S_2,S_3,S_4,\dots$ are all true.  

*Proof*. (Smallest counterexample)  
(1) Check that the first statement $S_1$ is true  
(2) For the sake of contradiction, suppose not every $S_n$ is true.  
(3) Let $k>1$ be the smallest integer for which $S_k$ is **false**.  
(4) Then $S_{k-1}$ is true and $S_k$ is false. Use this to get a contradiction. $\blacksquare$  

---
**Proposition** If $n\in\mathbb{N}$, then $4\mid(5^n-1)$.  

*Proof*. We use proof by smallest counterexample.  
(1) If $n=1$, then the statement $4\mid(5^1-1)$ or $4\mid4$, which is true.  
(2) For the sake of contradiction, suppose it's not true that $4\mid(5^n-1)$ for all $n$.  
(3) Let $k>1$ be the smallest integer for which $4\mid(5^k-1)$.  
(4) Then $4\mid(5^{k-1}-1)$, so there is an integer $a$ for which $5^{k-1}=4a$. Then
$$
\begin{aligned}
5^{k-1}&=4a\\
5(5^{k-1}-1)&=5\cdot4a\\
5^k-5&=20a\\
5^k-1&=20a+4\\
5^k-1&=4(5a+1)
\end{aligned}
$$
This means that $4\mid(5^k-1)$, a contradiction, because $4\nmid(5^k-1)$ in Step 3.  
Thus, we were wrong in Step 2 to assume that it is untrue that $4\mid(5^n-1)$ for every $n$.  
Therefore, $4\mid(5^n-1)$ is true for every $n. \blacksquare$  

---
# 10.4 The Fundamental Theorem of Arithmetic
The **fundamental theorem of arithmetic** states that any integer greater than 1 has a unique prime factorization.

---
**Theorem 10.1** (Fundamental Theorem of Arithmetic) Any integer $n>1$ has a unique prime factorization. "Unique" means that if $n=p_1\cdot p_2\cdot p_3\dots p_k$ and $n=a_1\cdot a_2\cdot a_3\dots a_\ell$ are two prime factorizations of $n$, then $k=\ell$, and the primes $p_i$ and $a_i$ are the same, except that they may be in different orders.  

*Proof*. Suppose $n>1$. We first use strong induction to show that $n$ has a prime factorization. For the basis step, if $n=2$ it is a prime, so it is already it's own prime factorization. Let $n\ge2$ assume every integer between 2 and $n$ (inclusive) has a prime factorization. Consider $n+1$. If it is prime, then it is its own prime factorization. If it is not prime, then it factors as $n+1=ab$ with $a,b>1$. Because $a$ and $b$ are both less than $n+1$ they have prime factorizations $a=p_1\cdot p_2\cdot p_3\dots p_k$ and $b=p'_1\cdot p'_2\cdot p'_3\dots p'_\ell$. Then $$n+1=ab=(p_1\cdot p_2\cdot p_3\dots p_k)(p'_1\cdot p'_2\cdot p'_3\dots p'_\ell)$$ is a prime factorization of $n+1$. This completes the proof by strong induction because every integer greater than $1$ has a prime factorization.  

Next, we use proof by smallest counterexample to prove that the prime factorization of any $n\ge2$ is unique. If $n=2$, then $n$ clearly has only one prime factorization, namely itself. Assume for the sake of contradiction that there is an $n>2$ that has different prime factorizations $n=p_1\cdot p_2\cdot p_3\dots p_k$ and $n=a_1\cdot a_2\cdot a_3\dots a_\ell$. Assume $n$ is the smallest number with this property. From $n=p_1\cdot p_2\cdot p_3\dots p_k$ we see that $p_1\mid n$, so $p_1\mid(a_1\cdot a_2\cdot a_3\dots a_\ell)$. By Proposition 10.1, $p_1$ divides one of the primes $a_i$. As $a_i$ is prime, we have $p_1=a_i$. Dividing $n=p_1\cdot p_2\cdot p_3\dots p_k=a_1\cdot a_2\cdot a_3\dots a_\ell$ by $p_1=a_i$ yields $$p_2\cdot p_3\cdots p_k=a_1\cdot a_2\cdot a_3\dots a_{i-1}\cdot a_{i+1}\dots a_\ell.$$ These two factorizations are different, because the two prime factorizations of $n$ were different. But also the above number $p_2\cdot p_3\dots p_k$ is smaller than $n$, and this contradicts the fact that $n$ was the smallest number with two different prime factorizations. $\blacksquare$  

---
# 10.5 Fibonacci Numbers
The Fibonacci Sequence is determined by the rules $F_1=1, F_2=1, F_n=F_{n-1}+F_{n-2}$, and make a great set up for proofs by induction.  

---
# Exercises for Chapter 10
