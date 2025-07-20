# Quant_fin
## Project Title:

Bitcoin (BTC/USD) 20-Day Moving Average Momentum Strategy Backtest

## Description: 

This repository contains a Python-based backtest of a simple 20-day Simple Moving Average (SMA) momentum strategy applied to Bitcoin (BTC/USD). The primary goal is to demonstrate basic quantitative trading strategy implementation, data acquisition, performance calculation, and visualization using popular Python libraries.
This project serves as an introductory exercise into algorithmic trading concepts and provides a foundational template for exploring more complex strategies.

## Methodology

### Strategy Logic

The strategy follows a basic trend-following rule:
1.  **Go Long (Buy/Hold):** When the daily **closing price** of Bitcoin (BTC/USD) crosses **above** its 20-day Simple Moving Average (SMA).
2.  **Go to Cash (Sell):** When the daily **closing price** of Bitcoin (BTC/USD) crosses **below** its 20-day Simple Moving Average (SMA).

For simplicity, this backtest assumes:
* Trades are executed at the next day's opening price based on the previous day's signal (to avoid look-ahead bias).
* No transaction costs (e.g., exchange fees, network fees).
* No slippage (perfect execution at the specified price).
* No short selling (only long positions or cash).

### Data Source

Historical daily BTC/USD price data is fetched using the `yfinance` library, which sources data from Yahoo Finance. This method was chosen for its ease of use and reliability in accessing historical financial data without requiring API keys or encountering common geographical access restrictions.

## Results & Analysis

The backtest was conducted on BTC/USD daily data from [July 20,2022] to [July 20,2025].

### Price vs. Moving Average

![BTC Price vs MA Plot](https://raw.githubusercontent.com/AryanC2576/Quant_fin/refs/heads/main/price_ma_plot.png)

### Cummulative Performane

![Cummulative Performance Plot](https://raw.githubusercontent.com/AryanC2576/Quant_fin/refs/heads/main/cummulative_performance_plot.png)

### Key Observations

The "Buy and Hold" strategy generated a cumulative return of [X.XX]x over the period.

The "MA Crossover Strategy" generated a cumulative return of [Y.YY]x over the same period.

### Performance Comparison: 
The MA strategy generally lagged behind buy-and-hold during strong bull markets but showed better capital preservation during extended downtrends

Annualized Sharpe Ratio: The strategy achieved an Annualized Sharpe Ratio of [Z.ZZ]. [e.g., "This indicates a moderate (or good/poor) risk-adjusted return compared to simply holding the asset."].
