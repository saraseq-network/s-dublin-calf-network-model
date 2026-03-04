# Salmonella Dublin calf movement network model

This repository contains the R code used to simulate transmission of *Salmonella Dublin* across a network of calf movements in the United States.

The model integrates:

- empirical calf movement networks
- environmental transmission
- carrier dynamics
- targeted biosecurity interventions

The model was developed as part of the PhD dissertation of **Sara C. Sequeira** at The Ohio State University.

---

## Software requirements

The model was implemented in **R (version 4.5.1)**.

Required packages:

- tidyverse
- ggplot2
- igraph
- sf
- rnaturalearth

---

## Repository structure

salmonella-dublin-calf-network-model/
├── R/
│   ├── model_core.R              # run_resSICR(), draw_movers(), pick_seed_zips(), etc.
│   ├── network_metrics.R         # high-centrality ZIP selection helpers (optional)
│   └── utils.R                   # small helpers (median_ci, clamp01, etc.)
│
├── scripts/
│   ├── 00_make_example_data.R    # generates data_example/*.csv (so repo runs out-of-box)
│   ├── 01_run_simulation.R       # loads example data + runs baseline scenarios
│   ├── 02_calibration_beta.R     # your Calibration_B1 logic
│   └── 03_figures_results.R      # your Figures:Results logic
│
├── data_example/
│   ├── movement_data.csv
│   └── zip_herd_sizes_us.csv
│
├── output/                       # gitignored (where results are written)
├── figures/                      # can include 1–2 example outputs (optional)
├── README.md
├── LICENSE
├── .gitignore
└── CITATION.cff                  # optional but nice

---

## Data availability

Raw livestock movement data cannot be publicly shared yet due to data-use agreements.

Example input files are provided to illustrate the model structure and allow code execution.

---


## Author

Sara C. Sequeira  
PhD Candidate – Veterinary Epidemiology  
The Ohio State University


