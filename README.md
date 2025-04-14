# sc-ts-forecasting-arima-vs-lstm
Supply Chain Forecasting in a fast-moving globaleconomy: Review, Limits and Future Directions

# Time Series Forecasting: LSTM vs ARIMA on Diverse Demand Patterns

This repository contains code to compare **LSTM** and **ARIMA** models across four types of time series demand patterns:

- **Smooth**
- **Intermittent**
- **Erratic**
- **Lumpy**

The analysis is based on the [Favorita Grocery Sales Forecasting dataset](https://www.kaggle.com/competitions/favorita-grocery-sales-forecasting).

---

## 📂 Overview

### 📁 `prepare_dataset.ipynb`

This notebook:
- Loads the Favorita dataset
- Preprocesses and categorizes time series into four groups
- Outputs cleaned datasets into four folders:
  - `data/smooth/`
  - `data/intermittent/`
  - `data/erratic/`
  - `data/lumpy/`

### 📁 Group Training and Testing

Each of the following notebooks trains and compares **ARIMA** and **LSTM** models on a different demand type:

- `Smooth TS Group Training Test.ipynb`
- `Intermittent TS Group Training Test.ipynb`
- `Erratic TS Group Training Test.ipynb`
- `Lumpy TS Group Training Test.ipynb`

---

## ⚙️ Environment Setup (via Conda)

Use the following commands to set up the environment:

```bash
# Create environment
conda create --name ts-forecast-env python=3

# Activate it
conda activate ts-forecast-env

# Install dependencies
conda install -c conda-forge matplotlib
conda install -c anaconda scikit-learn
conda install -c anaconda numpy 
conda install -c anaconda pandas
conda install -c anaconda scipy
conda install -c conda-forge pmdarima
conda install ipykernel

# Register environment as Jupyter kernel
python -m ipykernel install --user --name ts-forecast-env --display-name "Python (ts-forecast-env)"

# Install deep learning frameworks
pip install tensorflow keras
