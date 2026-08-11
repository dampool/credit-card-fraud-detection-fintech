# Reproducibility instructions

## Environment

Python 3.x

Install:

```bash
pip install -r requirements.txt
```

## Input

Place the authorized third-party dataset at:

`data/creditcard.csv`

## Primary analysis

Run `reproducible_reanalysis.ipynb`.

The primary feature set is:

`V1, V2, V3, V4, V5, V7, V9, V10, V11, V12, V14, V16, V17, V18`

The primary split is a stratified 80:20 train/test split with `random_state=42`.

Random oversampling uses `sampling_strategy=1.0` and is applied only to the training data.

## Metrics

- ROC-AUC from predicted probabilities
- PR-AUC / average precision
- Precision
- Recall
- F1-score
- Specificity
- Confusion-matrix counts

## Original vs journal reanalysis

The original Colab notebook is preserved as `original_analysis_notebook.ipynb`.

The original workflow used an unseeded train/test split and calculated the reported AUC from predicted class labels. The journal version corrects this by using a stratified seeded split and probability-based ROC-AUC, and adds PR-AUC.
