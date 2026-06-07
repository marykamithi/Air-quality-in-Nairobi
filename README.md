# Air Quality in Nairobi

This project explores Nairobi air quality data using MongoDB and Python-based time series modeling. The focus is on PM2.5 particulate matter measurements and forecasting using baseline regression, autoregressive models, and ARMA model tuning.

## Project Structure

- `031-data-wrangling-with-mongodb.ipynb`
  - Connects to MongoDB and loads Nairobi air quality measurement data.
  - Converts JSON documents into a clean pandas DataFrame.
  - Resamples data into hourly averages and prepares it for modeling.

- `032-linear-regression-with-time-series-data.ipynb`
  - Builds a regression dataset with lagged PM2.5 values.
  - Trains a linear regression model.
  - Evaluates performance with mean absolute error (MAE).

- `033-autoregressive-models.ipynb`
  - Uses time series methods and autoregression.
  - Generates ACF and PACF plots.
  - Performs walk-forward validation for better forecast realism.

- `034-arma-models-and-hyperparameter-tuning.ipynb`
  - Explores ARMA(p, q) modeling.
  - Runs grid search across ARMA parameter combinations.
  - Compares models using MAE and residual diagnostics.

## What this project does

- Reads air quality readings from a MongoDB database.
- Processes and resamples noisy sensor data to a regular hourly time series.
- Trains and evaluates both regression and time series forecasting models.
- Shows how to select and validate models for PM2.5 forecasting.

## Dependencies

- Python 3
- pandas
- pymongo
- scikit-learn
- statsmodels
- matplotlib
- plotly
- jupyter

## How to run

1. Install the required packages:

```bash
pip install pymongo pandas scikit-learn statsmodels matplotlib plotly jupyter
```

2. Make sure MongoDB is running and the `air-quality` database is accessible.
3. Open the notebooks in Jupyter or JupyterLab.
4. Run the notebooks in sequence from `031` through `034`.

## Notes

- The notebooks are designed to work with a MongoDB collection named `nairobi` inside the `air-quality` database.
- The analysis is a clean pipeline; any embedded videos or external branding have been removed.
- If the MongoDB host settings differ, update the `host` and `port` values in the first notebook.

## Summary

This repo provides a step-by-step progression from data ingestion to forecasting:
- `031` prepares the dataset.
- `032` builds a baseline regression model.
- `033` introduces autoregressive forecasting.
- `034` performs hyperparameter tuning for ARMA models.

The goal is to make the PM2.5 modeling workflow easy to follow and to show how time series methods can improve forecast quality.
