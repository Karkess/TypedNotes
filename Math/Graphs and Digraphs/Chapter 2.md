---
title: Chapter 2

---

# Chapter 2 - Connected Graphs and Distance
## 2.1 Connected Graphs
**Walks, Trails, and Paths**

For two vertices $u$ and $v$ in a graph $G$, a $u-v$ **walk** $W$ in $G$ is a sequence of vertices in $G$, beginning with $u$ and ending at $v$, such that consecutive vertices in $W$ are adjacent in $G$. Such a walk $W$ in $G$ can be expressed as $$W=(u=v_0,v_1,\dots,v_k=v),$$ where $v_iv_{i+1}\in E(G)\text{ for }0\le i\le k-1.$

The number of edges included in $W$ is the **length** of $W$. 

A walk whose initial and terminal vertices are distinct is an **open walk**; otherwise, it is a **closed walk**.

A walk in graph $G$ where no edge is repeated is called a **trail** in $G$. 

A walk in graph $G$ where no vertex is repeated is called a **path** in $G$. 

---
**Theorem 2.1** *Let $u$ and $v$ be two vertices of a graph $G$. For every $u-v$ walk $W$ in $G$, there exists a $u-v$ path $P$ such that every edge of $P$ belongs to $W$.*

---
**The Adjacency Matrix of a Graph**

Suppose that $G$ is a graph of order $n$, where $V(G)=\{v_1,v_2,\dots,v_n\}$. The **adjacency matrix** of $G$ is the $n\times n$ zero-one matrix $A(G)=[a_{ij}]$, or simply $A=[a_{ij}]$, where $$a_{ij}=\begin{cases}1\quad \text{if }v_iv_j\in E(G)\\0\quad\text{if }v_iv_j\not\in E(G).\end{cases}$$

---
**Theorem 2.2** *Let $G$ be a graph with vertex set $V(G)=\{v_1,v_2,\dots,v_n\}$ and adjacency matrix $A$. For each positive integer $k$, the number of different $v_i-v_j$ walks of length $k$ in $G$ is the $(i,j)$-entry in the matrix $A^k$.*

---
**Circuits and Cycles**

A nontrivial closed walk in a graph $G$ in which no edge is repeated is a **circuit** in $G$. 

A circuit $$C=(v=v_0,v_1,\dots,v_k=v),$$ $k\ge2$, for which the vertices $v_i,\,0\le i\le k-1$, are distinct is a **cycle** in $G$. 

A cycle $C$ of length $k$ is called a $k$**-cycle**. A 3-cycle is referred to as a **triangle**. A cycle of even length is an **even cycle**, and a cycle of odd length is an **odd cycle**. 


The length of the smallest cycle in a graph $G$ (containing cycles) is the **girth** of $G$, denoted by $g(G)$. 

The length of the longest cycle in a graph $G$ (containing cycles) is the **circumference** of $G$, denoted by $c(G)$. 

---
**Connected Graphs**

Two vertices $u$ and $v$ in a graph $G$ are **connected** if $G$ contains a $u-v$ path. 

The graph $G$ itself is **connected** if every two vertices of $G$ are connected.

A connected subgraph $H$ of a graph $G$ is a **component** of $G$ if $H$ is not a proper subgraph of any connected subgraph of $G$. Thus, every component of $G$ is an induced subgraph of $G$. 

The number of components in a graph $G$ is denoted by $k(G)$. Therefore, $G$ is connected if and only if $k(G)=1$. 

---
**Theorem 2.3** *If $G$ is a nontrivial graph of order $n$ such that $\mathrm{deg}\,u+\mathrm{deg}\,v\ge n-1$ for every two nonadjacent vertices $u$ and $v$ of $G$, then $G$ is connected.*

**Corollary 2.4** *If $G$ is a graph of order $n$ with $\delta(G)\ge(n-1)/2$, then $G$ is connected.*

**Theorem 2.5** *If $G$ is a graph of order $n\ge2$ and size $m\ge\binom{n-1}{2}+1$, then $G$ is connected.*

## 2.2 Distance in Graphs

The **distance** $d_G\,(u,v)$ from a vertex $u$ to a vertex $v$ in a connected graph $G$ is the smallest length of a $u-v$ path in $G$. 

A path of length $d(u,v)$ is called a $u-v$ **geodesic**.

The distance $d$ defined above satisfies the following properties in a connected graph $G$:
(1) $d(u,v)\ge0$ for every two vertices $u$ and $v$ of $G$;
(2) $d(u,v)=0$ if and only if $u=v$;
(3) $d(u,v)=d(v,u)$ for all $u,v\in V(G)$ (the **symmetric property**);
(4) $d(u,w)\le d(u,v)+d(v,w)$ for all $u,v,w\in V(G)$ (the **triangle inequality**).

Since $d$ satisfies the four above properties, $d$ is a **metric** on $V(G)$ and $(V(G),d)$ is a **metric space**. 

---
**Theorem 2.6** *A nontrivial graph $G$ is a bipartite graph if and only if $G$ contains no odd cycles.*

---
**The Eccentricity of a Vertex**

The **eccentricity** e(v) of a vertex $v$ in a connected graph $G$ is the distance between $v$ and a vertex farthest from $v$ in $G$. 

The **diameter** $\mathrm{diam}(G)$ of a connected graph $G$ is the largest eccentricity among the vertices of $G$.

The **radius** $\mathrm{rad}(G)$ is the smallest eccentricity among the vertices of $G$. 

A vertex with $e(v)=\mathrm{rad}(G)$ is called a **central vertex** of $G$.

A vertex with $e(v)=\mathrm{diam}(G)$ is called a **peripheral vertex** of $G$. 

Two vertices with $d(u,v)=\mathrm{diam}(G)$ are **antipodal vertices** of $G$. 

---
**Center and Periphery**

The subgraph induced by the central vertices of a connected graph $G$ is the **center** of $G$ and is denoted $\mathrm{Cen}(G)$. 

If every vertex of $G$ is a central vertex, then $\mathrm{Cen}(G)=G$ and $G$ is **self-centered**

The subgraph induced by the peripheral vertices of a connected graph $G$ is the **periphery** of $G$ and is denoted $\mathrm{Per}(G)$.

## Exercises
