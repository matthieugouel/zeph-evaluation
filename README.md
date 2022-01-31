# 🌬️ Zeph — Evaluation

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/dioptra-io/zeph-evaluation/HEAD)

This repository contains the code used to produce the results of the evalution section of the *Zeph & Iris* paper.

The Python notebooks provided in this repository allow you to:
- perform your own measurements from the [Iris platform](https://iris.dioptra.io) to reproduce the dataset used in the paper
- reproduce the analysis presented in the paper, either on your own dataset, or on the original dataset used in the paper

In addition, the source code of Zeph and Iris are available in the [`dioptra-io/zeph`](https://github.com/dioptra-io/zeph) and [`dioptra-io/iris`](https://github.com/dioptra-io/iris) repositories.

## 🧪 Experiments

Two notebooks are provided for each experiments: the *execution notebook* which contains the code to perform the measurements, and the *analysis notebook* which contains the code to analyse the measurement results and generate the plots.

### Prerequisites

1. Copy the sample configuration file [`config.example.json`](config.example.json) to `config.json` and fill-in your Iris credentials.
2.  Download [`zeph-evaluation-dataset.tar.gz`](https://minio.iris.dioptra.io/public/zeph-evaluation-dataset.tar.gz) (650MB) and extract it at the root of the repository:
```bash
wget https://minio.iris.dioptra.io/public/zeph-evaluation-dataset.tar.gz
tar xf zeph-evaluation-dataset.tar.gz
```

### Experiment 1

> **Hypothesis**  
> Zeph will be able to see almost the same as complete discovery
(= full IPv4 routable prefixes) but with a much-reduced probing budget.


* Execution notebook: [exp1_experiment.ipynb](exp1_experiment.ipynb)
* Analysis notebook: [exp1_analysis.ipynb](exp1_analysis.ipynb)

### Experiment 2

> **Hypothesis**  
> For the same per-agent probing budget, allocating prefixes to agents based on an adaptive approach
(with the possibility of a prefix to be probed from any number from 0 to n agents)
will allow more to be discovered than allocating prefixes to agents randomly (with each prefix being probed from precisely one agent).

* Execution notebook: [exp2_experiment.ipynb](exp2_experiment.ipynb)
* Analysis notebook: [exp2_analysis.ipynb](exp2_analysis.ipynb)

### Experiment 3

> **Hypothesis**  
> Zeph will work at scale with Diamond-Miner. 

* Execution notebook: [exp3_experiment.ipynb](exp3_experiment.ipynb)
* Analysis notebook: [exp3_analysis.ipynb](exp3_analysis.ipynb)

### Exploitation analysis

> **Hypothesis**  
> The exploitation budget of Zeph will be responsible of the most part of nodes and links discoveries. 

* Execution notebook: based on one experiment of [exp1_experiment.ipynb](exp1_experiment.ipynb)
* Analysis notebook: [exploitation_analysis.ipynb](exploitation_analysis.ipynb)

## 📚 Publications

```
```
