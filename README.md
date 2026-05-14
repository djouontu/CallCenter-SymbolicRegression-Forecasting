# Call Center Traffic Forecasting: Multiple Linear & Symbolic Regression

##  Business Objective
A time series is a series of data points ordered in time where the goal is typically to make a forecast for the future.This project aims to build a **Multiple Linear Regression (MLR)** model and a **Symbolic Regression** model to predict call volumes for the banking domain based on historical data and external traffic regressors.

##  Data Description
The project utilizes the "Call_centres" dataset, which contains monthly-level call data segregated by domain.
* **Rows & Columns:** ~130 rows and 8 columns.
* **Target Variable:** `banking`.
* **Independent Variables:** `no of phonelines` and `no of channels`.
* **Other Features:** Month, healthcare, telecom, technology, and insurance.

## Tech Stack
* **Language:** Python 
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `scipy`, `scikit-learn`, `gplearn` 

##  Solution Methodology
The approach follows a structured pipeline to ensure data normality and model accuracy:

1. **Data Pre-processing:** Setting the date as index and defining monthly frequency.
2.  **Exploratory Data Analysis (EDA):** Visualizing trends and checking for normality using **Density plots** and **Q-Q plots**.
3.  **Multiple Linear Regression:** * Split data into training and testing sets.
    * Train and fit the model to make predictions.
4.  **Residual Analysis:** Removing autocorrelation with varying lag values to refine the model
5.  **Symbolic Regression:** Implementing genetic programming to find the best mathematical functional relationships in the data.

##  Project Structure
The code is modularized for scalability and clarity:
```text
├── input/
│   └── CallCenterData.xlsx        # Raw dataset 
├── src/                           # Source code 
│   ├── Engine.py                  # Main execution script 
│   └── _ML_Pipeline/              # Core logic functions 
│       ├── MLR.py
│       ├── PreprocessPlots.py
│       └── SymbolicRegression.py
├── output/                        # Generated results 
│   ├── Visualization plots (.png)
│   └── symbolic_regression_model.pkl
└── lib/                           # Reference materials 
    └── MultipleLR.ipynb           # Original notebook for reference 
