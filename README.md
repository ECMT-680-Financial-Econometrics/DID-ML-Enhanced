# DID-ML-Enhanced
# README
#Overleaf
https://www.overleaf.com/read/ngcjkdvtsnvj#98cd4e
## Description
This project extends the analysis performed in "The Effect of Minimum Wages on Low-Wage Jobs" by Cengiz, Dube, Lindner, and Zipperer, which estimates the impact of minimum wage increases on employment using a difference-in-differences approach. Using ML techniques like Double-Lasso, this study replicates and refines the reference paper, revealing nuanced impacts across wage tiers and demographics. It confirms nuanced job distribution changes post-minimum wage hikes, aiding policymakers in crafting more informed, equitable labor policies.

## Files and Data
- `Figure2_for_QJE`: Contains state panel data for the years 1979-2016.
Datasets are identified with "statenum" and "quarterdate" to align the analyzed observations. (Download from: https://github.com/mjahangiralam/Data-Science-for-Economic-and-Social-Issues/tree/main/DiD/Cengiz-et-al)

- `StateMinimumWage_Changes.xlsx`: Contains the historical data on changes to the minimum wage across various states in the United States and employment rate. 

## Methods
The Double-Lasso model 

The key variables used in the analysis are:
-  `wagebinstate`, `weight'Y''b'`, `wtoverall1979`, `wmax`,`wmin`: Feature variables represent changes in minimum wages in each state.
- `treat_p.j`,`treat_m.j` `Ftreat_p.j`, `Ltreat_p.j``Ltreat_m.j`: The treatment variable whether the salary changes according to a certain time node in this paper.
- `overallcountpcall`: represents the percentage of the population corresponding to changes in the minimum wage.


## Analysis
- Double-Lasso enhances precision by selecting New York and Arkansas based on parallel trends.
- Plotting shows nuanced effects of minimum wage changes on different wage tiers.
- Model discerns subtle impacts, improving understanding of minimum wage effects.

## Results
- Replication process consolidates control variables into a single dataframe for regression analysis.
- Placebo test applied to regression output in DiD methodology reveals new coefficients.
- ML-enhanced Double-Lasso selects New York (treatment) and Arkansas (control) for analysis.

## How to Run
- Ensure `pandas`,`linearmodels.panel`, `matplotlib` libraries are installed in the Python environment.
- Load the datasets.
- Run the analysis script as detailed in the provided code snippets.

## Dependencies
- Python 3.8 or later
- Pandas library
- Linearmodels.panel library
- Matplotlib library

## Authors
- Original Study: Doruk Cengiz, Arindrajit Dube, Attila Lindner, Ben Zipperer
- Enhancement Analysis: Oscar Lu, Feya Yang, Weizi He, Lingfeng Shi, Qijin Liu, Nuha Alamri

## Links:
Colab of Replication:
Colab of Enhancement:
