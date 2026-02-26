# Inflation vs. Fertility Analysis

## Overview
This project investigates the relationship between inflation rates and fertility rates in the United States, exploring whether lagged inflation has a statistically significant impact on fertility decisions.

## Research Question
How does inflation (lagged 1-5 years) influence the fertility rate in the United States? Does the timing of inflation exposure matter for fertility outcomes?

## Data Sources
- **Fertility Rates**: CDC/NCHS Health, United States Data (Table Birth) - https://www.cdc.gov/nchs/hus/data-finder.htm
- **Inflation Rates**: Federal Reserve Economic Data (FRED) - https://fred.stlouisfed.org/series/FPCPITOTLZGUSA

The data was manually compiled and cleaned into a unified dataset covering multiple years, with inflation measured at the beginning of each year to represent the previous year's inflation.

## Methodology
The analysis uses Ordinary Least Squares (OLS) regression with the following key approaches:

1. **Standard Regression Model**: 
   - Regresses fertility rate on 1-year lagged inflation while controlling for year trends
   - Tests whether lagged inflation significantly predicts fertility rates

2. **Frisch-Waugh-Lovell (FWL) Decomposition**:
   - Partials out the year effect from both variables
   - Examines the pure relationship between inflation and fertility independent of secular trends
   - Runs a no-intercept regression of residuals for a clean partial correlation

3. **Lag Structure Analysis**:
   - Compares models with inflation lags of 1-5 years
   - Identifies which lag periods show the strongest relationship with fertility

## Key Findings
- R² shows the proportion of fertility variation explained by lagged inflation and year trends
- The coefficient on lagged inflation indicates the direction and magnitude of the effect
- Statistical significance is tested via t-statistics
- The FWL visualization clarifies the relationship after removing year trends

## Files
- `notebooks/Inflation_vs_Fertility.ipynb` - Main analysis notebook with code and visualizations
- `data/birth_inflation.csv` - Compiled dataset with fertility and inflation data
- `assets/HussarBold.otf` - Custom font used for professional visualization styling

## Usage
1. Install dependencies: `pandas`, `numpy`, `statsmodels`, `matplotlib`
2. Run the Jupyter notebook to reproduce the analysis and generate visualizations
3. The notebook automatically fetches the CSV from GitHub for reproducibility

## Author
Zan Merrill - MKT 382 (Marketing Analytics)  
October 2025  
*Generated with assistance from ChatGPT*
