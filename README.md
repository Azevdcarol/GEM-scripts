# Genome-Scale Metabolic Modeling Scripts

This repository contains Python scripts and computational workflows developed for **genome-scale metabolic modeling (GEM)**, with a focus on model reconstruction, curation, validation, simulation, and metabolic analysis.

The scripts were developed as part of research in **metabolic engineering and systems biology**, particularly for the study of microbial metabolism and the optimization of metabolite production.

## 🧬 Overview

The repository includes workflows for:

* Genome-scale metabolic model (GEM) reconstruction and curation
* Model quality assessment and validation
* Flux Balance Analysis (FBA)
* Flux Variability Analysis (FVA)
* Metabolic pathway and reaction analysis
* Reaction and metabolite annotation
* Identification of unbounded fluxes and stoichiometrically balanced cycles
* Gene and reaction knockout simulations
* Metabolic engineering analysis
* Visualization of metabolic simulation results
* Export and processing of simulation results

## 🛠️ Main Tools

The analyses use several tools and Python packages commonly employed in constraint-based metabolic modeling:

* [COBRApy](https://github.com/opencobra/cobrapy)
* [CarveMe](https://github.com/cdanielmachado/carveme)
* [MEMOTE](https://github.com/opencobra/memote)
* [Cameo](https://github.com/biosustain/cameo)
* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib

## 📁 Repository Structure ( building...)

```

├── README.md
│
├── reconstruction/
│   ├── model_reconstruction.py
│   └── model_curation.py
│
├── validation/
│   ├── memote_analysis.py
│   ├── unbounded_flux.py
│   └── cycle_analysis.py
│
├── simulations/
│   ├── fba.py
│   ├── fva.py
│   └── knockout_analysis.py
│    
├── visualization/
│   ├── heatmap.py
│   ├── ternary_plot.py
│   └── flux_plot.py
│
│
└── results/
```

> The directory structure may change as the project develops.

## ⚙️ Installation

It is recommended to use a dedicated Python environment.

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

cd YOUR-REPOSITORY

conda create -n mmeg python=3.11
conda activate mmeg
```

Install the main Python dependencies:

```bash
pip install cobra pandas numpy matplotlib jupyter
```

Additional dependencies may be required depending on the specific workflow.

## 🧪 Example

A basic FBA simulation using COBRApy can be performed as follows:

```python
import cobra

model = cobra.io.read_sbml_model("model.xml")

solution = model.optimize()

print("Status:", solution.status)
print("Objective value:", solution.objective_value)
```

## 📊 Analyses

### Flux Balance Analysis

FBA is used to estimate the optimal metabolic flux distribution under defined environmental and physiological constraints.

### Flux Variability Analysis

FVA is used to determine the feasible range of fluxes for individual reactions while maintaining a specified fraction of the optimal objective value.

### Model Validation

Model quality is evaluated using approaches such as:

* MEMOTE
* Flux variability analysis
* Detection of unbounded reactions
* Identification of stoichiometrically balanced cycles
* Mass and charge balance analysis
* Reaction directionality analysis

### Metabolic Engineering

The repository also contains scripts for evaluating the effects of reaction and gene knockouts on metabolic phenotypes and product formation.

## 🔬 Research Context

These scripts are being developed in the context of research involving **microbial metabolism, metabolic engineering, and genome-scale metabolic models**.

## 📌 Notes

The scripts in this repository are primarily intended for **research and educational purposes**. Specific workflows may depend on the metabolic model, solver, database, and computational environment used.

Model files and experimental datasets may be omitted from the repository when subject to licensing, database, or project-specific restrictions.

## 📚 References

The following resources provide background on the tools and methods used in this repository:

* COBRApy: https://github.com/opencobra/cobrapy
* MEMOTE: https://github.com/opencobra/memote
* CarveMe: https://github.com/cdanielmachado/carveme
* Cameo: https://github.com/biosustain/cameo

## 👩‍🔬 Author

**Caroline Azevedo de Araújo**

Research in bioinformatics, systems biology, and genome-scale metabolic modeling.
