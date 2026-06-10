# Findings

## Research Outcome

The addition of a Bitcoin-based regime filter improved the performance of the mean reversion strategy.

The strategy achieved:

- Sharpe Ratio: 0.541
- Equity: 4.42
- Lower turnover than S03
- Reduced drawdowns relative to S03

These results indicate that market regime plays an important role in determining when mean reversion strategies are effective.

---

## What Worked

### Regime Awareness Improved Mean Reversion

Restricting trades to bullish market environments improved performance across all major metrics.

The regime filter successfully avoided some of the prolonged declines that damaged the standalone mean reversion strategy.

---

### Drawdowns Were Reduced

Maximum drawdown improved from:

- S03: -97.96%
- S04: -90.87%

While still severe, the reduction confirms that market conditions influence the effectiveness of mean reversion signals.

---

### Turnover Declined

Turnover decreased from:

- S03: 0.303
- S04: 0.209

The regime filter reduced unnecessary trading activity during unfavorable environments.

---

## What Did Not Work

### Performance Remained Weak

Despite meaningful improvement, risk-adjusted returns remained substantially below those achieved by momentum-based strategies.

Sharpe Ratio Comparison:

- S02 Regime Momentum: 1.520
- S04 Regime Mean Reversion: 0.541

Momentum continued to dominate mean reversion by a large margin.

---

### Mean Reversion Remained Unstable

The strategy still experienced large drawdowns and failed to generate sufficiently attractive long-term growth.

This suggests that mean reversion opportunities in cryptocurrency markets are less persistent than momentum opportunities.

---

## Key Insight

Market regime matters for mean reversion.

However, regime awareness alone is insufficient to transform mean reversion into a competitive standalone strategy.

The underlying factor itself appears substantially weaker than momentum.

---

## Connection to Earlier Research

This result validates two findings from exploratory analysis:

- Mean reversion exists statistically.
- Market regime influences factor performance.

However, the experiment also demonstrates that statistical significance does not necessarily translate into economically significant alpha.

---

## Research Conclusion

Mean reversion can be improved through regime filtering, but remains materially weaker than momentum.

Future research effort should focus on stronger factors such as:

- Volume Leadership
- Volatility Compression
- Multi-Factor Models

rather than further optimization of standalone mean reversion.

---

## Next Research Question

Can abnormal trading volume predict future cryptocurrency returns?

This motivates:

**S05 – Volume Flow**