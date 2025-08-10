# Time Series Forecasting for Portfolio Management Optimization

This project is based on the **10 Academy AI Mastery Week 11 Challenge**.  
We aim to use time series forecasting techniques to predict Tesla's (TSLA) stock prices and apply portfolio optimization strategies with BND and SPY ETFs.

---

## **Project Structure**

```

📂 project/
├── data/                  # Optional: Store downloaded CSV data
├── notebooks/             # Jupyter notebooks for each task
│   ├── task1\_preprocessing.ipynb
│   ├── task2\_forecasting.ipynb
│   ├── task3\_future\_forecast.ipynb
│   ├── task4\_portfolio\_optimization.ipynb
│   ├── task5\_backtesting.ipynb
├── requirements.txt
├── README.md

````

---

## **Tasks Overview**

### **Task 1: Preprocess and Explore the Data**
- Fetch historical data (2015-07-01 to 2025-07-31) using `yfinance` for:
  - TSLA (Tesla)
  - BND (Vanguard Total Bond Market ETF)
  - SPY (S&P 500 ETF)
- Clean missing values, calculate daily returns, perform EDA.
- Check for stationarity using Augmented Dickey-Fuller (ADF) test.
- Calculate Value at Risk (VaR) and Sharpe Ratio.

### **Task 2: Develop Time Series Forecasting Models**
- Train and compare:
  - ARIMA/SARIMA (Statistical Models)
  - LSTM (Deep Learning)
- Chronological train/test split.
- Optimize hyperparameters (grid search, auto_arima).
- Evaluate with MAE, RMSE, MAPE.

### **Task 3: Forecast Future Market Trends**
- Use best model to forecast 6–12 months of Tesla prices.
- Include confidence intervals.
- Analyze trends, volatility, and risks.

### **Task 4: Optimize Portfolio Based on Forecast**
- Use forecasted TSLA returns + historical returns for BND and SPY.
- Calculate covariance matrix.
- Generate Efficient Frontier with `PyPortfolioOpt`.
- Identify Maximum Sharpe Ratio & Minimum Volatility portfolios.
- Recommend optimal weights and portfolio metrics.

### **Task 5: Strategy Backtesting**
- Backtest recommended portfolio against a 60% SPY / 40% BND benchmark.
- Plot cumulative returns.
- Compare Sharpe Ratio and total return.

---

## **Installation**
1. Clone the repository:
   ```bash
   git clone <your_repo_url>
   cd <your_repo_name>
````

2. Create a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scripts\activate      # Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## **Usage**

1. Open Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

2. Run each notebook in the `notebooks/` folder sequentially:

   * `task1_preprocessing.ipynb`
   * `task2_forecasting.ipynb`
   * `task3_future_forecast.ipynb`
   * `task4_portfolio_optimization.ipynb`
   * `task5_backtesting.ipynb`