# Seattle building energy and CO₂ forecast

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

![Project Workflow](images/flow.png) <!-- Diagramme de flux -->

1. **Data Import**
   - Load necessary libraries, set configurations, load the data and inspect initial characteristics.

3. **Data Preparation and Exploration**
   - **Data Cleaning**: Handle missing values, inconsistencies, and outliers in the dataset.
   - **Exploratory Data Analysis (EDA)**:
      - **Categorical Variables**: Analyze categorical data and correct typos where necessary.
      - **Numerical Variables**: Understand distributions of continuous variables.
      - **Correlations**: Examine relationships between features and with target variables.
      - **Target Variables Analysis**: Explore characteristics of `TotalGHGEmissions` and `SiteEnergyUse(kBtu)`.

4. **Feature Engineering**
   - Create new variables, encode categories, and normalize data to enhance model performance.

5. **Modeling and Predictions**
   - **Model Evaluation**: Test various models, including:
      - **Linear Regression**: A basic linear model.
      - **Lasso and Elastic Net**: Adds regularization to improve generalization.
      - **Random Forest and XGBoost**: Captures non-linear relationships.

   - **Selection of Best Models**: Identify models with optimal performance based on evaluation metrics.

   - **Making Predictions**:
      - **CO₂ Emissions Prediction**: Analyze predictions for `TotalGHGEmissions`.
      - **Energy Consumption Prediction**: Evaluate predictions for `SiteEnergyUse(kBtu)`.



6. **ENERGYSTARScore Evaluation**
   - **Comparison with/without ENERGYSTARScore**: Analyze the impact of excluding the `ENERGYSTARScore` variable on model accuracy to determine if it can be safely omitted, reducing data collection costs.

## ✅**Results**
- **Best Model**: Random Forest provided a good balance between prediction accuracy and computational efficiency.
- **ENERGYSTARScore Assessment**: Results suggest that excluding `ENERGYSTARScore` had a minimal impact on prediction accuracy, implying it could be safely omitted, thus reducing costs
  associated with data collection.

## 🚀**Potential Improvements**

- **Advanced Feature Engineering**: Further transformations and interactions among variables could potentially improve model accuracy.
- **Optimized Hyperparameter Tuning**: Using techniques like Bayesian Optimization could streamline tuning for complex models such as XGBoost.
