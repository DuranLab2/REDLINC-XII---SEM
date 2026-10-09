# Aggregated statistical outputs

This directory contains selected aggregate statistical results from the REDLINC XII structural equation modeling workflow.

| File | Description |
| --- | --- |
| `main_model_fit.csv` | Overall model-fit statistics and explained variance |
| `measurement_invariance_fit.csv` | Configural, metric, and scalar model-fit indices |
| `measurement_invariance_differences.csv` | Changes in CFI and RMSEA between invariance models |
| `measurement_invariance_lrt.csv` | Scaled likelihood-ratio comparisons between invariance models |

These four files contain model-level summary statistics rather than participant-level observations. They do not include the source dataset.

The measurement invariance values have been checked for consistency with the corresponding manuscript results, allowing for rounding. This numerical cross-check is distinct from authorization to disclose unpublished results.

Public dissemination of unpublished aggregate results remains subject to authorization by the responsible research team. These selected outputs do not constitute a complete reproduction package.

**Figure-generation note:** `notebooks/03_Figure_Generation.ipynb` currently reads `outputs/SEM_V7_Regresiones.csv`, `outputs/SEM_V7_Efectos_Indirectos.csv`, and `outputs/SEM_V7_Indices_Ajuste_R2.csv`. These additional summary files are not included in this public directory and must be generated or provided locally by an authorized user.
