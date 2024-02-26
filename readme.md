# Summary

Time series forecasting with sales data: 54 stores x 33 products families.

Toy notebook to test GPU with Darts:
- Apple M1 Metal: working, need to use specific Torch version
- Cuda: working, on Linux (Marco)


Testing:
 - Local models Exponential Smoothing : one per store-family series, 1782 models
 - Global models LightGBM: fit one model for each family (list of 54 series), 33 models


# Data

Kaggle Favorita sales forecasting competition. Retreived with Kaggle API.

Tracking ignored.

# Results

Lessons learned:
 - Exponential Smoothing as benchmark, no covariates
 - LightGBM is faster with GPU, allows high-dimension covariates: static, past and future
 - LGBM easy to overfit
 - No memory issue

Next steps: inspect models, tune parameters, ensemble forecast