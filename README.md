# From Fractional to Rough Volatility: Forecasting Performance of the Comte–Renault, RFSV and Rough Bergomi Models

**Master's Thesis – MSc Financial Risk and Data Analysis**  
**Sapienza University of Rome**

---

## Research Question

Over the last decade, rough volatility has emerged as one of the most influential developments in quantitative finance. By introducing fractional dynamics and rough paths into volatility modelling, these frameworks have demonstrated a remarkable ability to reproduce several empirical features of financial markets.

However, an important practical question remains:

> **Does greater model sophistication lead to more accurate volatility forecasts?**

This thesis investigates that question through a comparative study of three volatility models:

- Comte–Renault
- Rough Fractional Stochastic Volatility (RFSV)
- Rough Bergomi

Their forecasting performance is evaluated against the HAR-RV benchmark, one of the most widely used models in empirical volatility forecasting.

---

## Dataset

The analysis is based on daily realized volatility data from the Oxford-Man Realized Library and covers six major equity indices:

- EURO STOXX 50
- FTSE 100
- S&P 500
- NASDAQ Composite
- Nikkei 225
- Hang Seng Index

The sample spans approximately two decades of market data and includes multiple market regimes.

---

## Methodology

The empirical framework consists of:

1. Data preprocessing and volatility transformation.
2. Estimation and calibration of Comte–Renault, RFSV and Rough Bergomi models.
3. Hurst exponent estimation.
4. One-day-ahead volatility forecasting.
5. Out-of-sample evaluation.

Forecasts are assessed using:

- QLIKE Loss
- Mean Squared Error (MSE) on log-volatility

and statistically validated through Diebold–Mariano tests.

---

## Key Findings

The results challenge the common assumption that more sophisticated models necessarily deliver superior forecasting performance.

- HAR-RV achieved the best forecasting performance in **5 out of 6** equity indices.
- All estimated Hurst exponents were below **0.5**, confirming the rough nature of volatility.
- The Hang Seng Index was the only market where the alternative models consistently outperformed the benchmark.
- Rough volatility models captured important structural features of volatility dynamics but did not systematically improve forecasting accuracy at the daily frequency considered.

### Main Conclusion

> **Greater mathematical complexity does not automatically translate into better predictive accuracy.**

---

## Repository Contents

- `TESI_ELISA.pdf` — Full Master's thesis
- `PRESENTATION.pdf` — Thesis presentation
- `Project_Overview.md` — Detailed discussion of methodology, implementation and findings

Implementation notebooks and supporting material will be added progressively.

---

## Future Work

A natural extension of this research is the use of high-frequency intraday data, where roughness is expected to emerge more clearly and rough volatility models may become more competitive relative to traditional benchmarks.

---

## Author

**Elisa Battista**

MSc Financial Risk and Data Analysis  
Sapienza University of Rome

### Research Interests

- Quantitative Finance
- Volatility Modelling
- Rough Volatility
- Financial Econometrics
- Time Series Analysis
- Forecasting
