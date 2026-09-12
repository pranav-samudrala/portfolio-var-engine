
# Quantitative Portfolio Risk & VaR Engine

## Objective
Calculate Value-at-Risk (VaR), stress test multi-asset portfolios, and evaluate counterparty exposure (PFE/CVA) using Monte Carlo simulations. Tailored for MS Counterparty Risk, UBS QRM, and Morningstar.

## Tech Stack
- **Languages:** Python, SQL
- **Libraries:** pandas, numpy, statsmodels, arch, yfinance, matplotlib/seaborn
- **Dashboard:** Streamlit

## Project Blueprint
1. **Data Ingestion:** Download 5+ years of daily data for 5 assets (SPY, TLT, GLD, AAPL, MSFT) using `yfinance`.
2. **Risk Metrics:** Calculate daily returns, annualized volatility, Sharpe Ratio, Maximum Drawdown, and Correlation Matrix (store in SQL).
3. **VaR Modeling:** 
   - Historical VaR (95%, 99%)
   - Parametric VaR (Variance-Covariance)
   - Monte Carlo Simulation (Geometric Brownian Motion)
4. **Econometrics:** OLS regression (CAPM), Fama-French 3-factor model.
5. **Stress Testing:** Simulate a 2008-style crash (shock equity prices by -40%).
6. **Counterparty Exposure (PFE/CVA):**
   - Simulate interest rate/FX paths using GBM.
   - Calculate Expected Exposure (EE) profile.
   - Compute simplified CVA for a small derivatives portfolio.
