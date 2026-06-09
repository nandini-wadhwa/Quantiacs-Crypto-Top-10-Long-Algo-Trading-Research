# Findings

## Overview

The purpose of this analysis was to identify which market characteristics and quantitative factors exhibit predictive power within the Quantiacs Crypto Top10 universe.

Rather than building trading strategies immediately, the objective was to first understand how cryptocurrency markets behave and determine which signals are supported by empirical evidence.

The findings from this analysis directly motivated the strategy development process documented in later sections of this repository.

---

# Finding 1: Medium-Term Momentum Exists

## Research Question

Do assets that outperform over the previous month continue to outperform in the future?

## Evidence

A 21-day momentum factor was compared against future 21-day returns.

| Metric | Value |
|----------|---------:|
| Momentum Persistence Correlation | +0.0212 |

## Interpretation

The relationship is positive, indicating that assets which performed well over the previous month tended to continue outperforming over the following month.

Although the magnitude is modest, this level of predictive power is economically meaningful and consistent with momentum effects documented across many financial markets.

## Strategy Implication

This finding motivated the development of momentum-based strategies, including:

- Risk-Adjusted Momentum
- Drawdown Quality Momentum
- Regime-Aware Momentum

## Outcome

Momentum ultimately became the strongest source of alpha identified during the research process.

---

# Finding 2: Short-Term Mean Reversion Exists

## Research Question

Do recent losers outperform recent winners?

## Evidence

A 5-day return factor was compared against future 5-day returns.

| Metric | Value |
|----------|---------:|
| Mean Reversion Correlation | -0.0236 |

## Interpretation

The negative relationship indicates that short-term losers tended to outperform short-term winners over subsequent periods.

This confirms the presence of short-horizon reversal effects within the cryptocurrency market.

## Strategy Implication

This finding motivated the development of several mean-reversion strategies.

## Outcome

Despite the existence of a measurable reversal signal, the resulting strategies generated significantly lower Sharpe ratios than momentum-based approaches.

This suggests that while the signal exists statistically, it proved difficult to monetize after portfolio construction, turnover, and market noise were considered.

---

# Finding 3: Market Regimes Dominate Performance

## Research Question

Does the overall market environment matter more than individual asset selection?

## Evidence

Bitcoin was classified as bullish whenever it traded above its 200-day moving average.

Average returns within each regime were:

| Regime | Average Daily Return |
|----------|---------:|
| Bull Market | +0.503% |
| Bear Market | -0.199% |

Volatility remained elevated in both environments:

| Regime | Daily Volatility |
|----------|---------:|
| Bull Market | 6.42% |
| Bear Market | 5.36% |

## Interpretation

The cryptocurrency market exhibits a strong asymmetry between bullish and bearish environments.

Bull markets generate strongly positive expected returns, while bear markets produce negative expected returns.

The difference between the two environments is substantially larger than the predictive power of any individual factor.

## Strategy Implication

This finding motivated the introduction of a Bitcoin 200-day moving average regime filter.

Rather than remaining invested continuously, strategies were allowed to take risk only during favorable market conditions.

## Outcome

The regime filter improved the performance of the momentum strategy from approximately:

- Sharpe ≈ 1.29

to:

- Sharpe ≈ 1.52

This became the strongest strategy developed during the research process.

---

# Finding 4: Volume Contains Predictive Information

## Research Question

Do unusual increases in trading activity predict future returns?

## Evidence

A volume leadership factor was constructed using the ratio of current volume to its recent average.

| Metric | Value |
|----------|---------:|
| Volume Leadership Correlation | +0.0481 |

## Interpretation

Assets experiencing unusually high trading volume tended to generate stronger future returns.

This was the strongest predictive relationship identified among all tested factors.

Possible explanations include:

- Increased investor attention
- Information arrival
- Institutional participation
- Trend initiation

## Strategy Implication

This finding motivated the development of a Volume Flow Leadership strategy.

## Outcome

Volume-based signals demonstrated meaningful predictive power and represent a promising area for future research.

---

# Finding 5: Volatility Compression Predicts Future Expansion

## Research Question

Do periods of unusually low volatility precede large future moves?

## Evidence

A volatility compression factor was constructed using the ratio of short-term volatility to long-term volatility.

| Metric | Value |
|----------|---------:|
| Volatility Compression Correlation | +0.0242 |

## Interpretation

Periods of reduced volatility tended to be followed by larger future price movements.

This finding is consistent with the well-known volatility compression and expansion cycle observed across many financial markets.

## Strategy Implication

This finding motivated the development of a Volatility Compression strategy.

## Outcome

Although predictive power existed, the resulting strategy underperformed momentum-based approaches.

---

# Finding 6: Bitcoin Functions as the Dominant Market Factor

## Research Question

How independent are cryptocurrencies from one another?

## Evidence

The average pairwise correlation across the investable universe was:

| Metric | Value |
|----------|---------:|
| Average Pairwise Correlation | 0.498 |

Several major cryptocurrencies exhibited strong correlations with Bitcoin:

| Asset | Correlation with BTC |
|----------|---------:|
| XTZ | 0.847 |
| SUI | 0.817 |
| SOL | 0.729 |
| EOS | 0.715 |
| AVAX | 0.693 |

## Interpretation

A substantial portion of cryptocurrency return variation appears to be driven by market-wide factors rather than asset-specific effects.

Bitcoin acts as the primary market factor for the investable universe.

## Strategy Implication

This observation motivated the use of Bitcoin-based market regime indicators rather than relying solely on diversification across cryptocurrencies.

---

# Summary: Factor Efficacy Scorecard

| Factor | Evidence | Interpretation |
|----------|---------|---------|
| 21-Day Momentum | +0.0212 | Positive trend persistence |
| 5-Day Mean Reversion | -0.0236 | Short-term reversal |
| Volume Leadership | +0.0481 | Strongest predictive signal |
| Volatility Compression | +0.0242 | Compression precedes expansion |
| Market Regime | Bull: +0.503%, Bear: -0.199% | Most important structural effect |
| BTC Dominance | Avg Corr: 0.498 | Market-wide factor exposure |

---

# Key Takeaways

1. Momentum effects exist within the cryptocurrency market and can be monetized through cross-sectional portfolio construction.

2. Mean reversion effects exist statistically but proved difficult to convert into attractive trading strategies.

3. Trading volume appears to contain meaningful information about future returns and represents a promising area for future research.

4. Volatility compression exhibits predictive power and may provide useful signals for identifying upcoming price expansion.

5. Bitcoin acts as the dominant market factor, limiting the effectiveness of diversification alone.

6. The strongest finding of the study is the importance of market regime. Asset selection alone is insufficient when the broader market environment is unfavorable.

7. The highest-performing strategy developed during this research combined momentum signals with a Bitcoin-based regime filter, achieving a Sharpe ratio of approximately 1.52.

---

## Transition to Strategy Development

The findings documented above motivated the next phase of research: systematic strategy construction and testing.

The following sections investigate whether these empirical observations can be converted into robust, investable trading strategies.