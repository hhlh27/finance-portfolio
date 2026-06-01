# finance-portfolio
# Finance Portfolio — Quantitative Finance & Fintech Projects

A collection of Python notebooks built while learning quantitative finance
and fintech engineering. Each month covers progressively more advanced topics,
from market data analysis to backtesting trading strategies.

---

## Month 1 — Python for Finance Foundations

**Tools:** Python, pandas, numpy, matplotlib, yfinance

### What I built
- Downloaded and analysed 1 year of daily OHLCV market data for 
  SPY, QQQ, GLD, TLT using yfinance
- Computed daily and log returns, rolling 20-day volatility, 
  and return distribution with kurtosis analysis
- Built a 50/200-day moving average crossover signal detector
- Computed proper Sharpe ratio (with risk-free rate), max drawdown,
  and annualised volatility across 4 asset classes
- Plotted call and put options payoff diagrams with breakeven analysis
- Built a 6-asset correlation heatmap and interpreted diversification
  properties across equities, bonds, gold, crypto and real estate

### Key findings
- QQQ and SPY correlation of 0.95 — largely redundant for diversification
- TLT showed near-zero correlation with equities (~0.09 with SPY),
  breaking the historical negative relationship post-2022 rate hikes
- BTC now 0.50 correlated with SPY — institutional flows have 
  eroded the uncorrelated narrative
- SPY return distribution shows excess kurtosis — fat tails mean
  normal distribution models underestimate real risk

---

## Month 2 — Backtesting & Fintech Stack

**Tools:** Python, pandas, numpy, matplotlib, SQLite, REST APIs

### What I built
- Built a backtesting engine from scratch on a 50/200-day MA 
  crossover strategy applied to SPY over 5 years
- Implemented proper signal shifting (+1 day) to eliminate 
  lookahead bias
- Computed full performance tearsheet: total return, annualised
  return, volatility, Sharpe ratio, max drawdown
- Measured transaction costs and trade frequency (5 trades / 5 years)

### Strategy results vs benchmark
| Metric | MA Crossover | Buy & Hold SPY |
|--------|-------------|----------------|
| Total Return | 69.86% | 93.00% |
| Ann. Return | 11.36% | 14.67% |
| Ann. Volatility | 11.95% | 17.06% |
| Sharpe Ratio | 0.57 | 0.60 |
| Max Drawdown | -18.76% | -24.50% |

### Key finding
The strategy successfully avoided the 2022 bear market by sitting
in cash, preserving capital while buy-and-hold fell ~22%. Despite
underperforming on total return, the strategy achieved a near-
identical Sharpe ratio with significantly lower volatility and
a shallower max drawdown — a meaningful tradeoff for risk-averse
investors.

---

## How to run

1. Clone the repository
   git clone https://github.com/hhlh27/finance-portfolio.git

2. Install dependencies
   pip install pandas numpy matplotlib yfinance seaborn jupyter

3. Launch Jupyter
   jupyter notebook

4. Open any notebook and run all cells (Kernel → Restart & Run All)

---
