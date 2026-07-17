# Mortality Prediction in U.S. Metropolitan Areas

## Overview

This project investigates the determinants of mortality rates across metropolitan areas in the United States using classical and robust regression techniques.

The analysis focuses on regression diagnostics, multicollinearity assessment, variable selection and robust estimation strategies to identify the most important predictors of mortality while ensuring model interpretability and stability.

## Dataset

The study uses the historical metropolitan mortality dataset compiled by McDonald and Schwing (1973), containing mortality measurements and fifteen explanatory variables from 60 U.S. metropolitan areas.

Variables include:

- Climate indicators
- Air pollution measurements
- Population characteristics
- Socioeconomic variables
- Housing quality indicators

## Objectives

- Identify the main determinants of mortality variability.
- Assess model assumptions and influential observations.
- Evaluate multicollinearity among predictors.
- Compare alternative variable selection procedures.
- Investigate the robustness of model estimates.
- Explore potential structural nonlinearities using segmented regression.

## Methods

### Classical regression analysis
- Ordinary Least Squares (OLS)
- Residual diagnostics
- Influence analysis
- Variance Inflation Factors (VIF)
- Condition number assessment

### Variable selection
- Backward elimination
- Forward selection
- Stepwise regression
- AIC optimization
- Adjusted R² criterion
- Mallows' Cp criterion

### Robust modelling
- Huber M-estimators
- Least Trimmed Squares (LTS)
- Bootstrap confidence intervals

### Nonlinear modelling
- Piecewise regression
- Segmented regression

## Main Findings

- Severe multicollinearity was identified among several socioeconomic and environmental variables.
- A reduced six-variable model achieved similar explanatory performance to the full model while improving interpretability.
- Robust regression methods produced estimates highly consistent with OLS results, suggesting limited sensitivity to influential observations.
- Piecewise regression provided little evidence for strong structural nonlinearities in predictor effects.

## Tools and Packages

- R
- tidyverse
- bestglm
- car
- MASS
- robustbase
- segmented
- leaps
- lmtest

## Skills Demonstrated

- Regression diagnostics
- Feature selection
- Multicollinearity analysis
- Robust statistics
- Model comparison
- Statistical inference
- Predictive modelling

## Author

Giselle Piro Martino
Bioinformatics and Biostatistics
