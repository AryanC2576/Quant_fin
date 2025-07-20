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

The "Buy and Hold" strategy generated a cumulative return of 5.09x over the period.

The "MA Crossover Strategy" generated a cumulative return of 2.31x over the same period.

### Performance Comparison: 
The MA strategy generally lagged behind buy-and-hold during strong bull markets but showed better capital preservation during extended downtrends

### Annualized Sharpe Ratio

The strategy achieved an Annualized Sharpe Ratio of 0.97. This range is often considered low risk/low reward or sub-optimal by some, but others classify anything above 0 as positive. A 0.97 is on the higher end of this range.

## Limitations of Current Backtest
-No Transaction Costs: Real-world trading involves fees which would reduce profitability, especially for a strategy with frequent trades.

-No Slippage: Assumes perfect trade execution at the calculated price, which is unrealistic in volatile markets.

-Single Asset Focus: Strategy is tested only on BTC/USD. Its effectiveness may vary greatly across other assets.

-Simple Moving Average: More advanced moving average types or adaptive indicators might yield different results.

-No Risk Management: Lacks explicit stop-loss or take-profit mechanisms.

-No Position Sizing: Assumes a fixed position size.

## Future Enhancements (Next Steps for the Project)
-Introduce Transaction Costs & Slippage: Incorporate realistic trading fees and an estimation of slippage into the return calculation.

-Optimize MA Window: Test different window values (e.g., 50, 100 days) to find potentially better performance.

-Implement Dual Moving Average Crossover: Develop a strategy using two MAs (e.g., short-term vs. long-term MA).

-Add Additional Indicators: Explore combining the MA with RSI, MACD, or volume analysis for stronger signals.

-Implement Risk Management: Add dynamic stop-loss and take-profit levels.

-Explore Short Selling: Allow the strategy to profit from downtrends by taking short positions.

-Multi-Asset Backtesting: Test the strategy across a portfolio of cryptocurrencies.

-Visual Enhancements: Add trade entry/exit points to the plots for clearer visualization.

-Modularize Code: Refactor the notebook into separate Python functions or modules for better organization.

## Disclaimer

This code is provided for educational and illustrative purposes only. It does not constitute financial advice, and past performance is not indicative of future results. Trading cryptocurrencies carries substantial risk, and you could lose all of your capital. Always conduct your own thorough research and consult with a qualified financial professional before making any investment decisions.

## License
