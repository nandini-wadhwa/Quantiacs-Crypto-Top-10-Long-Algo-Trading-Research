# Findings

## Research Outcome

The volatility compression strategy generated positive returns but failed to achieve the performance of momentum-based strategies.

The strategy achieved:

* Sharpe Ratio: 0.670
* Equity: 9.12
* Average Turnover: 0.241
* Average Holding Time: 8.98 Days

These results suggest that volatility compression contains useful information, but is insufficient as a standalone trading factor.

---

## What Worked

### Volatility Compression Contains Predictive Information

The strategy generated positive risk-adjusted returns, confirming the exploratory finding that volatility compression is associated with future market activity.

Assets exhibiting unusually low short-term volatility often experienced larger subsequent moves.

---

### Moderate Holding Period

The strategy naturally produced holding periods of approximately 9 days, indicating that volatility expansion tends to occur relatively quickly after compression develops.

---

### Positive Standalone Performance

Despite relying on a single factor, the strategy achieved a positive Sharpe ratio and outperformed both mean reversion strategies.

This validates volatility compression as a legitimate source of information within cryptocurrency markets.

---

## What Did Not Work

### Performance Remained Below Momentum

Sharpe Ratio Comparison:

* S02 Regime Momentum: 1.520
* S01 Momentum: 1.285
* S06 Volatility Compression: 0.670

Momentum remained substantially more effective than volatility compression.

---

### Drawdowns Remained Severe

The strategy continued to experience large drawdowns during unfavorable market conditions.

Compression alone did not provide protection against broader market weakness.

---

### Direction Was Missing

The primary weakness of the factor is that volatility compression predicts the likelihood of a future move, but not its direction.

A compressed asset may subsequently break higher or lower.

The signal identifies opportunity but not directional bias.

---

## Key Insight

Volatility compression appears to predict future activity rather than future returns.

The factor is informative, but lacks directional information.

This limits its effectiveness as a standalone strategy.

---

## Connection to Earlier Research

The result aligns with exploratory analysis:

* Volatility Compression IC: +0.0242
* Momentum IC: +0.0212

Although compression displayed predictive power statistically, the resulting portfolio remained weaker than momentum-based implementations.

This reinforces the distinction between statistical significance and tradable alpha.

---

## Research Conclusion

Volatility compression is a useful supporting factor but is unlikely to serve as a primary source of alpha on its own.

The factor appears better suited as a confirmation signal within a broader multi-factor framework.

---

## Cross-Strategy Comparison

| Strategy                   | Sharpe |
| -------------------------- | -----: |
| S02 Regime Momentum        |  1.520 |
| S01 Momentum               |  1.285 |
| S05 Volume Flow            |  1.003 |
| S06 Volatility Compression |  0.670 |
| S04 Regime Mean Reversion  |  0.541 |
| S03 Mean Reversion         |  0.367 |

Momentum remains the strongest standalone factor tested so far.

---

