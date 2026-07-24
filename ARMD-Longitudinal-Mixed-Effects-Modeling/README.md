# Linear Mixed-Effects Modeling of Visual Acuity in an Age-Related Macular Degeneration Clinical Trial

## Overview

This project presents a complete longitudinal data analysis workflow using **linear mixed-effects models** to investigate visual acuity trajectories in patients with **age-related macular degeneration (ARMD)**.

The analysis is based on data from a multicenter randomized clinical trial evaluating the effect of **interferon alfa-2a treatment** on visual acuity over a 52-week follow-up period.

The main objective was to characterize changes in visual acuity over time while accounting for the correlation induced by repeated measurements within the same patient.

This project demonstrates the application of statistical modeling techniques commonly used in **clinical research, biostatistics, and longitudinal data analysis**.

---

## Project Goals

The analysis aimed to:

- Explore longitudinal visual acuity patterns across treatment groups.
- Evaluate missing data patterns and their implications for longitudinal modeling.
- Transform and prepare repeated-measures clinical data for analysis.
- Assess within-subject correlation and variability structures.
- Develop and compare several linear mixed-effects models.
- Select the most appropriate model based on goodness of fit, complexity, and clinical interpretability.
- Perform model diagnostics and evaluate statistical assumptions.

---

## Dataset Description

A subset of **150 patients** was randomly selected from the original ARMD clinical trial dataset.

Each patient had repeated visual acuity measurements collected at:

- Baseline (week 0)
- Week 4
- Week 12
- Week 24
- Week 52

Main variables:

| Variable | Description |
|---|---|
| `subject` | Patient identifier |
| `visual0` | Baseline visual acuity |
| `visual4` | Visual acuity at week 4 |
| `visual12` | Visual acuity at week 12 |
| `visual24` | Visual acuity at week 24 |
| `visual52` | Visual acuity at week 52 |
| `treat.f` | Treatment group |
| `miss.pat` | Missing data pattern |

---

## Methodology

### 1. Data Preparation

The original dataset was provided in **wide format** and transformed into **long format** to facilitate longitudinal analysis.

Steps included:

- Reshaping repeated measurements.
- Creating a time variable.
- Retaining baseline visual acuity as a covariate.
- Preparing data for mixed-effects modeling.

---

### 2. Exploratory Data Analysis

Exploratory analyses included:

- Descriptive statistics by treatment group and follow-up time.
- Mean and median visual acuity comparisons.
- Individual trajectory plots.
- Boxplots across follow-up visits.
- Assessment of missing data patterns.

Main observations:

- Considerable variability existed between patients.
- Measurements closer in time showed stronger correlation.
- Visual acuity tended to decline throughout follow-up.
- Missing observations increased at later visits.

---

## Statistical Modeling Approach

Because measurements were repeatedly collected from the same individuals, observations were not independent.

A sequence of linear mixed-effects models was evaluated using the `nlme` R package.

The general model structure was:

\[
Visual_{it} =
Fixed\ Effects +
Random\ Effects +
Residual\ Error
\]

where:

- Fixed effects captured population-level trends.
- Random effects accounted for patient-specific variability.
- Residual structures modeled within-subject variability.

---

## Models Compared

### Model 1 — Random Intercept Model

Included:

- Baseline visual acuity
- Time
- Treatment
- Treatment × Time interaction
- Patient-specific random intercept

Purpose:

Evaluate individual differences in baseline visual acuity.

---

### Model 2 — Time-Dependent Variance Model

Added:

- Heterogeneous residual variance over time (`varPower`)

Purpose:

Account for increasing variability during follow-up.

---

### Model 3 — Random Intercept + Random Slope

Added:

- Patient-specific time trajectories

Purpose:

Allow patients to have different rates of visual acuity change.

---

### Model 4 — Uncorrelated Random Effects

Modified the previous model by assuming:

- No correlation between random intercept and random slope.

Purpose:

Evaluate whether the additional correlation improved model fit.

---

### Final Model Selection

Models were compared using:

- Akaike Information Criterion (AIC)
- Likelihood ratio tests
- Residual diagnostics
- Clinical interpretability

The final selected model included:

- Baseline visual acuity adjustment
- Time effect
- Treatment effect
- Random intercept
- Random slope for time
- Time-dependent residual variance

---

# Key Findings

## Baseline Visual Acuity

Baseline visual acuity was the strongest predictor of future measurements.

Patients with higher initial visual acuity tended to maintain higher values throughout follow-up.

---

## Time Effect

A significant decline in visual acuity was observed over the study period.

The temporal evolution was not identical among patients, supporting the inclusion of random slopes.

---

## Treatment Effect

No strong evidence of a beneficial treatment effect was identified.

The treatment group showed a slightly different trajectory compared with placebo, but the clinical interpretation requires caution.

---

## Patient-Level Variability

Substantial heterogeneity existed between individuals:

- Patients differed in baseline visual acuity.
- Patients showed different rates of change over time.

This variability justified the use of mixed-effects models.

---

# Model Diagnostics

The final model was evaluated through:

- Pearson residual plots.
- Residual distribution assessment.
- Normal Q-Q plots.
- Random effects diagnostics.
- Observed vs predicted trajectories.

Overall:

- Residual patterns were acceptable.
- No major violations of assumptions were detected.
- The model adequately captured population and individual-level variability.

---

# Tools & Technologies

## Programming Language

- R

## Main Packages

- `nlme` — Linear mixed-effects modeling
- `tidyverse` — Data manipulation and visualization
- `ggplot2` — Data visualization
- `lattice` — Statistical graphics
- `RLRsim` — Restricted likelihood ratio tests

## Statistical Methods

- Longitudinal data analysis
- Linear mixed-effects models
- Random intercept models
- Random slope models
- Variance structure modeling
- Missing data pattern analysis
- Model comparison and diagnostics

---


# Reproducibility

All analyses were performed in R using reproducible code.

The complete workflow includes:

1. Data preparation
2. Exploratory analysis
3. Model development
4. Model comparison
5. Diagnostics
6. Interpretation

---

# Skills Demonstrated

This project demonstrates experience with:

- Clinical trial data analysis
- Longitudinal modeling
- Statistical inference
- Mixed-effects models
- Reproducible research workflows
- R programming
- Scientific reporting
- Data visualization

---

# References

- Gałecki, A., & Burzykowski, T.  
  *Linear Mixed-Effects Models Using R: A Step-by-Step Approach.*

- Arnau Gras, J., & Bono Cabré, R. (2008).  
  Longitudinal studies: design and analysis models.  
  *Escritos de Psicología.*

- Pinheiro et al.  
  `nlme`: Linear and Nonlinear Mixed Effects Models in R.

---

## Author

**Giselle Piro Martino**

Portfolio project focused on longitudinal statistical modeling and clinical data analysis.
