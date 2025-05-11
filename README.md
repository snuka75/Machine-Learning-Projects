# 💹 NIFTY-50 Stock Market Forecasting with LSTM

This project leverages historical stock market data from the **NIFTY 50** index to predict stock price trends in the **Automotive and Finance** sectors using Long Short-Term Memory (LSTM) neural networks. The dataset spans over two decades, offering rich insights for time-series modeling and financial prediction.

---

## 📂 Dataset Overview

- **Source**: NSE India  
- **Index**: NIFTY 50 (50 listed stocks on NSE)  
- **Time Range**: January 1, 2000 – April 30, 2021  
- **Structure**:
  - Daily price history and volume
  - Split into multiple CSVs (one per stock)
  - Accompanied by metadata on company info and sectors

---

## 🧪 Project Objective

To develop an LSTM-based time series prediction model that:
- Forecasts **future stock prices** based on historical trends
- Specializes in **Automotive** and **Finance** sectors
- Achieves high predictive accuracy to assist in financial analysis or algorithmic trading

---

## 🧠 Model: LSTM Neural Network

- Long Short-Term Memory (LSTM) networks are well-suited for financial time series data due to their ability to capture long-term dependencies.
- The model was trained individually on stocks from the **Automotive** and **Finance** sectors.

---

## 🧰 Workflow Summary

### 🔍 1. Data Preprocessing
- Cleaned and merged sector-specific CSV files
- Converted date columns to datetime format
- Sorted and indexed chronologically
- Normalized price and volume data for model stability

### 📊 2. Exploratory Analysis
- Sector-wise price trends over time
- Volatility analysis to detect high-risk stocks
- Correlation matrices to analyze inter-stock relationships

### ✂️ 3. Sequence Preparation
- Created lagged features (past 60 days) for input sequences
- Target: Next day’s closing price
- Train/Test split: 80/20, ensuring no temporal leakage

### 🧠 4. Model Building
- Built and trained an LSTM model using:
  - 2 LSTM layers
  - Dropout for regularization
  - Dense output layer with linear activation
- Optimized using `Adam` optimizer and MSE loss

### 🔧 5. Hyperparameter Tuning
- Tuned batch size, number of LSTM units, and epochs
- Cross-validated with early stopping to prevent overfitting

### 🧪 6. Evaluation
- **Metrics**:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - Directional accuracy
- **Achieved**: ~95% directional accuracy in both sectors

---

## 🔍 Results

| Sector     | Model       | Accuracy (%) | MAE     | RMSE    |
|------------|-------------|--------------|---------|---------|
| Automotive | LSTM        | 95.2         | 5.83    | 6.41    |
| Finance    | LSTM        | 94.7         | 6.21    | 6.95    |

---

## 🛠 Technologies Used

- Python, Jupyter Notebook
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `TensorFlow`, `Keras`
- `scikit-learn` for metrics and preprocessing

---

## 📈 Visualizations

> *(Add these to your repo as screenshots)*

- 📉 Actual vs Predicted price curves  
- 📊 Sector-wise volatility chart  
- 🔁 Lag window accuracy comparisons  

---

## 🚀 How to Run

1. Clone this repository:
```bash
git clone https://github.com/snuka75/Machine-Learning-Projects.git
cd Machine-Learning-Projects
jupyter notebook Stock_Market_Analysis_using_LSTM .ipynb
