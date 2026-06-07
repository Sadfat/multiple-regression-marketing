# Multiple Linear Regression — Multi-Channel Marketing Analysis

## Project Overview
This project analyses 572 marketing campaign records to model the combined effect of TV, Radio, Social Media, and Influencer spend on Sales using Multiple Linear Regression (OLS). Unlike simple regression, this model captures how all channels simultaneously influence Sales while controlling for each other.

## Tools Used
- Python | Pandas | NumPy | Seaborn | Matplotlib | Statsmodels | SciPy

## Dataset
| Column | Type | Description |
|---|---|---|
| TV | Categorical | Budget level: Low / Medium / High |
| Radio | Numeric | Radio ad spend ($000s) |
| Social Media | Numeric | Social media spend ($000s) |
| Influencer | Categorical | Type: Micro / Macro / Mega / Nano |
| Sales | Numeric | Target variable — Sales revenue ($000s) |

## Methodology
1. Load dataset and perform EDA
2. Encode categorical variables (TV, Influencer) using one-hot encoding
3. Check multicollinearity using Correlation Matrix and VIF
4. Fit Multiple OLS Regression model (all predictors)
5. Evaluate model using Adjusted R² and p-values
6. Validate assumptions: Linearity, Normality, Homoscedasticity
7. Interpret coefficients in business language
8. Deliver prioritised budget recommendation

## Key Results
| Metric | Value |
|---|---|
| Adjusted R² | 0.9030 |
| F-statistic p-value | < 0.001 |
| Multicollinearity | None severe (all VIF < 10) |

## Significant Predictors (p < 0.05)
- **TV Category** — High budget drives the largest Sales uplift
- **Radio Spend** — Each additional $1K → ~$2.97K increase in Sales

## Non-Significant Predictors (p > 0.05)
- Social Media — no significant independent effect
- Influencer type — no significant difference between types

## Business Recommendation
1. **Prioritise High TV budget** — greatest Sales impact
2. **Invest in Radio** — proven ROI at ~$2.97K Sales per $1K spend
3. **Review Social Media allocation** — reallocate to TV/Radio
4. **Influencer type** — choose by cost, not type

## Installation
```bash
pip install pandas seaborn matplotlib statsmodels scipy numpy
```

## Files
- `multiple_regression_analysis.ipynb` — Full executed notebook
- `marketing_data_multi.csv` — Dataset (572 records)
- `requirements.txt` — Python dependencies
