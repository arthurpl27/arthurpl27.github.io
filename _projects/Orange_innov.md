---
layout: page
title: <strong>Quantum Computing for Molecular Simulation</strong>
permalink: /projects/4_project/
description: Research Internship 
img: assets/img/fermionic.jpg
importance: 1
category: Quantum
related_publications: true
---
<strong>Orange Innovation</strong>, Rennes (France) in Spring 2026.

<hr>

The potential of Quantum Computing (QC) in medicine began to emerge more clearly with advances in quantum algorithms and hardware during the 2010s. A major breakthrough was the development of quantum algorithms for molecular simulation, motivated by the difficulty of classically modelling complex molecular systems and thus opening the possibility of applying QC to drug discovery. Another promising direction is the emergence of Quantum Machine Learning (QML), with applications to genomic data analysis, medical diagnostics and personalised medicine{% cite Chow2024 %}.
These developments have established healthcare as a promising area for quantum computing. However, current quantum technologies remain limited by hardware constraints, noise and scalability, making the integration of QC into medical applications an ongoing challenge{% cite Chow2024 %}. This report explores the emerging intersection between quantum computing and medicine, with a core emphasis on the development of quantum simulation methods for the study of molecular systems.

The global theme of the report is on the use of quantum computers for the design of new drug molecules. This is a very tough problem since, for the time being, designing a new compound roughly takes 10-20 years and costs billions of dollars. There already were some methods that have been developed mainly based on Artificial Intelligence models, such as the renowned `AlphaFold` system which predicts the structure of proteins and other biomolecules from their amino acid sequences. There was a first attempt in 2022 to make a quantum-approach system named `QFold`{% cite Casares_2022 %}, however this was only presented as a proof-of-concept. Another idea is to centre the research on quantum-classical methods by mixing traditional Machine Learning models with the help of a quantum computer. This is for instance the case of the `QCA-MolGAN`{% cite thomas2025qcamolganquantumcircuitassociative %} system which samples bitstrings from a quantum circuit that will then act as a prior distribution for a Generative Adversarial Network (GAN) with the aim to design novel drug molecules with desired target
properties. Initially, we will focus on the core problem of creating novel drug molecules which can be understood via *Protein-Ligand Interactions*. The situation is sketched below and can be described as follows: our immune system is responsible to generate a response to some potential malignant cells. Among them, cancer cells are usually treated by our immune system with the proliferation of T-cells, for which their role is to destroy infected cells and regulate immune responses. We now mention that on the surface of a T-cell lives some proteins which are enormous molecules of hundreds of atoms, whereas a cancer cell has some ligands (binding molecules) on its surface. However, it turns out that specific proteins and ligands may bind together, where for instance it is the case of the Programmed Cell-death Protein (PD-1) and the Programmed Death-Ligand 1 (PD-L1). If this binding occurs, the power of the T-cell to destruct the cancer cell is inhibited. Thus, developing an effective cancer treatment requires finding a molecule capable of disrupting the PD-1/PD-L1 interaction, thereby restoring the T-cell's ability to destroy cancer cells. It turns out that understanding this binding requires evaluating the corresponding *binding energy*. For protein-ligand interactions, the energy of interest is the binding energy $E_{\text{Bind}}$ which is given by the difference between the energy of the Protein/Ligand Complex $E_{\text{P/L Complex}}$ and the sum of the energies of the protein $E_{\text{Protein}}$ with the one of the ligand $E_{\text{Ligand}}$. Formally we have:

$$E_{\textup{Bind}}=E_{\text{P/L Complex}}-E_{\text{Protein}}-E_{\text{Ligand}}.$$ 

<div style="text-align: center; margin: 1.5rem 0;">
  <img
    src="{{ '/assets/img/PL.png' | relative_url }}"
    alt="Simplified representation of protein-ligand interactions"
    style="width: 400px; max-width: 100%; height: auto;"
  >
</div>

Thus, at the level of this simplified description, the problem reduces to evaluating the energies of the complex and its constituent fragments. It turns out that several crucial problems in Quantum Chemistry could be interpreted as the estimation of an energy. Of particular interest is the so-called *ground-state energy* $E_0$, which corresponds to the lowest level of energy of a system. In fact, the ground-state energy plays a central role in describing important chemical phenomena, such as bond formation and dissociation. However, computing the (ground-state) binding energy accurately remains a challenging problem for classical computers, as protein–ligand complexes can contain tens of thousands of atoms, making their exact high-accuracy quantum-mechanical description computationally intractable for current methods. For this reason, we initially investigated several approaches to approximately estimate the ground-state energy, including molecular fragmentation techniques such as *Density Matrix Embedding Theory (DMET)* {% cite Kirsopp_2022 %}. However, these methods quickly proved prohibitively demanding for the available computational resources. Consequently, we decided to focus on ground-state energy estimation for small-scale molecular systems.

In this report, we investigate different methods to estimate the ground-state energy of a quantum-mechanical system. We first briefly review the foundations of Quantum Mechanics, Quantum Chemistry, and Quantum Computing in order for the reader to be able to follow the later sections. We then investigate *Quantum Subspace Methods*, which seek to simplify the energy estimation problem by focusing the analysis on a smaller part of the original problem. We also explore *Neural Quantum States*, a machine-learning approach designed to represent and study complex many-body quantum systems. Throughout the report, the theoretical developments are complemented by numerical implementations, allowing the different methods to be tested on concrete examples.

The full report, along with the final presentation of the internship (in French), and a GitHub repository on Neural Quantum States, can be found below.  

<div style="height: 0.3rem;"></div>

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem;
            align-items: flex-start; margin-top: 1.5rem;">

  <img
    src="{{ '/assets/img/report.png' | relative_url }}"
    alt="Dissertation preview"
    style="width: 220px; max-width: 100%; border-radius: 6px;
           box-shadow: 0 2px 10px rgba(0,0,0,0.2);"
  >

  <div style="flex: 1; min-width: 200px;">
    <h3 style="margin-top: 0;">
      <a href="{{ '/assets/pdf/Stage_Orange_Innovation___Rapport_Technique copy.pdf' | relative_url }}"
         target="_blank"
         rel="noopener noreferrer">
        Technical Report
      </a>
    </h3>

    <p>
      Internship report 
    </p>
  </div>

</div>


<div style="height: 0.3rem;"></div>

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem;
            align-items: flex-start; margin-top: 1.5rem;">

  <img
    src="{{ '/assets/img/final_presentation.png' | relative_url }}"
    alt="Dissertation preview"
    style="width: 220px; max-width: 100%; border-radius: 6px;
           box-shadow: 0 2px 10px rgba(0,0,0,0.2);"
  >

  <div style="flex: 1; min-width: 200px;">
    <h3 style="margin-top: 0;">
      <a href="{{ '/assets/pdf/Final_QM_Presentation___Orange_Innovation__Copy_.pdf' | relative_url }}"
         target="_blank"
         rel="noopener noreferrer">
        Internship Presentation (in French)
      </a>
    </h3>

    <p>
      Final internship presentation 
    </p>
  </div>

</div>


<div style="height: 0.3rem;"></div>
<div style="display: flex; flex-wrap: wrap; gap: 1.5rem;
            align-items: flex-start; margin-top: 1.5rem;">

  <img
    src="{{ '/assets/img/with_SR.png' | relative_url }}"
    alt="SR GitHub repository preview"
    style="width: 220px; max-width: 100%; border-radius: 6px;
           box-shadow: 0 2px 10px rgba(0,0,0,0.2);"
  >

  <div style="flex: 1; min-width: 200px;">
    <h3 style="margin-top: 0;">
      <a href="https://github.com/arthurpl27/Neural_Quantum_States"
         target="_blank"
         rel="noopener noreferrer">
        Neural Quantum States — GitHub Repository
      </a>
    </h3>

    <p>
      Source code and experiments on Neural Quantum States.
    </p>
  </div>

</div>

<div style="height: 3rem;"></div>

<style>
  a.citation {font-size: 0.8em;}
</style>