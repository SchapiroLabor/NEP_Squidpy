# Squidpy and CellCharter for NEP comparison
Squidpy's nhood_enrichment function from Palla et al. 2022 (https://www.nature.com/articles/s41592-021-01358-2) and CellCharter's nhood_enrichment function from Varrone et al. (2023) (https://www.nature.com/articles/s41588-023-01588-4) for NEP comparison. 

# Introduction

Squidpy's nhood_enrichment function finds statistically enriched NEPs between cell phenotypes in cellular neighborhoods. We performed NEP using the nhood_enrichment function extracting counts and z-scores for downstream comparison. 
CellCharter offers a nhood_enrichment function that calculates asymmetric NEPs between cells that belong to priorly defined niches. We run the function with inputting phenotype labels as clusters instead of niches. 

# Usage

## Installation

### Squidpy
We ran Squidpy 3.10.15 with Python version 3.10.15 and installed it with 

```
conda create -n "cellcharter_env" python=3.10.15
conda activate cellcharter_env
pip install squidpy==3.10.15
pip install ipykernel==6.29.5
conda install jupyter==1.1.1
```
### CellCharter
We ran CellCharter 0.3.3 with python version 3.9.21 The environment was created with: 
```
conda create -n "cellcharter_env" python=3.9.21
conda activate cellcharter_env
pip install cellcharter==0.3.3
pip install ipykernel==6.29.5
conda install jupyter==1.1.1
```
The scripts were run on an M2 MacBookPro.

## Source

The Squidpy script was written following this tutorial by the authors https://squidpy.readthedocs.io/en/stable/notebooks/examples/graph/compute_nhood_enrichment.html

## Data

### In silico tissue (IST) data
Simulated .csv data with x, y, and ct annotation columns were used. The asymmetric and symmetric in silico tissue (IST) datasets were generated as described here: https://github.com/SchapiroLabor/NEP_IST_generation. 

### Myocardial infarction (MI) data

UPDATE PATH

## Scripts

`/notebooks`:
- `/MI_data`: 
    - `/cellcharter_MI_nbh_enrichment.ipynb`: This script runs CellCharter's nhood_enrichment function with phenotypes as clusters on the MI data using a knn (k=5) as neighborhood definition. Depending on the only-inter paramter set by the user, it includes or excludes links of homotypic interactions.   
    - `/squidpy_MI_nbh_enrichment.ipynb`: This script runs Squidpy's nhood_enrichment function with phenotypes as lables on the MI data using a knn (k=5) as neighborhood definition. It outputs both, z-scores and the interaction counts.
- `/simulation_data`: 
    - `/ct_abundances_differences_appendix.ipynb`: This script runs scimap on the MI data using a knn (k=5) as neighborhood definition. 
    - `/cellcharter_simulation_nbh_enrichment.ipynb`: This script runs CellCharter's nhood_enrichment function with phenotypes as clusters on the simulated data (asymmetric or symmetric) using a Delaunay triangulation as neighborhood definition. Depending on the only-inter paramter set by the user, it includes or excludes links of homotypic interactions.  
    - `/squidpy_simullation_nbh_enrichment.ipynb`: This script runs Squidpy's nhood_enrichment function with phenotypes as lables on the simulated data (asymmetric or symmetric) using a Delaunay triangulation as neighborhood definition. It outputs both, z-scores and the interaction counts.
