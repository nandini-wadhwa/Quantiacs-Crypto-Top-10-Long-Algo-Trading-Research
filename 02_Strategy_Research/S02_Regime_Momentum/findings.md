# Findings

## Research Outcome

The addition of a Bitcoin-based market regime filter significantly improved momentum strategy performance.

The strategy achieved:

* Sharpe Ratio: 1.520
* Equity: 2209
* Turnover: 0.091

and outperformed the continuously invested momentum strategy from S01.

---

## What Worked

### Market Regime Was Highly Informative

The Bitcoin 200-day moving average successfully identified periods where momentum strategies were more likely to perform well.

Restricting exposure to bullish market environments improved both returns and risk-adjusted performance.

---

### Drawdowns Were Reduced

The regime filter avoided a portion of the losses experienced during broad cryptocurrency market downturns.

This reduced portfolio drawdowns relative to the baseline momentum strategy.

---

### Turnover Improved

The strategy exhibited lower turnover than S01.

This suggests that the regime filter reduced unnecessary trading during unstable market conditions.

---

## Key Insight

The largest source of performance improvement did not come from better asset selection.

It came from better market participation.

Knowing when to be invested was more important than refining the momentum signal itself.

---

## Connection to Earlier Research

This result directly validates:

* Finding 3: Regime Impact on Returns
* Finding 7: Diversification Fails During Bear Markets

The exploratory analysis suggested that market environment dominates asset-level effects.

S02 confirms this hypothesis in a portfolio implementation.

---

## Research Conclusion

Market regime filtering appears to be one of the most powerful enhancements tested so far.

Future strategy development should incorporate regime awareness as a core component rather than an optional overlay.

---

## Next Research Question

Can weaker factors such as mean reversion be improved through regime awareness?

This motivates S03 – Mean Reversion.
