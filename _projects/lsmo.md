---
layout: page
permalink: /projects/lsmo
title: Simulating La₁₋ₓSrₓMnO₃ Superconductor with LAMMPS
description: Simulating Sr-doped La₁₋ₓSrₓMnO₃ (LSMO) using Python + LAMMPS with XRD, density, and composition analysis.
img: assets/img/xrd.png
date: 2025-05-02
importance: 1
category: science
related_publications: false
---

### Simulating Sr-Doped La₁₋ₓSrₓMnO₃ (LSMO) Superconductor Using LAMMPS

This project demonstrates a Python-based workflow to simulate the synthesis and analyze the structural properties of Sr-doped La₁₋ₓSrₓMnO₃ (LSMO), a complex perovskite material known for its rich magnetic and electronic behavior.

Using **LAMMPS**, we:
- Created doped crystal structures by replacing La with Sr
- Performed atomistic relaxation
- Analyzed the structure using **X-ray diffraction (XRD)**, **density**, and **elemental composition** plots

The workflow offers a foundation for **high-throughput simulation studies** of doped perovskites and can be extended for advanced material discovery pipelines.

Explore the complete code on [GitHub](https://github.com/Pratikbhanuse/LSMO-Synthesis-Computationally)

For a deeper dive into the process and results, read the [Medium article](https://pratiksletters.medium.com/simulating-la₁-ₓsrₓmno₃-superconductor-with-lammps-doping-effects-and-material-analysis-e514ed48adc8){:target="_blank"}.

Here are some visualizations from the project:

<div class="caption">
    Simulation of Sr-doped La₁₋ₓSrₓMnO₃ with structural relaxation and XRD analysis.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/video/simulation.gif" title="Simulation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Smoothed XRD pattern showing diffraction peaks after atomic relaxation.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lsmo/xrd_smoothed.png" title="XRD Plot" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Elemental composition pie chart showing La, Sr, Mn, and O distribution.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lsmo/composition_pie.png" title="Composition Chart" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
