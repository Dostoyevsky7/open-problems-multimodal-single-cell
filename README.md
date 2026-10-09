# open-problems-multimodal-single-cell              
# Multimodal Single-Cell Integration

This repository contains the code for my mini-project based on the
NeurIPS 2021 Open Problems – Multimodal Single-Cell Integration
competition.

## Tasks

The project addresses both prediction tasks:

1. **CITE-seq:** predicting surface protein abundance from gene expression.
2. **Multiome:** predicting gene expression from chromatin accessibility.

## Models

- **CITE-seq:** Truncated SVD followed by Ridge regression.
- **Multiome:** Truncated SVD of the ATAC-seq inputs, target-space SVD,
  and an MLP ensemble.

## Repository structure

| Notebook | Description |
|---|---|
| `CITE_01_Training_and_Validation.ipynb` | Data preprocessing, validation, model selection, and final CITE-seq model training |
| `CITE_02_Final_Inference.ipynb` | Generation of the final CITE-seq test predictions |
| `Multiome_01_Training_and_Validation.ipynb` | Dimensionality reduction, validation, baseline comparison, and Multiome model training |
| `Multiome_02_Final_Inference.ipynb` | Reconstruction and generation of the final Multiome test predictions |

For each task, the training notebook should be executed before the
corresponding inference notebook.

## Results

| Evaluation | Score |
|---|---:|
| Kaggle public leaderboard | 0.803684 |
| Kaggle private leaderboard | 0.751565 |

## Data

The original data are available from the Kaggle competition:

https://www.kaggle.com/competitions/open-problems-multimodal/

The original datasets, large intermediate matrices, trained model files,
and submission files are not included because of their size. The paths
used in the notebooks follow the Kaggle directory structure.

## Environment

The notebooks were developed in the Kaggle Python environment. The main
packages used were NumPy, pandas, SciPy, scikit-learn, TensorFlow/Keras,
h5py, and joblib.
