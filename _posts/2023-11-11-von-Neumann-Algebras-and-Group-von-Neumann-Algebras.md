---
title: 'von Neumann Algebras and Group von Neumann Algebas'
date: 2023-11-05
permalink: /posts/2023/11/von-Neumann-Algebras-and-Group-von-Neumann-Algebas/
tags:
  -von Neumann Algebras
  -Group von Neumann Algebras
---

### von Neumann Algebras and Group von Neumann Algebas

### von Neumann Algebras

We first recall that a vector space $\mathcal{H}$ over $\mathbb{C}$ is called a Hilbert space if it is equipt with an inner product and is complete in the topology induced by the norm associated with the inner product. Further recall that a bounded operator on a Hilbert space $\mathcal{H}$ is a $\mathbb{C}$-linear map $x: \mathcal{H} \rightarrow \mathcal{H}$ such that: $sup_{\zeta \in \mathcal{H}} \frac{\vert \vert x \zeta \vert \vert}{\vert \vert \zeta \vert \vert} < \infty$ and this supremum is called the operator norm of the operator $x$ and is denoted $\vert \vert x \vert \vert$.

Also recall that the adjoint of the operator $x$, denoted $x^{\star}$, is the unique bounded operator determined by $\langle x \zeta, \eta \rangle = \langle \zeta, x^* \eta \rangle$ where $\zeta, \eta \in \mathcal{H}$.  Now note that the set of bounded operators on $\mathcal{H}$ denoted by $\mathcal{B}(\mathcal{H})$ is a $\star-algebra$. 

Recall that a $\star$-algebra is a Banach algebra (that is an associative algebra over $\mathbb{C}$ that is at the same time a Banach space (that is a normed space that is complete in the metric induced by the norm) together with an involution satisfying the properties of the adjoint where multiplication is given by composition. Also note since $\mathcal{B}(\mathcal{H})$ is closed under the operation of norm and for all $x \in \mathcal{B}(\mathcal{H})$ we have that $\vert \vert x^{\star} x \vert \vert = \vert \vert x \vert \vert^{2} = \vert \vert x^{\star} \vert \vert^2$, then $\mathcal{B}(\mathcal{H})$ is a $C^{\star}-algebra$.

Now in order to introduce von Neumann algebras, we will first introduce a few topologies on $\mathcal{B}(\mathcal{H})$. The most natural and strongest (or finest) topology on $\mathcal{B}(\mathcal{H})$ is that induced by the operator norm.

Following this, we define the strong operator topology using the notion of strong convergence. First recall that defining a notion of convergence defines a topology as a notion of convergence specifies the open sets of a space. This is because open sets are those sets for which every sequence converging to a point inside of the open set remains entirely inside of the open set after some point - that is open sets are used in the definition of convergence.

Let $(x_{\alpha}) \subset \mathcal{B}(\mathcal{H})$ be a net of bounded operators and let $x \in \mathcal{B}(\mathcal{H})$. Then $(x_{\alpha})$ converges strongly to $x$ if $\lim_{\alpha} \vert \vert (x_{\alpha} - x) \vert \vert = 0$ for all $\zeta \in \mathcal{H}$. In other words, the above says that the distance in the operator norm of applying the operator $(x_{\alpha} - x)$ to a vector $\zeta$ in the Hilbert space is results in the zero vector in the limit. This notion of strong convergence here can be thought of as "pointwise convergence" where as convergence under the operator norm should be thought of as "uniform convergence" as a result of the use of the supremum in the definition. Now we say that the topology induced by strong convergence is called the strong operator topology. 

Similarily, we let $(x_{\alpha}) \subset \mathcal{B}(\mathcal{H})$ be a net of bounded operators, and let $x \in \mathcal{B}(\mathcal{H})$. Then we say that $(x_{\alpha})$ converges weakly to $x$ if $\lim_{\alpha} \langle (x_{\alpha} - x) \zeta, \eta \rangle = 0$ for all $\zeta, eta \in \mathcal{H}$. In other words, for all pairs of vectors $\zeta, \eta \in \mathcal{H}$, applying the operator $(x_{\alpha} - x)$ to $\zeta$ and taking its inner product with $\eta$ gives zero in the limit as the inner product of any vector with zero is zero. The topology induced by this notion of convergence is called the weak operator topology. 

Another way to conceptualize the weak and strong operator topologies on $\mathcal{B}(\mathcal{H})$ is as follows: the weak operator topology is the weakest (or coarsest) topology on $\mathcal{B}(\mathcal{H})$ such that functional sending $x \in \mathcal{B}(\mathcal{H})$ to a complex number $\langle x \zeta, \eta \rangle$ is continuous for all $\zeta, \eta \in \mathcal{H}$.

Now, we say that a unital $\star$-subalgebra $1 \in M \subset \mathcal{B}(\mathcal{H})$ is a von Neumann algebra if it is closed in the weak operator topology. Furthermore, the center of $M$, denoted $\mathcal{Z}$, is the von Neumann subalgebra $M \cap M'$ and if $\mathcal{Z}(M) = \mathbb{C}1$, then $M$ is called a factor.

One simple example of a von Neumann algebra is the ring $L^{\infty}(\mathbb{R})$ of essentially bounded measureable functions on the real line (that is the functions on the real line that are measureable and whose absolute value is bounded by some real number almost everywhere in its domain) whose elements act as multiplication operators by pointwise multiplication of functions on the Hilbert space $L^2(\mathbb{R})$ of square-integrable functions (the measureable functions for which the integral of the square of the absolute value is finite). Note that here $L^{\infty}(\mathbb{R})$ is the set of bounded operators and each square integralable function in $L^2(\mathbb{R})$ is a vector in a Hilbert space. 

A simple example of a von Neumann algebra is the following: let $\mathcal{H} = \mathbb{C^d}$ be finite dimensional and $\mathcal{B}(\mathcal{H})$ be the $d \times d$ matrices over $\mathbb{C}$. 

Another example of a von Neumann algebras appears in measures spaces. Let $(X, \Sigma, \mu)$ be a $\sigma-$finite measure space (that is a measure space that has a countable decomposition into measureable sets of finite measure) with $\mathcal{H} = L^2(X, \mu)$, for each $f \in L^{\infty}(X, \mu)$ identify it with the following bounded operator on $\mathcal{H}$: $ m_f \zeta : = f \zeta$ for all $\zeta \in \mathcal{H}$. 


### Group von Neumann Algebras

Now, having introduced von Neumann algebras and given a few basic examples, we will now discuss group von Neumann algebras which can be thought of as the von Neumann algebra of operators on a Hilbert space that are constructed from a group $G$ and are important tools in representation theory. 

Let $G$ be a discrete group and consider the compact (or finitely) supported functions $a: G \rightarrow \mathbb{C}$ and equipt these functions with a convolution $(a,b) \rightarrow a \star b$. Now, the set of these functions can be identified with the group algebra $\mathbb{C}[G]$ of formal finite linear combinations of elements in $G$ with complex coefficients, $a = \sum_{g \in G}a(g)g$, where only finitely many $a(g) \neq 0$. Also, we define integration over these functions with respect to the counting measure (that is the measure which asigns the measure of a set to be its cardinality) and thus write the convolution of them as follows: $a \star b = \sum_{g \in G}(a \star b)(g)g = \sum_{g \in G}(\sum_{h \in G} a(h)b(h^{-1}g))g = \sum_{h \in G}a(h)h \sum_{k \in G}b(k)k = ab$ which tells us that convolution here is just group multiplication.

Now, we can also define an inner product on the group algebra $\mathbb{C}[G]$ by taking $\langle g,h \rangle = 1$ if $g = h$ and $\langle g,h \rangle = 0$ if $g \neq h$. We can also define the two norm by $\vert \vert a \vert \vert_2^{2} = \langle a,a \rangle $. Therefore, $(\mathbb{C}[G], \vert \vert \cdot \vert \vert_2)$ is a normed vector sapce. The completion of this space with respect to the norm is all $a : G \rightarrow \mathbb{C}$ such that $\sum_{g \in G}\vert a(g) \vert^2 < \infty$, that is the all the functions that are square integrable, and is denoted by $l_2(G)$. Observe that since this is a complete normed vector space, it is a Hilbert space which we can now use to construct a representation of $G$ with. 

First recall that a unitary representation is a special representation (that is a homomorphism $\rho: G \rightarrow GL(V)$) where the transformation $\rho(g)$ are unitary operators on a Hilbert space $H$, that is for each $g \in G$, the operator $\rho(g)$ satisfies the following: $langle \rho(g) v, \rho(g)w \rangle = \langle v,w \rangle$ where $\langle \cdot, \cdot \rangle$ is the inner product in the Hilbert space. Intuitively, this says that applying the transformations does not change the inner product which loosely means that the transformations preserve angles.

Now consider the following unitary group representation $\lambda: G \rightarrow \mathcal{U}(l_2(G))$, which is from the group to the set of unitary operators on a the Hilbert space $\mathcal{U}(l_2(G))$, and is defined by $\lambda(g) \cdot \sum_{h \in G} a(h)h : = \sum_{h \in G}a(h)gh$, which is the left regluar representation of $G$ on the Hilbert space $l_2(G)$. Now we extend the domain of $\lambda$ from $G$ to $\mathbb{C}[G]$ by: $\lambda(a) = \lambda(\sum_{g \in G}a(g)g) = \sum_{g \in G}a(g)\lambda(g)$, that is for each $a \in \mathbb{C}[G]$, recall that here $\mathbb{C}[G]$ can be identified with the set of compactly supported conintuous functions $a: G \rightarrow \mathbb{C}$ and $\lambda(a)$ can be thought of as a finite sum of unitary operators on $l_2(G)$. Therefore, $\lambda$ is an algebra homomorphism $\lambda: \mathbb{C}[G] \rightarrow \mathcal{B}(l_2(G))$ or a representation of the group algebra on $l_2(G)$. 

Having defined the representation of group algebra on the space of bounded square integrable functions on the group, we define a new algebra via this representation. The group von Neuman algebra of G, denoted $\mathcal{L}(G)$, is the closure of $\lambda(\mathbb{C}[G])$ in the strong operator topology on $\mathcal{B}(l_2(G))$. To put it succinctly, given a countable group $G$, its closure in the strong-operator topology of the algebra of operators generated by the left-regular representations $\lambda$ of $G$ in $\mathcal{B}(l_2(G))$ is the group Veunmann algebra.

One long standing open problem about von Neumann algebras which lead Voiculescu to develop the theory of free probabilty is the following: Let $m,n \geq 2$ (and possibly equal to $\infty$ and $n \neq m$ and $\mathbb{F_n}$ and $\mathbb{F}_m$ be the free groups on $n$ and $m$ generators. Are the von Neumann algebras $\mathcal{L}(\mathbb{F_n})$ and $\mathcal{L}(\mathbb{F_m})$ isomorphic? 





















































