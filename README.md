# Portfolio Optimization with Market-Implied Risk Aversion

This project implements a **constrained Markowitz mean–variance portfolio optimization**
framework using real historical market data from Tiingo. The objective is to construct
a diversified portfolio that maximizes risk-adjusted returns while remaining consistent
with market-equilibrium risk preferences.

## Key Features

- Mean–variance portfolio optimization under realistic allocation constraints
- Efficient frontier construction using annualized returns and covariance
- Estimation of **market-implied risk aversion** from equilibrium risk premia
- Visualization of investor **indifference curves** and utility-maximizing portfolio
- Empirical validation via **benchmark dominance** against an equal-weight portfolio

## Asset Universe

The portfolio is constructed using liquid, long-history ETFs representing
multiple asset classes:

- Broad market equities (SPY)
- Sector ETFs: Financials, Technology, Consumer Staples, Healthcare
- Gold ETF as a diversification hedge

## Methodology Overview

1. Historical adjusted close prices are retrieved from Tiingo
2. Log returns are computed and annualized
3. Expected returns and covariance matrix are estimated
4. Portfolio optimization is performed by maximizing the Sharpe ratio subject to:
   - Long-only weights
   - Full investment
   - Asset concentration limits
5. The efficient frontier is constructed
6. Market-implied risk aversion is inferred from the market portfolio
7. Indifference curves are overlaid to identify the utility-maximizing portfolio
8. Performance is benchmarked against an equal-weight allocation


## Results Summary

- The optimized portfolio lies on the efficient frontier and maximizes investor utility
  under market-implied risk preferences.
- The portfolio **outperforms an equal-weight benchmark in Sharpe ratio**, confirming
  superior risk-adjusted performance.
- Constraints lead to realistic corner solutions, reflecting practical portfolio construction.

All numerical results and plots are saved in the `results_Portfolio/` directory.

## Tools and Libraries

- Python
- NumPy, Pandas
- SciPy (optimization)
- Matplotlib
- Tiingo API (market data)
- FRED (risk-free rate)

## How to Run

1. Add your Tiingo API key in the notebook
2. Run all cells top to bottom
3. Final results and plots will be saved automatically

## Author

Anish Deshmukh  
Portfolio Optimization Project
