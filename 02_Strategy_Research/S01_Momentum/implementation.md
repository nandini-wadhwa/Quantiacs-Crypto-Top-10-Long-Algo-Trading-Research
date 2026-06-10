# Implementation

## Universe

The strategy operates on the Quantiacs Crypto Daily universe.

Only assets classified as liquid using the provided `is_liquid` flag are eligible for inclusion.

This ensures the portfolio remains investable and avoids assets with insufficient liquidity.

---

## Signal Construction

The strategy combines three momentum-related signals.

### 1. Short-Term Momentum

21-day returns are used to measure recent price strength.

Assets with stronger recent performance receive higher scores.

### 2. Risk-Adjusted Momentum

63-day returns are scaled by recent volatility.

This rewards assets that have generated strong returns while controlling for risk.

### 3. Drawdown Quality

Assets trading close to their 90-day highs receive higher scores.

This helps distinguish persistent trends from temporary rebounds.

---

## Composite Momentum Score

The final ranking score combines the three components:

| Component | Weight |
|------------|---------:|
| 21-Day Momentum | 45% |
| Risk-Adjusted Momentum | 35% |
| Drawdown Quality | 20% |

All signals are ranked cross-sectionally before aggregation.

---

## Portfolio Construction

### Asset Selection

Assets are ranked by the composite momentum score.

The highest-ranked assets are selected for inclusion in the portfolio.

### Position Sizing

Inverse-volatility weighting is applied.

Lower-volatility assets receive larger allocations while higher-volatility assets receive smaller allocations.

### Weight Normalization

Portfolio weights are normalized to ensure full capital deployment.

---

## Risk Management

No market timing or regime filter is used in this version.

The portfolio remains invested continuously.

Risk is controlled only through:

- Liquidity filtering
- Cross-sectional ranking
- Inverse-volatility weighting

---

## Research Objective

This strategy represents the first attempt to monetize the momentum persistence identified during the exploratory data analysis phase.

Its performance will establish the baseline against which all future strategies are evaluated.