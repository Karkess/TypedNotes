---
title: Book of Proof - Ch. 8

---

# Chapter 8 - Proofs Involving Sets

Set definitions:
$$
\begin{aligned}
A\times B&=\{(x,y):x\in A,y\in B\},\\
A\cup B &=\{x:(x\in A)\lor(x\in B)\},\\
A\cap B &=\{x:(x\in A)\land(x\in B)\}\\
A\setminus B &=\{x:(x\in A)\land(x\notin B)\}\\
\overline{A} &= U\setminus A\\
\mathcal{P}(A) &=\{X:X\subseteq A\}
\end{aligned}
$$

---
# 8.1 How to Prove $a\in A$

**How to Show $a\in\{x:P(x)\}$**  
Show that $P(a)$ is true.  

**How to show that $a\in\{x\in S:P(x)\}$**  
1. Verify that $a\in S$.  
2. Show that $P(a)$ is true.  

---
**Example 8.1** Let's investigate elements of $A=\{x:x\in\mathbb{N}\text{ and }7\mid x\}$. This set has the form $A=\{x:P(x)\}$ where $P(x)$ is the open sentence $(x\in\mathbb{N})\land(7\mid x)$. Thus $21\in A$ because $P(21)$ is true. Similarly, 7,14,28,35, etc., are all elements of $A$. But $8\notin A$ because $P(8)$ is false.  

---
# 8.2 How to Prove $A\subseteq B$

**Direct Approach**  
*Proof*. Suppose $a\in A$.  
$\,\,\,\,\,\,\,\,\,\,\,\vdots$  
Therefore $a\in B$.  
Thus $a\in A$ implies $a\in B$,  
so it follows that $A\subseteq B. \blacksquare$

---
**Contrapositive Approach**  
*Proof*. Suppose $a\notin B$.  
$\,\,\,\,\,\,\,\,\,\,\,\vdots$  
Therefore $a\notin A$.  
Thus $a\notin B$ implies $a\notin A$,
so it follows that $A\subseteq B. \blacksquare$

---
**Example 8.5** Prove that $\{x\in\mathbb{Z}:18\mid x\}\subseteq\{x\in\mathbb{Z}:6\mid x\}$  

*Proof*. Suppose that $a\in\{x\in\mathbb{Z}:18\mid x\}$.  
This means that $a\in\mathbb{Z}$ and $18\mid x$.  
By definition of divisibility, there is an integer $c$ for which $a=18c$.  
Consequently, $a=6(3c)$, and from this we deduce that $6\mid a$.  
Therefore $a$ is one of the integers that $6$ divides, so $a\in\{x\in\mathbb{Z}:6\mid x\}$.  
We've shown that $a\in\{x\in\mathbb{Z}:18\mid x\}$ implies that $a\in\{x\in\mathbb{Z}:6\mid x\}$, so it follows that $\{x\in\mathbb{Z}:18\mid x\}\subseteq\{x\in\mathbb{Z}:6\mid x\}$. 

---
# 8.3 How to Prove A=B

*Proof*.  
Prove that $A\subseteq B$  
Prove that $B\subseteq A$  

Therefore, since $A\subseteq B$ and $B\subseteq A$,  
it follows that $A=B.\blacksquare$  

---

# 8.4 Examples: Perfect Numbers

**Definition 8.1** A number $p\in\mathbb{N}$ is *perfect* if it equals the sum of its positive divisors less than itself. Some examples:  
- The number 6 is perfect since $6=1+2+3$  
- The number 28 is perfect since $28=1+2+4+7+14$  
- The number 496 is perfect since $496=1+2+4+8+16+31+62+124+248$.  

---
# Exercises for Chapter 8

1 6 8 10 12 25 31

---
**1.** Prove that $\{12n:n\in\mathbb{Z}\}\subseteq\{2n:n\in\mathbb{Z}\}\cap\{3n:n\in\mathbb{Z}\}$.  

Suppose that $a\in\{2n:n\in\mathbb{Z}\}\cap\{3n:n\in\mathbb{Z}\}$  
By definition of intersection, we know this means $a\in\{x\in\mathbb{Z}\:3n\}$ and $a\in\{x\in\mathbb{Z}\:2n\}$.  
Thus we know $a$ is a product of both $2n$ and $3n$. Let us say $a$ is a product of $2c$, where $c\in\mathbb{Z}$. Plugging this into $3n$ we see that $a\in3(2c)\implies a\in6c$.  
Now looking at $12n$ we see it can be expressed $6(2n)$, thus $\{12n:n\in\mathbb{Z}\}\subseteq\{2n:n\in\mathbb{Z}\}\cap\{3n:n\in\mathbb{Z}\}. \blacksquare$

**Note** Direction of proof reversed. That was a dumb mistake. Start by assuming $a\in\{12n:n\in\mathbb{Z}\}$ and then show basically the same thing as above. 


---
**6.** Suppose $A,B$, and $C$ are sets. Prove that if $A\subseteq B$, then $A\setminus C\subseteq B\setminus C$.  

*Proof*. (Direct) Suppose $A\subseteq B$.  
Let $x\in A\setminus C$.  
By definition of set difference we have $x\in A$ and $x\notin C$.  
Since $A\subseteq B$, we have $x\in B$.  
Hence $x\in B$ and $x\notin C$, so $x\in B\setminus C$.  
Therefore, every element of $A\setminus C$ is an element of $B\setminus C$. $A\setminus C\subseteq B\setminus C. \blacksquare$  

I am not great at these set proofs. This took me three attempts. Getting it a bit better now though.  

---
**8.** If $A,B$, and $C$ are sets, then $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$.  

*Proof*. (Direct) Suppose $a$ in $A\cup(B\cap C)$, by the definitions of intersection and union this means that $a\in A \lor (a\in B\land a \in C)$.  
Now suppose $a \in (A\cup B)\cap(A\cup C)$ This means that $(a\in A \lor a\in B)\land(a\in A \lor a\in C)$. By the distributive law in logic we see that this is equivalent to $a\in A \lor (a\in B\land a \in C)$, thus $A\cup(B\cap C)=(A\cup B)\cap(A\cup C). \blacksquare$  

Sike (Psych? Psyche?) this was one of my cleaner proofs I'm a legend at set proofs. (Note: Not a legend at set proofs.)

---
**10.** If $A$ and $B$ are sets in a universal set $U$, then $\overline{A\cap B}=\overline{A}\cup\overline{B}$.  

---
**12.** If $A, B$, and $C$ are sets, then $A\setminus(B\cap C)=(A\setminus B)\cup(A\setminus C)$.  

---
**25.** Suppose $A,B,C$, and $D$ are sets. Prove that $(A\times B)\cup(C\times D)\subseteq(A\cup C)\times(B\cup D)$.  

---
**31.** Suppose $B\neq\varnothing$ and $A\times B\subseteq B\times C$. Prove that $A\subseteq C$.  

---

For time I am skipping the rest of these for now, but 10 and 12 are relatively straightforward. 25 I think I see how to do but I'm not sure if I'd hit a snag, either way it'd be good practice to do a cartesian product problem. 31 is a little less obvious how to approach it as a proof, since I'm not totally positive how to handle the empty set in terms of the notation. Should come back.
