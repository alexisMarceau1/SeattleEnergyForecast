# SeattleEnergyForecast

**Project Overview**

This project aims to predict the energy consumption (`SiteEnergyUse(kBtu)`) and CO₂ emissions (`TotalGHGEmissions`) of non-residential buildings in Seattle using data from 2015 and 2016. 
By forecasting these metrics, companies can identify opportunities to reduce **energy costs** and **enhance the sustainability** of their operations.

In alignment with Seattle's goal of achieving carbon neutrality by 2050, these predictions provide a means to optimize energy performance while minimizing data collection costs. Specifically, we investigate if omitting certain costly metrics like ENERGYSTARScore could still yield accurate predictions.

Objectives
Primary Goal: Predict energy consumption and CO₂ emissions to support energy management and sustainability efforts.
Secondary Goal: Assess the necessity of the ENERGYSTARScore in predictions, exploring if we can exclude it to reduce data collection costs without compromising model accuracy.
Data Sources
Main Dataset: Seattle Energy Benchmarking Data (2015-2016)
Dataset Description: Building Energy Benchmarking Details
Project Structure
This project is divided into two main notebooks:

Data Preparation and Exploration: Cleaning, feature engineering, and exploratory data analysis (EDA) of the dataset.
Modeling and Evaluation: Implementation and evaluation of various prediction models to find the best approach for our targets. We also compare model performance with and without ENERGYSTARScore.
Methodology
Data Cleaning and Feature Engineering: Addressed missing values, encoded categorical variables, and engineered additional features.
Model Selection: Evaluated several models, including:
Linear Regression
Lasso and Elastic Net (to explore regularization impacts)
Random Forest and XGBoost (for potential non-linear relationships)
Model Evaluation: Focused on metrics such as:
Mean Absolute Error (MAE): for prediction accuracy.
R² Score: to evaluate the variance explained by the model.
Feature Importance Analysis: Analyzed feature importance using Random Forest to understand which variables significantly impact predictions.
Results
Best Model: Random Forest provided a good balance between prediction accuracy and computational efficiency.
ENERGYSTARScore Assessment: Results suggest that excluding ENERGYSTARScore had a minimal impact on prediction accuracy, implying it could be safely omitted, thus reducing costs associated with data collection.
Potential Improvements
Advanced Feature Engineering: Further transformations and interactions among variables could potentially improve model accuracy.
Ensemble Methods: Combining models may yield more robust predictions.
Optimized Hyperparameter Tuning: Using techniques like Bayesian Optimization could streamline tuning for complex models such as XGBoost.
