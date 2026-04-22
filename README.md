**AI-Enhanced Algorithmic Trading Backtester**
**Overview**

This project is a Python-based algorithmic trading simulation system that uses machine learning to generate trading signals and evaluate strategy performance through backtesting.

The system builds an end-to-end pipeline that fetches real stock market data, trains a predictive model, generates buy/sell signals, simulates trades, and evaluates portfolio performance using financial metrics.

This project was developed as an academic machine learning and data analysis project.

**Project Workflow**

The project follows a modular pipeline:

1.Data Acquisition & Preprocessing
2.Machine Learning Trading Strategy
3.Signal Confirmation
4.Backtesting Simulation
5.Performance Evaluation
6.Visualization

**Key Features**
**Real Market Data Integration**
Fetches historical stock data using yFinance API
Uses OHLCV market data (Open, High, Low, Close, Volume)
Automatically downloads the latest data up to today

**Data Preprocessing & Feature Engineering**

The system prepares data by:

1.Cleaning missing values
2.Calculating daily returns
3.Computing 20-day rolling volatility
4.Creating lag features for prediction


**Machine Learning Trading Strategy**

A Linear Regression model is used to predict the next day’s closing price.

Trading signals are generated as:

| Condition                       | Signal |
| ------------------------------- | ------ |
| Predicted price > Current price | BUY    |
| Predicted price < Current price | SELL   |
| No clear signal                 | HOLD   |

The system also includes **manual confirmation for the latest trading day**, allowing human-in-the-loop decision making.

**Backtesting Engine**

The backtester simulates real trading by:

1.Starting with an initial capital
2.Buying shares when BUY signals occur
3.Selling all shares on SELL signals
4.Tracking daily portfolio value
5.Recording all trades automatically

This simulates a real trading workflow.

**Performance Metrics**

After the simulation, the system evaluates the strategy using:

1.Final Portfolio Value
2.Total Return (%)
3.Maximum Drawdown (%)
4.Annualized Return (%)
5.Sharpe Ratio

These metrics measure profitability and risk.

**Visualization**

The project generates two key charts using Matplotlib:

1.Stock Price with Buy/Sell Signals
2.Portfolio Equity Curve

These visualizations help analyze strategy behavior and performance.

**Project Structure**

project/
│
├── data_manager.py        # Fetches and preprocesses market data
├── strategy.py            # Machine learning trading strategy
├── backtester.py          # Trade simulation engine
├── main.py                # Runs the full pipeline

**Technologies Used**
1.Python
2.Pandas
3.NumPy
4.Scikit-learn
5.Matplotlib
6.yFinance API






