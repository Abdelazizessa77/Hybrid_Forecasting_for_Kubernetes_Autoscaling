# Title: Hybrid Forecasting for Kubernetes Autoscaling (Prophet + LSTM)

Description:

This repository contains the full implementation of a two-phase hybrid forecasting framework developed to support predictive autoscaling in Kubernetes environments.

Phase 1 forecasts incoming request rates using a combination of Facebook Prophet (for trend and seasonality) and LSTM (for residual correction).

Phase 2 uses the predicted request rates to forecast CPU usage across multiple microservices using a multi-output LSTM model.

The code is structured to support:

Multi-window input evaluation

Short-horizon forecasting (1–15 minutes)

Accuracy tracking across metrics: MAE, RMSE, R², MAPE, and Accuracy (%)

Heatmap and line plot visualizations

Export to high-resolution figures for publication

Model saving, loading, and inference pipeline integration

Datasets used:

usask.sec.min_short.csv: Public web request trace data

Workload_metrics_V2.csv: Custom collected resource metrics from a Kubernetes-deployed microservices application on GCP
