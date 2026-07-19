# Prediction for Patient Readmission

## Overview

This project applies machine learning techniques to predict early hospital readmission risk among diabetic patients using real clinical data. The project focuses on building a reliable prediction system by exploring data quality issues, handling class imbalance, comparing different models, and explaining predictions using **SHAP**.

## Dataset

This project uses the **Diabetes 130-US Hospitals Dataset**, which contains hospital admission records of diabetic patients from 130 US hospitals between 1999 and 2008.

Files used:
- **`diabetic_data.csv`** — main dataset used for preprocessing and model development.
- **`IDs_mapping.csv`** — reference file for interpreting coded variables.

## Tools and Methods Used

- **Logistic Regression** — baseline model for comparison.
- **XGBoost** — main machine learning model for predicting readmission risk.
- **SHAP** — used for global and local model explanations.
- **Pandas** — data cleaning and preprocessing.
- **Scikit-learn** — feature processing, model training, and evaluation.
- **Matplotlib** — visualization and result analysis.

The project includes:
- Data quality assessment and preprocessing
- Leakage risk investigation
- Class imbalance handling
- Model evaluation using appropriate metrics
- SHAP-based interpretability analysis
- Fairness analysis across demographic groups
