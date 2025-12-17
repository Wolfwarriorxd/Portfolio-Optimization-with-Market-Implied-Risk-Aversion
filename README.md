# Portfolio Optimization using Market-Implied Risk Aversion

This project implements a **Markowitz mean–variance portfolio optimization framework**
to study the risk–return tradeoff across a diversified set of market and sector ETFs.
The analysis combines efficient frontier construction, investor indifference curves,
and market-implied risk preferences to derive an economically consistent optimal portfolio.

## Project Overview

- Built a **market-level Markowitz portfolio** using real historical price data
- Analyzed the **risk–return tradeoff** using the efficient frontier
- Incorporated **investor indifference curves** to identify the utility-maximizing portfolio
- Estimated optimal portfolio weights using **SciPy-based constrained optimization**
- Benchmarked optimized allocations against an **equal-weight market proxy** to analyze deviations

## Asset Universe

The portfolio is constructed using liquid, long-history ETFs representing multiple asset classes:

- Broad market equity (SPY)
- Sector ETFs: Financials, Technology, Consumer Staples, Healthcare
- Gold ETF as a diversification hedge

This setup enables meaningful diversification and realistic portfolio construction.

## Methodology

1. Retrieved adjusted close prices from **Tiingo**
2. Computed log returns and annualized expected returns and covariance
3. Constructed the **efficient frontier** under realistic allocation constraints
4. Optimized portfolio weights by **maximizing the Sharpe ratio**
5. Estimated **market-implied risk aversion** from equilibrium market returns
6. Overlaid **indifference curves** to identify the utility-maximizing portfolio
7. Benchmarked the optimized portfolio against an equal-weight allocation

## Key Results

- Optimized portfolio achieved an **expected annual return of ~13.7%**
- Portfolio volatility of **~15.0%**, reflecting controlled risk exposure
- **Sharpe ratio improvement of ~11%** over the equal-weight benchmark
- Optimal allocation concentrated in market and technology ETFs, with gold providing
  significant diversification benefits
- Certain assets were endogenously excluded due to inferior risk-adjusted contribution

All numerical outputs and plots are saved in the `results_Portfolio/` directory.

## Interpretation

The optimized portfolio lies on the **efficient frontier** and corresponds to the
tangency point with the **highest attainable indifference curve**, confirming that
the solution maximizes investor utility under market-implied risk preferences rather
than arbitrary assumptions.

Benchmark comparison shows that the optimized portfolio **dominates a naive
equal-weight allocation in risk-adjusted terms**, validating the economic value
of the optimization.

## Tools Used

- Python
- NumPy, Pandas
- SciPy (optimization)
- Matplotlib
- Tiingo API (market data)
- FRED (risk-free rate)

## How to Run

1. Add your Tiingo API key in the notebook
2. Run the notebook end-to-end
3. Results and plots are saved automatically in `results_Portfolio/`

## Author

Anish Deshmukh  
Portfolio Optimization Project

