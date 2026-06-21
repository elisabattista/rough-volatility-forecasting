# Project Overview

## Why This Project?

Volatility is one of the most important quantities in finance. It plays a central role in risk management, derivative pricing, portfolio allocation, and trading decisions. Despite decades of research, accurately forecasting volatility remains a challenging task.

In recent years, rough volatility models have become one of the most influential developments in quantitative finance. Their ability to reproduce several empirical features of financial markets has attracted significant attention from both academia and industry.

This naturally raises a practical question:

> **If rough volatility models describe financial markets more realistically, do they also produce better volatility forecasts?**

This thesis was motivated by that question.

Rather than focusing exclusively on theoretical properties, the project investigates whether the additional mathematical sophistication introduced by fractional and rough volatility models is justified by improved forecasting performance.

---

## From Long Memory to Rough Volatility

The project follows the evolution of volatility modelling from fractional dynamics to modern rough volatility frameworks.

The starting point is the observation that volatility exhibits persistence and dependence structures that cannot be fully explained by classical stochastic volatility models.

The first step in this direction is represented by the **Comte–Renault model**, which introduces fractional Brownian motion and long-memory effects into volatility dynamics.

More recent empirical evidence suggests that volatility is not only persistent but also highly irregular at short time scales. This observation led to the development of the **rough volatility paradigm**, where volatility paths are considerably rougher than previously assumed.

To investigate these ideas, the thesis studies:

- Comte–Renault
- Rough Fractional Stochastic Volatility (RFSV)
- Rough Bergomi

and compares their forecasting performance with the widely used **HAR-RV benchmark**.

Together, these models provide a natural progression from fractional volatility to modern rough volatility frameworks.

---

## Implementation

A major objective of the project was not only to study these models theoretically, but also to implement and compare them within a common forecasting framework.

The empirical analysis involved:

- Data preprocessing and volatility transformation
- HAR-RV implementation
- Comte–Renault implementation
- RFSV implementation
- Rough Bergomi implementation
- Hurst exponent estimation
- Model calibration and parameter selection
- Out-of-sample forecasting
- Rolling-window evaluation
- Statistical comparison through Diebold–Mariano tests

Particular attention was devoted to ensuring that all models were evaluated under the same forecasting setting, allowing for a fair comparison of their predictive performance.

---

## Dataset

The analysis is based on realized volatility data from the Oxford-Man Realized Library.

Six major equity indices were considered:

- EURO STOXX 50
- FTSE 100
- S&P 500
- NASDAQ Composite
- Nikkei 225
- Hang Seng Index

These markets provide a diverse set of volatility dynamics across different geographical regions and market environments.

The study focuses on one-day-ahead volatility forecasting using approximately two decades of observations.

---

## What the Data Revealed

One of the most interesting findings emerged before the forecasting exercise itself.

Across all six indices, the estimated Hurst exponents were consistently below 0.5, providing empirical evidence in favour of the rough volatility hypothesis.

In other words, the data strongly support the idea that volatility behaves as a rough process.

This result is important because it confirms one of the main empirical motivations behind rough volatility models.

However, identifying roughness is only part of the story.

The crucial question remains whether capturing roughness translates into better forecasts.

---

## Key Findings

The empirical results revealed a clear and somewhat surprising pattern.

Although the data exhibit rough volatility behaviour and the rough models successfully capture important structural features of volatility dynamics, they do not systematically outperform the benchmark.

The HAR-RV model achieved the best overall forecasting performance in five of the six indices considered.

The Hang Seng Index was the only market where the alternative models consistently showed an advantage over the benchmark.

The results therefore suggest that:

> **A model can provide a more realistic description of volatility without necessarily delivering more accurate forecasts.**

This is the central conclusion of the thesis.

---

## Lessons Learned

One of the most valuable lessons from this project is the distinction between explanation and prediction.

A model may be theoretically elegant, mathematically sophisticated, and empirically realistic, yet still fail to generate superior forecasts.

The rough volatility framework has significantly improved our understanding of volatility dynamics, but forecasting performance ultimately remains an empirical question.

For this reason, theoretical advances should always be accompanied by rigorous out-of-sample evaluation.

---

## Future Research

The analysis was conducted using daily realized volatility data.

A natural extension of this work is the use of high-frequency intraday data, where roughness is expected to emerge more clearly and where rough volatility models may have greater scope to outperform traditional benchmarks.

Future research could also investigate:

- Dynamic parameter estimation
- Alternative calibration procedures
- Intraday volatility forecasting
- Option-implied volatility information
- Continuous-time calibration methods

These extensions would help determine whether the limited forecasting gains observed at the daily frequency are due to the models themselves or to the characteristics of the data used in the analysis.

---

## Key Takeaway

> **The existence of rough volatility in financial markets does not automatically imply that rough volatility models will outperform simpler alternatives in forecasting applications.**

This thesis shows that understanding volatility and forecasting volatility are related, but fundamentally different challenges.
