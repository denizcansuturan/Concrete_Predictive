# Concrete Strength Prediction
## Overview

This repository contains the code and analysis for predicting the compressive strength of concrete mixtures using various machine learning models. The goal is to optimize the quality assurance processes in construction by accurately predicting concrete strength based on its composition and curing conditions.

## Dataset 

[The dataset](https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength) used in this project is obtained from the UCI Machine Learning Repository. It contains 1030 observations with 9 attributes related to the components and properties of concrete:

- Cement (kg/m³)
- Blast Furnace Slag (kg/m³)
- Fly Ash (kg/m³)
- Water (kg/m³)
- Superplasticizer (kg/m³)
- Coarse Aggregate (kg/m³)
- Fine Aggregate (kg/m³)
- Age (days)
- Compressive Strength (MPa) [Target variable]

## Models and Methodology
### Preprocessing

- Data scaling using Z-score normalization.
- Feature selection with Sequential Feature Selection (SFS).
- Polynomial feature expansion.

### Machine Learning Models

- **XGBoost**
- **LightGBM** (best performing model)
- **Stacking Ensemble** (combines MLPs and XGBoost)

### Model Evaluation Metrics

- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R-squared (R²) Score**

## Installation

To run the code in this repository, clone it and install the required dependencies:

```bash
git clone https://github.com/yourusername/concrete-strength-prediction.git
cd concrete-strength-prediction
pip install -r requirements.txt
```

## Key Findings

- **LightGBM** model outperformed other models with an RMSE of 3.793 and an R² score of 0.944.
- **Stacking Ensemble** showed competitive performance but was less accurate than LightGBM.
- Feature importance analysis and SHAP values were used to interpret model predictions, highlighting the significance of components like cement and fine aggregate.
  
## Results
The repository includes detailed Jupyter notebooks that walk through the entire process from data exploration to model evaluation. Key visualizations and performance metrics are also provided.

