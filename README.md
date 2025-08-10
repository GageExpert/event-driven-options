# Earnings Calendar Options Scanner

## Overview
This project scans equity options for earnings-related calendar spread opportunities.  
It compares front-week implied volatility (IV) vs back-month IV, and outputs trades  
where near-term IV is unusually high before earnings.

## Data
- Earnings dates: manually collected or from API (e.g., Yahoo Finance)
- Options chain: downloaded from yfinance

## Outputs
- List of tickers with large IV term structure gaps
- Recommended calendar spreads (strike, expiry, entry price)
- Breakevens and P&L chart

## Example Chart
![Equity Curve](figs/example_chart.png)

## Skills Demonstrated
- Python (pandas, numpy, matplotlib)
- Options Greeks (delta, theta, vega)
- Trade structuring
- Backtesting basics
