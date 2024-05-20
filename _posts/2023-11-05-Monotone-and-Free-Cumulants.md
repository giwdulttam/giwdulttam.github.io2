---
title: 'Monotone and Free Cumulants'
date: 2023-11-05
permalink: /posts/2023/11/Monotone-and-Free-Cumulants/
tags:
  -Cumulants
  -Free Cumulants
---

### Monotone and Free Cumulants

In this post, we will continue our discussion of moments and cumulants and begin to explore the interactions that arise between random variables by considering non-crossing and monotone partitions. Recall that the relationship between moments (denoted $m_n$, which corresponded to the total number of graphs on a vertex set $[n]$ and cumulants, (denoted $c_n$, which corresponded to the total number of connected graphs on a vertex set $[n]$) was: 

$$m_n(X_1,...,X_n) = \sum_{\pi \in p(n)} \prod_{B \in \pi} c_{|B|}(X_i : i \in B)$$

where the summation was taken over the partitions of the vertex set $n$. Now we can consider a variation of this relationship where the connected graphs on the vertex set $[n]$ are replaced with geometrically connected graphs on the vertex set $[n]$. If we visualize the vertex set $[n]$ as a circle of vertices, then the geometrically connected graphs are the graphs for which you can move from every vertex in the graph to another by moving along the edges (not all geometrically connected graphs are connected as in geometrically connected graphs you can move between two disconnected components if their edges cross). Now, let us denote the number of geometrically connected graphs by $\kappa_n$. In this case, the partitions that we are summing over represent the different geometrically connected components and it turns out that these are non-crossing partitions. More formally, a partition $\pi$ of a set $[m]$ with blocks $\pi = \{B_1,...,B_r\}$ is said to be non-crossing if one cannot find integers $p_1, q_1, p_2, q_2$ such that $1 \leq p_1 \leq q_1 \leq p_2 \leq q_2 \leq m$, $p_1, p_2$ are in the same block of $\pi$, $q_1, q_2$ are in the same block of $\pi$ and the $p_i's$ are not in the same block of $\pi$ as the $q_i's$. Intuitively, when the vertex set is displayed in a circle, these are the partitions for which the convex polygons corresponding to the blocks of the partition do not cross. We will denote the set of partition of $[n]$ by $\mathcal{P}(n)$ and let $\mathcal{NC}(n)$ be the set of all non-crossing partitions of $[n]$. Using non-crossing partitions, we can write:

$$m_n = \sum_{\pi \in \mathcal{NC}(n)} \prod_{B \in \pi}\kappa_{|B|}$$

Similarily we can write: 

$$m_n = \sum_{\pi \in \mathcal{NC}(n)} \prod_{B \in \pi}\kappa_{|B|}(X_i : i \in B)$$

where here $\kappa_{n}$ are the free cumulants and $m_n$ are the free moments. This alternative expression allows us to associate the moment sequence of a random variable $X$ in a noncommutative probability space an associated free cumulant sequence. Furthermore, similar to how cumulants in the classical setting satisfy the relation that if the random variables $X$ and $Y$ are independent, then $c_n(X + Y) = c_n(X) + c_n(Y)$, we have analogous relationship. We say that if the noncommutative random variables $X$ and $Y$ are freely independent, then $\kappa_n(X + Y) = \kappa_n(X) + \kappa_n(Y)$. This new version of independence in the noncommutative setting gives rise to fascinating analogues of facts that use the independence of random variables in the noncommutative setting. For instance, the central limit theorem in classical probabilty which states that summations of idependent and identically distributed random variables converges in distribution to a Gaussian has an analogue in the free or noncommutative world which states that the summation of idependent and identically distributed noncommutative random variables converge in distribution to the Wigner semicircle distribution. We refer to the interested reader to the post of free central limit theorems for more details. 



Now, we can construct more types of cumulants by consider the summation over different types of partitions. We will now introduce the notion of monotone partitions and monotone cummulants. A monotone partition is defined by a pair $(\pi, \lambda)$ where $\pi \in \mathcal{P}(n)$ and linear ordering $\lambda$ of the blocks of $\pi$. It is useful to use the notation $\pi = \{ V_1 < V_2 < ... < V_l\}$. Then, the set of monotone partitions is defined as follows:

$$\mathcal{M}(n) = \{(\pi, \lambda); \pi \in \mathcal{NC}(n), \text{if } V, W \in \pi \text{and } V \text{is in the inner side of } W, \text{then }, V >_{\lambda} W \}$$


This essentially states that the monotone partitions are the subset of non-crossing partitions that satisfy the property that if a block is contained or surrounded by another block in the partition then it is greater in the linear order on the blocks in the partition. Now for the monotone partitions we have a similar relation between the monotone moments and monotone cumulants: 

$$ m_n = \sum_{(\pi, \lambda) \in \mathcal{M}(n)} \frac{r(\pi)}{\lvert \pi \rvert !} $$

where $r(\pi)$ are the monotone cummulant and $\lvert \pi \rvert$ is the size of the partition. 



















