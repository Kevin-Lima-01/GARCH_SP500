# GARCH Model Comparison for S&P 500 Volatility Forecasting

This repository contains the final project and supporting codes developed as part of a **Time Series Econometrics** course. The study performs a comparative analysis of **GARCH-type models** to identify the best specification for forecasting **S&P 500** volatility. The evaluation relies on multiple performance metrics and formal statistical tests to assess predictive accuracy.

## Research Objective

The central goal is to determine which GARCH specification delivers the most accurate volatility forecasts for the S&P 500 index. Beyond pure predictive performance, the project engages with a broader academic debate: **the importance of modeling the error distribution** in financial and macroeconomic time series.

## Models Compared

Four GARCH specifications are estimated and compared:

| Model | Description |
|-------|-------------|
| **GARCH (standard)** | Baseline symmetric model with normal error distribution. |
| **t-GARCH** | GARCH model with Student's *t*-distributed errors to capture fat tails. |
| **EGARCH** | Exponential GARCH capturing asymmetric volatility responses (leverage effects). |
| **GJR-GARCH** | Glosten-Jagannathan-Runkle GARCH, also modeling asymmetry in volatility dynamics. |

## Evaluation Metrics

Model performance is assessed using a comprehensive set of criteria:

- 🔹 **Mean Absolute Error (MAE)**
- 🔹 **Mean Squared Error (MSE)**
- 🔹 **Root Mean Squared Error (RMSE)**
- 🔹 **Log-Likelihood**
- 🔹 **Diebold-Mariano Test** — formal pairwise comparison of predictive accuracy

## Key Findings

The comparison yielded the following insights:

- **t-GARCH** outperforms GJR-GARCH on MSE, RMSE, and log-likelihood criteria, suggesting better in-sample and out-of-sample fit.
- However, the **Diebold-Mariano test** indicates that the difference in predictive accuracy between t-GARCH and GJR-GARCH is **not statistically significant**.
- This result highlights a critical methodological point: **favorable point metrics do not guarantee a statistically superior model**.
- The analysis reinforces the academic argument that **modeling the error distribution matters**, as the t-GARCH specification — which accounts for heavy tails — consistently ranks among the top models.

> *We contribute to the academic debate by demonstrating that while distributional assumptions improve fit statistics, the empirical gains in predictive accuracy may not always be statistically distinguishable.*

## Data Source

- **S&P 500 Index:** Daily closing prices sourced from Yahoo Finance or FRED.

