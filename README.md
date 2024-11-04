# Seattle Building Energy and CO₂ Forecast

![Seattle Skyline](images/seattle.jpg) <!-- Image d'introduction -->

## 🏢**Project Overview**

This project aims to predict the **energy consumption** (`SiteEnergyUse(kBtu)`) and **CO₂ emissions** (`TotalGHGEmissions`) of non-residential buildings in Seattle using data from 2015 and 2016. 
By forecasting these metrics, companies can identify opportunities to reduce **energy costs** and **enhance the sustainability** of their operations.

In alignment with Seattle's goal of achieving carbon neutrality by 2050, these predictions provide a means to optimize energy performance while minimizing data collection costs.
Specifically, we investigate if omitting certain costly metrics like `ENERGYSTARScore` could still yield accurate predictions.

## 🎯**Objectives**

- **Primary Goal**: Predict energy consumption and CO₂ emissions to support energy management and sustainability efforts.
- **Secondary Goal**: Assess the necessity of the ENERGYSTARScore in predictions, exploring if we can exclude it to reduce data collection costs without compromising model accuracy.

## 📊**Data Sources**
- **Main Dataset**: [Seattle Energy Benchmarking Data (2015-2016)](https://www.seattle.gov/environment/climate-change/buildings-and-energy/energy-benchmarking/data-and-reports)
- **Dataset Description**: [Seattle Energy Benchmarking Data Description](https://data.seattle.gov/Built-Environment/2016-Building-Energy-Benchmarking/2bpz-gwpy/about_data)


## **Project Structure**
This project is divided into two main notebooks:

1. **Data Preparation and Exploration**: Cleaning, feature engineering, and exploratory data analysis (EDA) of the dataset.
2. **Modeling and Evaluation**: Implementation and evaluation of various prediction models to find the best approach for our targets. We also compare model performance with and without ENERGYSTARScore.

## 🔬 Methodology

### 1. Data Preparation
- 🧹 **Data Cleaning**: Managed missing values and prepared data for modeling.
- 🔧 **Feature Engineering**: Created new features and encoded categorical variables.

### 2. Model Selection
- Tested several models, including:
    - **Linear Regression**
    - **Lasso and Elastic Net** for regularization analysis
    - **Random Forest and XGBoost** for non-linear relationships

### 3. Evaluation Metrics
- **Mean Absolute Error (MAE)**: Primary metric for prediction accuracy.
- **R² Score**: Measures variance explained by the model.

### 4. Feature Importance Analysis
- Identified key features in the Random Forest model to highlight influential variables.

## ✅**Results**
- **Best Model**: Random Forest provided a good balance between prediction accuracy and computational efficiency.
- **ENERGYSTARScore Assessment**: Results suggest that excluding `ENERGYSTARScore` had a minimal impact on prediction accuracy, implying it could be safely omitted, thus reducing costs
  associated with data collection.

## 🚀**Potential Improvements**

- **Advanced Feature Engineering**: Further transformations and interactions among variables could potentially improve model accuracy.
- **Optimized Hyperparameter Tuning**: Using techniques like Bayesian Optimization could streamline tuning for complex models such as XGBoost.
