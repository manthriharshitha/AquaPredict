# AquaPredict

AquaPredict is a machine-learning project for analyzing water-quality observations and classifying contamination levels using chemical, physical, and biological measurements.

## Project contents

- `acquapredict.ipynb` - End-to-end notebook for loading, cleaning, merging, exploring, and modeling the water-quality data.
- `swq_chemical_parameter_manual_cpcb_ap_2021_2025.csv` - Chemical water-quality measurements.
- `swq_physical_parameter_manual_cpcb_ap_2021_2025.csv` - Physical water-quality measurements.
- `swq_biological_parameter_manual_cpcb_ap_2021_2025.csv` - Biological water-quality measurements.
- `catboost_info/` - CatBoost training output generated while running the notebook.

## What the notebook does

1. Loads the three CPCB water-quality datasets.
2. Cleans and standardizes column names.
3. Converts measurement columns to numeric values where appropriate.
4. Finds shared identifiers and merges the chemical, physical, and biological data.
5. Creates a binary `Contamination` target using a biochemical oxygen demand (BOD) threshold of `3.0 mg/L`.
6. Prepares numeric features, missing-value indicators, and train/test data.
7. Trains and evaluates classification models, including:
   - Random Forest
   - Extra Trees
   - XGBoost
   - CatBoost
8. Reports classification metrics and generates evaluation visualizations.

## Requirements

Python 3.9 or later is recommended. Install the notebook dependencies with:

```bash
pip install numpy pandas matplotlib scikit-learn xgboost catboost shap openpyxl jupyter
```

## Running the notebook

1. Clone the repository:

   ```bash
   git clone https://github.com/manthriharshitha/AquaPredict.git
   cd AquaPredict
   ```

2. Start Jupyter:

   ```bash
   jupyter notebook
   ```

3. Open `acquapredict.ipynb` and run the cells from top to bottom.

The notebook currently contains local Windows dataset paths near the beginning. Update those paths, or replace them with paths relative to the repository, before running it on another computer.

## Data source

The included datasets contain Andhra Pradesh surface-water quality observations from 2021–2025 and include chemical, physical, and biological parameters.

## Disclaimer

This project is intended for data analysis and research. Model predictions should not be treated as a substitute for official water-quality testing or regulatory decisions.
