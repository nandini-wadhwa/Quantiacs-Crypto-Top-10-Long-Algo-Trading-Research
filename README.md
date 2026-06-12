# Quantiacs Crypto Top-10 — Long-Only Algorithmic Trading Research

> **Systematic factor research on the large-cap cryptocurrency universe.**  
> Built for the [Quantiacs Crypto Top-10 Long-Only Contest](https://quantiacs.com).

---

## What This Repository Is

This is an end-to-end quantitative research project, not a collection of scripts.

Every strategy traces back to a numbered empirical finding. Every finding traces back to a data exploration test. Every negative result is documented and explained. The goal was to understand *why* things work or fail in large-cap crypto — not just to find a high Sharpe ratio.

**Universe:** Top-10 cryptocurrencies by market cap (dynamic)  
**Constraint:** Long-only · Daily rebalancing · `is_liquid == 1` hard mask  
**Period:** January 2015 – June 2026  
**Platform:** [Quantiacs](https://quantiacs.com) · `qnt` Python library

---

## Repository Structure

```
├── 00_Research_Framework/        Research hypothesis, design decisions, methodology
├── 01_Data_Exploration/          Market characteristics, factor ICs, empirical findings
├── 02_Strategy_Research/         9 individual strategies — one per factor hypothesis
├── 03_Multi_Factor_Research/     Combining proven signals — S10, S11, S12
└── 04_Academic_Replication/      Published papers replicated on Quantiacs data
    └── R01_Financial_And_Social_Features/
```

---

## The Research Story

The project followed a strict hypothesis-first process:

```
Explore data  →  measure factor ICs  →  form hypothesis
      ↓
Build simplest possible strategy  →  measure result
      ↓
Explain what worked and what failed  →  build next iteration
```

## Phase 1 — Data Exploration

Data exploration revealed eight key empirical findings regarding the behaviour of large-cap cryptocurrencies.

| Finding                    | Metric                                                                     | Implication                                               |
| -------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------- |
| F1: Momentum persistence   | Positive Information Coefficient                                           | Winners continue to outperform over intermediate horizons |
| F2: Mean reversion         | Negative Information Coefficient                                           | Short-term reversals exist but are economically weak      |
| F3: Regime asymmetry       | Bull markets significantly outperform bear markets                         | Market regime filters materially improve performance      |
| F4: Volume leadership      | Strongest Information Coefficient among tested factors                     | Relative volume contains predictive information           |
| F5: Volatility compression | Positive Information Coefficient                                           | Quiet periods often precede larger directional moves      |
| F6: BTC dominance          | Average pairwise correlation ≈ 0.50                                        | Bitcoin acts as the dominant market factor                |
| F7: Correlation in stress  | Correlation rises sharply during bear markets                              | Diversification deteriorates during market stress         |
| F8: Fat-tail behaviour     | Extreme events occur far more frequently than predicted by Gaussian models | Risk-adjusted sizing is essential                         |

Phase 2 tested each finding as a standalone strategy.

Phase 3 combined independently validated factors into multi-factor frameworks.

Phase 4 evaluates whether published academic findings generalise to the Quantiacs Top-10 cryptocurrency universe.

---

## Complete Strategy Results

### Phase 2 — Individual Strategies

| ID  | Strategy                | Signal                         | Sharpe |  Max DD | Finding                   |
| --- | ----------------------- | ------------------------------ | -----: | ------: | ------------------------- |
| S01 | Momentum Baseline       | 21d + 63d return ranks         |  1.285 | -92.21% | F1                        |
| S02 | Regime Momentum         | Momentum + BTC SMA200 gate     |  1.520 | -86.92% | F1 + F3                   |
| S03 | Mean Reversion          | Negative 21d return rank       |  0.367 | -97.96% | F2 — negative result      |
| S04 | Enhanced Mean Reversion | Mean Reversion + Regime Filter |  0.541 | -90.87% | F2 + F3 — negative result |
| S05 | Volume Flow             | Relative volume rank           |  1.003 |     TBD | F4                        |
| S06 | Volatility Compression  | Short-vol / Long-vol ratio     |  0.670 |     TBD | F5                        |
| S07 | BTC Relative Strength   | Coin return − BTC return       |  1.561 | -87.80% | F6                        |
| S08 | Correlation Regime      | Rolling pairwise correlation   |  1.145 |     TBD | F7                        |
| S09 | Tail Risk Timing        | 3σ+ daily move detection       |  0.888 |     TBD | F8                        |

### Phase 3 — Multi-Factor Research

| ID  | Strategy                          | Components                          | Sharpe |  Max DD | Research Question                                 | Conclusion                    |
| --- | --------------------------------- | ----------------------------------- | -----: | ------: | ------------------------------------------------- | ----------------------------- |
| S10 | BTC RS + Momentum                 | 0.50 × BTC RS + 0.50 × Momentum     |  1.561 | -87.80% | Is momentum independent of BTC Relative Strength? | No — BTC RS subsumes momentum |
| S11 | BTC RS + Volume                   | BTC RS + volume confirmation        |  1.544 | -87.40% | Does volume add independent alpha?                | No — marginal contribution    |
| S12 | BTC RS + Correlation Risk Scaling | BTC RS + dynamic correlation sizing |  1.715 | -69.30% | Can correlation improve risk-adjusted returns?    | Yes — best overall strategy   |

---

## Complete Rankings

| Rank | Strategy                              | Sharpe | Max Drawdown |
| ---- | ------------------------------------- | -----: | -----------: |
| 1    | S12 BTC RS + Correlation Risk Scaling |  1.715 |       -69.3% |
| 2    | S07 BTC Relative Strength             |  1.561 |       -87.8% |
| 3    | S10 BTC RS + Momentum                 |  1.561 |       -87.8% |
| 4    | S11 BTC RS + Volume                   |  1.544 |       -87.4% |
| 5    | S02 Regime Momentum                   |  1.520 |       -86.9% |
| 6    | S01 Momentum Baseline                 |  1.285 |       -92.2% |
| 7    | S08 Correlation Regime                |  1.145 |          --- |
| 8    | S05 Volume Flow                       |  1.003 |          --- |
| 9    | S09 Tail Risk Timing                  |  0.888 |          --- |
| 10   | S06 Volatility Compression            |  0.670 |          --- |
| 11   | S04 Enhanced Mean Reversion           |  0.541 |       -90.9% |
| 12   | S03 Mean Reversion                    |  0.367 |       -98.0% |

---

## Key Research Findings

**1. BTC Relative Strength is the dominant alpha factor (Sharpe 1.561).**  
Assets outperforming Bitcoin generated superior forward returns. This is a crypto-native mechanism — capital rotating from BTC into alts creates persistent relative momentum that plain absolute momentum does not independently add to.

**2. BTC Relative Strength subsumes absolute momentum.**  
S10 combined BTC RS with momentum at equal weight and achieved exactly 1.561 — identical to S07 alone. Assets outperforming Bitcoin are already the assets with the strongest absolute momentum. The two signals measure the same underlying phenomenon from different angles.

**3. Volume does not add independent alpha on top of BTC RS.**  
S11 added volume as a confirmation layer (Sharpe 1.544) — a slight decline from S07 (1.561). Volume contains useful information as a standalone signal, but assets attracting capital tend to already be identified through relative strength. Volume is better used as a filter than as a scoring component.

**4. Correlation is the most effective risk management tool.**  
S12 used rolling pairwise correlation as a position-sizing mechanism — not as a binary timing signal. This reduced maximum drawdown from −87.8% to −69.3% while increasing Sharpe from 1.561 to 1.715. The key distinction: correlation failed as an alpha signal (S08: 1.145) but succeeded as a risk overlay.

**5. Mean reversion failed three times — a robust negative result.**  
Raw (0.367), trend-filtered (0.541), regime-filtered (~0.50) — all below 1.0. Large-cap cryptocurrencies exhibit trend persistence. Three independent failures are evidence, not coincidence.

**6. Regime awareness was the single most impactful early enhancement.**  
The BTC SMA200 gate improved pure momentum Sharpe from 1.285 to 1.520 (+0.235) from one binary rule, motivating all subsequent regime-aware strategies.

---

## The Multi-Factor Insight

The progression from S07 → S10 → S11 → S12 answers a structured sequence of questions:

```
S07  Does BTC Relative Strength work alone?          → Yes (1.561)
S10  Is momentum independent of BTC RS?              → No  (1.561 — identical)
S11  Does volume add to BTC RS?                      → No  (1.544 — marginal decline)
S12  Does correlation improve risk management?       → Yes (1.715 — best overall)
```

The conclusion is precise: **BTC Relative Strength generates the alpha. Correlation controls the risk. Nothing else adds materially to either.**

---

## Factor Classification (Updated)

**Alpha Generator**
- BTC Relative Strength — the primary source of returns across all tested combinations

**Risk Manager**
- Correlation regime scaling — reduces drawdown without sacrificing returns

**Subsumed by BTC RS**
- Absolute momentum — same underlying signal, different frame
- Volume confirmation — captured within relative strength already

**Useful but weaker standalone**
- BTC Regime Filter (SMA200) — strong as a binary gate, less precise than correlation scaling
- Correlation timing (S08) — works better as sizing than as signal

**Weak / Negative**
- Mean reversion (three implementations failed)
- Volatility compression (marginal)
- Tail risk timing (noisy)

---

## Academic Replication (`04_Academic_Replication`)

### R01 — Bonenkamp (2021)
**Paper:** *High-Frequency Algorithmic Bitcoin Trading Using Both Financial and Social Features*  
University of Amsterdam, Bachelor Econometrics, 2021.

**Paper's approach:** Random Forest trained on 9 financial indicators (RSI, MACD, ATR, Stochastic, OBV, CCI, EMA, ROC, Williams %R) plus Twitter sentiment and Google Trends. Tested on 5-minute Binance data. Achieved Sharpe 2.02 with social features vs 1.92 without — difference not statistically significant against Buy & Hold.

**Our adaptation:** Social data unavailable on Quantiacs. We replicate the financial indicator feature set as a cross-sectional scoring model across Top-10 assets, converting the paper's price direction classification problem into a daily asset ranking problem.

**Key constraint difference:** Paper uses 5-minute single-asset BTC trading. Our implementation uses daily cross-sectional ranking across 10 assets — testing whether the feature engineering insight generalises to a different problem structure.

---

## Next Phase — Academic Paper Research

The multi-factor phase is complete. The strongest strategy (S12: Sharpe 1.715) has been identified.

The next phase focuses on reviewing academic literature to identify:

1. **Papers that study the same factors we found to work** — BTC relative strength, correlation regimes, and regime-aware strategies — to validate our findings against published research and understand whether our results are consistent with the literature.

2. **Papers that propose novel signals not yet tested** — identifying factors from academic research that are implementable with Quantiacs OHLCV data and could complement BTC Relative Strength with genuinely independent alpha.

3. **Papers on crypto-specific market microstructure** — altcoin rotation cycles, BTC dominance dynamics, and cross-asset momentum in crypto markets, which may formalise the mechanism behind S07's outperformance.

The criterion for selecting papers to replicate: *does the paper propose a signal that is orthogonal to BTC Relative Strength?* If it does, it may add value. If it correlates with relative strength, it will not.

---

## Design Principles

All strategies follow these rules — each motivated by a data exploration finding:

- **Hard liquidity mask** — `close_liq = xr.where(is_liquid == 1, close, np.nan)` before every calculation. Prevents illiquid dead coins from contaminating signals.
- **Inverse-volatility sizing** — Motivated by F8: 5σ events are 6,281× more frequent than normal distributions predict. Equal weighting is not risk-neutral.
- **BTC SMA200 hard exit** — Applied as a mask on final weights. `weights = weights * bull_mask`. Cannot be overridden by scoring logic.
- **Broadcast-safe operations** — `btc_scalar.expand_dims(asset=close.asset).transpose("time","asset")` before any (time,) × (time, asset) multiplication. Prevents silent zero-out.
- **Concentrated positions** — Top-3 to top-5 assets. With pairwise correlation 0.498 (rising to 0.619 in bear markets), holding all 10 provides limited diversification.

---

## Running a Strategy

All strategies are Jupyter notebooks designed to run on the Quantiacs platform.

```python
import qnt.data   as qndata
import qnt.output as qnout
import qnt.stats  as qnstats

data    = qndata.cryptodaily_load_data(min_date="2015-01-01")
weights = strategy(data)
weights = qnout.clean(weights, data, "crypto_daily_long")
qnout.write(weights)

# Slice to 2016-2025 — future dates always show zeros in tail()
stats = qnstats.calc_stat(data, weights.sel(time=slice("2016-01-01", None)))
print(stats.to_pandas().loc["2016-01-01":"2025-12-31"][
    ["equity", "sharpe_ratio", "max_drawdown", "mean_return"]
].tail(10))
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| `qnt` | Quantiacs data, backtesting, output |
| `xarray` | N-dimensional time-series operations |
| `numpy` | Numerical computations |
| `pandas` | Stats display, rolling correlations |
| `scipy.stats` | Skewness, kurtosis, IC calculations |
| Jupyter Notebook | All strategy and exploration files |

---

*Research conducted for the Quantiacs Crypto Top-10 Long-Only Contest.*  
*All strategies are research-grade backtests. Past performance does not guarantee future results.*
