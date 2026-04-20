# 2026-Fifa-World-Cup-Predictor-
Author: Samuel E. Cardenas
Date: 2026

Project Overview
This project uses historical international soccer match data (1993–2022) to train a Random Forest Classifier that predicts the outcome of any match (Win / Draw / Lose from the home team's perspective). The trained model is then used to simulate the full 2026 FIFA World Cup tournament — group stage through the final — to predict the likely champion.

Dataset sources:

international_matches.csv — 23,921 international matches with FIFA rankings, scores, and team stats
Groupes_-_V3.csv — 2026 FIFA World Cup group stage draw (32 teams, 8 groups)
Method: Multi-class classification (Win / Draw / Lose) → tournament bracket simulation
