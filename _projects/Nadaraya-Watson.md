---
layout: page
title: Nonparametric Drift Estimation for SDEs
permalink: /projects/2_project/
description: MSc. Semester Project in Statistics
img: assets/img/SDE.png
importance: 2
category: Mathematics
related_publications: false
---
<strong>EPFL</strong>, supervised by Prof. Victor Panaretos in Fall 2025.

<hr>

In this project, we deal with the nonparametric Nadaraya-Watson estimator of the drift function computed from independent continuous observations of a stochastic differential equation (SDE). In particular, for $b,\sigma:\mathbb{R}\rightarrow\mathbb{R}$ two continuous functions and $(W_t)_{t\in[0,T]}$ a Brownian motion, we consider the following SDE:

$$X_t=x_0+\int_0^tb(X_s)ds+\int_0^t\sigma(X_s)dW_s,\hspace{0.5cm}t\in[0,T].$$
 
We provide a nonparametric estimator of the drift function $b(X_t)$ from $N\in\mathbb{N}^*$ i.i.d. copies $X_t^1,...,X_t^N$ solving the above SDE and from repeated continuous observations of the sample paths. We thus consider the following family of SDEs for $N$ i.i.d. copies of a Brownian motion $\{W^1,...,W^N\}$: 
 
$$X_t^i=x_0+\int_0^tb(X_s^i)ds+\int_0^t\sigma(X_s^i)dW_s^i,\hspace{0.5cm}t\in[0,T]\hspace{0.2cm}\text{and}\hspace{0.2cm} i\in\{1,...,N\}.$$

We then consider the access to the $N$ random paths through the noisy observations $Y^1,...,Y^N$ given by

$$Y^i=b(X^i)+\xi_i,\hspace{0.5cm}i\in\{1,..., N\},$$

such that the Nadaraya-Watson estimation concerns the estimation of the measurable function $b$ giving an estimator $\widehat{b}$, where $\xi_1,...,\xi_N$ are $N$ i.i.d. centred random variables with a strictly positive variance and independent of the SDE samples $X^1,..., X^N$. We moreover assume that the diffusion coefficient can be almost surely determined by the process, i.e. it can be estimated without any error through its continuous observation throughout a time interval.  

For some kernel functions $K_h$, we motivate the construction of a Nadaraya-Watson-type estimator for the drift function given by:

$$\widehat{b}_{N,h}(x)=\frac{\widehat{bf}_{N,h}(x)}{\widehat{f}_{N,h}(x)}:=\frac{\left(\frac{1}{N(T-t_0)}\sum\limits_{i=1}^N\int_{t_0}^TK_h(X_t^i-x)dX_t^i\right)}{\left(\frac{1}{N(T-t_0)}\sum\limits_{i=1}^N\int_{t_0}^TK_h(X_t^i-x)dt\right)}.$$

We provide risk-bounds for this estimator, i.e. a bound for the mean squared error $\mathbb{E}\lVert \widehat{b}_{N,h}-b\lVert^2$, along with the description of two methods to select the optimal bandwidth $h$ yielding an optimal bias-variance tradeoff.


<div style="height: 0.3rem;"></div>

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem;
            align-items: flex-start; margin-top: 1.5rem;">

  <img
    src="{{ '/assets/img/semester_project .png' | relative_url }}"
    alt="Dissertation preview"
    style="width: 220px; max-width: 100%; border-radius: 6px;
           box-shadow: 0 2px 10px rgba(0,0,0,0.2);"
  >

  <div style="flex: 1; min-width: 200px;">
    <h3 style="margin-top: 0;">
      <a href="{{ '/assets/pdf/Semester_Project___Methods_for_Parameter_Estimation_of_SDEs.pdf' | relative_url }}"
         target="_blank"
         rel="noopener noreferrer">
        Nonparametric Drift Estimation for SDEs
      </a>
    </h3>

    <p>
      Project document 
    </p>
  </div>

</div>
