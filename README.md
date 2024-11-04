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

### 1. Data Import
- **Objective**: Load the dataset from its source for analysis.
- **Tasks**: 
  - Import the 2015 and 2016 Seattle Energy Benchmarking dataset.
  - Verify data format compatibility with the tools used for processing.
  
### 2. Data Preparation
- **Objective**: Prepare the raw data for analysis.
- **Tasks**:
  - **Data Cleaning**: Handle missing values and correct inconsistencies to ensure data quality.
  - **Normalization and Encoding**: Normalize numerical variables and encode categorical variables to facilitate modeling.
  - **Target Variable Analysis**: Perform initial analysis on the target variables (`SiteEnergyUse(kBtu)` and `TotalGHGEmissions`) to understand their distribution and behavior.
  
### 3. Feature Engineering
- **Objective**: Enhance the dataset with meaningful features.
- **Tasks**:
  - **Feature Creation**: Generate new variables from existing ones to capture relevant information.
  - **Multivariate Analysis**: Explore relationships between multiple variables to detect potential interactions.
  - **Categorical Analysis**: Assess the impact of categorical variables on target variables.
  
### 4. Modeling
- **Objective**: Build predictive models to estimate energy use and emissions.
- **Tasks**:
  - **Model Selection**: Choose appropriate algorithms, such as Linear Regression, Lasso, Elastic Net, Random Forest, and XGBoost, to test for both linear and non-linear relationships.
  - **Training**: Train each model using the prepared dataset, applying cross-validation where necessary.
  
### 5. Model Evaluation
- **Objective**: Evaluate model performance to identify the best approach.
- **Tasks**:
  - **Error Metrics**: Calculate **Mean Absolute Error (MAE)** and **R² Score** on test data to gauge prediction accuracy.
  - **Comparative Analysis**: Compare performance across different models to determine the most accurate and computationally efficient solution.
  
### 6. Comparison with/without ENERGYSTARScore
- **Objective**: Determine the impact of omitting the `ENERGYSTARScore` feature on model performance.
- **Tasks**:
  - **Model Evaluation without ENERGYSTARScore**: Re-train and evaluate the best-performing models after removing `ENERGYSTARScore`.
  - **Cost-Benefit Analysis**: Assess if excluding `ENERGYSTARScore` significantly affects prediction accuracy, helping to reduce data collection costs if the impact is minimal.

## ✅**Results**
- **Best Model**: Random Forest provided a good balance between prediction accuracy and computational efficiency.
- **ENERGYSTARScore Assessment**: Results suggest that excluding `ENERGYSTARScore` had a minimal impact on prediction accuracy, implying it could be safely omitted, thus reducing costs
  associated with data collection.

## 🚀**Potential Improvements**

- **Advanced Feature Engineering**: Further transformations and interactions among variables could potentially improve model accuracy.
- **Optimized Hyperparameter Tuning**: Using techniques like Bayesian Optimization could streamline tuning for complex models such as XGBoost.
