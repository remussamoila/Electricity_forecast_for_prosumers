# ☀️ Solar Production Forecasting

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/remussamoila/solar-forecasting/blob/main/notebooks/03_modeling_lstm.ipynb)

> Forecasting solar electricity generation using weather data, time series modeling, and LSTM neural networks.

---

## 📊 Project Scope

We work with historical solar production data (2013–2025) and blended weather data (ECA&D). The project targets short- and medium-term forecasting horizons (e.g. 1h, 24h, 7d ahead), with high temporal resolution.

---

## 🔧 Modules & Tasks

### 📁 Phase 1: Data Preparation
- [x] Collect solar production data (Excel files, 2013–2025)
- [x] Extract temperature, wind, and sunshine data from ECA&D
- [x] Estimate or import solar irradiance (GHI/DNI/DHI)
- [x] Align and merge data into unified time-indexed DataFrames

### 🧪 Phase 2: Feature Engineering
- [ ] Time features: hour, day, season, holidays
- [ ] Weather features: sunshine, wind, temperature
- [ ] Lag/rolling window features for production and irradiance
- [ ] Astronomical features: solar elevation, azimuth (via `pvlib`)

### 🧠 Phase 3: Modeling
- [ ] Build baselines (linear regression, XGBoost)
- [ ] Train LSTM model on time-sequenced inputs
- [ ] Tune hyperparameters (Optuna or GridSearchCV)
- [ ] Validate using MAE, RMSE, MAPE

### 📈 Phase 4: Evaluation & Visualization
- [ ] Plot prediction vs. actual curves
- [ ] Compare models across multiple forecast horizons
- [ ] Analyze feature importances (where applicable)

### 🚀 Phase 5: Sharing & Automation
- [ ] Save model artifacts (HDF5, ONNX)
- [ ] Enable team collaboration via Colab + GitHub
- [ ] Optional: deploy REST API for on-demand forecasting

---

## 📂 Suggested Repository Structure

```
solar_forecast/
├── data/                    # Raw & processed data
│   ├── raw/                 # Original solar and weather data
│   └── processed/           # Cleaned, merged DataFrames
├── notebooks/               # Development notebooks (Colab/Jupyter)
│   ├── 01_data_prep.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modeling_lstm.ipynb
│   └── 04_evaluation.ipynb
├── scripts/                 # Modular scripts (for reuse & CLI)
│   ├── data_loader.py
│   ├── feature_builder.py
│   └── train_model.py
├── models/                  # Saved models
├── reports/                 # Evaluation plots, figures
├── README.md
└── .gitignore
```

---

## 📦 Dependencies

```bash
pandas
numpy
tensorflow or pytorch
scikit-learn
matplotlib / seaborn
pvlib
```

---

## 📌 To Do
- [ ] Integrate solar position features using `pvlib`
- [ ] Connect with satellite irradiance APIs (e.g., CAMS)
- [ ] Improve generalization via cross-regional training
- [ ] Publish Colab + GitHub workflow guide

---

## 📜 License

MIT License (or update if otherwise)

---

## 👥 Contributors

- Remus Samoila & collaborators
