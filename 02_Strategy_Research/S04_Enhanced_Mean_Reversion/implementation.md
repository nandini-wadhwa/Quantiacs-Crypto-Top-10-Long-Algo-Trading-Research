# Implementation

## Base Strategy

S04 uses the same mean reversion framework developed in S03.

Assets are ranked according to recent underperformance.

Recent losers are preferred.

---

## Mean Reversion Signal

A 5-day return is calculated.

Assets with the weakest recent performance receive the highest scores.

---

## Market Regime Filter

Bitcoin is used as a proxy for overall market conditions.

A 200-day moving average is calculated.

### Bull Regime

BTC Price > BTC 200-Day Moving Average

Strategy remains active.

### Bear Regime

BTC Price ≤ BTC 200-Day Moving Average

Portfolio moves to cash.

---

## Portfolio Construction

1. Rank assets using the mean reversion signal.
2. Select strongest candidates.
3. Apply inverse-volatility weighting.
4. Normalize portfolio weights.
5. Apply Bitcoin regime filter.

---

## Risk Management

Risk is controlled through:

* Liquidity filtering
* Cross-sectional diversification
* Inverse-volatility weighting
* Bitcoin regime filter

---

## Research Objective

Determine whether market regime awareness can improve the performance of mean reversion strategies within cryptocurrency markets.
