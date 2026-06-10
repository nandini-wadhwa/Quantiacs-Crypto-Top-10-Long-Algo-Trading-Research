# Implementation

## Tail Event Detection

Daily returns are calculated.

A rolling 60-day volatility estimate is used.

Tail Score:

Daily Return / 60-Day Volatility

---

## Tail Threshold

Assets are flagged when:

Tail Score > 3

indicating a move greater than three standard deviations.

---

## Ranking

Assets with the strongest tail events receive the highest scores.

---

## Portfolio Construction

1. Calculate daily returns.
2. Calculate rolling volatility.
3. Compute tail score.
4. Rank assets.
5. Select strongest candidates.
6. Apply inverse-volatility weighting.
7. Normalize portfolio weights.

---

## Risk Management

- Liquidity filtering
- Inverse-volatility weighting
- BTC SMA200 regime filter