# Implementation

## Base Strategy

S08 builds upon the BTC Relative Strength framework developed in S07.

The core asset selection process remains unchanged:

- Identify assets outperforming Bitcoin
- Rank assets by relative strength
- Apply inverse-volatility weighting

The new component is a correlation regime filter.

---

## Motivation

Exploratory analysis revealed that average cryptocurrency correlations increase significantly during periods of market stress.

Average Pairwise Correlation:

- Bull Market: 0.469
- Bear Market: 0.619

This suggests diversification becomes less effective during unfavorable environments.

---

## Correlation Regime Signal

Direct calculation of rolling pairwise correlations across all assets is computationally expensive.

Instead, the strategy uses cross-sectional return dispersion as a proxy for correlation.

### Dispersion

For each day:

Cross-Sectional Dispersion = Standard Deviation of Returns Across Assets

Interpretation:

- High Dispersion → Assets behaving differently → Lower Correlation
- Low Dispersion → Assets moving together → Higher Correlation

---

## Correlation Filter

A 60-day moving average of dispersion is calculated.

### Low Correlation Regime

Current Dispersion > 60-Day Average Dispersion

Portfolio remains active.

### High Correlation Regime

Current Dispersion ≤ 60-Day Average Dispersion

Portfolio moves to cash.

---

## Relative Strength Signal

A 21-day momentum measure is calculated for:

- Bitcoin
- All liquid assets

Relative Strength:

Asset Momentum − Bitcoin Momentum

Assets outperforming Bitcoin receive higher scores.

---

## Portfolio Construction

1. Calculate asset momentum.
2. Calculate Bitcoin momentum.
3. Compute relative strength versus Bitcoin.
4. Rank assets by relative strength.
5. Select highest-ranked assets.
6. Apply inverse-volatility weighting.
7. Normalize portfolio weights.
8. Apply correlation regime filter.

---

## Risk Management

Risk is controlled through:

- Liquidity filtering
- Inverse-volatility weighting
- Cross-sectional diversification
- Correlation regime filter

---

## Research Objective

Determine whether market structure provides useful information beyond trend and momentum signals.

If successful, the strategy would demonstrate that diversification effectiveness itself can be used as a predictive factor for portfolio allocation.