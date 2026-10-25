---
layout: page
title: Local Limits of Random Graphs
permalink: /projects/1_project/
description: BSc. Thesis in Random Graph Theory
img: assets/img/Proof_RG.jpg
importance: 1
category: academic
related_publications: false
---
<strong>King's College London (KCL)</strong>, supervised by Dr. Dominic Yeo.

<hr>

First introduced in 2001 by Benjamini and Schramm, local limits have been widely used to describe finite sparse random graphs. The process consists in simplifying the structure of (possibly large) random graphs using simpler models, where in the case of this project we consider approximations to branching processes. 

A local limit is an important concept to study possibly large and complex graphs. They give a tool to describe the notion that, in a graph, from the point of view of a vertex chosen at random and naturally creating a rooted graph, the resulting structure looks like a certain limiting graph.

Mathematically, let $\mathcal{G}$ be an ensemble of rooted graphs and set $B_r^G(\rho)$ to be the neighborhood of $\rho$ of radius $r$ in the graph $G$. Consider a sequence $(G_{n},\rho_{n})$ of random graphs with random root $\rho_{n}$. Let $(H,\rho_{H})$ be a rooted graph. Then, we say that $(G_{n},\rho_{n})$ <strong> converges locally weakly in probability </strong> to $(G,\rho)$ if, for all $r\geq 1$, and for all rooted graphs $H\in\mathcal{G}$: 

$$\mathbb{P}\big(B_{r}^{G_{n}}(\rho_{n})\cong (H,\rho_{H}) |G_{n}\big)\xrightarrow{\hspace{0.2cm}\mathbb{P}\hspace{0.2cm}}\mathbb{P}\big(B_{r}^{G}(\rho)\cong H\big)  .$$   

For instance, with $\lambda>0$, an Erdős-Rényi random graph $ER_{n}(\frac{\lambda}{n})$ converges locally in probability to a Poisson branching process.

As an even more profound role, it turns out that if we know the local graph limit we can also obtain the limits of a wide variety of local graph measures, such as the convergence of neighborhoods and even the convergence of its clustering coefficient. As a result, we can often make conclusions about global properties of the graph knowing the local behavior, and it is specifically the case for the study of the Giant Component. 

This dissertation presents the general theory of local limits through the study of branching processes, along with some applications on the study of the local limit of the Configuration Model under a specific degree sequence, and an analysis of the Giant Component in an Erdős-Rényi random graph taking the local limit as an assumption.

<div style="height: 0.3rem;"></div>

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem;
            align-items: flex-start; margin-top: 1.5rem;">

  <img
    src="{{ '/assets/img/BSc_Thesis_front_page.png' | relative_url }}"
    alt="Dissertation preview"
    style="width: 220px; max-width: 100%; border-radius: 6px;
           box-shadow: 0 2px 10px rgba(0,0,0,0.2);"
  >

  <div style="flex: 1; min-width: 200px;">
    <h3 style="margin-top: 0;">
      <a href="{{ '/assets/pdf/3rd_year_project___Local_Limits_of_Random_Graphs.pdf' | relative_url }}"
         target="_blank"
         rel="noopener noreferrer">
        Local Limits of Random Graphs
      </a>
    </h3>

    <p>
      Thesis document 
    </p>
  </div>

</div>