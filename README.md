# Stock-Prediction-Using-Lstm

Overview
Minimal end-to-end demo: fetch historical data with TuShare, keep the target as the last column, and train a simple Keras LSTM to predict the next-day close price. A ready CSV (000002-from-1995-01-01.csv) is included so the notebooks can run without fetching again.

Files
000002-from-1995-01-01.csv — Historical OHLCV+amount with close as the last column for modeling.

data-preparation.ipynb — Shows fetching/formatting and the “target-last” convention for modeling.

fetch_data.py — Fetches 3-year and long-range history and reorders columns via wash().

stock-prediction.ipynb — Keras LSTM example using normalized sequences to predict close.

Setup
Python packages: pandas, numpy, scikit-learn, keras/tensorflow, jupyter, tushare.

Quick install: pip install pandas numpy scikit-learn keras tensorflow jupyter tushare.

Quickstart
Option A: Open stock-prediction.ipynb and run cells using the provided CSV for immediate results.

Option B: python fetch_data.py to generate fresh CSVs, then open data-preparation.ipynb and run stock-prediction.ipynb.

Notes
Keep the target “close” as the final column whenever adding features to stay compatible with the pipeline.

The notebooks are a simple baseline meant for learning; extend with more features, better splits, and stronger models as needed.

