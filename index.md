

<h1 id="links">Quick Links</h1>

- [Paper](#paper)
- [Supplementary Materials](#supplementary-materials)
- [Project Code](#project-code)
- [Simulation and Datasets](#simulation-and-datasets)
  - [Electrostatic Potential (ESP)](#electrostatic-potential-esp)
  - [Heat Diffusion](#heat-diffusion)
- [Citation](#citation)
  - [ACM Reference Format](#acm-reference-format)
  - [ACM Reference BibTeX](#acm-reference-bibtex)

---

<h1 id="paper">Inverse Design for Generating Initial Conditions in Scientific Simulations</h1>

> Leslie Horace, Christin Whitton, Vanessa Job, William Jones, Nathan DeBardeleben  
> SC Workshops '25 | St Louis, MO, USA | November 17, 2025  
> **DOI:** `10.1145/3731599.3767343` | **LA-UR:** `LA-UR-25-28137`

<img src="./figures/acm_doi_qr_code.svg" width="22%" alt="DOI QR code"/>

---

<h2 id="supplementary-materials">Supplementary Materials</h2>

<h3 id="project-code">Project Code</h3>

- **Code release:** `Coming soon!` 

> Please refer to Readme.md for reproducing paper experiments.

<h3 id="simulation-and-datasets">Simulation and Datasets</h3>

<h3 id="electrostatic-potential-esp">Electrostatic Potential (ESP)</h3>

- **Dataset download:** https://oceans11.lanl.gov/electrostaticEquations/  
  
    <img src="./figures/electrostatic_dataset_qr_code.svg" width="22%" alt="Electrostatic dataset QR code"/>

- **Simulation code:** https://github.com/lezahlie/esp_simulation/releases/tag/v2.4.1

    > Reproduce the dataset:
    > ```bash
    > python esp_simulation/create_dataset.py \
    >   --output-path="path/to/datasets" \
    >   --output-folder="electrostatic_dataset_1k" \
    >   --min-seed=1 \
    >   --max-seed=1000 \
    >   --seed-step=100 \
    >   --ntasks=1 \
    >   --image-size=32 \
    >   --max-iterations=2000 \
    >   --convergence-tolerance=1e-4 \
    >   --conductive-cell-prob=0.5 \
    >   --conductive-material-range=1,10 \
    >   --save-states="first-20,interval-100"
    > ```

---

<h3 id="heat-diffusion">Heat Diffusion</h3>



- **Dataset download:** Paper Experiments Dataset (same host as above)  

    <img src="./figures/heat_dataset_qr_code.svg" width="22%" alt="Heat diffusion dataset QR code"/>

- **Simulation code:** https://github.com/lezahlie/heat_diffusion_simulation/releases/tag/v1.0.0

    > Reproduce the dataset:
    > ```bash
    > python heat_diffusion_simulation/create_dataset.py \
    >   --output-path="path/to/datasets" \
    >   --output-folder="heat_diffusion_dataset_1k" \
    >   --min-seed=1 \
    >   --max-seed=1000 \
    >   --seed-step=100 \
    >   --ntasks=1 \
    >   --grid-length=32 \
    >   --max-iterations=5000 \
    >   --boundary-condition="neumann" \
    >   --solver-name="crank_nicolson" \
    >   --convergence-tolerance=1e-4 \
    >   --save-states="first-20,interval-100"
    > ```


<h2 id="citation">Citation</h2>


<h3 id="acm-reference-format">ACM Reference Format</h3>

> Leslie Horace, Christin Whitton, Vanessa Job, William Jones, and Nathan DeBardeleben. 2025. Inverse Design for Generating Initial Conditions in Scientific Simulations. In Workshops of the International Conference for High Performance Computing, Networking, Storage and Analysis (SC Workshops '25), November 16-21, 2025, St Louis, MO, USA. ACM, New York, NY, USA 8 Pages. https://doi.org/10.1145/3731599.3767343

<h3 id="acm-reference-bibtex">ACM Reference BibTeX</h3>

```bibtex
@inproceedings{10.1145/3731599.3767343,
author = {Horace, Leslie and Whitton, Christin and Job, Vanessa and Jones, William and DeBardeleben, Nathan},
title = {Inverse Design for Generating Initial Conditions in Scientific Simulations},
year = {2025},
isbn = {9798400718717},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3731599.3767343},
doi = {10.1145/3731599.3767343},
abstract = {We propose a conditional normalizing flow (CNF) surrogate model to solve generative, many-to-one inverse problems in scientific simulations governed by partial differential equations (PDEs) with time-evolving interactions between heterogeneous materials. We present two case studies: electrostatic potential and heat diffusion, which serve as proxy simulations for generating diverse sets of initial conditions that can reproduce an observed output state (transient or steady). Finally, we provide a comprehensive overview of the synthetic datasets, the model specification, each stage of the experimental workflow, evaluation of training performance, and uncertainty quantification for the generated samples.},
booktitle = {Proceedings of the SC '25 Workshops of the International Conference for High Performance Computing, Networking, Storage and Analysis},
pages = {29–36},
numpages = {8},
keywords = {generative inverse design, machine learning surrogate modeling, conditional normalizing flow (CNF), negative log-likelihood (NLL)},
location = {
},
series = {SC Workshops '25}
}
```