## Important Notice
**DUE TO SUPPORT ISSUES, IRIS IS NOT CURRENTLY AVAILABLE AS A SERVICE TO THE PUBLIC TO RUN THEIR MEASUREMENTS.
WE HOPE TO MAKE IRIS AVAILABLE AGAIN TO THE PUBLIC IN THE NEAR FUTURE.**

# 🌬️ Zeph — Evaluation

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/dioptra-io/zeph-evaluation/HEAD)

This repository contains the code used to produce the results of the evalution section of the *Zeph & Iris* paper.

The Python notebooks provided in this repository allow you to:
- perform your own measurements from the [Iris platform](https://iris.dioptra.io) to reproduce the dataset used in the paper
- reproduce the analysis presented in the paper, either on your own dataset, or on the original dataset used in the paper

In addition, the source code of Zeph and Iris are available in the [`dioptra-io/zeph`](https://github.com/dioptra-io/zeph) and [`dioptra-io/iris`](https://github.com/dioptra-io/iris) repositories.

## 🧪 Experiments

### Prerequisites

1. Copy the sample configuration file [`config.example.json`](config.example.json) to `config.json` and fill-in your Iris credentials.
2.  Download [`zeph-evaluation-dataset.tar.gz`](https://minio.iris.dioptra.io/public/zeph-evaluation-dataset.tar.gz) (650MB) and extract it at the root of the repository:
```bash
curl -L https://minio.iris.dioptra.io/public/zeph-evaluation-dataset.tar.gz | tar x
```

### Notebooks

Two notebooks are provided for each section: the *execution notebook* which contains the code to perform the measurements, and the *analysis notebook* which contains the code to analyse the measurement results and generate the plots.

Section | Execution | Analysis
--------|-----------|---------
§6.2.1 — Zeph's reinforcement learning approach outperforms random allocation | [`zeph_allocation_execution.ipynb`](notebooks/zeph_allocation_execution.ipynb) | [`zeph_allocation_analysis.ipynb`](notebooks/zeph_allocation_analysis.ipynb)
§6.2.2 — Zeph/Iris conducting multipath traceroutes performs competitively with respect to current state-of-the-art internet scale topology discovery systems | [`zeph_topology_execution.ipynb`](notebooks/zeph_topology_execution.ipynb) | [`zeph_topology_analysis.ipynb`](notebooks/zeph_topology_analysis.ipynb)
§6.3 — Zeph probe savings | [`zeph_savings_execution.ipynb`](notebooks/zeph_savings_execution.ipynb) | [`zeph_savings_analysis.ipynb`](notebooks/zeph_savings_analysis.ipynb)
§6.4 — Reinforcement learning analysis | [`zeph_savings_execution.ipynb`](notebooks/zeph_savings_execution.ipynb) | [`rl_analysis.ipynb`](notebooks/rl_analysis.ipynb)

## 📚 Publications

```bibtex
@article{10.1145/3523230.3523232,
author = {Gouel, Matthieu and Vermeulen, Kevin and Mouchet, Maxime and Rohrer, Justin P. and Fourmaux, Olivier and Friedman, Timur},
title = {Zeph &amp; Iris Map the Internet: A Resilient Reinforcement Learning Approach to Distributed IP Route Tracing},
year = {2022},
issue_date = {January 2022},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
volume = {52},
number = {1},
issn = {0146-4833},
url = {https://doi.org/10.1145/3523230.3523232},
doi = {10.1145/3523230.3523232},
journal = {SIGCOMM Comput. Commun. Rev.},
month = {mar},
pages = {2–9},
numpages = {8},
keywords = {active internet measurements, internet topology}
}
```
