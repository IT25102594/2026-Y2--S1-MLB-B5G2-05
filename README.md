# Corporate Bankruptcy Prediction: Data Preprocessing Pipeline

## Project Overview

This project focuses on building a robust, unified data preprocessing and feature engineering pipeline for corporate bankruptcy prediction. The pipeline processes raw financial data through sequential stages including data quality checks, stratified splitting, outlier treatment, feature scaling, feature selection, dimensionality reduction (PCA), and class balancing (SMOTE). The final output is a model-ready dataset optimized for machine learning algorithms.

## Dataset Details

* **Name:** Taiwan Bankruptcy Dataset
* **Target Variable:** `Bankrupt?` (Binary: 0 = Non-Bankrupt, 1 = Bankrupt)
* **Features:** 95 continuous financial ratios and categorical flags.
* **Characteristics:** The dataset is highly imbalanced, with bankruptcy cases representing a small minority. Several continuous financial ratios are zero-inflated, requiring specialized handling during outlier treatment and quasi-constant feature filtering to prevent data loss.

## Group Member Roles

* **IT25101630 - Samaranayake S.R.E.T.A.H.W.B:** Member 1 – Data Quality Checks & Stratified Train/Test Split
* **IT25103479 - Hasara P.G.I:** Member 2 – Outlier Treatment (IQR Capping)
* **IT25100701 - Nithira R.M.P:** Member 3 – Feature Scaling (StandardScaler)
* **IT25102594 - Bandara O.A.A.Y.S:** Member 4 – Feature Selection (Quasi-constant, Target Correlation, and Multicollinearity Filters)
* **IT25101761 - Gunarathne R.G.N.S:** Member 5 – Dimensionality Reduction (PCA)
* **IT25103651 - Costa N.P.M.P:** Member 6 – Class Balancing (SMOTE) & Final Export

*(Note: I mapped Members 1-4 based on our previous code blocks. You will need to assign **Costa N.P.M.P (IT25103651)** and **Gunarathne R.G.N.S (IT25101761)** to the Member 5 and Member 6 slots.)*

## How to Run the Code

1. **Environment Setup:** Ensure you have Python 3.8+ installed. Install the required libraries using pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn

```


2. **Directory Structure:** Ensure your project folder contains the following structure before execution:
```text
project_root/
├── data/
│   └── raw/
│       └── data.csv
├── notebooks/
│   └── group_pipeline.ipynb
└── results/
    ├── eda_visualizations/
    └── outputs/

```


3. **Execution:**
* Open `group_pipeline.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
* Select **Kernel -> Restart & Run All**.
* The unified pipeline will execute sequentially entirely in-memory.
* The final model-ready datasets will be exported automatically to `results/outputs/final_preprocessed_train.csv` and `results/outputs/final_preprocessed_test.csv`.
