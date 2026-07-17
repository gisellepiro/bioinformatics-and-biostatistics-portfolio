# Survival Analysis of HIV Acquisition Risk Factors

## Overview

This project investigates demographic, behavioral, and socioeconomic determinants of HIV acquisition using survival analysis techniques in a longitudinal cohort study conducted between 2014 and 2019.

The analysis combines semi-parametric and parametric survival models to identify factors associated with HIV acquisition risk and to evaluate how these effects evolve over time.

## Dataset

The study included 9,503 individuals followed between 2014 and 2019.

Available variables included:

- Age group
- Gender
- Educational level
- Region of origin
- Number of casual sexual partners
- Chemsex practices
- Methamphetamine use
- GHB use
- Mephedrone use
- Time to HIV acquisition or censoring

## Objectives

- Identify factors associated with HIV acquisition risk.
- Evaluate interactions between demographic and behavioral variables.
- Assess socioeconomic inequalities in HIV acquisition.
- Verify the proportional hazards assumption.
- Compare semi-parametric and parametric survival models.
- Estimate adjusted survival probabilities across population subgroups.

## Methods

### Survival Analysis

- Kaplan-Meier estimation
- Adjusted survival curves
- Median survival estimation

### Cox Proportional Hazards Models

- Stratified Cox regression
- Interaction modeling
- Reduced multivariable models
- Hazard ratio estimation

### Model Diagnostics

- Schoenfeld residuals
- Harrell-Lee proportional hazards test
- Complementary log-log diagnostics
- Time-dependent covariate analysis

### Parametric Survival Models

- Weibull regression
- Exponential survival models
- Model comparison and simplification

## Main Findings

- Chemsex practices were strongly associated with increased HIV acquisition risk.
- The effect of chemsex was particularly pronounced among individuals younger than 25 years.
- Methamphetamine use emerged as the strongest predictor of HIV acquisition.
- Individuals reporting fewer casual sexual partners showed substantially lower risk.
- No strong evidence of socioeconomic inequalities according to educational level was identified after adjustment.
- The proportional hazards assumption was reasonably satisfied for all included covariates.

## Tools and Packages

- R
- survival
- survminer
- SurvRegCensCov
- dplyr
- ggplot2

## Skills Demonstrated

- Survival analysis
- Cox proportional hazards modeling
- Parametric survival models
- Interaction analysis
- Model diagnostics
- Time-dependent covariates
- Epidemiological data analysis

## Author

Giselle Piro Martino

MSc Bioinformatics and Biostatistics
