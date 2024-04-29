# DID-ML-Enhanced
# README
#Overleaf
https://www.overleaf.com/read/ngcjkdvtsnvj#98cd4e
## Description
This project extends the analysis performed in "The Effect of Minimum Wages on Low-Wage Jobs" by Cengiz, Dube, Lindner, and Zipperer, which estimates the impact of minimum wage increases on employment using a difference-in-differences approach. Using ML techniques like Double-Lasso, this study replicates and refines the reference paper, revealing nuanced impacts across wage tiers and demographics. It confirms nuanced job distribution changes post-minimum wage hikes, aiding policymakers in crafting more informed, equitable labor policies.

## Files and Data
- `Figure2_for_QJE`: Contains state panel data for the years 1979-2016.
Datasets are identified with "statenum" and "quarterdate" to align the analyzed observations.
-`StateMinimumWage_Changes.xlsx`: 

## Methods
The Double-Lasso model 

The key variables used in the analysis are:
-  `wagebinstate`, `weight'Y''b'`, `wtoverall1979`, `wmax`,`wmin`: Feature variables represent changes in minimum wages in each state.
- `treat_p.j`,`treat_m.j` `Ftreat_p.j`, `Ltreat_p.j``Ltreat_m.j`: The treatment variable whether the salary changes according to a certain time node in this paper.
- `overallcountpcall`: represents the percentage of the population corresponding to changes in the minimum wage.

The weights derived from the causal forest model signify the importance of each feature in predicting the treatment effect and were applied to the OLS regression.

## Analysis
1. 

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
- Enhancement Analysis: Oscar Lu, Feya Yang, Weizi He Lingfeng Shi, Qijin Liu, Nuha Alamri

## Links:
Colab of Replication:
Colab of Enhancement:
