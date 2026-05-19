---
title: Chapter 1

---

# 1. Introduction

## 1.1 Graphs
A **graph** $G$ is a finite nonempty set $V$ of objects called **vertices** together with a possibly empty set $E$ of 2-element subsets of $V$ called **edges**. 

Vertices are sometimes referred to as **points** or **nodes**, while edges are sometimes called **lines** or **links**. 

If $uv$ is an edge of $G$, then $u$ and $v$ are **adjacent vertices**. Two adjacent vertices are referred to as **neighbors** of each other. The set of neighbors of a vertex $v$ is called the **open neighborhood** of $v$ (or simply the **neighborhood** of $v$) and is denoted by $N_G(v)$, or $N(v)$ if the graph $G$ is understood. 

The number of vertices is the **order** of $G$.
The number of edges is the **size** of $G$.
A graph of order 1 is called a **trivial graph**. 
A graph of size 0 is called an **empty graph**. 
A graph with every two distinct vertices adjacent is called a **complete graph**. 

A complete graph of order $n$ is denoted by $K_n$ has size $\binom{n}{2}=\frac{n(n-1)}{2}$.

A **path** is denoted $P_n$ and is a graph of order $n$ with size $n-1$ whose vertices can be labeled $v_1,v_2,\dots,v_n$ and whose edges are $v_iv_{i+1}$ for $i=1,2,\dots,n-1$. 

For a graph of size and order $n$ that is cyclically connected we call it a **cycle** $C_n$. 

## 1.2 The Degree of a Vertex

The **degree of a vertex** $v$ is the number of vertices that are adjacent to $v$. This is also it's neighborhood $N(v)$. 

A vertex of degree $0$ is referred to as an **isolated vertex** and a vertex of degree $1$ is an **end-vertex** or **leaf**. 

An edge incident with an end-vertex is called a **pendant edge**. The largest degree among the vertices of $G$ is called the **maximum degree** of $G$ and is denoted by $\Delta(G)$. The smallest degree is called **minimum degree** of $G$ and is denoted by $\delta(G)$

---
**The First Theorem of Graph Theory:**  
**Theorem 1.4 (The First Theorem of Graph Theory)** *If $G$ is a graph of size $m$, then* $$\sum_{v\in V(G)}\mathrm{deg}\,v=2m.$$
**Proof.** When summing the degrees of the vertices of $G$, each edge of $G$ is counted twice, once for each of its two incident vertices.

---
**Even and Odd Vertices**
A vertex of a graph is **even** or **odd**, according to whether its degree in $G$ is even or odd. 

**Corollary 1.5** *Every graph has an even number of odd vertices.*

## 1.3 Isomorphic Graphs
Two graphs $G$ and $H$ are **isomorphic** if there exists a bijective function $\phi:V(G)\rightarrow V(H)$ such that two vertices $u$ and $v$ are adjacent in $G$ if and only if $\phi(u)$ and $\phi(v)$ are adjacent in $H$. 
The function $\phi$ is called an **isomorphism** from $G$ to $H$. If $\phi:V(G)\rightarrow V(H)$ is an isomorphism, then the inverse function $\phi^{-1}:V(H)\rightarrow V(G)$ is an isomorphism from $H$ to $G$. 
If $G$ and $H$ are isomorphic, then we write $G\cong H$ If there is no such function $\phi$ as described above, then $G$ and $H$ are **non-isomorphic graphs** and we write $G\not\cong H$. 

---
**Theorem 1.6** *If two graphs $G$ and $H$ are isomorphic, then they have the same order and the same size, and degrees of the vertices of $G$ are the same as the degrees of the vertices of $H$.*

The inverse of this is not necessarily true. Just because two graphs have the same order, same size, and same degrees of vertices, does not mean they are isomorphic. 

---
**Subgraphs**
A graph $H$ is a **subgraph** of a graph $G$ if $V(H)\subseteq V(G)$ and $E(H)\subseteq E(G)$, we write $H\subseteq G$. 
If $H$ is a subgraph of $G$, then $G$ is a **supergraph** of $H$. 
If $V(H)=V(G)$, then $H$ is a **spanning subgraph** of $G$. 
If $H$ is a subgraph of $G$ where $H\not\cong G$, then $H$ is a **proper subgraph** of $G$. 

---
**Induced Subgraphs**
For a nonempty subset $S$ of $V(G)$, the **subgraph** $G[S]$ of $G$ **induced by** $S$ has $S$ as its vertex set and two vertices $u$ and $v$ are adjacent in $G[S]$ if and only if $u$ and $v$ are adjacent in $G$. 

A subgraph $H$ of a graph $G$ is called an **induced subgraph** if there is a nonempty subset $S$ of $V(G)$ such that $H=G[S]$. Thus $G[V(G)]=G$. 

Another way to define this is that induced subgraphs have all of the edges of the original graph for the vertices chosen. 

## 1.4 Regular Graphs
A graph $G$ is **regular** if the vertices of $G$ have the same degree and is **regular of degree** $r$ if this degree is $r$. Such graphs are called $r$**-regular**. 

**Theorem 1.7** *For integers $r$ and $n$, there exists an $r$-regular graph of order $n$ if and only if $\,0\le r\le n-1$ and $r$ and $n$ are not both odd.*

---
**The Petersen Graph**
A 3-regular graph is also called a **cubic graph**. 
One of the best known cubic graphs is the **Petersen graph**, shown below.
![image](https://hackmd.io/_uploads/rklKVAnMbx.png)

## 1.5 Bipartite Graphs
A graph $G$ is **bipartite** if $V(G)$ can be partitioned into two sets $U$ and $W$ (called **partite sets**) so that every edge of $G$ joins with a vertex of $U$ and a vertex $W$. 

A graph $G$ is a **complete bipartite graph** if $V(G)$ can be partitioned into two sets $U$ and $W$ (called **partite sets** again) so that $uw$ is an edge of $G$ if and only if $u\in U$ and $w\in W$. If $\lvert U\rvert=s$ and $\lvert W\rvert=t$, then this complete bipartite graph has order $s+t$. 

The complete bipartite graph $K_{1,t}$ is called a **star**. The star $K_{1,3}$ is sometimes referred to as a **claw**. 

---
**Theorem 1.8** *The size of every bipartite graph of order $n$ is at most $\lfloor n^2/4\rfloor$.* 

**Theorem 1.9** *Every graph of order $n\ge3$ and size $m>\lfloor n^2/4\rfloor$ contains a triangle.*

---
**Complete Multipartite Graphs**
If a graph can be partitioned into $k$ subsets, it is called a $k$**-partite graph**. 

A **complete $k$-partite graph $G$** is a $k$-partite graph with the property that two vertices are adjacent in $G$ if and only if the vertices belong to different partite sets. 

## 1.6 Operations on Graphs
**The Complement of a Graph**

The **complement** $\overline{G}$ of a graph $G$ is that graph with vertex set $V(G)$ such that two vertices are adjacent in $\overline{G}$ if and only if these vertices are not adjacent in $G$. 

Any isomorphism from graph $G$ to a graph $H$ is also an isomorphism from $\overline{G}$ to $\overline{H}$. Consequently, $\overline{G}\cong\overline{H}$ if and only if $G\cong H$. 

If $G$ is a graph of order $n$ and size $m$, then $\overline{G}$ is a graph of order $n$ and size $n\choose 2$$-m$. 

A graph $G$ is **self-complementary** if $G$ is isomorphic to $\overline{G}$. 

---
**The Union and Join of Graphs**
The **union** $G=G_1+G_2$ of $G_1$ and $G_2$ has vertex set $V(G)=V(G_1)\cup V(G_2)$.

The **join** $G=G_1\vee G_2$ of $G_1$ and $G_2$ has a vertex set $V(G)=V(G_1)\cup V(G_2)$ and edge set $$E(G)=E(G_1)\cup E(G_2)\cup\{uv:u\in V(G_1),v\in V(G_2)\}.$$ With the join operation, we see that $\overline{K_s}\vee\overline{K_t}=K_{s,t}$. 

---
**The Cartesian Product of Graphs**
The **Cartesian Product** $G$ of two graphs $G_1$ and $G_2$, commonly denoted by $G_1\,\square\,G_2$ or $G_1\times G_2$, has the vertex set $$V(G)=V(G_1)\times V(G_2),$$ where two distinct vertices $(u,v)$ and $(x,y)$ of $G_1\,\square\,G_2$ are adjacent if either $$(1)\:u=x\text{ and }vy\in E(G_2)\text{  or  }(2)\:v=y\text{ and }ux\in E(G_1).$$

---
**Hypercubes**

The $n$**-cube** $Q_n$ is $K_2$ if $n=1$, while for $n\ge 2$, while for $n\ge2, Q_n$ is defined recursively as the Cartesian product $Q_{n-1}\,\square\,K_2$ of $Q_{n-1}$ and $K_2$.

## 1.7 Degree Sequences
A sequence $d_1,d_2,\dots,d_n$ of nonnegative integers is called a **degree sequence** of a graph $G$ of order $n$ if the vertices of $G$ can be labeled $v_1,v_2,\dots,v_n$ so that $\mathrm{deg}\,v_i=d_i$ for $1\le i\le n$. 

A finite sequence $s$ of nonnegative integers is a **graphical sequence** if $s$ is a degree sequence of some graph. Thus, 4,3,2,2,1 is graphical. 

---
**2-Switches**
Let $H$ be a graph containing four distinct vertices $u,v,w,$ and $x$ such that $uv,wx\in E(H)$ and $uw,vx\not\in E(H)$. The process of deleting edges $uv$ and $wx$ from $H$ and adding $uw$ and $vx$ to $H$ is referred to as a **2-switch**. 

**Theorem 1.11** *If $G$ and $H$ are two graphs with the same degree sequence, then $H$ can be transformed into $G$ by a (possibly empty) sequence of $2$-switches.*


---
**The Havel-Hakimi Theorem**
*A sequence $s: d_1,d_2,\dots,d_n$ of nonnegative integers with $\Delta=d_1\ge d_2\ge\dots\ge d_n$ and $\Delta\ge1$ is graphical if and only if the sequence $$s_1:d_2-1,d_3-1,\dots,d_{\Delta+1}-1,d_{\Delta+2},\dots,d_n$$ is graphical.*

---
**The Erdos-Gallai Theorem**
*A sequence $s:d_1,d_2,\dots,d_n\:(n\ge2)$ of nonnegative integers with $d_1\ge d_2\ge\dots,d_n$ is graphical if and only if $\sum^n_{i=1}d_i$ is even and for each integer $k$ with $1\le k\le n-1$*, $$\sum^k_{i=1}d_i\le k(k-1)+\sum^n_{i=k+1}\mathrm{min}\{k,d_i\}$$.

---
**Irregular Graphs**  
A nontrivial graph $G$ is **irregular** if $\mathrm{deg}\,u\neq\mathrm{deg}\,v$ for every two vertices $u$ and $v$ of $G$. 

**Theorem 1.14** *No graph is irregular*.


A graph of order $n\ge2$ is **nearly irregular** if exactly two vertices of $G$ have the same degree.

**Theorem 1.15** *For every integer $n\ge2$, there are exactly two nearly irregular graphs of order $n$.*

## 1.8 Multigraphs
A **multigraph** is a nonempty set of vertices, every two of which are joined by a finite number of edges. Hence a multigraph $H$ may be expressed as $H=(V,E)$, where $E$ is a multiset of 2-element subsets of $V$. 

Two or more edges that join the same pair of distinct vertices are called **parallel edges**. 

An edge joining a vertex to itself is called a **loop**.

Structures that permit both parallel edges and loops are sometimes called **pseudographs**.

---
**Theorem 1.16** *For every connected graph $G$ of order at least 3, there exists an irregular multigraph whose underlying graph is $G$.*

## Exercises 
3. A graph $G$ of order $26$ and size $58$ has $5$ vertices of degree $4$, $6$ vertices of degree $5$, and $7$ vertices of degree 6. The remaining vertices of $G$ all have the same degree. What is this degree?

$5*4+6*5+7*6=92$ edges in $18$ vertices. 
$\frac{92}{18}=5+\frac{8}{18}$, so there are at least 2 unconnected edges in this defined bunch.
Total degree sum is $2\lvert E\rvert=2(58)=116$. Subtracting the $92$ gives $116-92=24$. We have 8 unknown vertices, so we have $8v=24,\rightarrow v=3$. The remaining vertices have degree 3. 

---
7. (a) Determine whether $G_1\cong G_2$. - Yes
   (b) Determine whether $H_1\cong H_2$. - No
   
---
11. Show that if $G$ is a nonregular graph of order $n$ and size $rn/2$, for some integer $r$ with $1\le r\le n-2$, then $\Delta(G)-\delta(g)\ge2$. 

Order $n$ means $n$ vertices. Size $rn/2$ means $rn/2$ edges. Nonregular means not every vertex has the same number of degrees. $\Delta(G)$ is the vertex with the highest degree. $\delta(G)$ is the vertex with the lowest degree. 

---
19. A bipartite graph $G$ of order $n$ has partite sets $U$ and $W$ where $\lvert U\rvert=10.$ Every vertex of $U$ has degree $6$. In $W$, there are four vertices of degree $2$ and three vertices of degree $4$. All other vertices of $G$ have degree $8$. What is $n$?

Max is $\lfloor n^2/4\rfloor$. 
U has 10 vertices of degree 6
So W has 60 total degrees as well
$$
\begin{aligned}
60-4*2-3*4&=8x\\
60-8-12&=8x\\
40&=8x\\
5&=x
\end{aligned}
$$
Now we add all the vertices: $\lvert U\rvert+\lvert W\rvert=10+\lvert W\rvert.$
$\lvert W\rvert = 4+3+5=12$
$n=\lvert U\rvert +\lvert W\rvert=10+12=22$.

---
