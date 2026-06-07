# Forest-Fires-Predictive-Analysis

# Forest Fires Predictive Analysis: Regression and Classification

## Project Overview
This repository contains a comprehensive data science pipeline aimed at predicting the severity of forest fires using meteorological and geographic data. The primary objective is to provide actionable, data-driven insights to forestry management and emergency response teams, enabling them to optimize resource allocation, issue timely alerts, and mitigate fire damage.

By exploring both continuous prediction (Regression) and categorical risk assessment (Classification), this project highlights the trade-offs between model complexity, predictive accuracy, and practical business interpretability.

## Dataset
The project utilizes the **Forest Fires Dataset** from the UCI Machine Learning Repository. It includes various environmental and geographic factors, such as:
* **Temperature** (temp)
* **Relative Humidity** (RH)
* **Wind Speed** (wind)
* **Precipitation** (rain)
* **Categorical Time Data** (month, day)

## Tech Stack
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries & Tools:** * `pandas` & `numpy` for data manipulation
  * `matplotlib` & `seaborn` for exploratory data analysis (EDA)
  * `statsmodels` for statistical inference and diagnostics
  * `scikit-learn` for machine learning (Ridge, Lasso, Logistic Regression)

## Project Workflow
1. **Exploratory Data Analysis (EDA):** Analyzed feature distributions, right-skewness in the target variable (burned area), and correlations between meteorological conditions and fire size.
2. **Multiple Linear Regression:** Built baseline and complex OLS models (incorporating log-transformations, quadratic terms, and interaction effects) to predict continuous burned area.
3. **Regularization (Ridge & Lasso):** Applied L1 and L2 penalties to handle multicollinearity and perform feature selection, identifying the most critical environmental drivers.
4. **Binary Classification:** Transformed the volatile continuous target into a binary risk classification (High-Risk vs. Low-Risk) and trained a Logistic Regression model.
5. **Model Diagnostics:** Evaluated assumptions using Q-Q plots, residuals analysis, Cook's Distance, and Variance Inflation Factors (VIF).

## Key Insights & Conclusion
* **The Volatility of Regression:** Predicting the *exact* acreage of a forest fire using Multiple Linear Regression is highly volatile due to the severe right-skewness of the data and the unpredictable nature of massive outlier fires.
* **The Power of Feature Selection:** Lasso regression effectively shrunk complex interaction terms to zero, confirming that core metrics like temperature, wind, and seasonality hold the most predictive weight.
* **Strategic Deployment:** The **Logistic Regression (Classification)** model proved to be the most stable and interpretable approach. Rather than predicting exact acreage, providing a probability score for a "High-Risk/Large Fire" allows response teams to set effective alerting thresholds and allocate firefighting resources efficiently before a crisis escalates.

## How to Run
1. Clone this repository to your local machine.
2. Ensure you have the required Python libraries installed (`pip install pandas numpy matplotlib seaborn scikit-learn statsmodels ucimlrepo`).
3. Run the `C06M08Lab.ipynb` notebook cell by cell to reproduce the analysis and model outputs.
