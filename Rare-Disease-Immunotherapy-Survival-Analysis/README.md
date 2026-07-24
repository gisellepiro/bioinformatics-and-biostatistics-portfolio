# Survival Analysis of a Simulated Immunotherapy Trial

This project presents a survival analysis of a simulated clinical trial evaluating an experimental immunotherapy for patients with a rare disease.

The analysis was developed in **R** as part of a Master's degree in Data Science and focuses on the implementation of classical survival analysis techniques, combining manual calculations with R packages for validation.

## Project Overview

The dataset contains survival information for **10 patients** divided into two groups:

- **Treatment:** Experimental immunotherapy
- **Control:** Placebo

Several observations are right-censored and are incorporated into the analysis using standard survival analysis methods.

## Methods

The project includes:

- Manual computation of the **Kaplan–Meier estimator**
- **Greenwood variance** estimation
- Construction of **95% confidence intervals**
- Kaplan–Meier survival curves using the **survival** package
- **Restricted Mean Survival Time (RMST)** estimation
- Manual implementation of the **Log-Rank test**
- Comparison with additional weighted survival tests:
  - Wilcoxon (Gehan)
  - Tarone–Ware
  - Peto–Peto
  - Discussion of the Fleming–Harrington test

## Main Results

- The treatment group showed higher estimated survival probabilities throughout follow-up.
- The estimated RMST was larger for the treatment group (14.1 vs. 10.4 months).
- None of the statistical tests found a significant difference between groups (*p* > 0.05).
- The observed trend toward improved survival is likely limited by the very small sample size.

## Technologies

- R
- survival
- survRM2
- PHInfiniteEstimates


## Notes

This project intentionally includes several manual calculations (Kaplan–Meier estimator, Greenwood variance, confidence intervals, and Log-Rank statistic) to demonstrate the underlying methodology before validating the results with R packages.

The Fleming–Harrington test could not be executed because the packages referenced in the original course material are no longer compatible with current R versions. The repository documents the attempted implementation and discusses this limitation.

## Author

**Giselle Piro Martino**
