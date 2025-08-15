Overview

This project uses machine learning to forecast battery capacity over time by analyzing historical performance data. The resulting predictive model offers valuable insights for Battery Management Systems (BMS) to optimize lifespan, safety, and performance.

Table of Contents

Purpose

Workflow

Methods Used

Analysis & Results

Conclusions & Recommendations

Purpose

The goal is to build a machine learning model that predicts battery capacity degradation, identifies key influencing factors, and supports smarter battery management and safety measures.

Workflow

Data Loading – Import dataset from Excel

Data Cleaning & Preprocessing – Handle missing values, select relevant features, and transform data

Exploratory Data Analysis (EDA) – Visualize patterns and relationships

Feature Engineering – Create new features to improve model accuracy

Modeling – Train and validate multiple ML models

Model Evaluation – Compare models using performance metrics

Conclusions – Summarize findings and improvement ideas

Methods Used

Data Loading & Exploration

Libraries: pandas, numpy, matplotlib, seaborn, plotly

Dataset: 1255 records with features like Time[h], U[V], I[A], Ah[Ah], Command

Data Cleaning

Selected key columns (Time[h], t-Step[h], U[V], I[A], Ah[Ah], Command)

Handled missing values via imputation/removal

EDA

Visualized feature distributions and correlations

Feature Engineering

Added new features to enhance model performance

Models Tested

Linear Regression

Random Forest

Gradient Boosting (Best performer)

Support Vector Regressor (SVR)

K-Nearest Neighbors (KNN)

Evaluation Metrics

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Analysis & Results

Key Findings

Capacity (Ah[Ah]) decreases steadily over time — consistent with expected battery aging

Strong correlations between voltage (U[V]), current (I[A]), and capacity

Best Model

Gradient Boosting achieved the lowest MAE (0.373) and MSE (0.299)

Optimized parameters: learning_rate=0.2, max_depth=4, n_estimators=200

Conclusions & Recommendations

Gradient Boosting is the most effective among tested models

Can be integrated into BMS for real-time battery health predictions

Future Work

Test deep learning models (e.g., RNNs) for temporal pattern capture

Deploy in a real-time monitoring system

Expand dataset with varying temperature and load conditions

Add external factors for better generalization
