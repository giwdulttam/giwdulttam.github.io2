---
title: 'Cumulants as Functionals'
date: 2014-08-14
permalink: /posts/2023/11/Cumulants-as-Functionals/
tags:
  -Cumulants
  -Functionals
---


### Cumulants as Functionals

Having previously introduced cumulants as well as free and monotone cumulants, this post will provide a more general way of viewing cumulants. Mainly, as recognizing them as finite linear combinations of cumuants as continuous $\mathbb{R}$-valued, and convolution-additive functionals of probability measures. 

Let $X$ be a set with a $\sigma-$algebra $\mathcal{A}$ and let $Prob(X)$ denote the set of all probability measures on $\mathcal{A}$, that is the set of all functions $\mu : \mathcal{A} \rightarrow \mathbb{R}$ such that $\mu(X) = 1$. Also define:

$$Prob_r(\mathbb{R}) = \{ P \in Prob(\mathbb{R}) : \int |x|^r dP(x) < \infty \} \text{   } (r \in \mathbb{N}_0)$$


Also let the real line $\mathbb{R}$ be equipt with the Borel $\sigma$-algebra.  Now recall that for $P \in Prob(\mathbb{R})$, the Fourier transform or characteristic function is defined as: 

$$\hat{P}(t) = \int_\mathbb{R} e^{itx} dP(x) = \int_\mathbb{R} P(dx)e^{itx}$$

One nice property of the Fourier transform or characteristic functions of probability measures is that the Fourier transform of the convolution of two probability measures it the product of the Fourier transform or each measure:

$$\hat{(P \star Q)}(t) = \hat{P}(t) \cdot \hat{Q}(t) \hspace{15pt} (P, Q \in Prob(\mathbb{R}), t \in \mathbb{R})$$

Also recall how the convolution of two probability measures $\mu$ and $\nu$ is the law of the random $X + Y$ where $X$ and $Y$ are independent random variables taking values in $\mathbb{R}^n$ with laws $\mu$ and $\nu$ respectively. In this case note that this definition simply uses the log Fourier transform or log characteristic function instead of the logarithm of moment generating function which we used to define cumulants in the "Introduction to Moments and Cumulants" post. Now since $log \circ \hat{P}$ is $r$ times contiuously differentiable in the neighborhood of zero we can define the $r^{th}$ cumulant as:

$$\kappa_r = i^{-r}(D^r log \circ \hat{P})(0)$$ 

Where $D^r$ denotes the $r^{th}$ derivative. Now having defined cumulants in terms of Fourier transforms or characteristic functions, which allows more easily discuss the convolution of measures and the distributions of the sums of random variables, we also have the following relation: 

$$\kappa_r(P \star Q) = \kappa_r(P) + \kappa_r(Q) \hspace{15pt} (r \in \mathbb{N}, P, Q \in Prob_r(\mathbb{R}))$$

Thus it follows that for each $r \in \mathbb{N}, (Prob_r(\mathbb{R}), \star)$ is a semigroup on which $\kappa_r$ is an additive function, that is a homomorphism into the additive gropu $\mathbb{R}$. One fascinating result that we will not have time to prove in this post is that every continuous homomorphism from $(Prob_r(\mathbb{R}), \star)$ into $(\mathbb{R}, +)$ is a linear combination of cumulants of order at most $r$. Another cool result that will be discussed in a future post is that the free analogue of the logarithm of the Fourier transform of a probability measure is Voiculescu's R-transform. 


While redefining cumulants in this more general context may at first have seemed about arcane, the previous result illustrates how use a more general defition allows us to discover more of the many interesting properties of cumulants. 


References: "What are Cumulants?" by Lutz Mattner in Documenta Mathematica 4 (1999), 601-622























