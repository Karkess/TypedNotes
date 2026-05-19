---
title: Chapter 1

---

# Chapter 1
## 1.1. What Is a Graph?

Graph theory was said to have been born from the Konigsberg Bridge Problem, which can be represented with the following graph: 

![image](https://hackmd.io/_uploads/SJKHsouGbx.png)

**1.1.2. Definition.** A **graph** $G$ is a triple consisting of a **vertex set** $V(G)$, an **edge set** $E(G)$, and a relation that associates with each edge two vertices called its **endpoints**.  

In the above graph, the vertex set is $\{x,y,z,w\}$, and the edge set is $\{b1,b2,b3,b4,b5,b6,b7\}$. The assignments of the endpoints can be read by the picture.

**1.1.4. Definition.** A **loop** is an edge whose endpoints  are equal. **Multiple edges** are edges having the same pair of endpoints. 

A **simple graph** is a graph having no loops or multiple edges. 

**1.1.8. Definition.** The **complement** $\overline{G}$ of a simple graph $G$ is the simple graph with vertex set $V(G)$ defined by $uv\in E(\overline{G})$ if and only if $uv\not\in E(G)$. A **clique** in a graph is a set of pairwise adjacent vertices. An **independent set** (or **stable set**) in a graph is a set of pairwise nonadjacent vertices. 

**1.1.10. Definition.** A graph $G$ is **bipartite** if $V(G)$ is the union of two disjoint (possibly empty) independent sets called **partite sets** of $G$. 

**1.1.12. Definition.** The **chromatic number** of a graph $G$, written $\chi(G)$ is the minimum number of colors needed to label the vertices so that adjacent vertices receive different colors. A graph $G$ is  $k$**-partite** if and only if its chromatic number is at most $k$. 

**1.1.15. Definition.** A **path** is a simple graph whose vertices can be ordered so that two vertices are adjacent if and only if they are consecutive in the list. A **cycle** is a graph with an equal number of vertices and edges whose vertices can be placed around a circle so that two vertices are adjacent if and only if they appear consecutively around the circle. 

**1.1.16. Definition.** A **subgraph** of graph $G$ is a graph $H$ such that $V(H)\subseteq V(G)$ and $E(H)\subseteq E(G)$ and the assignments of endpoints to edges in $H$ is the same as in $G$. We then write $H\subseteq G$ and say that "$G$ **contains** $H$". A graph $G$ is **connected** if each pair of vertices in $G$ belongs to a path; otherwise, $G$ is **disconnected**. 

## Matrices and Isomorphism
**1.1.17. Definition.** Let $G$ be a loopless graph with vertex set $V(G)=\{v_1,\dots,v_n\}$ and the edge set $E(G)=\{e_1,\dots,e_n\}$. The **adjacency matrix** $M(G)$ is the $n$-by-$n$ matrix in which entry $a_{i,j}$ is the number of edges in $G$ with endpoints $\{v_i,v_j\}$. The **incidence matrix** $M(G)$ is the $n$-by-$m$ matrix in which entry $m_{i,j}$ is $1$ if $v_i$ is an endpoint of $e_j$ and otherwise is 0. The **degree** of a vertex $v$ (in a loopless graph) is the number of incident edges. 

**1.1.18. Remark.** An adjacency matrix is determined by a vertex ordering. Every adjacent matrix is **symmetric** $(a_{i,j}=a_{j,i}$ for all $i,j)$.

![image](https://hackmd.io/_uploads/S1lE_HiGWl.png)
<center>Consider the above graph.</center>  

We have an adjacency matrix A(G) and an incidence matrix M(G) as below: 
$$
\left(
\begin{array}{c|ccccc}
& a & b & c & d & e \\ \hline
w & 1 & 1 & 0 & 0 & 0 \\
x & 1 & 0 & 1 & 1 & 0 \\
y & 0 & 1 & 1 & 1 & 1 \\
z & 0 & 0 & 0 & 0 & 0
\end{array}
\right)
$$$$M(G)$$$$
\left(
\begin{array}{c|cccc}
& w & x & y & z \\ \hline
w & 0 & 1 & 1 & 0 \\
x & 1 & 0 & 2 & 0\\
y & 1 & 2 & 0 & 1\\
z & 0 & 0 & 1 & 0
\end{array}
\right)
$$$$A(G)$$
(I don't know how to render labels outside of a matrix in default KaTeX.)

---
**1.1.20. Definition.** An **isomorphism** from a simple graph $G$ to a simple graph $H$ is a bijection $f: V(G)\rightarrow V(H)$ such that $uv\in E(G)$ if and only if $f(u)f(v)\in E(H)$. We say "G is **isomorphic** to H", written $G\overset{\sim}{=}H$, if there is an isomorphism from $G$ to $H$. 

**1.1.22. Remark.** *Finding Isomorphisms*. presenting the adjacency matrices with vertices ordered so that the matrices are identical is one way to prove that two graphs are isomorphic. 

**1.1.24. Proposition.** The isomorphism relation is an equivalence relation on the set of (simple) graphs.  

**1.1.25. Definition.** An **isomorphism class** of graphs is an equivalence class of graphs under the isomorphism relation. 

---
**1.2.27. Definition.** The (unlabeled) path and cycle with $n$ vertices are denoted $P_n$ and $C_n$ respectively; an $n$**-cycle** is a cycle with $n$ vertices. A **complete graph** is a simple graph whose vertices are pairwise adjacent. The complete graph with $n$ vertices is denoted $K_n$. A **complete bipartite graph** or a **biclique** is a simple bipartite graph such that two vertices are adjacent if and only if they are in different partite set. When the sets have different sizes $r$ and $s$, the biclique is denoted $K_{r,s}\,$. 

## Decomposition and Special Graphs

**1.1.32. Definition.** A graph is **self-complementary** if it is isomorphic to its complement. A **decomposition** of a graph is a list of subgraphs such that each edge appears in exactly one subgraph in the list.  

