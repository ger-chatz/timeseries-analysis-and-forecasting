# Time Series Modeling and Forecasting of JTUAX Fund Returns (Publication Project)

## Overview

This project presents a full time series analysis and forecasting pipeline applied to the **US Mutual Fund JTUAX**. The entire process was conducted in **R** as part of a research-driven project intended for publication.

All statistical work was independently carried out by me, **Gerasimos Chatzopoulos**, as the lead analyst.

---

## Objectives

- Construct an appropriate time series from monthly return data
- Diagnose and resolve potential issues (stationarity, autocorrelation, heteroskedasticity)
- Fit and compare time series models (AR, GARCH, ARMA-GARCH)
- Evaluate multiple forecast methods including:
  - ARMA-GARCH models
  - GARCH Bootstrap
  - Neural networks (MLP)
- Assess predictive performance using metrics like **Mean Squared Forecast Error (MSFE)** and **Hit Ratio**

---

## Methodology

- **Stationarity Testing**: ADF tests and autocorrelation diagnostics (ACF, PACF, Box test)
- **Regression Modeling**: Initial multiple linear regression to explore explanatory variables
- **Residual Diagnostics**: Checked for autocorrelation and heteroskedasticity in residuals
- **Model Refinement**:
  - Used ARMA(1,0)-GARCH(1,1) with external regressors
  - Conducted backward elimination based on AIC/BIC to remove insignificant variables
- **Forecasting**:
  - ugarchforecast and ugarchboot (partial bootstrap)
  - MLP neural network forecasting via `nnfor` package

---

## Results

- The final chosen model: **ARMA(1,0)-GARCH(1,1)** with selected explanatory variables
- Residual diagnostics confirmed:
  - No autocorrelation
  - Homoscedastic residuals
  - Approximate normality
- Forecast evaluation:
  - **Hit Ratio**: 83.3% (percentage of correct sign predictions)
  - **MSFE**: 0.0133 (indicating good fit)

---

## Tools Used

- **R**: Time series modeling, forecasting, diagnostics
- **Packages**: `rugarch`, `tseries`, `urca`, `forecast`, `nnfor`
