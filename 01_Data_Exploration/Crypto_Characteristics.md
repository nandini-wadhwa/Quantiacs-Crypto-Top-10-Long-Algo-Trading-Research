# Crypto Market Characteristics

## Overview

This document summarizes the statistical characteristics of the Quantiacs Crypto Top10 universe. The objective is to understand the structure of the market before developing systematic trading strategies.

The analysis focuses on the investable universe defined by the Quantiacs `is_liquid` filter and covers the period from January 2015 through June 2026.

---

# 1. Dataset Overview

## Universe Construction

The Quantiacs Crypto Top10 dataset contains historical market data for 76 cryptocurrencies.

Available fields include:

* Open
* High
* Low
* Close
* Volume
* is_liquid

The `is_liquid` field defines whether an asset is investable on a given day and serves as the universe selection mechanism used by Quantiacs.

Although 76 assets appear throughout the sample period, only a subset is investable at any given time.

| Metric                | Value |
| --------------------- | ----: |
| Total Assets Observed |    76 |
| Average Liquid Assets |  9.80 |
| Minimum Liquid Assets |     7 |
| Maximum Liquid Assets |    10 |

The universe therefore behaves as a dynamic top-market-cap cryptocurrency universe.

---

## Asset Turnover

The investable universe changes over time as new cryptocurrencies enter the market and older assets lose relevance.

| Metric                 |         Value |
| ---------------------- | ------------: |
| Average Daily Turnover | 0.0453 Assets |

This corresponds to approximately 16–17 asset replacements per year.

Despite the rapid evolution of the cryptocurrency ecosystem, the investable universe remains relatively stable.

---

# 2. Return Distribution

## Return Statistics

To ensure that statistics reflect the actual investable universe, return calculations were restricted to assets satisfying the Quantiacs liquidity criterion.

| Metric             |   Value |
| ------------------ | ------: |
| Mean Daily Return  |  0.227% |
| Daily Volatility   |   6.04% |
| Skewness           |    3.07 |
| Kurtosis           |   67.79 |
| Largest Daily Gain |  183.5% |
| Largest Daily Loss | -100.0% |

---

## Observations

The cryptocurrency market exhibits substantially higher volatility than traditional asset classes.

Return distributions are strongly positively skewed, indicating that large upside moves occur more frequently than would be expected under a normal distribution.

The market also exhibits extreme excess kurtosis, demonstrating the presence of fat tails and frequent extreme events.

These findings suggest that risk management and position sizing are critical components of any systematic cryptocurrency strategy.

---

# 3. Volatility Characteristics

## Annualized Volatility

Volatility was computed using daily returns and annualized using the square-root-of-time rule.

| Metric                        |  Value |
| ----------------------------- | -----: |
| Average Annualized Volatility | 125.6% |

This level of volatility is substantially higher than that observed in traditional financial markets.

---

## Most Volatile Assets

| Asset | Annualized Volatility |
| ----- | --------------------: |
| STEEM |                306.3% |
| ZEC   |                274.8% |
| ICP   |                236.3% |
| IOTA  |                189.9% |
| XEM   |                180.0% |
| NEO   |                172.0% |
| PI    |                152.4% |
| UNI   |                134.7% |
| XMR   |                133.5% |
| THETA |                131.3% |

---

## Observations

Volatility varies substantially across assets.

Several legacy cryptocurrencies exhibit extreme volatility due to pronounced boom-bust cycles and changing market relevance over time.

The large dispersion in volatility across assets motivates the use of volatility-adjusted portfolio construction techniques.

---

# 4. Correlation Structure

## Average Correlation

The average pairwise correlation across the investable cryptocurrency universe was:

| Metric                       | Value |
| ---------------------------- | ----: |
| Average Pairwise Correlation | 0.498 |

This indicates a relatively high degree of co-movement among major cryptocurrencies.

---

## Bitcoin Dominance

Bitcoin exhibits strong positive correlations with most major cryptocurrencies.

| Asset | Correlation with BTC |
| ----- | -------------------: |
| XTZ   |                0.847 |
| SUI   |                0.817 |
| SOL   |                0.729 |
| EOS   |                0.715 |
| AVAX  |                0.693 |
| LINK  |                0.689 |
| UNI   |                0.688 |
| DOT   |                0.683 |

---

## Observations

The relatively high correlation structure implies that diversification alone may provide limited protection during periods of market stress.

Bitcoin functions as the dominant market factor within the cryptocurrency ecosystem.

---

# 5. Volume and Liquidity

## Average Trading Volume

Average daily trading volume was calculated across all periods in which an asset satisfied the Quantiacs liquidity criterion.

| Asset | Average Daily Volume (USD) |
| ----- | -------------------------: |
| BTC   |                     $22.9B |
| ETH   |                     $12.2B |
| SOL   |                      $3.1B |
| XRP   |                      $2.2B |
| BCH   |                      $1.9B |
| EOS   |                      $1.7B |
| ZEC   |                      $1.6B |
| LTC   |                      $1.5B |
| LINK  |                      $1.5B |
| BNB   |                      $1.5B |

| Metric                             |  Value |
| ---------------------------------- | -----: |
| Average Daily Volume Across Assets | $1.66B |

---

## Observations

Trading activity is heavily concentrated in Bitcoin and Ethereum.

Liquidity is unevenly distributed across the universe, suggesting that volume-based factors may contain useful information regarding market leadership and investor attention.

---

# 6. Market Regimes

## Bitcoin Trend Regimes

A bullish regime was defined as periods during which Bitcoin traded above its 200-day moving average.

| Metric                       | Value |
| ---------------------------- | ----: |
| Fraction of Bull Market Days | 59.7% |

---

## Observations

The cryptocurrency market spent approximately 60% of the sample period in bullish conditions.

This finding suggests that market-wide trend conditions may play a significant role in determining strategy performance.

The impact of market regimes will be investigated further in subsequent research.

# 7. Extreme Event Frequency

## Tail Risk Analysis

Cryptocurrency returns exhibit substantially heavier tails than predicted by a normal distribution.

The frequency of extreme return events was compared against the theoretical frequency expected under a Gaussian distribution.

| Threshold | Actual Frequency | Normal Distribution | Relative Frequency |
|------------|------------:|------------:|------------:|
| 2σ | 4.34% | 4.55% | 1× |
| 3σ | 1.50% | 0.27% | 6× |
| 4σ | 0.68% | 0.006% | 107× |
| 5σ | 0.36% | 0.0001% | 6,281× |

## Observations

The cryptocurrency market exhibits extreme tail risk.

Large price movements occur far more frequently than would be expected under standard statistical assumptions.

In particular, 5-standard-deviation events occur more than 6,000 times as often as predicted by a normal distribution.

These findings motivate the use of volatility-adjusted position sizing, diversification constraints, and regime-aware risk management.