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

<strong>Mathematically</strong>: Consider an undirected graph $G=(V,E)$ with edge weights $w_{uv}$ associated with each edge $(u,v)\in E$. Find $\mathbf{s}\in\{\pm1\}^{\lvert V\rvert}$ giving us

$$\max_{\mathbf{s}} C(\mathbf{s}):=\max_{\mathbf{s}}\sum_{(u,v)\in E}\frac{w_{uv}}{2}(1-s_us_v)\equiv-\min_{\mathbf{s}}\sum_{(u,v)\in E}s_us_vw_{uv}.$$


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