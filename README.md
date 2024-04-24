# DID-ML-Enhanced
# README
#Overleaf
https://www.overleaf.com/project/66292b6e0c9fdda94a7595af
## Description
This project extends the analysis performed in "The Effect of Minimum Wages on Low-Wage Jobs" by Cengiz, Dube, Lindner, and Zipperer, which estimates the impact of minimum wage increases on employment using a difference-in-differences approach. We enhance this original study by applying a machine learning approach using a causal forest model to derive treatment effect weights. These weights are then used to perform a weighted least squares (WLS) regression to obtain a refined estimation of the impact.

## Files and Data
- `combined_data_89-16.csv`: Contains state panel data for the years 1989-2016.
- `processed_VZ_mw_data.csv`: Contains processed data specifically focusing on minimum wage characteristics.

Both datasets were merged on `statenum` and `quarterdate` to align the observations for the analysis.

## Methods
The causal forest model was applied to estimate the heterogeneity of treatment effects across different states and time periods. This machine learning model provides an improved estimation of treatment effects by identifying the impact of minimum wage changes on various economic indicators.

The key variables used in the analysis are:
- `HSLcountall`, `teencountall`, `HSDcountall`, `gendercountall`, `Black_or_Hispanic`: Feature variables representing different demographic and economic factors.
- `T`: The treatment variable, which is the real minimum wage in this context.
- `avewage`: The outcome variable representing average wages.

The weights derived from the causal forest model signify the importance of each feature in predicting the treatment effect and were applied to the WLS regression.

## Analysis
1. A Causal Forest model was initialized and fitted using `GradientBoostingRegressor` for both outcome (`Y`) and treatment (`T`).
2. The treatment effects were estimated and visualized in a histogram to assess the distribution.
3. Confidence intervals for the treatment effects were obtained.
4. Feature importances from the Causal Forest were calculated and used to weight the WLS regression.
5. A weighted least squares regression was performed to estimate the impact of minimum wages on employment rates, using the feature importances as weights.

## Results
The results suggest that, when using a causal forest to determine feature importances as weights in a WLS regression, the overall number of low-wage jobs remains essentially unchanged over five years following the increase in the minimum wage. This complements the findings of the original study by providing a more nuanced analysis of the policy's impact across different segments of the labor market.

## How to Run
- Ensure `pandas`, `matplotlib`, `econml`, `sklearn`, and `statsmodels` libraries are installed in the Python environment.
- Load the datasets.
- Run the analysis script as detailed in the provided code snippets.

## Dependencies
- Python 3.8 or later
- Pandas library
- Matplotlib library
- EconML library
- Scikit-learn library
- Statsmodels library

## Authors
- Original Study: Doruk Cengiz, Arindrajit Dube, Attila Lindner, Ben Zipperer
- Enhancement Analysis: [Your Name]

## Acknowledgments
Special thanks to the authors of the original paper for their groundbreaking work on the impact of minimum wage policies, and to the organizations that provided the data used in this analysis.

