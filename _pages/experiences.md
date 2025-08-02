---
layout: page
title: experiences
permalink: /experiences/
description: mostly computational science. machine learning, and research software engineering...
nav: true
nav_order: 2
horizontal: false
---

Below are my "formal" work experiences. I also contribute to several open-source scientific software, and I consider that as an "experience" too (see **[/opensource](/opensource)**). I have also mentored several students and researchers who are new at writing code for research/scientific software (see **[/teaching](/teaching)**).

---

### TL;DR

---

- [Research Software Engineer](https://profiles.ucl.ac.uk/99635-saransh-chopra) \| June 2025 - Present \| [Advanced Research Computing Centre](https://www.ucl.ac.uk/advanced-research-computing){:target="_blank"}, [University College London](https://www.ucl.ac.uk){:target="_blank"}
- [Assistant Research Software Engineer](https://profiles.ucl.ac.uk/99635-saransh-chopra) \| August 2024 - June 2025 \| [Advanced Research Computing Centre](https://www.ucl.ac.uk/advanced-research-computing){:target="_blank"}, [University College London](https://www.ucl.ac.uk){:target="_blank"}
- [Research Fellow](https://iris-hep.org/about/team) (bachelor's thesis) \| January 2024 - August 2024 \| [CERN](https://home.cern){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}, [IRIS-HEP](https://researchcomputing.princeton.edu/research/iris-hep-software-institute){:target="_blank"}
- [Visiting Student Researcher (Mitacs Globalink Research Intern)](https://www.mitacs.ca/en/programs/globalink/globalink-research-internship){:target="_blank"} \| June 2023 - August 2023 \| [McMaster University](https://www.mcmaster.ca){:target="_blank"}
- [Research Fellow](https://iris-hep.org/fellows/Saransh-cpp.html){:target="_blank"} \| June 2022 - September 2022 \| [Institute for Research and Innovation in Software for High Energy Physics](https://researchcomputing.princeton.edu/research/iris-hep-software-institute){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}
- [Technical Writer and Open-Source Developer](https://julialang.org/jsoc/){:target="_blank"} \| May 2022 - October 2022 \| [FluxML](https://fluxml.ai){:target="_blank"}, [Julia Programming Language](https://julialang.org){:target="_blank"}
- [Google Summer of Code Developer](https://summerofcode.withgoogle.com){:target="_blank"} \| May 2021 - September 2021 \| [PyBaMM (Python Battery Mathematical Modeling)](https://pybamm.org){:target="_blank"}, [NumFOCUS](https://numfocus.org){:target="_blank"}

---
### Full-time experience
---

#### [Advanced Research Computing Centre](https://www.ucl.ac.uk/advanced-research-computing){:target="_blank"}, [University College London](https://www.ucl.ac.uk){:target="_blank"}
##### [Research Software Engineer](https://profiles.ucl.ac.uk/99635-saransh-chopra)
###### Dr. Sam Cunliffe
###### June 2025 - Present | London, United Kingdom
- “Generalist” staff member in the Research Software Engineering group of the Advanced Research Computing Centre. Mostly involved with the HPC, DevOps, and Education sub-groups, open-source research theme, and Python tooling.
- Worked on GPU and automatic differentiation support to large-scale cosmological simulations ([GLASS](https://glass.readthedocs.io/stable/)) for ESA's Euclid space mission  (GPU embedded Computational Science and Engineering grant by EPCC + Euclid space mission grant by the UKSA).
- Involved with observability and monitoring for UCL's XNAT service, and auditing UCL's HPC systems to make them more "green" and sustainable.
- See [/teaching](/teaching) for teaching and community activities.

##### [Assistant Research Software Engineer](https://profiles.ucl.ac.uk/99635-saransh-chopra)
###### Dr. Sam Cunliffe
###### August 2024 - June 2025 | London, United Kingdom
- Same work, but with less degree of independence/leadership/ownership.

---
### Research experience
---

#### [CERN](https://home.cern){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}
##### [Research Fellow](https://iris-hep.org/about/team) (bachelor's thesis)
###### Dr. Jim Pivarski (Princeton University)
###### January 2024 - August 2024 | Geneva, Switzerland

- Thesis titled "Computational upgrades to the high energy physics analysis pipeline for future LHC/HL-LHC runs."
- Worked on autodiff (JAX) support for Awkward Arrays, added symbolic (SymPy) computing support to vector manipulations, and extended autodiff and distributed computing support to a few other libraries.
- Implemented non-uniform rebinning for [boost-histogram](https://boost-histogram.readthedocs.io/en/latest/) and developed a new package for [histograms on CUDA](https://cuda-histogram.readthedocs.io/en/latest/).
- Migrated the vector manipulation backend of the analysis framework ([Coffea](https://github.com/CoffeaTeam/coffea)) used at Fermilab and CMS.

---

#### [McMaster University](https://www.mcmaster.ca){:target="_blank"}
##### [Visiting Student Researcher (Mitacs Globalink Research Intern)](https://www.mitacs.ca/en/programs/globalink/globalink-research-internship){:target="_blank"}
###### Prof. Jacques Carette
###### June 2023 - August 2023 | Hamilton, Ontario, Canada

- Worked with functional programming, type theory, and logic to add proofs and algorithms for data containers and mathematical operations in [Agda](https://wiki.portal.chalmers.se/agda/pmwiki.php)'s [standard library](https://github.com/agda/agda-stdlib).
- Significantly reduced library's compile time by refactoring the existing API and simplifying the dependency graph.

---

#### [IRIS-HEP](https://researchcomputing.princeton.edu/research/iris-hep-software-institute){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}
##### [Research Fellow](https://iris-hep.org/fellows/Saransh-cpp.html){:target="_blank"}
###### Dr. Henry Schreiner (Princeton University), Dr. Jim Pivarski (Princeton University)
###### June 2022 - September 2022 | Remote

<!-- - Work: -->
- Co-authored a Python-based Lorentz vector manipulation library with support for ragged data and JIT compilation.
- Worked on Scientific Python's developer guides and tools, and fixed bugs in the Scikit-HEP ecosystem.

<!-- - Impact:
  - Vector has **50+ GitHub stars** and **210,000+ installs**.
  - The releases are currently being used by researchers at **CERN**, **Princeton University**, **IRIS-HEP** and **other research institutes**. -->

<!-- - Positions of responsibility, volunteering, talks:
  - Joined vector's GitHub repository and Conda Feedstock as a maintainer.
  - Presented my work and vector at **21st International Workshop on Advanced Computing and Analysis Techniques in Physics Research**, **5th International Workshop on Python in High Energy Physics**, and multiple **IRIS-HEP**, **Princeton Research Computing** meetups (see **[/talks](/talks){:target="_blank"}**).
  - Invited to join **PyHEP 2023.dev** (first PyHEP developers meetup) at Princeton, but won't be able to make it 😢
  - I still maintain/contribute to vector! -->

---

### Other experience
---
#### [FluxML](https://fluxml.ai){:target="_blank"}, [Julia Programming Language](https://julialang.org){:target="_blank"}
##### [Technical Writer and Open-Source Developer](https://julialang.org/jsoc/){:target="_blank"}
###### Mr. Dhairya Gandhi (Julia Computing / JuliaHub)
###### May 2022 - October 2022 | Remote (Part-Time)

<!-- - Work: -->
<!-- - Developed the documentation + packaging infrastructure and fixed bugs in FluxML, an ML and DL ecosystem that provides lightweight abstractions on top of Julia’s native GPU and AD support.
- Wrote original Machine Learning/Deep Learning tutorials, documentation and API references for FluxML's ecosystem. -->

<!-- - Impact:
  - FluxML is Julia's primary ML and DL ecosystem with hundreds of thousands of downloads.
  - Flux.jl alone has **4000+ GitHub stars** and **110,000+ installs** (Julia-n ecosystems are not concentrated in a single library - for instance, there is a separate package under FluxML just for one-hot encoding - OneHotArrays.jl).
  - The documentation, infrastructue, and bug fixes impacted ML and DL researchers all around the world, including institutions and companies (MIT, AMD, UCL, CMU, and so on). -->

<!-- - Recognition, talks, and more:
  - Joined FluxML's GitHub organisation.
  - Will be presenting my work at **JuliaCon 2023** (see **[/talks](/talks){:target="_blank"}**).
  - My work was shared on FluxML's and JuliaLang's official **[Twitter](https://twitter.com/FluxML/status/1589255265559396352)** and **[LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:6995034692412456960/)** accounts.
  - I still contribute to FluxML! -->

---

#### [PyBaMM (Python Battery Mathematical Modeling)](https://pybamm.org){:target="_blank"}, [NumFOCUS](https://numfocus.org){:target="_blank"}
##### [Google Summer of Code Developer](https://summerofcode.withgoogle.com){:target="_blank"}
###### Dr. Valentin Sulzer (Carnegie Mellon University), Dr. Ferran Brosa Planella (University of Warwick), Dr. Robert Timms (University of Oxford)
###### May 2021 - September 2021 | Remote

<!-- - Work: -->
<!-- - Built a novel Twitter Bot ([BattBot](https://github.com/pybamm-team/BattBot)) capable of automatically constructing Mathematical Simulations of Batteries.
- Developed new API, fixed bugs, and created new documentation for the PyBaMM ecosystem.
- Developed the build and packaging infrastructures for the PyBaMM ecosystem and the upstream packages. -->

<!-- - Impact:
  - PyBaMM is a collaboration between multiple academic institutes with **550+ GitHub stars** and **300,000+ installs**.
  - My work impacted battery researchers worldwide as PyBaMM is the most adopted Python framework for Modeling of Batteries.
  - BattBot gained a lot of traction on Twitter and GitHub. -->

<!-- - Positions of responsibility, volunteering, talks:
  - I regularly supervise PyBaMM's GSoC projects.
  - Joined PyBaMM's GitHub organisation as a maintainer.
  - Presented my work at [PyBaMM's first training workshop](https://www.pybamm.org/training) and GSoC showcase.
  - Invited to join [PyBaMM's steering council](https://github.com/pybamm-team/PyBaMM/wiki/Governance#current-steering-council) (associated with NumFOCUS).
  - Joined [liionpack](https://github.com/pybamm-team/liionpack) as a core-developer.
  - I still maintain PyBaMM, liionpack, and BattBot! -->
