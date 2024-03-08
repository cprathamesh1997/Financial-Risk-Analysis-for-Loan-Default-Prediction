# Financial-Risk-Analysis-for-Loan-Default-Prediction
## The lending industry faces challenges in assessing creditworthiness, especially for applicants with limited credit history. Loan defaults pose financial risks to lending institutions.Our project aims to leverage Exploratory Data Analysis (EDA) and machine learning to predict loan default risk, assisting in minimizing financial losses.

![Cloud-CFO-Blog4-Machine Lea](https://github.com/cprathamesh1997/Financial-Risk-Analysis-for-Loan-Default-Prediction/assets/119093373/4a0f43fc-b323-4b05-9782-0e89be425355)

## 1. Introduction:
### The lending industry faces challenges in assessing creditworthiness, leading to financial risks due to loan defaults.
### Objective: Leverage EDA and machine learning to predict loan default risk, aiding in minimizing financial losses and optimizing lending decisions.

## 2. Data Import and Exploration:
### Imported necessary Python libraries for data manipulation and visualization.
### Imported two datasets: application_data and previous_application.

### Examined data dimensions:
    application_data: (307511, 122)
    previous_application: (1670214, 37)
## 3. Exploratory Data Analysis (EDA):
### Identified factors associated with default and non-default applicants.

## Notable insights:
    Less likely to default: Female applicants, higher income, academic degrees, etc.
    More likely to default: Male applicants, lower education level, lower income, etc.
## 4. Data Preprocessing:
## Addressed several issues during preprocessing:
### Missing values, skewed distributions, outliers, redundant features, and high dimensionality.

### Handling missing values:
    a.Removed features with >40% missing values.
    b.Employed missingness encoding for categorical features.
    c.Filled continuous features with median and discrete features with mode.
    d.Addressed skewed distributions and outliers using tree-based models.
    e.Encoded categorical features using LabelEncoder.
    f.Dropped redundant features and engineered new features from previous_application.
    g.Reduced dataset dimensionality using feature importance scores from a random forest classifier.

## 5. Model Training and Evaluation:
      a.Baseline model: Decision Tree classifier with max_depth = 3 and balanced class weights.
      b.Other models tested: Balanced Random Forest Classifier and XGB Classifier.
      c.Balanced Random Forest chosen to handle class imbalance.
      d.Hyperparameter tuning for Balanced Random Forest via randomized grid search.
      
## Evaluation metrics: class precision, recall, F1-score, ROC-AUC score, and test set confusion matrix.

## 6. Conclusion:

###   XGB Classifier emerged as the top performer, showing superior predictive accuracy and ability to distinguish between default and non-default cases.
###   Despite complexity and computational requirements, XGB Classifier offers the highest potential for accurate loan default prediction.
###   Decision Tree and Balanced Random Forest classifiers can still be viable options based on project requirements and computational resources.XGB Classifier outperforms both Decision Tree and Balanced Random Forest classifiers in accuracy and ROC-AUC scores.However,Decision Tree and Balanced Random Forest classifiers provide reasonably good results, especially considering their simplicity compared to XGB Classifier.

