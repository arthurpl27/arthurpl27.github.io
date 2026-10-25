---
layout: page
title: <strong>QAOA for MaxCut on Weighted Random Graphs</strong>
permalink: /projects/3_project/
description: Project in Quantum Optimisation 
img: assets/img/color.jpg
importance: 1
category: Quantum
related_publications: false
---
<strong>EPFL</strong>, in Fall 2025.

<hr>

<strong>Our MaxCut Problem Statement</strong>: Given an undirected weighted random graph, divide the nodes into two sets such that the sum of the weights is maximised.

<strong>Mathematically</strong>: Consider an undirected graph $G=(V,E)$ with edge weights $w_{uv}$ associated with each edge $(u,v)\in E$. Find $\mathbf{s}\in(\pm1)^{\lvert V\rvert}$ giving us:

$$\max_{\mathbf{s}} C(\mathbf{s}):=\max_{\mathbf{s}}\sum_{(u,v)\in E}\frac{w_{uv}}{2}(1-s_us_v)\equiv-\min_{\mathbf{s}}\sum_{(u,v)\in E}s_us_vw_{uv}.$$

The cost function $C(s)$ has been found by case analysis. Upon the cut, the graph will be separated in two groups of nodes $\mathcal{A}$ and $\mathcal{B}$. We would like to sum the contributions of nodes $(u,v)$ that do not belong to the same group, otherwise it means that the corresponding edge has not been cut. Now, assign the value $s=1$ for nodes in group $\mathcal{A}$ and $s=-1$ for nodes in group $\mathcal{B}$. Thus for two nodes in the same group, it must be that $s_us_v=1$, while for two nodes in different groups, $s_us_v=-1$. In other words, we need to account for all the cases where $s_u\neq s_v$. To have positive contributions we must consider $-s_us_v$,
and we need the value zero whenever $s_u=s_v$ which can be enforced by setting $1-s_us_v$. Finally, by symmetry $w_{uv}=w_{vu}$, leading to a double count of the weights hence the necessity to divide by 2 in the cost function.  

Now, recall that the Pauli-$Z$ operator is diagonal with eigenvalues $\pm 1$. Hence, $Z_uZ_v\ket{s}=(-1)^{s_u+s_v}\ket{s}$. As a result, we can encode the cost function on qubits, giving us a <strong> cost Hamiltonian</strong> $H_C$ of the form:

$$H_C=\sum_{(u,v)\in E}w_{uv}Z_uZ_v.$$

By construction, we have that $H_C\ket{s}=C(s)\ket{s}$ (up to an additive constant independent of $s$), and so maximising the cut value is equivalent to minimising the expectation $\bra{s}H_C\ket{s}$ of $H_C$. 

<div style="height: 0.3rem;"></div>

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem;
            align-items: flex-start; margin-top: 1.5rem;">

  <img
    src="{{ '/assets/img/MaxCut.png' | relative_url }}"
    alt="Dissertation preview"
    style="width: 220px; max-width: 100%; border-radius: 6px;
           box-shadow: 0 2px 10px rgba(0,0,0,0.2);"
  >

  <div style="flex: 1; min-width: 200px;">
    <h3 style="margin-top: 0;">
      <a href="{{ '/assets/pdf/Quantum_Computing_Final_Presentation___EPFL.pdf' | relative_url }}"
         target="_blank"
         rel="noopener noreferrer">
        QAOA for MaxCut on Weighted Random Graphs
      </a>
    </h3>

    <p>
      Project presentation slides 
    </p>
  </div>

</div>