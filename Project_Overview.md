# Project Overview

## Why This Project?

Volatility forecasting lies at the heart of quantitative finance. Accurate volatility estimates are essential for risk management, derivative pricing, portfolio allocation and systematic trading strategies. Despite decades of research, forecasting future volatility remains a challenging problem.

Over the last decade, rough volatility has emerged as one of the most influential developments in financial modelling. By incorporating fractional dynamics and rough paths into volatility processes, these models have demonstrated a remarkable ability to reproduce several stylized facts observed in financial markets.

This naturally raises an important practical question:

> **If rough volatility models describe market behaviour more realistically, do they also produce better volatility forecasts?**

This project was motivated by that question.

Rather than focusing exclusively on theoretical elegance, the objective was to evaluate whether the additional mathematical sophistication introduced by fractional and rough volatility models translates into measurable improvements in out-of-sample forecasting performance.

---

## From Fractional Dynamics to Rough Volatility

The project follows the evolution of volatility modelling from long-memory frameworks to modern rough volatility models.

The starting point is the Comte–Renault model, which extends classical stochastic volatility dynamics by introducing fractional Brownian motion and long-range dependence.

More recent empirical evidence suggests that volatility is not only persistent but also significantly rough at short time scales. This observation led to the development of the rough volatility paradigm, according to which volatility trajectories are substantially more irregular than previously assumed.

To investigate these ideas, the thesis studies three models:

* Comte–Renault
* Rough Fractional Stochastic Volatility (RFSV)
* Rough Bergomi

Their forecasting performance is then compared with the HAR-RV benchmark, one of the most widely used models in empirical volatility forecasting.

Together, these models provide a natural progression from fractional volatility frameworks to modern rough volatility modelling.

---

## Empirical Setting

The empirical analysis is based on daily realized volatility data from the Oxford-Man Realized Library.

Six major equity indices were considered:

* EURO STOXX 50
* FTSE 100
* S&P 500
* NASDAQ Composite
* Nikkei 225
* Hang Seng Index

The sample spans approximately two decades and covers multiple market conditions, including periods of low volatility, financial crises and market stress.

The study focuses on one-day-ahead volatility forecasting.

---

## Implementation

A major objective of the project was not only to study these models theoretically but also to implement them within a unified forecasting framework.

The empirical pipeline involved:

* Data preprocessing and volatility transformation
* HAR-RV benchmark construction
* Comte–Renault implementation
* RFSV implementation
* Rough Bergomi implementation
* Hurst exponent estimation
* Parameter calibration and model selection
* One-step-ahead forecasting
* Out-of-sample evaluation
* Statistical comparison through Diebold–Mariano tests

Particular attention was devoted to ensuring that all models were evaluated under the same forecasting framework, allowing a fair comparison of predictive performance.

---

## What the Data Revealed

One of the most interesting findings emerged before the forecasting exercise itself.

Across all six indices, the estimated Hurst exponents were consistently below 0.5.

This result provides empirical support for the rough volatility hypothesis and confirms that volatility behaves as a rough process across different financial markets.

In other words, the data strongly support one of the main empirical motivations behind rough volatility models.

However, identifying roughness is only part of the story.

The crucial question remains whether capturing roughness translates into superior forecasting performance.

---

## Key Findings

The empirical results revealed a clear and somewhat surprising pattern.

Although the data exhibit rough volatility behaviour and the rough models successfully capture important structural characteristics of volatility dynamics, they do not systematically outperform the benchmark.

The HAR-RV model achieved the best overall forecasting performance in five of the six indices considered.

The Hang Seng Index was the only market where the alternative models consistently showed an advantage over HAR-RV.

These results suggest that:

> **A model can provide a more realistic description of volatility without necessarily delivering more accurate forecasts.**

This is the central conclusion of the thesis.

---

## Lessons Learned

One of the most valuable lessons from this project is the distinction between explanation and prediction.

A model may be theoretically elegant, mathematically sophisticated and empirically realistic, yet still fail to generate superior forecasts.

The rough volatility framework has significantly improved our understanding of volatility dynamics, but forecasting performance ultimately remains an empirical question.

For this reason, theoretical advances should always be accompanied by rigorous out-of-sample evaluation.

---

## Future Research

The analysis was conducted using daily realized volatility data.

A natural extension of this work is the use of high-frequency intraday data, where roughness is expected to emerge more clearly and where rough volatility models may have greater potential to outperform traditional benchmarks.

Potential extensions include:

* Intraday volatility forecasting
* Dynamic parameter estimation
* Alternative calibration procedures
* Option-implied volatility information
* Continuous-time calibration methods

These directions may help determine whether the limited forecasting gains observed at the daily frequency are due to the models themselves or to the characteristics of the data used in the analysis.

---

## Key Takeaway

> **The existence of rough volatility in financial markets does not automatically imply that rough volatility models will outperform simpler alternatives in forecasting applications.**

Understanding volatility and forecasting volatility are closely related objectives, but they remain fundamentally different challenges.
