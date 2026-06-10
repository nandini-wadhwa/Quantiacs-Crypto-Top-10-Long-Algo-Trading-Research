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

# Finding 7: Diversification Fails During Bear Markets

## Research Question

Does diversification become less effective during market stress?

## Evidence

Average pairwise correlations were computed separately for bull and bear market regimes.

| Regime | Average Pairwise Correlation |
|----------|---------:|
| Bull Market | 0.469 |
| Bear Market | 0.619 |

## Interpretation

Cryptocurrency assets become substantially more correlated during bearish market environments.

The benefits of diversification decline precisely when downside protection is most needed.

This phenomenon is commonly observed across financial markets and reflects the increasing dominance of systematic risk during periods of stress.

## Strategy Implication

This finding provides additional justification for regime-based risk management.

Reducing market exposure during bearish conditions appears more effective than relying solely on diversification.

---

# Finding 8: Tail Risk Is Structural

## Research Question

How frequently do extreme market events occur?

## Evidence

Extreme return frequencies were compared with a normal distribution.

| Threshold | Actual Frequency | Normal Distribution |
|------------|------------:|------------:|
| 3σ | 1.50% | 0.27% |
| 4σ | 0.68% | 0.006% |
| 5σ | 0.36% | 0.0001% |

## Interpretation

Extreme price movements occur dramatically more often than predicted by traditional statistical models.

The cryptocurrency market exhibits persistent fat-tail behavior.

Large gains and losses are not rare anomalies but recurring features of the asset class.

## Strategy Implication

This finding motivated:

- Volatility-adjusted weighting
- Risk-adjusted momentum factors
- Regime-aware exposure control

rather than equal-weight portfolio construction.

---

# Summary: Factor Efficacy Scorecard

| Factor | Evidence | Interpretation |
|----------|---------|---------|
| 21-Day Momentum | +0.0212 | Positive trend persistence |
| 5-Day Mean Reversion | -0.0236 | Short-term reversal |
| Volume Leadership | +0.0481 | Strongest predictive signal identified |
| Volatility Compression | +0.0242 | Compression often precedes expansion |
| Market Regime | Bull: +0.503%, Bear: -0.199% | Most important structural effect |
| BTC Dominance | Avg Corr: 0.498 | Market-wide factor exposure |
| Diversification Breakdown | Bull Corr: 0.469, Bear Corr: 0.619 | Correlations rise during stress |
| Tail Risk | 5σ events occur 6,281× more often than normal | Extreme events are structural |

---

# Key Takeaways

### 1. Momentum Exists

Medium-term momentum exhibits positive predictive power within the cryptocurrency universe and represents a viable source of alpha.

### 2. Mean Reversion Exists but Is Difficult to Monetize

Short-term reversal effects are present statistically but generated weaker portfolio-level performance than momentum-based approaches.

### 3. Volume Is the Most Promising Factor

Among all factors tested, volume leadership demonstrated the strongest predictive relationship with future returns and represents a promising direction for future research.

### 4. Volatility Compression Contains Information

Periods of unusually low volatility tend to precede larger future price movements, supporting the development of breakout-oriented strategies.

### 5. Bitcoin Dominates Market Behaviour

Most cryptocurrencies remain heavily influenced by Bitcoin, limiting the effectiveness of diversification based solely on asset selection.

### 6. Diversification Weakens During Crises

Asset correlations increase substantially during bearish market environments, reducing diversification benefits precisely when downside protection is most needed.

### 7. Tail Risk Is a Defining Feature of Crypto Markets

Extreme return events occur far more frequently than predicted by normal distributions, motivating robust risk management and volatility-adjusted position sizing.

### 8. Market Regime Matters More Than Asset Selection

The strongest finding of the study is the dramatic difference between bullish and bearish market environments.

Bull markets generate strongly positive expected returns, while bear markets generate negative expected returns.

### 9. Regime-Aware Momentum Produced the Best Results

The highest-performing strategy developed during this research combined momentum signals with a Bitcoin-based regime filter, achieving a Sharpe ratio of approximately 1.52.

---

# Research Limitations

The factor diagnostics presented in this study were computed using the full available sample and should therefore be interpreted as exploratory in-sample analysis.

The objective of this phase was hypothesis generation and factor discovery rather than out-of-sample validation.

Future research will evaluate these factors using walk-forward testing, live performance monitoring, and alternative market environments.

---

## Transition to Strategy Development

The findings documented above motivated the next phase of research: systematic strategy construction and testing.

The following sections investigate whether these empirical observations can be converted into robust, investable trading strategies.