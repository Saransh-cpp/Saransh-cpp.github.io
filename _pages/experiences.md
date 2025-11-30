---
layout: page
title: experiences
permalink: /experiences/
description: mostly computational science, high-performance computing, devops, and research software engineering, with some type theory, functional programming, machine learning, and non-research software engineering, ...
nav: true
nav_order: 2
horizontal: false
---

Below are my "formal" work experiences and educational qualifications. I also contribute to several open-source scientific software, and I consider that as an "experience" too (see **[/opensource](/opensource)**). I have also mentored several students and researchers who are new at writing code for research/scientific software (see **[/teaching](/teaching)**). Finally, programming can be learnt without any formal degrees; hence, my skills/abilities are not limited by my courses.

---

### TL;DR

---

#### Education

- Master's in Computational Science and Engineering \| September 2025 - Present \| [École Polytechnique Fédérale de Lausanne](https://www.epfl.ch/en/){:target="_blank"}
- Summer University on High-Performance Computing and Data Analytics \| July 2025 - July 2025 \| [Swiss National Supercomputing Centre](https://www.cscs.ch){:target="_blank"}
- Bachelor's of Technology in Computer Science and Mathematics \| August 2020 - August 2024 \| [University of Delhi](https://www.du.ac.in){:target="_blank"}

---

#### Work

- Research Software Engineer \| June 2025 - September 2025 \| [Advanced Research Computing Centre](https://www.ucl.ac.uk/advanced-research-computing){:target="_blank"}, [University College London](https://www.ucl.ac.uk){:target="_blank"}
- Assistant Research Software Engineer \| August 2024 - June 2025 \| [Advanced Research Computing Centre](https://www.ucl.ac.uk/advanced-research-computing){:target="_blank"}, [University College London](https://www.ucl.ac.uk){:target="_blank"}
- Research Software Engineer \| January 2024 - August 2024 \| [CERN](https://home.cern){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}, [IRIS-HEP](https://researchcomputing.princeton.edu/research/iris-hep-software-institute){:target="_blank"}
- Visiting Student Researcher (Mitacs Globalink Research Intern) \| June 2023 - August 2023 \| [McMaster University](https://www.mcmaster.ca){:target="_blank"}
- Research Fellow \| June 2022 - September 2022 \| [Institute for Research and Innovation in Software for High Energy Physics](https://researchcomputing.princeton.edu/research/iris-hep-software-institute){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}
- Technical Writer and Open-Source Developer \| May 2022 - October 2022 \| [FluxML](https://fluxml.ai){:target="_blank"}, [Julia Programming Language](https://julialang.org){:target="_blank"}
- Google Summer of Code Developer \| May 2021 - September 2021 \| [PyBaMM (Python Battery Mathematical Modeling)](https://pybamm.org){:target="_blank"}, [NumFOCUS](https://numfocus.org){:target="_blank"}

---

### Education

---

#### [École Polytechnique Fédérale de Lausanne](https://www.epfl.ch/en/){:target="_blank"}
##### Master of Science in Computational Science and Engineering
###### September 2025 - Present | Lausanne, Switzerland

- Coursework: Concurrent computing, Machine Learning, Programming concepts in scientific computing.

---

#### [Swiss National Supercomputing Centre](https://www.cscs.ch){:target="_blank"}
##### Summer University on High-Performance Computing and Data Analytics
###### July 2025 - July 2025 | Remote

- Coursework: GPU architectures, GPU programming (CUDA), Programming model, Memory management, Performance optimization and scientific libraries, GPU-Accelerated Computing with Python, NumPy-like libraries for both CPUs and GPUS computing, Just-in-time compilation from Python code, Distributed workloads on HPC clusters.

---

#### [University of Delhi](https://www.du.ac.in){:target="_blank"}
##### Bachelor of Technology in Computer Science and Mathematics
###### September 2025 - Present | New Delhi, India

- Grade: 9.5/10; department rank: 2/55; DUET 2020 All India Rank: 42/~10,000
- Thesis at CERN: Computational upgrades to the high energy physics analysis pipeline for future LHC/HL-LHC runs.
- Lead Organizer of Convoke 5.0 (annual TechFest) and HashHacks (24-hour-long hackathon) (managed 30+ volunteers and 300+ attendees).
- Involved in leading several official teaching and mentoring workshops organised by CIC, including conducting yearly and one-time workshops. Some of the reports for these workshops are available on CIC’s website and some of them were lost with time.

---

### Full-time experiences

---

#### [Advanced Research Computing Centre](https://www.ucl.ac.uk/advanced-research-computing){:target="_blank"}, [University College London](https://www.ucl.ac.uk){:target="_blank"}
##### Research Software Engineer
###### Dr. Sam Cunliffe
###### June 2025 - September 2025 | London, United Kingdom
- “Generalist” staff member in the Research Software Engineering group of the Advanced Research Computing Centre. Mostly involved with the HPC, DevOps, and Education sub-groups, open-source research theme, and Python tooling.
- Added GPU and auto-differentiation support to large-scale cosmological simulations ([GLASS](https://glass.readthedocs.io/stable/)) for ESA's Euclid space mission  (GPU embedded Computational Science and Engineering grant by EPCC + Euclid space mission grant by the UKSA).
- Involved with porting [UCL's XNAT](https://www.ucl.ac.uk/advanced-research-computing/ucl-xnat-service) service from VMs to an in-house [kubernetes-based cloud infrastructure](https://indico.egi.eu/event/6638/contributions/20466/).
- Audited sustainability and user-behavior of UK's national tier 2 high performance computing cluster ([Young](https://mmmhub.ac.uk/young/)).
- See [/teaching](/teaching) for teaching and community activities.

##### Assistant Research Software Engineer
###### Dr. Sam Cunliffe
###### August 2024 - June 2025 | London, United Kingdom
- Same work, but with less degree of independence/leadership/ownership.

---

#### [CERN](https://home.cern){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}
##### Research Software Engineer
###### Dr. Jim Pivarski (Princeton University)
###### January 2024 - August 2024 | Geneva, Switzerland

- Extended auto-differentiation support for [high-energy physics libraries](https://scikit-hep.org/#basic) operating on ragged and JSON-like data.
- Added symbolic computing support and migrated the [vector manipulation](https://vector.readthedocs.io/en/latest/) backend of [Fermilab's analysis framework](https://coffea-hep.readthedocs.io/en/latest/).
- Implemented a non-uniform rebinning algorithm and CUDA support for [high-energy physics histograms in Python](https://scikit-hep.org/#histogramming).

---

### Research internships

---

#### [McMaster University](https://www.mcmaster.ca){:target="_blank"}
##### Visiting Student Researcher (Mitacs Globalink Research Intern)
###### Prof. Jacques Carette
###### June 2023 - August 2023 | Hamilton, Ontario, Canada

- Worked with functional programming, type theory, and logic to add proofs and algorithms for data containers and mathematical operations in [Agda](https://wiki.portal.chalmers.se/agda/pmwiki.php)'s [standard library](https://github.com/agda/agda-stdlib).
- Significantly reduced library's compile time by refactoring the existing API and simplifying the dependency graph.

---

#### [IRIS-HEP](https://researchcomputing.princeton.edu/research/iris-hep-software-institute){:target="_blank"}, [Princeton University](https://www.princeton.edu){:target="_blank"}
##### Research Fellow
###### Dr. Henry Schreiner (Princeton University), Dr. Jim Pivarski (Princeton University)
###### June 2022 - September 2022 | Remote

- Co-authored a [Python-based Lorentz vector manipulation library](https://vector.readthedocs.io/en/latest/) with support for ragged data and JIT compilation.
- Worked on Scientific Python's developer guides and tools, and fixed bugs in the Scikit-HEP ecosystem.

---

### Other experiences

---

#### [FluxML](https://fluxml.ai){:target="_blank"}, [Julia Programming Language](https://julialang.org){:target="_blank"}
##### Technical Writer and Open-Source Developer
###### Mr. Dhairya Gandhi (Julia Computing / JuliaHub)
###### May 2022 - October 2022 | Remote (Part-Time)

---

#### [PyBaMM (Python Battery Mathematical Modeling)](https://pybamm.org){:target="_blank"}, [NumFOCUS](https://numfocus.org){:target="_blank"}
##### Open-Source Developer (Google Summer of Code)
###### Dr. Valentin Sulzer (Carnegie Mellon University), Dr. Ferran Brosa Planella (University of Warwick), Dr. Robert Timms (University of Oxford)
###### May 2021 - September 2021 | Remote
