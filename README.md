# Milk Supply Chain AMR Emergence Model

Authors: [Muhammad Tulat Fiaz](https://github.com/TalatFiaz454) and [Furqan Awan](https://github.com/furqan915)

Supervisor: [Furqan Awan](https://github.com/furqan915)

An agent-based model (ABM) simulating the emergence of antimicrobial resistance (AMR) through horizontal gene transfer (HGT) during milk aggregation, transport, and storage.

## Model Workflow

Farm → Transport → Storage → Raw milk supply or Processing entry

During the transport stage, milk batch agents interact within a mixing pool and may acquire additional AMR genes through horizontal gene transfer. Bacterial loads increase during transport and storage, followed by branching into raw-milk supply or processing entry.

## Model Parameters

The model represents 30 farms with 6 milk batches per farm, giving 180 milk-batch agents in the main simulation setup.

Key parameters include:

* Initial bacterial load: 10³–10⁴
* Initial AMR genes: 0, 1, or 2; high-AMR farms may start with 2 or 3
* High-AMR farms: 10%
* Growth rate: 0.4 per simulation step
* Raw-milk pathway fraction: 0.5
* HGT density threshold: 5 × 10⁵
* HGT probability: 0, 0.05, 0.10, and 0.20

HGT occurs during the transport stage. The effective HGT probability depends on the specified HGT probability and the combined bacterial load of interacting milk batches.

## Simulation Setup

The model uses four specified HGT probability levels:

* 0
* 0.05
* 0.10
* 0.20

The simulation framework allows multiple runs using different random seeds. Each simulation is run for 3 time steps.

The model tracks:

* AMR gene states of milk batches
* Bacterial load
* HGT interactions
* Number of AMR genes
* Milk-batch movement through the supply chain
* Raw-milk supply and processing-entry pathways

## Files

### `agents.py`

Defines the milk batch agents, including bacterial growth, AMR gene states, HGT interactions, and movement through the milk supply chain.

### `model.py`

Defines the ABM-1 model structure, simulation parameters, initialization of milk batches, transport-stage mixing, and model calculations.

### `run.py`

Runs a single demonstration simulation of the model.

### `multi_run.py`

Runs the model across the specified HGT probability levels using multiple simulation runs.

### `plot_hgt_calibration.py`

Contains code for generating HGT-related visualizations.

### `plot_ABM1_multi_panel_figure.py`

Contains code for generating model visualizations.

### `requirements.txt`

Lists the Python packages required to run the model.

## Reproducibility

The repository contains the model code, simulation scripts, analysis scripts, and required Python packages needed to reproduce the computational workflow.

The software release is also archived in Zenodo.

## Citation

If you use this model or code in your research, please cite the associated research paper and software release.

Fiaz, M.T., M.H. Mushtaq, F. Awan and A. Riaz (2026). Detection of Multidrug-Resistant Milk-Associated Psychrotrophic Pseudomonas spp. Using Lab-Based and Agent-Based Modeling Approaches in Pakistan. J. Anim. Plant Sci.

Fiaz, M.T. and F. Awan (2026). Milk Supply Chain AMR Emergence Model (Version v1.0.0). Zenodo. DOI: 10.5281/zenodo.22773612

The paper DOI will be added after publication.

## Authors and Supervision

* [Muhammad Tulat Fiaz](https://github.com/TalatFiaz454) — Student researcher; data collection, analysis, organization, and documentation
* [Furqan Awan](https://github.com/furqan915) — Academic supervisor; model development and implementation

## Code Use and Attribution

If you use, modify, or build upon this code, please acknowledge the original work and cite the associated research paper and software release.

Please do not present this code, model, or substantial parts of it as your own original work.

## License

This project is released under the MIT License.








