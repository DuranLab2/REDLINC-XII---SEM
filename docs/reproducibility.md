# Reproducibility guide

## Runtime

- Python 3 with Jupyter and the dependencies listed in `requirements.txt` for visualization.
- R with `IRkernel` and the packages listed in `R-packages.txt`, plus any additional packages explicitly loaded in the notebooks.
- Jupyter configured with separate R (`IRkernel`) and Python (`ipykernel`) kernels.

## Execution order

1. `notebooks/01_Main_SEM_Analysis.ipynb`
2. `notebooks/02_Country_Sensitivity_LOCO.ipynb` (optional robustness analysis)
3. `notebooks/03_Figure_Generation.ipynb` (after preparing the required summary CSVs)

## Local inputs and outputs

The R notebooks use `Sys.getenv("SEM_WORKDIR", unset = "./")` to identify their working directory and read `analysis_input.xlsx` from that location. This input is **not distributed** in the repository. The scripts construct paths by concatenating the working-directory string and filename; if `SEM_WORKDIR` is set, it should therefore end with the appropriate path separator, or the path-building code should be adapted locally.

The R analysis writes summary CSVs to the configured working directory. The Python figure notebook currently expects the following files relative to its working directory:

- `outputs/SEM_V7_Regresiones.csv`
- `outputs/SEM_V7_Efectos_Indirectos.csv`
- `outputs/SEM_V7_Indices_Ajuste_R2.csv`

These three figure-input CSVs are **not** among the four aggregate tables currently published in `outputs/`. An authorized user must generate them locally and arrange the expected paths before running the figure notebook. Do not upload restricted inputs or unapproved results to make the example executable.

## Known limitations

- End-to-end execution has **not** been independently validated in a clean environment.
- Notebook dependencies, relative working directories, and output paths may require local adaptation.
- The four public aggregate CSVs do not provide all files needed to reproduce the figures.
- This repository does not provide a turnkey numerical reproduction of the study.
- Do not commit local inputs, unapproved analytical results, notebook cell outputs, or environment secrets.
