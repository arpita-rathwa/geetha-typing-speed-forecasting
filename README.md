# Geetha's Typing Speed Forecasting 🎯

## Overview
A time series forecasting project built for AI Club Induction 2026 at NIT Calicut.
The goal is to predict Geetha's typing performance metrics for Day 999 using 999 days 
of historical MonkeyType practice data.

## Dataset
- 999 days of typing practice data
- 4 target metrics: WPM, Accuracy, Raw WPM, Consistency
- Source: AI Club Induction 2026, NIT Calicut

## Approach
1. Exploratory Data Analysis — visualized trends across all 4 metrics
2. Feature Engineering — created 61 features including:
   - Lag features (last 7 days)
   - Rolling averages (7-day and 30-day)
   - Trend features (recent improvement direction)
   - Exponentially Weighted Moving Averages (EWM)
   - Day number (captures overall upward trend)
3. Model Comparison:
   - Gradient Boosting
   - Random Forest
   - XGBoost
4. Final model trained on complete dataset for Day 999 prediction

## Results

| Model | WPM MAE | Acc MAE | RawWPM MAE | Consistency MAE |
|-------|---------|---------|------------|-----------------|
| Gradient Boosting | 12.23 | 3.92 | 9.97 | 10.24 |
| Random Forest | 11.02 | 3.80 | 9.28 | 9.41 |
| RF + Trend Features | **10.75** | **3.71** | **9.18** | 9.45 |
| XGBoost | 13.02 | 3.68 | 10.47 | 9.67 |

**Random Forest with Trend Features selected as final model.**

## Final Predictions for Day 999

| Metric | Predicted Value |
|--------|----------------|
| WPM | 99.62 |
| Accuracy | 95.14 |
| Raw WPM | 107.78 |
| Consistency | 70.93 |

## Key Findings
- WPM and Raw WPM show clear upward trend from ~80 in 2023 to ~110 in 2025
- Accuracy already near ceiling at 96% average — hard to predict precisely
- Consistency is the most volatile metric
- Recent days (lag features) are stronger predictors than older history

## Tech Stack
Python · Pandas · NumPy · Scikit-learn · XGBoost · Matplotlib · Seaborn

## Author
**Arpita Rathwa** — EEE Undergrad @ NIT Calicut
[LinkedIn](https://linkedin.com/in/arpita-rathwa-677b6837a) · 
[Kaggle](https://kaggle.com/arpitarathwa)
