# Anomaly Detection in Building Energy Consumption

This project focuses on detecting anomalies in building energy consumption data. By analyzing various features related to buildings, weather, and time, the goal is to identify unusual patterns in meter readings that could indicate potential issues or inefficiencies.

## Project Overview

The project involves:
1.  **Data Loading and Exploration**: Loading the dataset and performing initial checks for missing values and data types.
2.  **Exploratory Data Analysis (EDA)**: Visualizing key distributions and relationships within the data, such as meter reading distribution, trends over time, and correlations between features.
3.  **Feature Engineering**: Creating new features from existing ones and transforming categorical variables.
4.  **Data Preprocessing**: Handling missing values and scaling numerical features.
5.  **Model Building**: Training several classification models to predict anomalies, including:
    *   Random Forest Classifier (and a tuned version)
    *   XGBoost Classifier
    *   Decision Tree Classifier
    *   K-Nearest Neighbors Classifier
6.  **Model Evaluation**: Assessing the performance of each model using metrics like accuracy, precision, recall, F1-score, and ROC AUC, and visualizing the results with confusion matrices and ROC curves.
7.  **Model Comparison**: Comparing the performance of the different models to identify the most effective one for this task.
8.  **Prediction on Sample Data**: Testing the best-performing models on a small sample of test data to demonstrate their prediction capabilities.
