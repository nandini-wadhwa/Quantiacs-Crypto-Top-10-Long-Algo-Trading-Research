# S12 – Correlation-Aware BTC Relative Strength

## Motivation

Previous research identified BTC Relative Strength as the strongest source of alpha within the cryptocurrency universe.

The BTC Relative Strength strategy achieved:

- Sharpe Ratio: 1.561

However, exploratory analysis also revealed that market correlations increase substantially during periods of stress.

Average Pairwise Correlation:

- Bull Market: 0.469
- Bear Market: 0.619

This suggests that diversification becomes less effective when risk is highest.

---

## Research Question

Can correlation information improve BTC Relative Strength when used as a risk-management overlay rather than a standalone trading signal?

---

## Hypothesis

BTC Relative Strength should remain the primary source of alpha.

Correlation should not be used to determine which assets to buy.

Instead, correlation should be used to determine how much risk to take.

When market-wide correlation is elevated, portfolio exposure should be reduced.

When correlations are lower and diversification is more effective, portfolio exposure can remain higher.

This should improve risk-adjusted returns without significantly reducing alpha generation.

---

## Expected Behaviour

The strategy should:

1. Continue selecting assets using BTC Relative Strength.
2. Maintain exposure during favorable market conditions.
3. Reduce exposure during periods of elevated market stress.
4. Improve Sharpe ratio through volatility and drawdown reduction.

---

## Risk Management Framework

### Alpha Generation

BTC Relative Strength

### Risk Control

Correlation Regime Scaling

### Market Filter

BTC 200-Day Regime Filter

---

## Success Criteria

- Sharpe Ratio greater than S07 (1.561)
- Lower volatility than S07
- Lower maximum drawdown than S07
- Demonstrate that correlation is more useful as a risk-management factor than as an alpha factor

---

## Why This Strategy Matters

Previous research showed:

- Momentum added little incremental value beyond BTC Relative Strength.
- Volume added little incremental value beyond BTC Relative Strength.
- Correlation performed poorly as a standalone timing signal.

This strategy tests a different hypothesis:

Correlation may not generate alpha, but it may improve the efficiency of alpha-generating strategies through superior risk management.

The strategy therefore represents the combination of the strongest alpha factor discovered during research (BTC Relative Strength) with the strongest risk-management insight discovered during research (Correlation Regime Awareness).