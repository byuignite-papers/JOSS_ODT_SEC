---
title:  
tags:
    - C++
    - Python
    - CFD
    - reacting flows
authors:
    - name: David O. Lignell
      orcid: 0000-0000-0000-0000
      affiliation: "1" 
    - name: John C. Hewson
      orcid: 0000-0000-0000-0000
      affiliation: "2"
    - name: Victoria B. Stephens
      orcid: 0000-0000-0000-0000
      affiliation: "1"
affiliations:
    - name: Department of Chemical Engineering, Brigham Young University, Provo, UT, USA 
      index: 1
    - name: Sandia National Laboratories, Albuquerque, NM, USA
      index: 2
date: 18 July 2019
bibliography: JOSS_odt_sec_paper.bib
---

# Summary

Turbulent flows characterize the vast majority of fluid flows in practical engineering
applications. Simulations involving turbulent flows aid researchers in modeling existing
phenomena and discovering new applications `[@Pope:2000]`. In particular, simulations of
reacting turbulent flows, namely combustion, rely on accurate, yet computationally efficient
tubulence models to attain accurate results. 

Turbulence is characterized by the transfer of kinetic energy between flow structures,
sometimes called eddies, of various size. This energy transfer occurs over the entire range of
length and time scales in the flow. Theoretically, a turbulent flow can be described perfectly
by the Navier-Stokes equations. Direct numerical simulations (DNS) resolve the full range of
length and time scales numerically via the Navier-Stokes equations, but doing so requires
intense computational resources, and this approach is intractable for flows with large
Reynolds numbers. DNS is a powerful research tool, but cannot be applied to most flows in
practical engineering situations. 

There are numerous models that describe turbulence and turbulent flows in order to make
practical turbulent flow problems tractable. Large-eddy simulation (LES) models do this by
directly resolving large-scale flow structures and modelling small-scale motion. In flows that
are dominated by large flow structures and motion, LES approaches provide simulation data that
is accurate and computationally efficient to produce. In cases where small-scale flow
structures are important, however, LES can introduce inaccuracies that are difficult to find
and rectify because small-scale flow structures are extremely difficult to observe
experimentaly. One alternative to LES is the One-dimensional turbulence model (ODT). Instead
of preferentially resolving large-scale structures like LES does, ODT relies on models for
large-scale turbulent advection (which is relatively well-understood) and resolves small-scale
turbulent structures directly. In development and previous studies, ODT has been shown capable
of attaining simulation data with accuracy comparable to DNS at a fraction of the
computational cost, making it an attractive model for complex turbulent flows. 

In this paper, we present the Stochastic Eddy Cascade (SEC) package, the current
implementation of the one-dimensional turbulence model (ODT). 



# Acknowledgements

This work is supported in part by the National Science Foundation under Grant No. CBET-1403403
and in part by the Sandia National Laboratories Advanced Simulation and Computing Physics and
Engineering Models program. Sandia National Laboratories is a multi-program laboratory
managed and operated by Sandia Corporation, a wholly owned subsidiary of Lockheed Martin
Corporation, for the U.S. Department of Energy’s National Nuclear Security Administration
under contract DE-AC04-94AL85000. 

# References
