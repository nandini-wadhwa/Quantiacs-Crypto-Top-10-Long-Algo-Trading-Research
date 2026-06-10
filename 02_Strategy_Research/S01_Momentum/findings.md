# Findings

## Research Outcome

The strategy successfully converted the momentum persistence identified during exploratory analysis into a profitable trading strategy.

The results demonstrate that cross-sectional momentum is a viable source of alpha within the cryptocurrency market.

---

## What Worked

### Momentum Persistence Is Real

Assets that exhibited strong recent performance tended to continue outperforming weaker assets.

This confirms the positive momentum relationship identified during factor diagnostics.

The strategy generated attractive risk-adjusted returns while maintaining relatively low turnover.

---

### Risk-Adjusted Ranking Improved Portfolio Quality

Combining momentum with volatility adjustment improved the quality of asset selection.

Assets generating strong returns with lower volatility were generally more robust than assets selected solely on raw performance.

---

### Assets Near Highs Outperformed Recovering Assets

The drawdown-quality component provided useful information.

Assets trading near recent highs tended to maintain stronger trends than assets attempting to recover from deep drawdowns.

---

## What Did Not Work

### Market Direction Dominated Asset Selection

Although the strategy successfully identified stronger assets, performance remained highly sensitive to the overall market environment.

Periods of broad market weakness resulted in significant portfolio drawdowns despite effective asset ranking.

---

### Diversification Alone Was Insufficient

Holding multiple cryptocurrencies reduced idiosyncratic risk but did not provide adequate protection during market-wide selloffs.

This observation is consistent with the earlier finding that correlations increase during bearish regimes.

---

## Key Insight

The primary limitation of the strategy was not asset selection.

The primary limitation was remaining fully invested during unfavorable market conditions.

This suggests that market regime may be more important than security selection alone.

---

## Connection to Earlier Research

This result aligns with several findings from the exploratory analysis:

* Momentum persistence was positive.
* Bear markets exhibited negative expected returns.
* Correlations increased during periods of market stress.

Together these observations suggest that a market-regime filter may improve strategy performance.

---

## Next Research Question

Can momentum performance be improved by conditioning exposure on the broader cryptocurrency market regime?

This question motivates the development of:

**S02 – Regime-Aware Momentum**
