# Decision Trees, LASSO, and Boosting for Regression

## Project Overview

This project focuses on **Decision Trees**, **LASSO regression**, and **Boosting techniques**. The datasets used in this homework include the **Acute Inflammations** dataset and the **Communities and Crime** dataset. The primary objectives are to build interpretable decision tree models, use regularization techniques for regression, and implement boosting for improving model performance.

## Table of Contents

- [Project Overview](#project-overview)
- [Datasets](#datasets)
- [Task 1: Decision Trees](#task-1-decision-trees)
- [Task 2: LASSO and Boosting for Regression](#task-2-lasso-and-boosting-for-regression)
- [How to Run](#how-to-run)
- [Results](#results)
- [License](#license)

## Datasets

### 1. **Acute Inflammations Dataset**
- **Source**: [UCI Machine Learning Repository - Acute Inflammations](https://archive.ics.uci.edu/ml/datasets/Acute+Inflammations)
- This dataset includes patient data used for diagnosing acute inflammations and predicting different types of diseases. It is a multi-label classification dataset.

### 2. **Communities and Crime Dataset**
- **Source**: [UCI Machine Learning Repository - Communities and Crime](https://archive.ics.uci.edu/ml/datasets/Communities+and+Crime)
- This dataset consists of community-level statistics related to crime rates. It includes demographic, economic, and law enforcement-related variables.

## Task 1: Decision Trees

### (a) Build a Decision Tree
- A decision tree was built using the **Acute Inflammations** dataset. The tree structure was visualized using Scikit-learn.
  
### (b) Convert Decision Rules into IF-THEN Rules
- The decision tree was converted into a set of **IF-THEN rules** using Python code based on Scikit-learn models. These rules were simplified for better interpretability.
  
### (c) Cost-Complexity Pruning
- To improve the interpretability of the decision tree, **cost-complexity pruning** was applied to reduce the size of the tree without sacrificing too much accuracy.

### (d) Minimal Decision Tree
- A pruned decision tree with high interpretability was generated along with the corresponding decision rules.

## Task 2: LASSO and Boosting for Regression

### (a) Data Preprocessing
- **Communities and Crime** dataset was preprocessed:
  - Missing values were handled using imputation techniques.
  - Non-predictive features were ignored based on the dataset documentation.
  
### (b) Correlation Analysis
- A **correlation matrix** was plotted to explore the relationships between features in the dataset.

### (c) Coefficient of Variation (CV)
- The **Coefficient of Variation (CV)** was calculated for each feature, and the top features were selected for further analysis. Scatter plots and box plots were generated to analyze their significance.

### (d) Linear Regression
- A **linear regression model** was trained using the least squares method on the training data. The test error was reported.

### (e) Ridge Regression
- A **ridge regression model** was trained, and the regularization parameter (λ) was selected via cross-validation. The test error was calculated.

### (f) LASSO Regression
- **LASSO regression** was implemented, and λ was selected using cross-validation. The selected variables and test errors were reported. The analysis was repeated with standardized features, and results for both cases were compared.

### (g) Principal Component Regression (PCR)
- A **PCR model** was built with the number of principal components (M) chosen by cross-validation. The test error was reported.

### (h) Boosting
- A **boosting tree** model was fitted to the data using **XGBoost** with L1-penalized regression at each node. The regularization parameter (α) was chosen using cross-validation.

## How to Run

### Requirements

- Python 3.x
- Jupyter Notebook
- Required Python libraries (can be installed via `pip`):
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `xgboost`

### Instructions

1. Clone the repository and navigate to the project folder.
2. Open the Jupyter Notebooks (`Huang_Bor-Sheng.ipynb`).
3. Run the notebook cells to execute the tasks and view the results.

## Results

- **Decision Trees**:
  - The decision tree was pruned to reduce complexity, and the resulting model was converted into IF-THEN rules for interpretability.
  
- **LASSO Regression**:
  - Test errors for the LASSO models with and without standardization were reported.
  - Variables selected by the LASSO model were listed.
  
- **Boosting**:
  - The best boosting model was found using XGBoost with L1-penalization, and the test error was reported.

## License

This project is intended for academic purposes and is based on the DSCI 552 course material.
