# Data Description

This project uses a real-world, nine-year operational dataset (2015–2024) collected from a municipal wastewater treatment plant (WWTP) in Algeria.

## Overview
- **Time period**: January 2015 – May 2024
- **Sampling frequency**: Irregular (~3–4 samples per month)
- **Total records**: 410 initial observations → 357 after preprocessing

## Measured Parameters
All variables were measured at both influent (inlet) and effluent (outlet):

| Parameter            | Unit | Notes                             |
|----------------------|------|-----------------------------------|
| pH                   |   –  |                                   |
| BOD₅                 | mg/L | Target: BOD5_out                  | 
| COD                  | mg/L | Chemical Oxygen Demand            |
| Conductivity         | μS/cm|                                   |
| TSS                  | mg/L | Total Suspended Solids            |
| Temperature          | °C   |                                   |
| Dissolved Oxygen(O₂) | mg/L | Excluded due to >60% missing data |

Additionally, 9 engineered features were created using domain knowledge:
- COD removal efficiency
- pH change (out – int)
- COD/BOD₅ ratio (int & out)
- Interaction terms (e.g., BOD5_int × pH_int)
- Ratios (e.g., TSS/BOD5_int)

## Data Availability
Due to institutional policies and data ownership by the WWTP, the **raw dataset cannot be shared publicly**.

However:
- A **sample dataset** (`data_sample.csv`) with synthetic but realistic data is provided in `/data/sample_data.csv` for demonstration.
- The **full preprocessing pipeline** (handling missing values, outlier removal, feature engineering) is fully documented in the Jupyter notebooks.
- All code is designed to work on similar datasets from other WWTPs.
- [`data/sample_data.csv`](data/sample_data.csv): A synthetic but realistic dataset for demonstration and testing.
  
For research collaboration or data access requests, please contact:  
📧 bouragbilakhdar@gmail.com
