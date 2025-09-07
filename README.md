## AIDS Virus Infection Prediction

### Project Overview

This project aims to predict the **presence of AIDS virus infection** based on a variety of patient-specific data. By analyzing features such as patient demographics (age), clinical measurements (weight), and various medical test results (e.g., `cd40`, `cd420`, `cd80`, `cd820`), the goal is to develop a machine learning model that can accurately classify a patient's infection status. This can be a vital tool for medical diagnosis and public health surveillance.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - AIDS Virus Infection Prediction](https://www.kaggle.com/datasets/aadarshvelu/aids-virus-infection-prediction)
  * **Size**: 50,000 entries, 23 columns.
  * **Key Features**:
      * **Demographics & Clinical**: `age`, `wtkg`, `gender`.
      * **Medical History**: `drugs`, `karnof` (Karnofsky score), `homo`, `hemo`.
      * **Lab Results**: `cd40`, `cd420`, `cd80`, `cd820`.
  * **Approach**:
      * **Data Cleaning**: The dataset was clean with no missing values or duplicates.
      * **Exploratory Data Analysis**: The code checks basic statistics, null values, duplicates, and unique values for all columns.
      * **Outlier Handling**: Outliers in numerical columns were handled by replacing them with the lower and upper bounds of the IQR.
      * **Data Standardization**: `StandardScaler` was applied to all feature columns to ensure they are on a similar scale.
      * **Binary Classification**: The target variable `infected` indicates whether a patient is infected (1) or not (0). The dataset is imbalanced (34494 non-infected vs 15506 infected), and this imbalance was handled implicitly by the choice of models.
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **70.6%** with Gradient Boosting and SVC.
      * **70.5%** with AdaBoost.
      * **70.4%** with Logistic Regression.
      * The moderate accuracies suggest that while the models have some predictive power, predicting AIDS infection from these features is a challenging task, and there is room for improvement.

-----

### Purpose and Applications

  * Assist medical professionals in the **preliminary screening for AIDS virus infection**.
  * Support public health initiatives by enabling a better understanding of risk factors and the spread of the virus.
  * Provide a tool for educational purposes in epidemiology and medical data analysis.
  * Serve as a foundational model for developing more comprehensive public health prediction systems.

-----

### Installation

Clone the repository and extract the data from the zip file.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for all models to ensure robustness.
  * Investigating the impact of different preprocessing techniques, especially for handling outliers and imbalanced data.
  * Exploring more advanced feature engineering, such as creating new features from the existing lab results.
  * Adding explainability (e.g., SHAP or LIME) to understand which medical parameters are the most critical for infection prediction.
