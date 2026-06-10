# Implementation

## Base Strategy

S02 uses the same cross-sectional momentum framework developed in S01.

The following components remain unchanged:

* 21-Day Momentum
* 63-Day Risk-Adjusted Momentum
* Drawdown Quality
* Inverse Volatility Weighting
* Liquidity Filtering

---

## Market Regime Filter

A 200-day moving average is calculated using Bitcoin prices.

Bitcoin is used because it acts as the dominant market factor within the cryptocurrency ecosystem.

### Bull Regime

BTC Price > BTC 200-Day Moving Average

Portfolio remains active.

### Bear Regime

BTC Price ≤ BTC 200-Day Moving Average

Portfolio moves entirely to cash.

---

## Portfolio Construction

Portfolio construction follows the same process as S01:

1. Rank assets by composite momentum score.
2. Select highest-ranked assets.
3. Apply inverse-volatility weighting.
4. Normalize weights.

The regime filter is applied after portfolio construction.

---

## Risk Management

The Bitcoin regime filter serves as a market-level risk management overlay.

Rather than attempting to predict individual asset behaviour during market stress, the strategy removes exposure when the broader market trend becomes unfavorable.

---

## Research Objective

Determine whether market regime awareness improves momentum performance relative to the continuously invested baseline established in S01.
