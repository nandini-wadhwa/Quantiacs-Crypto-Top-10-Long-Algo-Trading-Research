# S04 – Regime-Aware Mean Reversion

## Motivation

S03 demonstrated that a standalone mean reversion strategy produced poor risk-adjusted performance.

Although a weak mean reversion effect was identified during exploratory analysis, the resulting portfolio generated a Sharpe ratio of only 0.37 and suffered severe drawdowns.

Previous research showed that market regime strongly influences cryptocurrency returns.

Bull Market Average Return: +0.503%

Bear Market Average Return: -0.199%

This suggests that temporary pullbacks may be more likely to recover during bullish environments than during bearish environments.

---

## Research Question

Can mean reversion performance be improved by restricting trades to bullish market regimes?

---

## Hypothesis

Recent losers will exhibit stronger recovery behaviour when the broader cryptocurrency market is in an uptrend.

Applying a Bitcoin-based regime filter should improve the performance of the mean reversion strategy.

---

## Expected Behaviour

### Bull Markets

Temporary pullbacks should recover more frequently.

Mean reversion should perform better.

### Bear Markets

Recent losers may continue declining.

The strategy should avoid these environments.

---

## Success Criteria

Compared to S03:

* Higher Sharpe Ratio
* Lower Maximum Drawdown
* Lower Turnover
* Improved Equity Growth

---

## Link to Previous Research

Finding 2: Mean Reversion Exists

Finding 3: Market Regime Dominates Performance

This strategy combines both findings.
