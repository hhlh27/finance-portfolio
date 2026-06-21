# finance-portfolio
# Finance Portfolio — Quantitative Finance & Fintech Projects

A collection of Python notebooks built while learning quantitative finance
and fintech engineering. Each month covers progressively more advanced topics,
from market data analysis to backtesting trading strategies.

---

## Showcase Project — Algorithmic Trading Strategy

**File:** showcase_ma_strategy.ipynb


### What it does
End-to-end systematic trading strategy covering:
- Live market data pipeline via Alpaca brokerage API + SQLite
- 3-year backtest of 50/200-day MA crossover on SPY, QQQ, GLD
- Full performance tearsheet: Sharpe, drawdown, transaction costs
- Multi-asset comparison across SPY, QQQ, GLD
- Portfolio correlation analysis across 6 asset classes
- Options payoff diagram with breakeven analysis

### Key results

**SPY — core strategy**
| Metric          | MA Strategy | Buy & Hold SPY |
|-----------------|-------------|----------------|
| Total Return    | 29.34%      | 31.02%         |
| Ann. Return     | 8.93%       | 10.20%         |
| Ann. Volatility | 12.94%      | 18.46%         |
| Sharpe Ratio    | 0.34        | 0.31           |
| Max Drawdown    | -18.98%     | -22.76%        |

**Multi-asset comparison**
| Asset | Strategy Return | Buy & Hold | Strategy Sharpe |
|-------|----------------|------------|-----------------|
| SPY   | 29.34%         | 31.02%     | 0.34            |
| QQQ   | 57.30%         | 46.08%     | 0.67            |
| GLD   | 44.48%         | 69.57%     | 0.59            |

**Correlation findings**
- SPY-QQQ: 0.94 — nearly identical, limited diversification benefit
- SPY-TLT: 0.15 — stock-bond relationship weakened post-2022 rate hikes
- SPY-GLD: 0.32 — gold offers partial diversification
- SPY-BTC: 0.51 — crypto now moves with equities

### Key finding
Strategy avoided the 2022 bear market — held cash while SPY dropped ~20%.
QQQ strategy outperformed buy-and-hold on both return (57.30% vs 46.08%)
and Sharpe (0.67 vs 0.43) — the strongest result across all assets tested.

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
