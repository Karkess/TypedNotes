---
title: Book of Proofs - Ch. 5

---

# 5.1 Contrapositive Proof

**Proposition** If $P$, then $Q$.  
If we want to take this into contrapositive form, instead of  
$$P\implies Q$$
We write  
$$\neg P\implies\neg Q$$

These two statements are logically equivalent.  

---
**Outline for Contrapositive Proof**  

**Proposition** If $P$, then $Q$.  
*Proof*. Suppose $\neg Q$.  
$\,\,\,\,\,\,\,\vdots$  
Therefore $\neg P$.  

---

**Examples**  

---
**Proposition** Suppose $x\in\mathbb{Z}$. If $7x+9$ is even, then $x$ is odd.  

*Proof*. (Direct) Suppose $7x+9$ is even.  
Thus $7x+9=2a$ for some integer $a$.  
Subtracting $6x+9$ from both sides, we get $x=2-6x-9$.  
Thus $x=2a-6x-9=2a-6x-10+1=2(a-3x-5)+1$.  
Consequently $x=2b+1$, where $b=a-3x-5\in\mathbb{Z}$.  
Therefore $x$ is odd.  

*Proof*. (Contrapositive) Suppose $x$ is not odd.  
Thus $x$ is even, so $x=2a$ for some integer $a$  
Then $7x+9=2b+1$, where $b$ is the integer $7a+4$.  
Consequently $7x+9$ is odd.  
Therefore $7x+9$ is not even.  

---
**Proposition** Suppose $x\in\mathbb{Z}\text{. If }x^2-6x+5$ is even, then $x$ is odd.  

*Proof*. (Direct) A direct proof would be tough, since x would have to be isolated from the quadratic.  

*Proof*. (Contrapositive) Suppose $x$ is not odd.  
Thus $x$ is even, so $x=2a$ for some integer $a$.  
So $x^2+6x+5=(2a)^2-6(2a)+5=4a^2-12a+4+1=2(2a^2-6a+1)+1$.  
Therefore $x^2-6x+5=2b+1$, where $b$ is the integer $2a^2-6a+2$.  
Consequently, $x^2-6x+5$ is odd.  
Therefore $x^2-6x+5$ is not even.  

---

**Proposition** Suppose $x,y\in\mathbb{R}\text{. If }y^3+yx^2\le x^3+xy^2\text{, then }y\le x.$  

*Proof*. (Contrapositive) Suppose it is not true that $y\le x\text{, so }y>x$.  
Then $y-x>0$. Multiply both sides of $y-x>0$ by the positive value $x^2+y^2$. 
$$
\begin{aligned}
(y-x)(x^2+y^2) &> 0(x^2+y^2)\\
yx^2+y^3-x^3-xy^2 &> 0\\
y^3+yx^2 &> x^3+xy^2
\end{aligned}
$$
Therefore $y^3+yx^2>x^3+xy^2$, so it is not true that $y^3+yx^2\le x^3+xy^2$.  

---
**Proposition** Suppose $x,y\in\mathbb{Z}\text{. If }5\nmid xy\text{, then }5\nmid x\text{ and }5\nmid y$.  

*Proof*. (Contrapositive) Suppose it is not true that $5\nmid x$ **and** $5\nmid y$.  
By DeMorgan's law, it is not true that $5\nmid x$ **or** it is not true that $5\nmid y$.  
Therefore $5\mid x\text{ or }5\mid y$. We consider these possibilities separately.  
**Case 1** Suppose $5\mid x$. Then $x=5a$ for some $a\in\mathbb{Z}$.  
From this we get that $xy=(5a)y=5(ay)$, and that means $5\mid xy$.  
**Case 2** Suppose $5\mid y$. Then $y=5a$ for some $a\in\mathbb{Z}$.  
From this we get $xy=x(5a)=5(xa)$, and that means $5\mid xy$.  
The above cases show that $5\mid xy$, so it is not true that $5\nmid xy$.  

--- 
# 5.2 Congruence of Integers

**Definition 5.1** Given integers $a$ and $b$ and $n\in\mathbb{N}$, we say that $a$ and $b$ are **congruent modulo n** if $n\mid(a-b)$. We express this as $a\equiv b\pmod{n}$. If $a$ and $b$ are not congruent modulo $n$, we write this as $a\not\equiv b\pmod{n}$. 

---
**Proposition** Let $a,b\in\mathbb{Z}\text{ and }n\in\mathbb{N}\text{. If }a\equiv b\pmod{n}\text{, then }a^2\equiv b^2\pmod{n}$.  

*Proof*. We will use a direct proof. Suppose $a\equiv b\pmod{n}$.  
By definition of congruence of integers, this means $n\mid(a-b)$.  
Then by definition of divisibility, there is an integer $c$ for which $a-b=nc$.  
Now multiply both sides of this equation by $a+b$.  
$$
\begin{aligned}
a-b &= nc\\
(a-b)(a+b) &= nc(a+b)\\
a^2-b^2 &= nc(a+b)
\end{aligned}
$$
Since $c(a+b)\in\mathbb{Z}$, the above equations tells us $n\mid(a^2-b^2)$.  
According to Definition 5.1, this gives us $a^2\equiv b^2\pmod{n}$.  

---
**Proposition** Let $a,b,c\in\mathbb{Z}\text{ and }n\in\mathbb{N}\text{. If }a\equiv b\pmod{n}\text{, then}ac\equiv bc\pmod{n}$.  

*Proof*. We employ direct proof. Suppose $a\equiv b\pmod{n}$. By definition 5.1, it follows that $n\mid(a-b)$. Therefore, by definition of divisibility, there exists an integer $k$ for which $a-b=nk$. Multiply both sides of this equation by $c$ to get $ac-bc=n(kc)\text{ where }kc\in\mathbb{Z}$, which means $n\mid(ac-bc).$  
By Definition 5.1, we have $ac\equiv bc\pmod{n}$.  

---

**Proposition** Suppose $a,b \in\mathbb{Z}\text{ and }n\in\mathbb{N}$. If $12a\not\equiv 12b\pmod{n}\text{, then }n\nmid12$.  

*Proof*. (Contrapositive) Suppose $n\mid12$. Then $12=nc$ for some $c\in\mathbb{Z}$. Thus $$12(a-b)=nc(a-b)$$ From this, $12a-12b=n(ca-cb)$. Because $ca-cb\in\mathbb{Z}$, we get $n\mid(12a-12b)$. This in turn means $12a\equiv12b\pmod{n}$.  

---
# 5.3 Mathematical Writing

1. Begin each sentence with a word, not a mathematical symbol.
2. End each sentence with a period.
3. Separate mathematical symbols and expressions with words
4. Avoid misuse of symbols.
5. Avoid using unnecessary symbols.
6. Use the first person plural.
7. Use the active voice.
8. Explain each new symbol. 
9. Watch out for "it."
10. Since, because, as, for, so.
11. Thus, hence, therefore, consequently.
12. Clarity is the gold standard of mathematical writing.

---
# Exercises
To-do: 1 3 4 9 11 18 21 22 24

---
**1.** Suppose $n\in\mathbb{Z}$. If $n^2$ is even, then $n$ is even.  

*Proof*. (Contrapositive) Suppose $n^2$ is not even.  
Thus $n$ is odd, so $n=2a+1$ for some integer $a$.  
Then $n^2=(2a+1)^2=4a^2+4a+1=2(2a^2+2a)+1$  
Therefore, $n^2=2b+1$, where $b$ is the integer $2a^2+2a$.  
Consequently $n^2$ is odd.  
Hence, by contrapositive, if $n^2$ is even then $n$ is even.


---
**3.** Suppose $a,b\in\mathbb{Z}$. If $a^2(b^2-2b)$ is odd, then $a$ and $b$ are odd.  

*Proof*. (Contrapositive) Suppose $a$ and $b$ are not odd.  
Thus $a$ and $b$ are even, so $a=2c$ and $b=2d$ for some integers $c$ and $d$.  
So
$$
\begin{aligned}
a^2(b^2-2b)&=(2c)^2((2d^2)-2(2d))\\
&=4c^2(4d^2-4d)\\
&=2(c^2(2d^2-2d))
\end{aligned}
$$
Therefore $a^2(b^2-2b)=2x$, where $x$ is the integer $c^2(2d^2-2d)$.  
Consequently, $a^2(b^2-2b)$ is even.  
Hency, by contrapositive, if $a^2(b^2-2b)$ is odd, then $a$ and $b$ are odd. 

---
**4.** Suppose $a,b,c\in\mathbb{Z}$. If $a$ does not divide $bc$, then $a$ does not divide $b$.  

*Proof*. (Contrapositive) Suppose $a\mid b$.  
Then, $b=ad$ for some $d\in\mathbb{Z}$.  
Taking $b\mid bc$ we see that $bc=be$ with $e\in\mathbb{Z}$.  
Substituting $b=ad$ in the divisor we arrive at $bc=ade$. Setting $de=x$ we see that $a\mid bc$ by definition 4.4.  
Therefore $a\mid bc$.  
Hence, by contrapositive, if $a\nmid bc$, then $a\nmid b$. 

---
**9.** Suppose $n\in\mathbb{Z}\text{. If }3\nmid n^2\text{, then }3\nmid n$.  

*Proof*. (Contrapositive) Suppose $3\mid n$.  
Then $n=3a$, where $a\in\mathbb{Z}$.  
Squaring both sides gives $n^2=9a^2$  
Taking $x=3a^2\in\mathbb{Z}$ we get $n^2=3x$.  
Therefore, $3\mid n^2$.  
Hence, by contrapositive, if $3\nmid n^2\text{, then }3\nmid n$. 

---
**11.** Suppose $x,y\in\mathbb{Z}$. If $x^2(y+3)$ is even, then $x$ is even or $y$ is odd.  

*Proof*. (Contrapositive) Suppose $x$ is odd or $y$ is even.  
If $x$ is odd, then $x=2a+1\text{, where }a\in\mathbb{Z}$.  
If $y$ is even, then $y=2b\text{, where }b\in\mathbb{Z}.$
This results in  

$$
\begin{aligned}
x^2(y+3)&=(2a+1)^2((2b)+3)\\
&=(4a^2+4a+1)(2b+3)\\
&=8a^2b+8ab+2b+12a^2+12a+3\\
&=2(4a^2b+4ab+b+6a^2+6a+1)+1\\
&=2c+1
\end{aligned}
$$

Where $c=4a^2b+4ab+b+6a^2+6a+1\in\mathbb{Z}$. 
Therefore, $x^2(y+3)$ is odd when $x$ is odd and $y$ is even.  
Hence, by contrapositive and DeMorgan's Law $x^2(y+3)$ is even when $x$ is odd or $y$ is even.


---
**18.** If $a,b\in\mathbb{Z}$, then $(a+b)^3\equiv a^3+b^3\pmod{3}$.  

*Proof.* (Direct) Taking $(a+b)^3\equiv a^3+b^3\pmod{3}$ to give the relationship $3\mid((a+b)^3-a^3-b^3)$ if $(a+b)^3-a^3-b^3=3n, n\in\mathbb{Z}$.  
$$
\begin{aligned}
3n&=(a+b)^3-a^3-b^3\\
&=a^3+3a^2b+3ab^2+b^3-a^3-b^3\\
&=3a^2b+3ab^2\\
3n&=3a^2b+3ab^2\\
n&=a^2b+ab^2
\end{aligned}
$$
Since $n\in\mathbb{Z}$ the above equation tells us that $(a+b)^3\equiv a^3+b^3\pmod{3}$.  

---
**21.** Let $a,b\in\mathbb{Z}\text{ and }n\in\mathbb{N}$. If $a\equiv b\pmod{n}$,then $a^3\equiv b^3\pmod{n}$.  

*Proof*. (Direct) Let $a\equiv b\pmod{n}$.  
By definition, $a-b=nc, c\in\mathbb{Z}$  
$$
\begin{aligned}
a-b&=nc\\
(a-b)(a+b)&=nc(a+b)\\
(a^2-b^2)&=nc(a+b)\\
(a^2-b^2)(a+b)&=nc(a+b)^2\\
(a^3-b^3)&=nc(a+b)^2
\end{aligned}
$$
Since $c(a+b)^2\in\mathbb{Z}$, the above equation tells us that $n\mid(a^3-b^3)$.  
According to Definition 5.1, this gives us $a^3\equiv b^3\pmod{n}$.  

---
**22.** Let $a\in\mathbb{Z}\text{, }n\in\mathbb{N}$. If $a$ has a remainder $r$ when divided by $n$, then $a\equiv r\pmod{n}$.  

*Proof*. (Direct) Let $a\in\mathbb{Z}\text{, }n\in\mathbb{N}$  
Then $a\equiv r\pmod{n}=n\mid(r-a)$  
By Definition 4.4 $n\mid(r-a)\rightarrow r-a=cn$  
Adding r to both sides we arrive at $a=cn+r$.  
By Definition 4.4 $n\mid a\rightarrow a=cn$  
Adding a remainder that is not divided results in $a=cn+r$.  
We can see that this is equivalent to the definition of $a\equiv r\pmod{n}$  

Kind of sloppy from trying to avoid just using the division algorithm. Correct path is simply invoking the divison algorithm and then just deriving $a\equiv r\pmod{n}=n\mid(r-a)$ in like one step. 

*Proof*. (Direct) Let $a$ has a remainder $r$ when divided by $n$, so $a=nc+r$.  
Subtracting $r$ from both sides we arrive at $a-r=nc$.
By Definition 4.4, this is $a\equiv r\pmod{n}$. 

---
**24.** If $a\equiv b\pmod{n}$ and $c\equiv d\pmod{n}$, then $ac\equiv bd\pmod{n}$.  

Cut for brevity. Straightforward.

---