---
layout: page
title: Fluid Dynamics Using Lattice Boltzmann Model
description: 
img: assets/video/simulation.gif
importance: 1
category: science
related_publications: false
---

### Numerical Simulation of Fluid Flow Using the Lattice Boltzmann Method: A Study on Convergence and Stability


The Lattice Boltzmann Method (LBM) is a versatile and efficient numerical approach for solving fluid dynamics problems, particularly the Navier-Stokes equations. This project explores the application of LBM to a two-dimensional (2D) fluid simulation, focusing on the convergence and stability of solutions for varying relaxation times (τ). The simulation captures fluid dynamics with embedded density peaks and velocity distributions using the D2Q9 model, enhanced with non-linear equilibrium corrections. To assess stability, a convergence test was conducted across multiple τ values, revealing critical thresholds for numerical instability. The results provide insight into the delicate balance between computational accuracy and physical fidelity. This project includes visualizations such as time-evolving density maps, 3D scatter plots, and convergence behavior in logarithmic scale, making it accessible to a broad audience.

Here's the entire code on [Github](https://github.com/Pratikbhanuse/Lattice_Boltzmann_Model)

If you want to read the full report illustrating the theory, approach taken, and results then please [click here](/assets/pdf/LBM_Report.pdf){:target="_blank"}.  


Here are the some visualisations from the project.

<div class="caption">
    Fluid Dynaics Simulatiion using LBM 2DQ9 configuration.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lbm/simulation.gif" title="simluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


<div class="caption">
    3-D Density Plot showing the distribution of fluid density over the time across the grid.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lbm/3d_scatter_plot.png" title="simluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Convergence test to check the reliability of numerical method and the model.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lbm/convergence_test.png" title="simluation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

