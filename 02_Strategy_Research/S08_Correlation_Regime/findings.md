# Findings

## Research Outcome

The correlation regime strategy improved drawdown characteristics but reduced overall performance relative to BTC Relative Strength.

The strategy achieved:

- Sharpe Ratio: 1.145
- Max Drawdown: -81.2%
- Equity: 192.9

---

## What Worked

### Correlation Contains Risk Information

Periods of elevated market correlation were associated with increased portfolio risk.

The correlation filter successfully reduced drawdowns relative to S07.

---

### Diversification Failure Was Real

The exploratory finding that diversification becomes less effective during stress periods was confirmed.

Assets became increasingly synchronized during adverse market environments.

---

## What Did Not Work

### Alpha Was Reduced

While risk decreased, return generation declined substantially.

The strategy underperformed the BTC Relative Strength benchmark.

---

### Filter Was Too Restrictive

The correlation regime frequently switched the strategy on and off.

This resulted in:

- High turnover
- Very short holding periods
- Lost exposure during profitable trends

---

## Key Insight

Correlation regime appears more useful as a risk management overlay than as a primary timing signal.

Bitcoin trend remains a stronger indicator of market conditions than cross-sectional correlation.

---

## Research Conclusion

The BTC regime filter captures most of the useful market timing information contained within correlation regimes.

Correlation should likely be used as a secondary risk-control mechanism rather than a standalone portfolio filter.

---

## Cross-Strategy Comparison

| Strategy | Sharpe |
|-----------|---------:|
| S07 BTC Relative Strength | 1.561 |
| S02 Regime Momentum | 1.520 |
| S01 Momentum | 1.285 |
| S08 Correlation Regime | 1.145 |
| S05 Volume Flow | 1.003 |
| S06 Volatility Compression | 0.670 |
| S04 Regime Mean Reversion | 0.541 |
| S03 Mean Reversion | 0.367 |