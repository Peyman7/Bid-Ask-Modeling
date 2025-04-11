# Bid-Ask-Modeling

This project develops a hybrid quoting model for foreign exchange (FX) trading. The model predicts competitive bid and ask quotes across various liquidity levels using historical LP quote data. It combines a rule-based VWAP model for small sizes and a machine learning model for larger sizes.

---

## Problem Statement

The task is to build a quoting engine that:
- Generates bid and ask prices for liquidity levels [1, 3, 5, 10, 50, 75, 100, 150] million
- Attracts liquidity and remains competitive
- Is evaluated using market metrics like top-of-book coverage, crossing rates, spread width, and interpolation quality

---

## Environment & Dependencies

- **Python version:** 3.8+
- **Platform:** Jupyter Notebook
- **Libraries used:**
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn lightgbm pyarrow scipy
  ```

---


## File Structure

- `./notebooks/FX_Quoting_Model.ipynb` – Main notebook with:
  - Loading Data
  - Exploratory Data Analysis
  - Trend Analytics
  - Bid-Ask Strategies (VWAP logic, hybrid using VWAP an Machine Learning)
  - Feature engineering
  - Model training (bid and ask)
  - Hybrid model generation
  - Evaluation metrics and plots
- `./data/lp_quotes/*.parquet` – dataset of bid/ask quotes at different martket days
- `./data/trade_data/trade_data.parquet` – Synthetic trade data for bonus inventory analysis

---

## How to Run

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Open the `FX_Quoting_Model.ipynb` notebook

3. Run each cell **sequentially**, starting from data loading, through feature generation, training, and final evaluation.

---

## Output

The notebook will generate:
- Bid/Ask prediction 
- Time-of-day spread/mid-price trends
- In-sample vs out-of-sample evaluation metrics

---


