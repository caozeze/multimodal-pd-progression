# Exploring Multimodal Data for Disease Progression Prediction

This repository contains the code and notebooks accompanying the MSc Data Science and Machine Learning dissertation: *Exploring Multimodal Data for Disease Progression Prediction*. The project investigates how baseline multimodal data (demographics, clinical assessments, MRI, DaTScan, biomarkers, and genetics) can be integrated to predict Parkinson’s disease (PD) progression.

## Repository Structure

The analysis is organised into five Jupyter notebooks, corresponding to the main stages of the study:

1. **`1_data_mri.ipynb`**  
   Processing and quality control of baseline MRI data (FreeSurfer-derived imaging-derived phenotypes). Includes residualisation and dimensionality reduction (PCA).

2. **`2_data_curated.ipynb`**  
   Preparation of curated non-imaging datasets, including demographics, clinical scales, DaTScan, fluid biomarkers, and genetics. Covers cleaning, encoding, and harmonisation.

3. **`3_data_curated_mri_vif.ipynb`**  
   Integration of MRI and curated datasets. Includes multicollinearity checks (VIF) and feature selection for downstream modelling.

4. **`4_model_rq12.ipynb`**  
   Modelling for RQ1 (slope prediction) and RQ2 (survival analysis). Implements a range of regression and survival models (linear, ensemble, neural, penalised Cox, RSF, AFT).

5. **`5_model_multitask.ipynb`**  
   Modelling for RQ4 (multi-task learning). Implements shared-encoder networks with regression and survival heads, with hyperparameter search and evaluation.

## Data Access

The analyses rely on data from the Parkinson’s Progression Markers Initiative (PPMI). Access requires registration and approval from the PPMI data committee. Data files are **not included** in this repository due to licensing restrictions. See: [https://www.ppmi-info.org/access-data-specimens/download-data](https://www.ppmi-info.org/access-data-specimens/download-data)

## Environment and Dependencies

The project was developed using Python 3.10. Key packages include:

- `numpy`, `pandas`, `scikit-learn`
- `xgboost`, `lightgbm`, `catboost`
- `lifelines`, `scikit-survival`
- `torch` (PyTorch) for deep learning models
- `shap` for interpretability
- `matplotlib`, `seaborn` for visualisation

A full list of package versions is provided in the Appendix of the dissertation.

## Reproducibility

To reproduce the analyses:

1. Obtain PPMI access and download the relevant datasets.  
2. Place data files in the expected directory structure (see within each notebook for paths).  
3. Create a Python virtual environment and install dependencies.  
4. Run the notebooks sequentially from `1_data_mri.ipynb` to `5_model_multitask.ipynb`.

---

*Disclaimer: This repository contains academic research code and is intended for reproducibility and educational purposes.*
