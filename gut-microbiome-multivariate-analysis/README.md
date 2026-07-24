# Gut Microbiome Analysis in Type 2 Diabetes

Multivariate statistical analysis of gut microbiome data from patients with Type 2 Diabetes (T2D) and healthy controls using R.

This project reproduces and extends part of the analyses presented in:

> Qin J. et al. (2012). *A metagenome-wide association study of gut microbiota in type 2 diabetes*. Nature.

---

## Project Overview

The objective of this project is to explore whether gut microbiome composition differs between individuals with Type 2 Diabetes and healthy controls using multivariate statistical methods.

The analysis was performed on a balanced subset of 60 individuals (30 T2D and 30 healthy controls) from the **curatedMetagenomicData** Bioconductor package.

---

## Methods

The project includes:

- Data preprocessing and feature filtering
- Diversity analysis (Species Richness and Shannon Index)
- Principal Component Analysis (PCA)
- Non-metric Multidimensional Scaling (NMDS)
- Correspondence Analysis (CA)
- Outlier detection using Euclidean and Mahalanobis distances
- Interpretation of microbiome composition by disease group

---

## Dataset

Source:

- **curatedMetagenomicData** (Bioconductor)
- Dataset:
  `2021-10-14.QinJ_2012.relative_abundance`

The original publication is:

Qin J. et al. (2012). *Nature* 490:55–60.

---

## Technologies

- R
- Bioconductor
- curatedMetagenomicData
- SummarizedExperiment
- vegan
- FactoMineR
- factoextra
- corpcor
- ggplot2

---

## Main Findings

- No clear multivariate separation between T2D and healthy controls.
- PCA and NMDS showed substantial overlap between groups.
- Correspondence Analysis identified significant differences in bacterial phylum composition.
- Results are consistent with the moderate dysbiosis reported in the original publication.


---

## Author

Giselle Piro Martino
