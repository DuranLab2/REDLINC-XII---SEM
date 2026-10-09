# Methodology

## Primary analysis
The primary workflow uses structural equation modeling with the `lavaan` R package. It estimates measurement and structural relationships across BMI-defined groups, with model-fit summaries, direct and indirect effects, and cognitive outcome associations.

## Model evaluation
The notebooks implement fit diagnostics, Wald tests, and multigroup measurement-invariance comparisons. Review the notebook code for the exact estimator, covariate coding, and constraints used in each model.

## Sensitivity analyses
A leave-one-country-out procedure re-estimates the analysis after excluding one country at a time. The primary workflow also contains alternative operationalization checks.

## Visualization
The figure notebook reads analysis-generated summary tables and produces a path diagram and effect visualization. Figures are not pre-populated with study findings in this release.

## Interpretation
Observational SEM estimates should not be interpreted as causal effects without additional identifying assumptions. Check missingness, measurement comparability, multiplicity adjustments, and convergence before reporting results.
