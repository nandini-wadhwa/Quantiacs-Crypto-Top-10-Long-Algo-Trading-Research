# Findings

## Research Outcome

The addition of correlation-based risk scaling significantly improved the performance of BTC Relative Strength.

The strategy achieved:

- Sharpe Ratio: 1.715
- Max Drawdown: -69.3%
- Volatility: 0.547

This represents the strongest risk-adjusted performance observed during the research process.

---

## What Worked

### Correlation Improved Risk Management

Unlike S08, which used correlation as a binary market-timing signal, S12 used correlation as a position-sizing mechanism.

This preserved exposure during favorable periods while reducing risk during periods of elevated market stress.

---

### Significant Drawdown Reduction

Maximum drawdown improved from:

-87.8%

to

-69.3%

representing one of the largest drawdown improvements observed during the study.

---

### Improved Risk-Adjusted Returns

Sharpe ratio increased from:

1.561

to

1.715

demonstrating that correlation contains valuable risk information when used appropriately.

---

## Key Insight

Correlation is not an effective alpha signal.

However, correlation is highly effective as a risk-management signal.

The strongest results were achieved when BTC Relative Strength generated alpha and correlation controlled position sizing.

---

## Research Conclusion

The primary source of alpha in cryptocurrency markets appears to be BTC Relative Strength.

The primary source of risk control appears to be correlation regime awareness.

Combining these two elements produced the strongest strategy developed during the research process.

---

## Cross-Strategy Comparison

| Strategy | Sharpe |
|-----------|---------:|
| S12 BTC RS + Correlation Risk | 1.715 |
| S07 BTC Relative Strength | 1.561 |
| S10 BTC RS + Momentum | 1.561 |
| S11 BTC RS + Volume | 1.544 |
| S02 Regime Momentum | 1.520 |