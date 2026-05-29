# Task:3 

_Task Objective:_
The primary objective of this notebook is to predict heart disease using various patient attributes. The problem is framed as a binary classification task, where the goal is to classify whether a patient has heart disease (1) or not (0).

_Dataset Used_
Name: **Heart Disease Data, downloaded from KaggleHub (redwankarimsony/heart-disease-data).**
**Original Columns:** The dataset initially contained 16 columns including id, age, sex, dataset, cp, trestbps, chol, fbs, restecg, thalch, exang, oldpeak, slope, ca, thal, and num.

**Preprocessing:**

1) id and dataset columns were dropped as they were not relevant.
2) The num column, which had values from 0 to 4, was transformed into a binary target variable (0 for no heart disease, 1 for heart disease).
3) Missing values in numerical columns (trestbps, chol, thalch, oldpeak, ca) were imputed with their respective medians.
4) Missing values in categorical columns (fbs, restecg, exang, slope, thal) were imputed with their respective modes.
5) Categorical features were one-hot encoded.

_Models Applied_

**Logistic Regression:** A Logistic Regression model was trained for the binary classification task.
1) The data was split into training (70%) and testing (30%) sets using train_test_split with random_state=42 and stratify=y.
2) The liblinear solver was used for the Logistic Regression model.

# **Key Results and Findings**

**Model Evaluation:**
_Accuracy:_0.8261
_ROC AUC Score:_ 0.8892
_Confusion Matrix:_
[[ 99  24]
 [ 24 129]]
 
This indicates that out of 276 test samples, the model correctly predicted 99 cases of no heart disease (True Negatives) and 129 cases of heart disease (True Positives). There were 24 False Positives and 24 False Negatives.
Feature Importance (Top 10 Logistic Regression Coefficients):

cp_atypical angina (Coefficient: -1.68)

cp_non-anginal (Coefficient: -1.13)

sex_Male (Coefficient: 1.06)

exang_True (Coefficient: 1.05)

ca (Coefficient: 0.80)

slope_flat (Coefficient: 0.71)

cp_typical angina (Coefficient: -0.63)

oldpeak (Coefficient: 0.50)

thal_normal (Coefficient: -0.42)

fbs_True (Coefficient: 0.40)

Features like cp_atypical angina, cp_non-anginal, sex_Male, exang_True, and ca appear to have a strong influence on the prediction.

**Future Improvement Strategies:** The notebook suggests exploring more sophisticated models, hyperparameter tuning, feature engineering, advanced imputation techniques, and addressing class imbalance to further improve model accuracy beyond 82.6%.
