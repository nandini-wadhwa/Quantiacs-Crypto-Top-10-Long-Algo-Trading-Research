# Implementation

## Base Idea

Exploratory analysis revealed that Bitcoin acts as the dominant market factor within the cryptocurrency ecosystem.

Rather than treating all assets independently, this strategy evaluates each asset relative to Bitcoin.

The objective is to identify cryptocurrencies that are outperforming the market leader.

---

## Signal Construction

### Bitcoin Momentum

A 21-day return is calculated for Bitcoin.

BTC Momentum:

BTC Price / BTC Price 21 Days Ago - 1

---

### Asset Momentum

A 21-day return is calculated for every cryptocurrency in the liquid universe.

Asset Momentum:

Asset Price / Asset Price 21 Days Ago - 1

---

### Relative Strength

Relative Strength is defined as:

Asset Momentum - Bitcoin Momentum

Assets outperforming Bitcoin receive positive scores.

Assets underperforming Bitcoin receive negative scores.

---

## Market Regime Filter

A 200-day moving average is calculated using Bitcoin prices.

### Bull Market

BTC Price > BTC 200-Day Moving Average

Portfolio remains active.

### Bear Market

BTC Price ≤ BTC 200-Day Moving Average

Portfolio moves to cash.

---

## Portfolio Construction

1. Calculate Bitcoin momentum.
2. Calculate asset momentum.
3. Compute relative strength versus Bitcoin.
4. Rank assets by relative strength.
5. Select highest-ranked assets.
6. Apply inverse-volatility weighting.
7. Normalize portfolio weights.
8. Apply Bitcoin regime filter.

---

## Risk Management

Risk management is controlled through:

- Liquidity filtering
- Inverse-volatility weighting
- Cross-sectional diversification
- Bitcoin regime filter

---

## Research Objective

Determine whether relative strength versus Bitcoin provides a stronger signal than traditional momentum.

If successful, this would support the hypothesis that Bitcoin acts as the dominant market factor and that leadership should be measured relative to Bitcoin rather than in absolute terms.