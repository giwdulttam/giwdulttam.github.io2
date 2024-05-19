---
title: 'An Introduction to Moments and Cumulants'
date: 2023-09-20
permalink: /posts/2023/09/An-Introduction-to-Moments-and-Cumulants/
tags:
  - cool posts
  - category1
  - category2
---

### An Introduction to Moments and Cumulants

In statistics and probability, quantitative measures called moments are typically used to shape of a distribution. The most commonly encountered moments are the first and second central moments which are typically referred to as the mean and variance of a distribution. The useful thing about moments is that not only do they describe the shape of a distribution, but they also uniquely determine it. In particular, if two distributions have the same collection of moments, then they are the same distribution. In order to keep track of the list of moments for a distribution, it is convient to "string them up on a clothes line" or display them with the help of a moment generating function. The moment generating function is defined as $M_X(t) = \mathbb{E}[e^{Xt}]$. Now to motivate this definition a bit, recall that the follow is true: $M_X(t) = \mathbb{E}[e^{tX}] = \mathbb{E}[ \sum_{k=0}^{\infty} \frac{(tX)^k}{k!}] = \mathbb{E}[\sum_{k=0}^{\infty} \frac{t^k X^k}{k!}] = \sum_{k=0}^{\infty} \frac{\mathbb{E}[X^k]t^k}{k!}$ and recall that the Taylor series expansion of a function that is infinitely differential at a point $a$ is given by $\sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$ which implies that the moments $m_k = \mathbb{E}[X^k] = f^{(k)}(0)$. This allows us to obtain the moments of a our distribution by differentiating the moment generating function and plugging in zero. 

While moments are an important descriptor of distributions, it turns out that in some situations dealing with the moments of a distribution can be difficult and it is helpful to use a related quantity called cumulants. Similar to moments, the cumulants of a random variable $X$ can also be displayed with the help of a generating function. The cumulant-generating function is defined as the natural logarithm of the moment-generating funciton: $K_X(t) = log\mathbb{E}[e^tX] = \sum_{k = 1}^{\infty}\kappa_n \frac{t^k}{k!}$ From this definition it is clear that there is a close relationship between cumulants and moments. In combinatorics, taking logarithms of power series can turn series that count disconnected structures into power series that count connected structures. It turns out that the generating functions of moments and cumulants can be related and conceptualized through this combinatorial framework. 

Let $m_n$ denote the number of graphs (disconnected graphs are allowed) on a vertex set $[n]$ and $c_n$ denote the number of connected graphs on a vertex set $[n]$. One way to construct a relationship between $m_n$, the total number of graphs, and the $c_n$, the total number of connected graphs, is to find a way to break up the set of all graphs on the vertex set $[n]$ into disjoint subsets and then sum over all these disjoint subsets to obtain the total number of graphs. One way to do this is to consider partitions of the vertex set $[n]$ and for each block in the partition find the total number of connected graphs on the vertices in this block and then multiply the number of connected graphs that can be formed on each block (since constructing connected graphs on each blocks are independent of each other) and then sum over each partition $\pi \in p(n)$. Formally, this counting argument can be represented as: $m_n = \sum_{\pi \in p(n)} \prod_{B \in \pi} c_{\lvert B \rvert}$

A version of this relationship can be used to express the relationship between moments and cumulants: 

$$m_n(X_1,..., X_n) = \sum_{\pi \in p(n)} \prod_{B \in \pi} c_{\lvert B \rvert}(X_i : i \in B)$$

For instance, this tells us that $m_2(X_1, X_2) = c_2(X_1, X_2) + c_1(X_1)c_1(X_2)$. While this relationship between momments and cumulants in terms of partitions is interesting, it might not be entirely clear what exactly are cumulants other than a than a polynomial transformation of moments. First consider the following relations between cumulants and moments: $c(X) = \mathbb{E}(X)$ $c(X_1 X_2) = \mathbb{E}[X_1 X_2] - \mathbb{E}[X_1]\mathbb{E}[X_2]$ which is the definition of covariance of $X_1$ and $X_2$. Also consider the expression of the joint first moment in terms of joint cumulants of four random variables: $\mathbb{E}[X_1 X_2 X_3] = c(X_1 X_2 X_3) + c(X_1 X_2)c(X_3) + c(X_1 X_3)c(X_2) + c(X_2 X_3)c(X_1) + c(X_1)c(X_2)c(X_3)$ Examining these expressions reveals that mixed moments of random variables quantify all interactions of a set of random variables, cumulants quantify the interactions of a set of $n$ random variables that are of n-body type. This fact is seen combinatorially by how cumulants are related to and count the number of connected graphs that can be formed on a vertex set $[n]$ and how moments are related to the total number of graphs on a vertex set $[n]$ which can be expressed a sum over each partition. 

While partitions of $[n]$ were used to relate moments and cumulants, in the next post we will consider what happens when general partitions of $[n]$ are replaced with other types of partitions like non-crossing and monotone partitions and begin to explore the consequences and relations that are generated for moments and cumulants. 












