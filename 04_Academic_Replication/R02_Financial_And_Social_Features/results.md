# Results

## Feature Correlation Analysis

The feature engineering stage produced 19 technical indicators.

Correlation analysis revealed that most indicators belong to a small number of feature families rather than representing independent sources of information.

### Trend Cluster

The following features exhibited extremely high correlations:

* ret_21d
* ret_63d
* RSI14
* MACD
* Price vs SMA50
* Price vs SMA200

These indicators are primarily measuring trend strength.

### Volume Cluster

Volume Ratio features demonstrated lower correlation with trend indicators and may provide independent information.

### Volatility Cluster

Volatility measures were highly correlated with each other and represent a separate risk factor.

---

## Feature IC Analysis

| Feature               |      IC |
| --------------------- | ------: |
| BTC Relative Strength |  0.0094 |
| Volume                |  0.0081 |
| Short-Term Return     |  0.0078 |
| Trend                 | -0.0134 |
| Bollinger Width       | -0.1080 |
| Volatility            | -0.1388 |

### Findings

* BTC Relative Strength produced the highest positive Information Coefficient.
* Volume provided a small positive contribution.
* Traditional trend indicators displayed weak predictive power.
* Volatility and Bollinger Width demonstrated strong negative relationships with future returns.
* Most technical indicators collapse into a single trend factor.

---

## Strategy Test

### Paper Feature Composite

The following factors were combined:

* BTC Relative Strength
* Volume Ratio
* Volatility
* Bollinger Width

Composite Score:

Score =
0.40 × BTC RS
+ 0.30 × Volume
− 0.15 × Volatility
− 0.15 × Bollinger Width

---

## Backtest Performance

| Metric               |   Value |
| -------------------- | ------: |
| Equity               | 5831.08 |
| Sharpe Ratio         |   1.477 |
| Max Drawdown         |  -0.853 |
| Average Turnover     |   0.329 |
| Average Holding Time |    3.81 |

---

## Benchmark Comparison

| Strategy                                    | Sharpe |
| ------------------------------------------- | -----: |
| S12 Correlation-Aware BTC Relative Strength |  1.715 |
| Paper Feature Composite                     |  1.477 |

---

## Conclusion

The paper-inspired feature framework failed to outperform the internally developed BTC Relative Strength framework.

While volume contributed positively, the addition of volatility and Bollinger-based features reduced overall performance.

The results suggest that BTC-relative strength remains a stronger source of alpha than traditional technical indicators within the Quantiacs crypto universe.

The replication is therefore considered complete.
