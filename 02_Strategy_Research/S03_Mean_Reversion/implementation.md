# Implementation

## Universe

Quantiacs Crypto Daily Universe.

Only assets satisfying the liquidity filter are eligible.

---

## Signal Construction

The strategy uses short-term price weakness as the primary signal.

### 5-Day Return

Recent returns are calculated over a 5-day horizon.

Assets experiencing the largest declines receive the highest scores.

---

## Ranking Logic

Unlike momentum strategies, rankings are inverted.

Recent losers are preferred.

Recent winners are avoided.

---

## Portfolio Construction

### Asset Selection

Assets are ranked according to their mean reversion score.

The strongest mean reversion candidates are selected.

### Position Sizing

Inverse-volatility weighting is applied.

### Weight Normalization

Weights are normalized to ensure full capital deployment.

---

## Risk Management

Risk management is limited to:

* Liquidity filtering
* Cross-sectional diversification
* Inverse-volatility weighting

No market regime filter is applied.

---

## Research Objective

Determine whether the mean reversion effect observed during exploratory analysis can be translated into a profitable trading strategy.
