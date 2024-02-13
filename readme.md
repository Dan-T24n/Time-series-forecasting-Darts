# Summary

Time series forecasting with sales data: 54 stores x 33 products families.

Testing *Apple M1 Metal GPU*:
 - Local models Exponential Smoothing : one per store-family series, 1782 models
 - Global models LightGBM: fit one model for each family (list of 54 series), 33 models

Lessons learned:
 - Exponential Smoothing is slow, but quite accurate
 - LightGBM is faster, allows high-dimension static covariates
 - LGBM easy to overfit, need careful cross-validation
 - No memory issue

Next step: build ensemble forecasts.

# Project structure

3 main folders: code, data, output.  Data and draft code folders are not tracked with git (too large).

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
└── Kaggle_template
```
