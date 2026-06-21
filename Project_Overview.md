# Project Overview

## Why This Project?

Volatility forecasting lies at the heart of quantitative finance. Accurate volatility estimates are essential for risk management, derivative pricing, portfolio allocation, and systematic trading strategies. Despite decades of research, forecasting future volatility remains a challenging problem.

Over the last decade, rough volatility has emerged as one of the most influential developments in financial modelling. By incorporating fractional dynamics and rough paths into volatility processes, these models have demonstrated a remarkable ability to reproduce several stylized facts observed in financial markets.

This naturally raises an important practical question:

> **If rough volatility models describe market behaviour more realistically, do they also produce better volatility forecasts?**

This project was motivated by that question.

Rather than focusing solely on theoretical elegance, the objective was to evaluate whether the additional mathematical sophistication introduced by fractional and rough volatility models translates into measurable improvements in out-of-sample forecasting performance.

---

## From Long Memory to Roughness

The project follows the evolution of volatility modelling from fractional dynamics to modern rough volatility frameworks.

The starting point is the observation that volatility exhibits persistence and dependence structures that cannot be fully captured by classical stochastic volatility models.

The **Comte–Renault model** represents an important step in this direction by introducing fractional Brownian motion and long-memory effects into volatility dynamics.

More recent empirical evidence suggests that volatility is not only persistent but also highly irregular at short time scales. This insight gave rise to the rough volatility paradigm, according to which volatility trajectories are considerably rougher than previously assumed.

To investigate this evolution, the thesis studies three models:

* Comte–Renault
* Rough Fractional Stochastic Volatility (RFSV)
* Rough Bergomi

and compares their forecasting performance against the widely used **HAR-RV benchmark**.

Together, these models provide a natural progression from long-memory volatility modelling to modern rough volatility frameworks.

---

## Data and Empirical Framework

The analysis is based on daily realized volatility data from the Oxford-Man Realized Library and covers six major equity indices:

* EURO STOXX 50
* FTSE 100
* S&P 500
* NASDAQ Composite
* Nikkei 225
* Hang Seng Index

The sample spans approximately two decades and includes a wide range of market environments, from periods of relative stability to episodes of extreme financial stress.

For each index, realized volatility series are used to estimate model parameters, generate one-day-ahead forecasts, and evaluate predictive performance.

The empirical framework is designed to ensure a fair comparison across all models through a common forecasting and evaluation procedure.

---

## Forecasting Framework

The analysis follows four main steps:

1. Construction of the HAR-RV benchmark.
2. Calibration of the Comte–Renault, RFSV, and Rough Bergomi models.
3. Estimation of the Hurst exponent to assess volatility roughness.
4. Generation and evaluation of one-day-ahead volatility forecasts.

Forecast accuracy is assessed using:

* QLIKE Loss
* Mean Squared Error (MSE) on log-volatility

Statistical significance is evaluated through Diebold–Mariano tests.

---

## Main Findings

The empirical results reveal a clear distinction between descriptive realism and forecasting performance.

All six equity indices exhibit rough volatility behaviour, with estimated Hurst exponents significantly below 0.5.

However, the superior ability of rough volatility models to describe volatility dynamics does not automatically translate into superior forecasting performance.

The HAR-RV benchmark achieved the best overall out-of-sample results in five of the six markets considered, while the Hang Seng Index was the only market in which the alternative models consistently outperformed the benchmark.

Overall, the findings suggest that increased model sophistication alone is not sufficient to guarantee better forecasts at the daily frequency.

---

## Future Directions

The results obtained in this study are specific to daily realized volatility forecasting.

A natural extension is the use of high-frequency intraday data, where volatility roughness is expected to be more pronounced. Future research will investigate whether rough volatility models become more competitive when forecasting volatility at finer time scales and under richer information sets.

* EURO STOXX 50
* FTSE 100
* S&P 500
* NASDAQ Composite
* Nikkei 225
* Hang Seng Index

The study focuses on one-day-ahead volatility forecasting using approximately two decades of observations.

To ensure a fair comparison, all models are evaluated within the same forecasting framework and assessed using identical training, validation, and test procedures.

Forecasting performance is measured through:

* QLIKE Loss
* Mean Squared Error (MSE) on log-volatility

and further evaluated through Diebold–Mariano tests.

---

## Implementation

A central component of this project was the complete implementation and comparison of all models within a unified empirical framework.

The work involved:

* Data preprocessing and volatility transformation
* HAR-RV implementation
* Comte–Renault implementation
* RFSV implementation
* Rough Bergomi implementation
* Hurst exponent estimation
* Model calibration and parameter selection
* Out-of-sample forecasting
* Rolling-window performance analysis
* Statistical comparison of competing forecasts

Particular attention was devoted to model calibration and out-of-sample evaluation, ensuring that forecasting results reflected genuine predictive performance rather than in-sample fit.

---

## What the Data Revealed

Before the forecasting exercise even began, an important result emerged from the data itself.

Across all six equity indices, the estimated Hurst exponents were consistently below 0.5, providing strong empirical evidence in favour of the rough volatility hypothesis.

In other words, the data support the idea that volatility behaves as a rough process.

This finding is important because it confirms one of the central empirical motivations behind rough volatility models.

However, identifying roughness is only part of the story.

The more challenging question is whether capturing roughness actually improves forecasting performance.

---

## Key Findings

The empirical results revealed a clear and somewhat unexpected pattern.

Although the alternative models successfully capture important structural features of volatility dynamics, they do not systematically outperform the benchmark.

The HAR-RV model achieved the best overall forecasting performance in five of the six equity indices considered.

The Hang Seng Index was the only market where the alternative models consistently showed an advantage over HAR-RV.

The results therefore suggest that:

> **A model can provide a more realistic description of volatility without necessarily producing more accurate forecasts.**

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

A natural extension of this work is the use of high-frequency intraday data, where roughness is expected to emerge more clearly and where rough volatility models may have greater potential to outperform traditional benchmarks.

Future research could also explore:

* Dynamic parameter estimation
* Alternative calibration procedures
* Intraday volatility forecasting
* Option-implied volatility information
* Continuous-time calibration methods

These extensions would help determine whether the limited forecasting gains observed at the daily frequency are due to the models themselves or to the frequency of the data used in the analysis.

---

## Key Takeaway

> **The existence of rough volatility in financial markets does not automatically imply that rough volatility models will outperform simpler alternatives in forecasting applications.**

The main lesson of this thesis is that understanding volatility and forecasting volatility are related, but fundamentally different challenges.

A richer description of market dynamics does not necessarily translate into superior predictive performance.
