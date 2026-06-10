# Implementation

## Universe

Quantiacs Crypto Daily Universe.

Only liquid assets are eligible.

---

## Signal Construction

A volume ratio is calculated.

Volume Ratio:

Current Volume / 20-Day Average Volume

Assets exhibiting unusually high volume receive higher scores.

---

## Ranking Logic

Assets are ranked cross-sectionally according to volume abnormality.

Higher volume relative to recent history results in higher rankings.

---

## Portfolio Construction

1. Calculate volume ratio.
2. Rank assets.
3. Select highest-ranked assets.
4. Apply inverse-volatility weighting.
5. Normalize weights.

---

## Risk Management

Risk is controlled through:

- Liquidity filtering
- Cross-sectional diversification
- Inverse-volatility weighting

No regime filter is applied in this baseline version.

---

## Research Objective

Determine whether abnormal volume contains predictive information that can be converted into a profitable trading strategy.