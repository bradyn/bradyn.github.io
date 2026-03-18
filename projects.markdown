---
layout: page
title: Projects
permalink: /projects/
---

---

## Macroeconomic Forecasting: Can Statistical Models Beat the Experts?

[GitHub](https://github.com/bradyn/forecast_comparison)

This project compares statistical forecasting methods against professional
forecaster benchmarks for three major macroeconomic series: real GDP
growth, CPI inflation, and unemployment. Methods include autoregressive
(AR) models, Elastic Net, Random Forest, Gradient Boosted Trees, and a
multilayer perceptron neural network. All methods are evaluated against
consensus forecasts from the Philadelphia Fed's Survey of Professional
Forecasters.

The analysis uses real-time vintage data from the Philadelphia Fed's
Real-Time Data Set for Macroeconomists, which ensures that no model has
access to data that would not have been available at the forecast date.

**Implementation:** Built in Python using pandas, scikit-learn, and
statsmodels, with a modular code structure (separate modules for data
loading, cleaning, modeling, and analysis). I wrote a custom
autoregressive model wrapper to handle vintage-aware
predictors and recursive multi-step forecasts, which off-the-shelf
implementations from statsmodels and scikit-learn cannot handle jointly.

**Key findings:**

- Simple AR models are competitive with more complex ML methods for GDP
  growth and inflation across all horizons.
- Performance on unemployment is more mixed. Tree-based methods substantially
  underperform at short horizons but outperform at the longest horizons.
- Professional forecasters generally outperform statistical methods,
  especially at short horizons.
- The forecasters' advantage is concentrated in recession periods.
  During expansions, simple statistical methods are competitive,
  particularly at longer horizons.

---
