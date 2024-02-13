# Intro

Time series forecasting with sales data: 54 stores x 33 products families.

Testing 2 main approaches:
 - Local models: one per store-family series, Exponential Smoothing, 1782 models
 - Global models: fit one model for all family group of series, LightGBM, 33 models

Next step: build ensemble forecasts.

# Project structure

3 main folders: code, data, output.  Data and draft code folders is not tracked with git (set by .gitignore).

- Data: raw data and processed data. Unzip Kaggle data into data/raw folder to start.

- Code: contain data processing and modelling.

- Output: output files, including tables and graphs. Ignored.

Folder structure:

```
.
├── code
│   ├── draft
│   └── test
├── data
│   ├── clean
│   └── raw
├── output
│   ├── graph
│   └── table
└── Kaggle_api_template
```
