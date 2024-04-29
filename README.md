# DID-ML-Enhanced
# README
#Overleaf
https://www.overleaf.com/project/66292b6e0c9fdda94a7595af
## Description
This project extends the analysis performed in "The Effect of Minimum Wages on Low-Wage Jobs" by Cengiz, Dube, Lindner, and Zipperer, which estimates the impact of minimum wage increases on employment using a difference-in-differences approach. We enhance this original study by applying a machine learning approach using a causal forest model to derive treatment effect weights. These weights are then used to perform a weighted least squares (WLS) regression to obtain a refined estimation of the impact.

## Files and Data
- `Figure2_for_QJE`: Contains state panel data for the years 1979-2016.
Datasets are identified with "statenum" and "quarterdate" to align the analyzed observations.

## Methods
The causal forest model was applied to estimate the heterogeneity of treatment effects across different states and time periods. This machine learning model provides an improved estimation of treatment effects by identifying the impact of minimum wage changes on various economic indicators.

The key variables used in the analysis are:
-  `wagebinstate`, `weight'Y''b'`, `wtoverall1979`, `wmax`,`wmin`: Feature variables represent changes in minimum wages in each state.
- `treat_p.j`,`treat_m.j` `Ftreat_p.j`, `Ltreat_p.j``Ltreat_m.j`: The treatment variable whether the salary changes according to a certain time node in this paper.
- `overallcountpcall`: represents the percentage of the population corresponding to changes in the minimum wage.

The weights derived from the causal forest model signify the importance of each feature in predicting the treatment effect and were applied to the OLS regression.



## Authors
- Original Study: Doruk Cengiz, Arindrajit Dube, Attila Lindner, Ben Zipperer
- Enhancement Analysis: Lu yu xin, Yang jin chen, Shi lingfeng, He wei zi, Liu qi jin

# Minimum Wage Change Analysis

## Overview
This repository conducts a comparative analysis of state-level minimum wage changes, utilizing a Lasso regression approach to identify states with patterns similar to Arkansas between 1990 and 1995.

## Dependencies
- Python 3
- Pandas: `pip install pandas`
- Scikit-learn: `pip install scikit-learn`

## Dataset
The dataset `/content/final_processed_with_ratio_in_mw.csv` should be placed in the root of the project directory.

## How to Run
1. Clone this repository.
2. Navigate to the cloned directory.
3. Execute the script with Python: `python analysis_script.py`

## Analysis Results
The analysis results output the state that most closely aligns with the minimum wage change pattern of Arkansas, determined by the highest score from the LassoCV regression.

## Acknowledgements
Special thanks to all contributors and data providers who made this analysis possible. The collaboration and data availability were crucial for the successful completion of this study.



