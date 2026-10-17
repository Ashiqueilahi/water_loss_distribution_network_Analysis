# Water Distribution Network Loss Analytics

A data analytics and machine learning project to analyze water distribution losses and estimate leakage across different zones of Chennai using Python, MySQL, Power BI, and Streamlit.

## Project Overview

This project analyzes water distribution network records to understand water loss patterns, explore factors associated with estimated leakage, and predict leakage using machine learning.

It combines data analysis, SQL queries, interactive Power BI dashboards, and a Streamlit application to support network monitoring and maintenance decisions.

## Objectives

- Analyze water distribution data across Chennai zones.
- Clean and preprocess data for analysis.
- Calculate water loss and loss percentage.
- Perform exploratory data analysis (EDA) using Python.
- Use SQL queries to analyze leakage and water loss patterns.
- Build and evaluate machine learning regression models.
- Develop an interactive Power BI dashboard.
- Provide leakage predictions and risk assessments through Streamlit.

## Technologies Used

- **Programming:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Database:** MySQL
- **Machine Learning:** Scikit-learn
- **Dashboard:** Power BI
- **Application:** Streamlit
- **Development Environment:** Jupyter Notebook, MySQL Workbench

## Dataset Description

The dataset contains 12,000 records representing water distribution network conditions in Chennai.

**Zones covered:**
- North Zone
- Central Zone
- South Zone
- West Zone

**Important features:**
- Pipe length, diameter, material, and age
- Water supply and water demand
- Flow rate and pressure
- Temperature and rainfall
- Maintenance events
- Estimated leakage
- Leakage incident indicator

**Target variable:** `Leakage_L_per_day`

## Project Workflow

1. Data collection and loading
2. Data cleaning and preprocessing
3. Feature engineering
4. Exploratory data analysis
5. SQL-based analysis using MySQL
6. Machine learning model development
7. Model evaluation and comparison
8. Interactive Power BI dashboard development
9. Streamlit application for leakage prediction and risk assessment

## Data Analysis

The analysis explores:

- Water loss across different zones
- Average leakage by zone
- Water loss percentage
- Pipe age and estimated leakage patterns
- Pressure and flow rate relationships
- Leakage patterns by pipe material
- Maintenance events and leakage
- Correlations between network parameters

## SQL Analysis

MySQL was used to perform structured queries, including:

- Counting total records
- Calculating average leakage by zone
- Comparing total water loss across zones
- Analyzing leakage by pipe material
- Studying leakage patterns by pipe age
- Counting leakage incidents by zone
- Filtering high-leakage records for further investigation

SQL query screenshots are available in the `sql_screenshots` folder.

## Machine Learning

Three regression models were developed and evaluated:

- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor

### Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 1,440.83 | 1,819.63 | 0.9839 |
| Random Forest | 1,750.83 | 2,198.58 | 0.9766 |
| Gradient Boosting | 2,297.16 | 2,846.72 | 0.9607 |

Linear Regression achieved the best results among the three models on the selected test split and was chosen as the final model.

*Note: These metrics reflect evaluation on the project dataset and do not establish equivalent performance on real-world water distribution networks.*

## Power BI Dashboard

The Power BI dashboard contains three pages:

### 1. Water Loss Overview
- Total water supply
- Total water demand
- Total water loss
- Average loss percentage
- Average leakage
- Leakage incidents
- Zone-wise comparisons

### 2. Network Analysis
- Pipe age versus leakage
- Pressure versus leakage
- Flow rate versus leakage
- Leakage by pipe material
- Leakage by maintenance events

### 3. Risk & Leakage Analysis
- Leakage incidents by zone
- Total water loss by zone
- Leakage incident distribution
- Average leakage by pipe age
- Average water loss percentage by zone
- Average maintenance events by zone

The dashboard uses MySQL as its data source.

## Streamlit Application

The Streamlit application allows users to enter network parameters and obtain:

- Predicted leakage
- Leakage risk category
- Calculated water loss
- Water loss percentage
- Suggested monitoring and maintenance actions

Recommendations are decision-support suggestions and should be verified through field inspections.

## Conclusion

This project demonstrates how Python, MySQL, Machine Learning, and Power BI can be used to analyze water distribution network data. It identifies water loss patterns across zones, compares leakage prediction models, and presents key insights through an interactive dashboard. The Streamlit application provides leakage predictions, risk assessment, and maintenance recommendations to support data-driven decision-making.
