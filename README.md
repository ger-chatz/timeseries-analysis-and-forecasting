# Time Series Modeling and Forecasting of JTUAX Fund Returns  
*MSc Applied Statistics Coursework Project*

## Overview

This project was completed as part of the MSc in Applied Statistics program and focuses on the time series modeling and forecasting of the **JTUAX US mutual fund returns** using R. The analysis includes model selection, diagnostic testing, and forecast evaluation using both classical and machine learning methods.

The work was conducted independently by **Gerasimos Chatzopoulos** as a full course project, integrating statistical theory and applied forecasting techniques.

---

## Objectives

- Build and evaluate time series models for monthly JTUAX fund returns
- Diagnose issues related to stationarity, autocorrelation, and heteroskedasticity
- Apply ARMA-GARCH and neural network models for forecasting
- Compare model performance using MSFE and hit ratios

---

## Methodology

- **Preliminary Analysis**: Stationarity testing via ADF; autocorrelation examined using ACF/PACF and Box tests
- **Model Fitting**:
  - Linear regression with external variables
  - Residual diagnostics and GARCH modeling
  - ARMA(1,0)-GARCH(1,1) chosen as final model
- **Forecasting Approaches**:
  - ARMA-GARCH forecasts with `ugarchforecast`
  - GARCH-based bootstrap using `ugarchboot`
  - Multilayer perceptron (MLP) neural networks with `nnfor`

---

## Results Summary

- Residual diagnostics confirmed a well-specified final model
- **Final model**: ARMA(1,0)-GARCH(1,1) with selected regressors
- **Forecast evaluation**:
  - Mean Squared Forecast Error (MSFE): 0.0133
  - Hit Ratio: 83.3% (correct sign predictions)

---

## Tools

- **R Programming Language**
- Key libraries: `rugarch`, `tseries`, `forecast`, `urca`, `nnfor`

---

## Author

**Gerasimos Chatzopoulos**  
MSc in Applied Statistics  
Athens University of Economics and Business  
All analysis and reporting were conducted independently as part of academic coursework.

---
