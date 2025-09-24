# A High-Accuracy Stacked Ensemble Model for Predicting Effluent BOD₅ in WWTPs

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

This repository contains the code, data description, and materials for the study:

> **"A High-Accuracy Stacked Ensemble Model for Predicting Effluent BOD₅ in Wastewater Treatment Plants Using Operational Data"**

The model uses a **stacked ensemble** of LightGBM, XGBoost, and CatBoost with performance-based weighting (0.13, 0.75, 0.12) to predict effluent BOD₅ (BOD5_out) from routine operational data. Trained on **9 years of real-world data (2015–2024)** from a full-scale WWTP in Algeria, it achieves an exceptional **R² = 98.44%** and **MSE = 0.02**, outperforming individual models.

This work enables **real-time BOD₅ estimation**, transforming it from a delayed compliance check into a dynamic control variable for smarter wastewater management.

## Key Features

- **Stacked Ensemble**: Combines LightGBM, XGBoost, and CatBoost via weighted averaging.
- **Time-Based Validation**: Chronological train/test split (80/20) ensures realistic forecasting performance.
- **Domain-Informed Feature Engineering**: 9 new features (e.g., COD removal efficiency, pH change, COD/BOD₅ ratio) improve interpretability and accuracy.
- **Robust Preprocessing**: Missing value handling, outlier removal (IQR) for BOD5_out, and temporal sorting.
- **Deployable Soft Sensor**: Can be integrated into SCADA systems or used standalone.


