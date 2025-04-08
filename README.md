# README
# Acute Myeloid Leukemia Heatmap Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Analysis of RNA-seq data from acute myeloid leukemia (AML) mouse models using clustering heatmaps.

## Overview

This repository contains an analysis pipeline for visualizing gene expression patterns in AML mouse models using hierarchical clustering heatmaps. The analysis focuses on identifying gene expression patterns across different treatment conditions and mutations.

## Key Features

* RNA-seq data analysis from 19 AML model mice samples
* Hierarchical clustering with heatmap visualization
* Treatment condition and mutation annotations
* Gene variance filtering for significant genes
* Reproducible workflow with R Markdown

## Dataset Information

* Source: [refine.bio](https://www.refine.bio/)
* Accession: SRP070849
* Samples: 19 AML model mice
* Data Type: Quantile normalized RNA-seq expression data
* Original Study: Shih et al., 2017 ([PubMed ID: 28193779](https://pubmed.ncbi.nlm.nih.gov/28193779/))

## Dependencies

Required R packages:
```r
library(pheatmap)
library(magrittr)
library(readr)
library(dplyr)
library(tibble)
library(sessioninfo)
```

## Analysis Pipeline

1. Data Preparation
   - Sample organization
   - Metadata processing
   - Gene expression matrix loading

2. Data Processing
   - Gene variance calculation
   - Top quartile gene selection
   - Sample ordering synchronization

3. Visualization
   - Hierarchical clustering
   - Custom color scaling
   - Annotation overlay

## Directory Structure
```markdown
project_root/
├── data/
│   └── SRP070849/
│       ├── SRP070849.tsv
│       └── metadata_SRP070849.tsv
├── plots/
│   └── aml_heatmap.png
└── results/
    └── top_90_var_genes.tsv
```

## Usage

1. Clone the repository
2. Create the required directories using the setup code
3. Download the dataset from [refine.bio](https://www.refine.bio/)
4. Run the analysis pipeline

## Output Files

* `aml_heatmap.png`: Hierarchical clustering heatmap
* `top_90_var_genes.tsv`: Genes selected by variance filtering

## Acknowledgments

This analysis was adapted from the [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html) and modified for this repository by Candace Savonen.

## License

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.