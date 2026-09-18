# Fama-and-French-Project
Analysis of Fama–French Model Assumptions and Regression Diagnostics: GARCH Modelling and Stock Clustering
# Fama–French Diagnostics, GARCH Modelling and Stock Clustering

This project combines factor-model analysis, volatility modelling and unsupervised learning to investigate the behaviour of selected stocks.

## Main objectives

- Analyze the assumptions of the Fama–French three-factor model.
- Perform regression diagnostics on the estimated models.
- Test for heteroskedasticity, autocorrelation and residual non-normality.
- Estimate GARCH models to capture time-varying volatility.
- Extract stock-specific GARCH parameters, including:
  - omega
  - alpha
  - beta
  - degrees of freedom of the Student-t distribution
- Standardize the estimated parameters.
- Apply K-Means clustering to identify stocks with similar volatility and risk profiles.
- Use PCA to visualize the resulting clusters in two dimensions.

## Methodology

The analysis starts by computing stock log-returns and merging them with the Fama–French market, size and value factors. For each stock, a factor regression is estimated and its residuals are analyzed through several diagnostic tests.

GARCH models are then fitted to the residual series using a Student-t innovation distribution. The estimated parameters are collected into a feature matrix and standardized before applying K-Means clustering.

## Results

The project produces:

- Estimated Fama–French factor exposures.
- Regression diagnostic statistics.
- GARCH volatility and residual estimates.
- A matrix of stock-specific GARCH parameters.
- Cluster assignments for each stock.
- Cluster-level average GARCH profiles.
- PCA plots for the visualization of the stock groups.

The resulting clusters represent stocks with similar estimated volatility dynamics and risk characteristics.
