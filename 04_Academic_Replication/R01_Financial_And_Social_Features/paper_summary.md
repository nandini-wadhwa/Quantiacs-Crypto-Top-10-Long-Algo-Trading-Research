# High-Frequency Algorithmic Bitcoin Trading Using Both Financial and Social Features

[link reference: https://www.researchgate.net/publication/329498105_A_High-Frequency_Algorithmic_Trading_Strategy_for_Cryptocurrency]

## Objective

This paper investigates whether combining traditional financial indicators with social-media-derived features can improve cryptocurrency trading performance.

The authors argue that cryptocurrency markets are heavily influenced by investor sentiment and online activity. Therefore, models that incorporate both market data and investor behaviour may outperform models based solely on technical indicators.

---

## Research Question

Can machine learning models trained on both financial and social features generate superior trading performance compared to models using only traditional market indicators?

---

## Financial Features

The paper uses several categories of financial indicators:

### Returns and Momentum

* Daily Returns
* Lagged Returns
* Momentum Measures

### Trend Indicators

* Moving Averages
* Price Relative to Moving Averages
* Trend Strength Measures

### Volatility Indicators

* Rolling Volatility
* Price Dispersion Measures

### Volume Indicators

* Trading Volume
* Relative Volume
* Volume Momentum

### Technical Indicators

* RSI
* MACD
* Bollinger Bands

---

## Social Features

The original paper incorporates social-media-derived variables such as:

* Positive Sentiment
* Negative Sentiment
* Social Activity
* Investor Attention
* Social Volume

These features are intended to capture investor behaviour not reflected in price data.

---

## Replication Scope

The Quantiacs crypto dataset does not provide social-media data.

Therefore, this replication focuses exclusively on financial features.

---

## Benchmark

The benchmark strategy for this replication is:

### S12 – Correlation-Aware BTC Relative Strength

Sharpe Ratio: 1.715

This represents the strongest internally developed strategy prior to paper replication.

---

## Success Criteria

The replication is considered successful if the paper-inspired feature framework can match or exceed the performance of S12.

Any model significantly below the benchmark suggests that traditional technical indicators are less informative than BTC-relative strength signals in the Quantiacs crypto universe.
