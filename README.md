# Credit Card Fraud Detection — Reproducibility Package

This repository accompanies the manuscript:

**Reassessing Classification Models for Credit Card Fraud Detection under Severe Class Imbalance**

Author: **Oluwadamilola Oluwole**

## Contents

- `reproducible_reanalysis.ipynb` — clean notebook for the journal reanalysis.
- `original_analysis_notebook.ipynb` — archival copy of the original Colab analysis.
- `results/` — derived result tables used in the manuscript.
- `figures/` — publication figures.
- `requirements.txt` — Python dependencies.
- `CITATION.cff` — citation metadata for the code/reproducibility package.
- `DATA_README.md` — instructions and restrictions concerning the third-party dataset.
- `REPRODUCIBILITY.md` — execution instructions and methodological notes.

## Data

The raw `creditcard.csv` file is **not redistributed** in this repository because it is a third-party dataset. Obtain it from its authorized public source and place it at:

`data/creditcard.csv`

## Reproduction

1. Create a Python environment.
2. Install dependencies from `requirements.txt`.
3. Obtain the authorized dataset and place it at `data/creditcard.csv`.
4. Open `reproducible_reanalysis.ipynb`.
5. Run the notebook from top to bottom.
6. The notebook writes tables to `results/` and figures to `figures/`.

## Citation

After this repository is published through Zenodo, replace the placeholder DOI in `CITATION.cff` and the manuscript's Data Availability Statement with the DOI assigned to the release.

## Important methodological distinction

The original analysis computed ROC-AUC from hard class predictions. The journal reanalysis computes ROC-AUC from predicted probabilities and additionally reports PR-AUC, precision, recall, F1-score, and specificity. Oversampling is applied only to the training portion of the data.
