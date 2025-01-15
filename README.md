# Leads Classification Project

## Table of Contents
- [Project Overview](#project-overview)
- [Data Preparation and Preprocessing](#data-preparation-and-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Development](#model-development)
- [Model Evaluation](#model-evaluation)
- [Insights and Recommendations](#insights-and-recommendations)
- [Future Work](#future-work)

---

## Project Overview
This project focuses on  Leads classifications in a dataset exhibiting significant class imbalance. Two machine learning models, Support Vector Machine (SVM) and Random Forest (RF), were developed and evaluated for their performance. The goal was to assess the effectiveness of each model in handling the imbalanced dataset and providing actionable insights.

---

## Data Preparation and Preprocessing
### Data Understanding and Cleanup
- The dataset contained numerical, categorical, and datetime features.
- Missing values were imputed using:
  - **Mean Imputation** for numerical features.
  - **Mode Imputation** for categorical features.

### Feature Engineering
- **Categorical Features**: Encoded using one-hot and label encoding techniques.
- **Datetime Features**: Converted to Unix timestamp format to retain chronological significance.

### Handling Class Imbalance
- The target variable exhibited a class imbalance:
  - Class 0 (Majority): 9256 instances
  - Class 1 (Minority): 744 instances
- Synthetic Minority Oversampling Technique (SMOTE) was used to balance the classes.

---

## Exploratory Data Analysis (EDA)
- **Descriptive Statistics**: Summarized numerical and categorical features.
- **Correlation Analysis**: Identified highly correlated features to minimize multicollinearity.
- **Visualizations**:
  - Histograms, bar charts, and scatter plots were used to visualize the
distribution of the target variable, class distribution, and feature correlations.

---

## Model Development
### Model Selection
1. **Support Vector Machine (SVM)**:
   - Linear kernel.
   - `class_weight='balanced'` to handle class imbalance.
2. **Random Forest (RF)**:
   - Ensemble method aggregating multiple decision trees.

### Hyperparameter Tuning
- **Random Forest**: Tuned using `RandomizedSearchCV` for parameters like:
  - Number of estimators.
  - Maximum depth.
- **SVM**: Applied default settings with minor adjustments for imbalance.

---

## Model Evaluation

### SVM Results
SVM Classification Report

- **Accuracy**: 97.8%
- **Precision (Class 0)**: 98%
- **Recall (Class 0)**: 99%
- **F1-Score (Class 1)**: 85%
- **Macro Average**:
  - Precision: 94%
  - Recall: 90%
  - F1-Score: 92%

### Random Forest Results
Random Forest Classification Report

- **Accuracy**: 99.6%
- **Precision (Class 0)**: 100%
- **Recall (Class 0)**: 100%
- **F1-Score (Class 1)**: 97%
- **Macro Average**:
  - Precision: 99%
  - Recall: 99%
  - F1-Score: 99%

---

## Insights and Recommendations

### Class Imbalance Handling
- Random Forest demonstrated superior performance, particularly for the minority class.

### Recommendations
- Utilize Random Forest for operational deployment due to its high accuracy and robustness.
- Explore advanced ensemble methods like XGBoost or LightGBM for further enhancements.

---

## Future Work
- Incorporate additional data sources to balance the dataset and improve model generalization.
- Investigate advanced feature engineering techniques for interaction effects.
- Test alternative class imbalance methods, such as undersampling or advanced oversampling techniques.

---
[Summary Report PDF](https://drive.google.com/file/d/1Htx0p02_tMV1i5DLLIcGbkL8r7EUoivR/view?usp=sharing)
