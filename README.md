# Hospital Discharge Analysis

This repository contains a Jupyter Notebook for analyzing hospital discharge data and modeling key metrics.

## 📁 Repository Structure

- **`hospital_discharge_analysis_fixed.ipynb`** – Main analysis notebook:
  - Loads and cleans discharge, cost, and charge data (1.19 M records).
  - Trains XGBoost models to predict:
    - Discharges per facility and total discharges by DRG
    - Mean cost, median cost, and median charge
  - Evaluates performance (MAE, R²) and prints summary metrics.

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or later
- Jupyter Notebook or JupyterLab

### Installation

Install the required Python packages:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib
```

### Running the Analysis

1. Open `hospital_discharge_analysis_fixed.ipynb` in your Jupyter environment.
2. Run all cells sequentially:
   - Data loading & cleaning
   - Feature engineering & model training
   - Performance evaluation & summary outputs
3. Inspect printed metrics, tables, and plots for insights.

## 📊 Results Summary

- **Discharge prediction**:
  - Per‑facility: MAE ≈ 43.6 patients, R² ≈ 0.60
  - Total by DRG: MAE ≈ 3 462 patients, R² ≈ 0.60

- **Cost models**:
  - Mean cost: MAE ≈ \$11 000, R² ≈ 0.37
  - Median cost: MAE ≈ \$10 742, R² ≈ 0.35
  - Median charge: MAE ≈ \$32 403, R² ≈ 0.45

- **Key insights**:
  - Volume forecasts (discharges) are significantly more reliable than financial predictions.
  - Cost and charge variance suggest need for additional features (e.g., payer mix, length of stay).

## 🔮 Next Steps

- **Feature engineering**: incorporate patient demographics, comorbidities, payer mix, length‑of‑stay.
- **Model tuning**: perform grid or Bayesian hyperparameter search.
- **Validation**: implement time‑series cross-validation and residual analysis to detect biases.

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request to:

- Add new visualizations or analyses
- Improve data cleaning and feature extraction
- Explore alternative modeling approaches

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
