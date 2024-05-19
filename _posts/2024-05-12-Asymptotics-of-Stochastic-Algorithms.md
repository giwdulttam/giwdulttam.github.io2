---
title: 'Asymptotics of Stochastic Algorithms'
date: 2024-05-12
permalink: /posts/2012/08/blog-post-4/
tags:
  -Machine Learning
  -Stochastic Processes
  -Stochastic Gradient Descent
---

Stochastic gradient algorithms are widely used for large scale optimization and sampling especially when the computational cost of traditional deterministic methods is high. However, the main problem with stochastic gradient algorithms is that tuning them is often based on heuristics and trial and error. In order to better understand how these algorithms work and to characterize their large-scale asympototic behavior, recent work by Huggins, Negrea, et al. "Tuning Stochastic Gradient Algorithms for Statistical Inference via Large-Sample Asymptotics" showed that the sample paths of a very general class of preconditioned stochastic gradient algorithms converge to the sample paths of an Ornstein-Uhlenbeck process under relatively mild conditions.

First consider a stochastic gradient meta-algorithm that subsumes both stochastic gradient descent as well as stochastic gradient Langevin dynamics. The algorithm has the following one-step update:

  

$$\theta_{k+1}^{(n)} = \theta_{k}^{(n)} + \frac{h^{(n)} \Gamma}{2} \hat{G}_k^{(n)} + \sqrt{\frac{h^{(n)} \Lambda}{\beta^{(n)}}} \xi_k $$



Here, $\Gamma \in \mathbb{R}^{d \times d}$ is the gradient preconditioner, $\Lambda \in \mathbb{R}^{d \times d}$ is the positive-definite diffusion anisotropy matrix, $\xi_k$ are i.i.d. $N_d(0, I_d)$, and $\hat{G}_k^{(n)}$ depends on the batch size. 

Also recall that $\hat{G_k^{(n)}}$ is the unbiased gradient estimate of the potential function $\mathcal{U}^{(n)}(\theta) := r(\theta) + \sum_{i=1}^{n}l(\theta, X_i)$ where $l$ is the log-liklihood and $r(\theta)$ is a regularizer or (possibly improper) log prior $log \pi^{(0)}(\theta)$ that is everywhere positive on $\Theta$. That is: 



$$\hat{G_k^{(n)}} := \frac{1}{n} \nabla r(\theta_k^{(n)}) + \frac{1}{b^{(n)}} \sum_{j=1}^{b^{(n)}} \nabla l(\theta_k^{(n)} ; X_{I_k^{(n)}(j)})$$

where $(I_{k}^{(n)})_{k \in \mathbb{N}} \in ([n]^b)^{\mathbb{N}}$ are an independent and identically distributed sequence of uniform random samples from $\{1,...,n\}$ of size $b^{(n)}$, which are formed wither with or without replacement. 




### Theorem 1 (Scaling limit of the meta-algorithm)

If Assumptions 1 to 5 hold, there exists $\theta_{\star} \in \Theta$ such that $\hat{\theta}^{(n)} \rightarrow \theta_{\star}$ in probability, and there exists $\vartheta_{0} \in$ $\mathcal{M}$ $(\Theta)$ such that $\vartheta_{0}^{(n)}$ $\rightsquigarrow$ $\vartheta_{0}$, then for $t \in \mathbb{R_+}$, $( \vartheta_{t}^{(n)} ) \rightsquigarrow (\vartheta_{t})$ is an Ornstein-Uhlenbeck process given by

$$ d\vartheta_t = -\frac{1}{2}B \vartheta_t dt + \sqrt{A} d W_t$$

with $W_t$ a d-dimensional standard Brownian motion, $B := c_h \Gamma \mathcal{J_{\star}}$ the drift matrix, $A := \mathbb{I}(b + h < t)$ $\frac{c^2_h}{\overline{c_b} 4 c_{b}}$ $\Gamma \mathcal{I_{\star}}$ $\Gamma^T + \mathbb{I}(t < b + h) \frac{c_{h}}{c_{\beta}} \Lambda$
 the positive semi-definite diffusion matrix, and $\overline{c_b} := 1 - c_b \mathbb{I}_{[b = 1, "no- replacement"]}$ the batch constant. 







### Assumptions:

1.)

$\nabla r$ is $L_0$-Lipschitz, and $l(\cdot, x) \in C^2(\Theta)$ for each $x \in \mathcal{X}$

2.)

$h - m - a/3 > 0$ and $\mathbb{E}[\left|\left| \nabla l(\theta_{*}; X_1)\right|\right|^{p_2}]< \infty$ for some $p_2 > \frac{1}{h} - m - a/3$

3.) 

For some $q_3 \in [0, m)$ and $p_3 := \frac{1}{h} - m - a/3, \left|\left|\hat{\theta}^{(n)} - \theta_{*}\right|\right| \in o_p (1/n^{q_3})$ and $\mathbb{E}[\left|\left|\nabla^{2 \otimes} l(\cdot;X_1) \right|\right|^{p_3}_{\infty}]<\infty$


4.)

There is a non-decreasing sequence $r_{\mathcal{J}, n} \stackrel{\text{n \rightarrow \infty}}{\rightarrow} \infty $ such that $sup_{\theta \in B^{(n)}(r_{\mathcal{J,n}})} \left|\left| \hat{\mathcal{J}}^{(n)}(\theta) - \mathcal{J}(\theta_{*})\right|\right| \stackrel{\text{p}}{\rightarrow} 0$. 

5.) 

There is a non-decreasing sequence $r_{\mathcal{I}, n} \rightarrow \infty$ where $n \rightarrow \infty$ such that $sup_{\theta \in B^{(n)} (r_{\mathcal{I}}, n)} \left|\left|\hat{\mathcal{I}}^{(n)}(\theta) - \mathcal{\theta_{*}}\right|\right| \rightarrow 0$$ in probability.











