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

The Stochastic Eddy Cascade (SEC) package is a set of models and tools used to simulate
turbulent flow systems in which turbulence is modeled by stochastic processes that map
so-called "eddy events" onto the domain. Most notably, SEC includes the most current
implementation of the one-dimensional turbulence model (ODT), which has been successfully used
to simulate turbulent reacting and nonreacting flows with high accuracy and relatively low
computational cost `[@Lignell_2018]`. In addition to ODT, SEC also offers a flamelet model for
combustion systems, which is useful for model validation and testing. 

Turbulent flows characterize the vast majority of fluid flows in practical engineering
applications, and simulations of turbulent flows provide researchers with valuable insights
into complex systems, particularly reacting turbulent flows such as combustion processes
`[@Pope_2000]`. Turbulence is a complex phemonenon that occurs over the full range of the
flow's length and time scales. As a result, resolving the entire flow field by numerically
solving the Navier-Stokes equations of fluid flow, as is done in direct numerical simulations
(DNS), requires intense computational resources. DNS is a powerful research tool, but its high
computational cost makes this approach intractable for most practical engineering flows. In
order to achieve solutions to practical flow problems, turbulence is most often modeled. For
example, large-eddy simulation (LES) approaches directly resolve large-scale flow structures
but model small-scale motion, which often results in accurate, computationally efficient
simulation data. Unfortunately, LES approaches can introduce empiricism into flow simulations,
and errors can be difficult to isolate and quantify. The one-dimensional turbulence model (ODT)
functionally reverses the LES approach, modeling large-scale turbulent advection (which is
relatively well-understood) and directly resolving small-scale flow structures. In previous
studies, ODT has been shown capable of attaining accuracy comparable to DNS at a fraction of
the computational cost `[@Lignell_2015]`, making it an attractive model for simulating
turbulent flows, particularly in combustion systems. 

ODT has been applied to a wide range of flows. Early applications focused on homogenous
turbulence, wakes, and mixing layers `[@Kerstein_1999; @Kerstein_2001]`. Later extension to
variable-density flows and a spatial downstream coordinate system facilitated its growth and
application to more complex flows, including combustion in jet flames and fires
`[@Echekki_2001; @Hewson_2001; @Hewson_2002; @Jozefik_2015; @Lignell_2015; @Lignell_2012;
@Punati_2011]` and particle flows `[@Goshayeshi_2015; @Schmidt_2009; @Sun_2014; @Sun_2011]`.
ODT has also served to complement LES through subgrid modeling studies `[@Cao_2008;
@Schmidt_2003; @Schmidt_2010]`. Most recently, the ODT code was extended to include cylindrical
and spherical coordinate systems `[@Lignell_2018]`. During this implementation, the ODT code
was drastically overhauled, resulting in the SEC package presented here. Further detail on the
current ODT model formulation and implementation can be found in the literature
`[@Ashurst_2005; @Kerstein_2001; @Lignell_2013; @Lignell_2018]`.

Ongoing research involving ODT and SEC spans multiple research groups and subject areas. ODT is
currently being used to investigate soot formation and destruction in ethylene jet flames via
parametric modeling studies `[@Hewson_2015]`. The SEC package framework is also being used to
develop the hierarchical parcel swapping model (HiPS), which models turbulence with an
economical, hierarchical network that represents the fluid as individual parcels capable of
switching positions within the tree `[@Kerstein_2013; @Kerstein_2014]`. In the future, SEC may
also be extended to include the linear eddy model (LEM) `[@Kerstein_1991]` and LES approaches. 

# Acknowledgements

This work is supported in part by the National Science Foundation under Grant No. CBET-1403403
and in part by the Sandia National Laboratories Advanced Simulation and Computing Physics and
Engineering Models program. Sandia National Laboratories is a multi-program laboratory
managed and operated by Sandia Corporation, a wholly owned subsidiary of Lockheed Martin
Corporation, for the U.S. Department of Energy’s National Nuclear Security Administration
under contract DE-AC04-94AL85000. 

# References
