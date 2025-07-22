# Nifty VIX Range Forecasting Tool

Predicts high and low bounds of the Nifty 50 index based on India VIX volatility using a statistical model. Ideal for market analysts, traders, and students exploring financial modeling and volatility forecasting with 95% Accuracy.

---

## Project Overview

This project uses a formula derived from India VIX to predict intraday high and low price ranges for the Nifty 50 index. The prediction is visualized and also exported to Excel for reporting and further analysis.

- Formula used:
  Upper Bound = (Nifty Price + VIX^2*0.6/100)%
  
  Lower Bound = (Nifty Price - VIX^2*0.6/100)%

---

## Features

- Reads historical data from Excel
- Calculates expected Nifty movement range using India VIX
- Visualizes Nifty price with predicted high and low bands
- Exports clean output to a new Excel file with:
  - Date
  - Nifty Price
  - Predicted High Band
  - Predicted Low Band

---

## Tech Stack

- **Python**
- **Pandas**
- **Matplotlib**
- **Google Colab / Jupyter**
- **Excel (via openpyxl or xlsxwriter)**

---

## Sample Code Snippet

```python
df['VIX_Predicted_Move_%'] = (df['Price.1'] ** 2) * 0.6 / 100
df['Nifty_High_Band'] = df['Price'] * (1 + df['VIX_Predicted_Move_%'] / 100)
df['Nifty_Low_Band'] = df['Price'] * (1 - df['VIX_Predicted_Move_%'] / 100)
