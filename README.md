# Squidpy for NEP comparison (counts and z-scores)
Squidpy's nbh_enrichment function from Palla et al. 2022 for NEP comparison. https://www.nature.com/articles/s41592-021-01358-2

# Introduction

Squidpy finds statistically enriched NEPs between cell phenotypes in cellular neighborhoods. The original method uses Delaunay graph or distance for neighborhood definition. We performed NEP using the nbh_enrichment function extracting counts an z-scores for downstream comparison. 

# Installation

We ran Squidpy 1.6.1 with Python version 3.10.15 and installed it with 

```
pip install squidpy
```

## Dependencies


## Source

The script was written following this tutorial by the authors https://squidpy.readthedocs.io/en/stable/notebooks/examples/graph/compute_nhood_enrichment.html

## Usage

The input path and output path need to be set at the top of the script.
The scripts in the folder scripts were used to create the results on simulated data (scripts/squidpy_simulation_nbh_enrichment.ipynb) and the myocardial infarction dataset from Wuennemann et al. (scripts/squidpy_MI_nbh_enrichment.ipynb) in the Schiller et al. (2025) manuscript on NEP comparison. 
The script was run on an M2 MacBookPro. 
