# Exoplanet Equilibrium Temperature Prediction

## Overview
This project uses machine learning to predict the equilibrium temperature of exoplanets from observed planetary and stellar properties. The goal is to evaluate how well data-driven models can capture known astrophysical relationships, particularly the dependence of temperature on stellar radiation.


## Project Structure

```bash
├── figures/                    # Plots used in the report
├── Final-Project.ipynb         # Main notebook with full analysis
├── PS_2026.03.31_09.54.32.csv  # Original data downloaded from the NASA Exoplanet Archive (OPTIONAL)
├── README.md                   # Project description
├── data.csv                    # Data used in the .ipynb file
```

## Methods
Two regression models were implemented:
- Random Forest Regressor: an ensemble of decision trees that reduces variance and captures nonlinear relationships
- XGBoost Regressor: a gradient boosting method that iteratively improves prediction accuracy
Both models were trained on planetary, orbital, and stellar features, with equilibrium temperature (pl_eqt) as the target variable.


## Evaluation Metrics
Model performance was evaluated using:
- R² (coefficient of determination): measures explained variance
- RMSE (Root Mean Squared Error): penalizes large prediction errors
- MAE (Mean Absolute Error): provides average prediction error in Kelvin


## Key Results
- Both models achieved strong predictive performance
- XGBoost slightly outperformed Random Forest
- Insolation flux (pl_insol) was the dominant feature
- Removing insolation flux significantly reduced model accuracy
- Results align with physical expectations that planetary temperature depends strongly on incident stellar radiation
