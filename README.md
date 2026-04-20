# 2026-Fifa-World-Cup-Predictor-
Author: Samuel E. Cardenas
Date: 2026

# Project Overview
This project uses historical international soccer match data (1993–2022) to train a Random Forest Classifier that predicts the outcome of any match (Win / Draw / Lose from the home team's perspective). The trained model is then used to simulate the full 2026 FIFA World Cup tournament — group stage through the final — to predict the likely champion.

# Requirements
Python 
Libraries: Pandas, Numpy, matplotlib, seaborn, sklearn

# Dataset sources

international_matches.csv — 23,921 international matches with FIFA rankings, scores, and team stats
Groupes_-_V3.csv — 2026 FIFA World Cup group stage draw (32 teams, 8 groups)

# Method
Multi-class classification (Win / Draw / Lose) → tournament bracket simulation

# Summary
This project built a complete machine learning pipeline to predict the 2026 FIFA World Cup winner:

# Data Wrangling 
We cleaned 23,921 historical international matches (1993–2022), removed leakage variables, high-missingness columns, and standardized team names.

# EDA 
We found that home advantage is significant (~5% higher win rate on home ground), and that FIFA ranking and FIFA points are strong predictors of match outcomes.

# Model 
A Random Forest Classifier was selected as the final model, outperforming both the majority-class baseline and Logistic Regression on the test set.

# Tournament Simulation 
We ran 1000 Monte Carlo simulations of the full 2026 World Cup bracket (group stage through final), giving each team a championship probability.

# Key Findings
FIFA rank difference and FIFA points difference are the most important features for predicting match outcomes.
The model favors historically strong, highly-ranked teams as tournament favorites.
Predicted champion probabilities reflect real-world expectations based on historical performance.
# Limitations
The dataset only goes up to June 2022, so very recent form and roster changes are not captured.
The model uses team-level statistics and does not account for individual player quality or injuries.
Draw prediction is inherently difficult in soccer and contributes to model error.
There is no handling of time based splitting thus leading to some data leakage.
The usage of all international matches rather than just World Cup mathces leads to misrepresentation of World Cup patterns.
The usage of each teams most recenet FIFA rank is from 2022, thus not properly representing for 2026.
