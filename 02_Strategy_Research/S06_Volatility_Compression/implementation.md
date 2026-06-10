# Implementation

## Signal Construction

The strategy compares:

20-Day Volatility

to

60-Day Volatility

Volatility Compression Ratio:

20D Volatility / 60D Volatility

---

## Interpretation

Low values indicate:

- Current volatility is unusually low
- Market is consolidating
- Volatility expansion may follow

Assets with the strongest compression receive the highest scores.

---

## Portfolio Construction

1. Calculate daily returns
2. Calculate 20-day volatility
3. Calculate 60-day volatility
4. Compute compression ratio
5. Rank assets
6. Select strongest candidates
7. Apply inverse-volatility weighting
8. Normalize weights

---

## Risk Management

- Liquidity filtering
- Cross-sectional diversification
- Inverse-volatility weighting

No regime filter is applied in the baseline version.