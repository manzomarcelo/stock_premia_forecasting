# Forecasting stock premia

The proposal of this project is to scrutinize risk premia measurement through machine learning lenses, in order to leverage the ability of machine learning methods to capture nonlinear interaction of the characteristic factors. The goal of this project is to establish a sure way to build and select factors to price assets and forecast risk premia. The characteristics used were based on the paper "Deep Learning in Asset Pricing" by Chen, Pelger and Zhu (2019). Unfortunately, the data cannot be shared.

Methodology:

1- Returns were shifted in order to establish a lag-relationship with characteristics in order to avoid forward-looking bias.

2- For data splitting, I used a recursive performance evaluation scheme, by gradually includeing more recent observations in the training window. Thus, recursive scheme always retains the entire history in the training sample.

3 For performance evaluation, I used the ouf-of-sample R-squared, but without demeaning the sum of squared excess returns. The reason for this is that in by forecasting excess returns with historical averages, we'd be underperforming a naive forecast of zero by a considerable margin. In other words, the historical mean stock return is very noisy.

4- Monthly results were similar to the ones obtained in the paper "Empirical Asset Pricing via Machine Learning" by Gu, Kelly and Xui(2019)


For future implementations:

a) Expand design matrix by creating interactions between firm-characteristics and macroeconomic indicators

b)Repeat procedure at annual and monthly horizons

c)Construct value-weighted and equal-weighted portfolio based on forecasts
