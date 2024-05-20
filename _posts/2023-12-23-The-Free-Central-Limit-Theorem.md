---
title: 'The Free Central Limit Theorem'
date: 2023-12-23
permalink: /posts/2023/09/The-Free-Central-Limit-Theorem/
tags:
  -Free Probability
  -Free Central Limit Theory
---

### The Free Central Limit Theorem:


First recall that the classical central limit theorem says that the limiting distribution of the sum of $N$ independent, identically distributed random variables, each with mean $0$, divided by $\sqrt{N}$ is the normal distribution. In this post will we discuss the case in which these random variables are replaced with non-commutative random variables which are freely independent. 

First a non-commutative probability space $(\mathcal{A},\phi)$ consists of a unital algebra $\mathcal{A}$ and a linear function $\phi: \mathcal{A} \rightarrow \mathbb{C}$, such that $\phi(1_{\mathcal{A}}) = 1$. Any element $a \in \mathcal{A}$ is called a free or non-commutative random variable. 

Now recall the classical notion of independence. Let $(\mathcal{B}, \phi)$ be a commutative probability space, and let $b_1, ..., b_n$ in $\mathcal{B}$ be distinct random variables. Then $b_1,...,b_n$ are (classically) independent if $b_i b_j = b_j b_i$ for $1 \leq i, j \leq n$, and $\phi(b_1 b_2 ... b_n) = 0$ whenever $\phi(b_i) = 0$ for $i \leq i \leq n$. Now the definition of free independence for non-commutative random is as follows: Let $(\mathcal{A}, \phi)$ be a non-commutative probability space and let I be a fixed index set. For each $i \in I$, let $\mathcal{A_i} \subset \mathcal{A}$ be a subalgebra. The subalgebras $(\mathcal{A_i}$ are called freely independent if $\phi(a_1 ... a_k) = 0$ whenever we have the following: 1.) $k$ is a positive integer, 2.) $a_j \in \mathcal{A}_{i(j)}$ with $i(j)$ for all $j = 1,2,...,k$, 3.) $\phi(a_j) = 0$ for all $j = 1,2,...,k$, 4.) neighbouring elements from different subalgebras, $i(1) \neq i(2), i(2) \neq i(3), ... , i(k-1) \neq i(k)$. This idea of free independence can be used in mixed moments calculations. 

Just as the sum of independent and identically distributed random variables in classical probability converges to a normal distribution, in free probability sums of freely independent and identically distributed non-commutative random variables will converge to a semicirular distribution. Consider the following definitions:

Let $(\mathcal{A},\phi)$ be a non-commutative probability space and $T \in \mathcal{A}$. We say that $T$ is a standard semicircular random variable if the n-th moment of $T$ is given by: $\phi(T^n) = \frac{1}{2 \pi} \int_{-2}^{2}t^n \sqrt{4 - t^2} dt$.

Before discussing the central limit theorems, we recall the following definition for random variables be identically distributed and the definition for convergence in distirbution:

A collection of random variables $\{ a_i \}$ for $i \in \mathbb{N}$ is called identically distributed if each random variable $a_i$ for $i \in \mathbb{N}$ has the same probability distribution $\{\phi(a_i^n)\}^{\infty}_{n = 0}$. 

Let $(\mathcal{A_k}, \phi_k)$ for $k \in \mathbb{N}$, and $(\mathcal{A}, \phi)$ be non-commutative probability spaces. Then, if $(b_k)$ for $k \in \mathbb{N}$ is a sequence of non-commutative random variables with $b_k \in \mathcal{A_k}$ and let $b \in \mathcal{A}$, then we say that $b_k$ converges in distribution to $b$, denoted by $b_k \rightarrow b$, if $\lim_{k \rightarrow \infty} \phi_k(b_k^n) = \phi(b^n)$ for any fixed $n \in \mathbb{N}$. 

Also, let $I$ be an index set. For each $i \in I$, let $b_k^{(i)} \in \mathcal{A_k}$ for each $k \in \mathbb{N}$ and $b^{(i)} \in \mathcal{A}$. We say that $(b_k^{(i)})$ for $i \in I$ converges in distribution to $(b^{(i)})$ for $i \in I$, denoted by $(b_k^{i}) \rightarrow (b^{(i)})$ for $i \in I$ if $\lim_{k \rightarrow \infty} \phi_k(b_k^{(i_1)} ... b_k^{(i_n)}) = \phi(b_k^{(i_1)} ... b_k^{(i_n)})$ for all $n \in \mathbb{N}$ and all $i_1,...,i_n \in I$. 

Now we would like to look at the convergence in distribution of random variables $(S_k)$ for $k \in \mathbb{N}$ and look at the limit. It then follows that: 

$$\lim_{k \rightarrow \infty} \phi(S_k^n) = \sum_{\pi \in \mathcal{P_2}(n)} \phi(\pi)$$

or in other words the only partitions which contribute to the sum in the $k \rightarrow \infty$ are those with exactly $n/2$ blocks or the partitions each of whose blocks has size $2$ which are called pairings and are denoted by $\mathcal{P_2}(n)$. For the details behind this reasoning, we refer the interested reader to Chapter 2 in Mingo and Speicher's "Free Probability and Random Matrices". We also note that when $n$ is odd then $\mathcal{P_2}(n) = \emptyset$ meaning that the odd limiting moments vanish. In order to determine the evening limiting moments we look at the clasical and free cases separately. 

Starting with the classical case, we have that the random variables commute and factorize with respect to $\phi$. We also denote $\phi(a_i)^2 = \sigma^2$ as the common variance and observe that for any pairing $\pi \in \mathcal{P_2}(n)$ we have that $\phi(\pi) = \sigma^n$. Thus:

$$ \lim_{k \rightarrow \infty} \phi(S_k^n) = \sum_{\pi \in \mathcal{P_2}(n)} \sigma^n = \sigma^n (n-1)(n-3)...(5)(3)(1)$$ 

when $n$ is even and $0$ when $n$ is odd which are the moments for a Gaussian random variable with mean $0$ and variance $\sigma^2$ which proves the central limit theorem in the classical case. 

Now in the free case, we have that our random variables are freely independent and that the only terms that contribute ot the moment calculation are the ones that correspond to non-crossing partitions which here are the non-crossing pairings which we denote by $NC_2(2n)$. Thus it follows that: 

$$\lim_{k \rightarrow \infty} \phi(S_k^{2n}) = \sigma^{2n} \lvert NC_2(2n) \rvert$$

Now we observe that $\lvert NC_2(2n)\rvert = C_n$ of the Catalan numbers. Therefore, it follows that $ \lvert NC_2(2n) \rvert = \frac{1}{n+1} \binom{2n}{n}$. Now consider the following definition:

A self adjoint random variable $s$ with odd moments $\phi(s^{2n+1}) = 0$ and even moments $\phi(s^{2n}) = \sigma^{2n}C_n$ where $C_n$ is the n-th Catalan number and $\sigma>0$ is a constant, is called a semi-circular element of variance $\sigma^2$. in the case that $\sigma = 1$, we call it the standard semi-circular element. 

With this definition we have the free central limit theorem:

If $(a_i)$ for $i \in \mathbb{N}$ are self-adjoint, freely independent, and identically distributed with $\phi(a_i) = 0$ and $\phi(a_i) = \sigma^2$, then $S_k$ converges in distribution to a semi-circular element of variance $\sigma^2$ as $k \rightarrow \infty$. 




































