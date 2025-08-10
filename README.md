# Earnings Calendar Options Scanner

## Overview
This project scans equity options for earnings-related **calendar spread** opportunities.  
It compares **front-week implied volatility (IV)** vs **back-month IV** into earnings,  
and outputs trades where near-term IV is unusually high before the earnings date.

## Workflow
1. Load a list of tickers and their upcoming earnings dates.
2. Pull options chain data for each ticker (using `yfinance` or similar).
3. Calculate front-week and back-month IV.
4. Flag tickers where **front IV / back IV > threshold** (e.g., 1.25).
5. Suggest calendar spreads: buy back-month ATM, sell front-week ATM.
6. Output breakevens, max loss, and P&L scenarios.

## Data
- `data/earnings.csv`: sample tickers with earnings dates
- Options chain from Yahoo Finance (via `yfinance`)

## Outputs
- CSV of candidate trades with strike, expiry, IVs
- P&L chart for each candidate
- Greeks snapshot for each trade

## Example Chart
![Calendar Spread P&L](figs/example_chart.png)

## Skills Demonstrated
- Python (pandas, numpy)
- Financial data collection with `yfinance`
- Options Greeks (delta, theta, vega)
- Volatility term structure analysis
- Data visualization with matplotlib
