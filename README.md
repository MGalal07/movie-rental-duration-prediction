# Movie Rental Duration Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-0.24%2B-orange)
![pandas](https://img.shields.io/badge/pandas-1.1%2B-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## Project Overview
This project aims to develop a predictive model to accurately forecast **movie rental durations** using transaction data. The goal is to achieve a **Mean Squared Error (MSE) of 3 or lower**, making the model a reliable tool for predicting rental durations based on various features.

## Table of Contents
- [Objectives](#objectives)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis and Feature Selection](#exploratory-data-analysis-and-feature-selection)
- [Modeling Process](#modeling-process)
- [Best Model and Results](#best-model-and-results)
- [Installation](#installation)
- [Usage](#usage)
- [Author](#author)

## Objectives
1. **Data Exploration and Preprocessing**: Clean and prepare the data for analysis.
2. **Model Experimentation**: Test various machine learning models to identify the best predictive approach.
3. **Model Optimization**: Fine-tune models to meet the target **MSE of 3** or below.

## Data Preprocessing
- **Rental Duration Calculation**: Created a `rental_length_days` feature representing the number of days each movie was rented.
- **Dummy Variable Generation**: Generated dummy variables from the `special_features` column for additional insights.
- **Feature Matrix and Target Definition**: Defined **X** (feature matrix) and **y** (target variable) to avoid any data leakage.

## Exploratory Data Analysis and Feature Selection
Analyzed feature correlations to reduce multicollinearity, setting an upper correlation threshold of **80%**. Removed one feature from each highly correlated pair to enhance model performance.

## Modeling Process
1. **Decision Tree Regressor**:
   - **Initial Model**: MSE of 9.998
   - **Tuned Model (GridSearchCV)**: Improved MSE but above target

2. **Random Forest Regressor**:
   - **Initial Model**: MSE of 6.084
   - **Tuned Model (GridSearchCV)**: MSE reduced to 5.315

3. **Gradient Boosting Regressor**:
   - **Initial Model**: MSE of 5.12
   - **Tuned Model (RandomizedSearchCV)**: Achieved a final MSE of **1.4998**

## Best Model and Results
The **Gradient Boosting Regressor with RandomizedSearchCV** proved to be the most effective model, achieving an MSE of **1.4998**, well below the target MSE of 3. This model provides accurate predictions for movie rental durations.

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Mgalal07/movie-rental-duration-prediction.git
