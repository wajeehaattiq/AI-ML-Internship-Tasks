# AI-ML-Internship-Tasks
Here is all the task i have done in my 6 weeks internship
task:2 
Resources
Task Objective
The primary objective of this notebook is to predict stock closing prices using historical stock data.

Dataset Used
The notebook uses stock price data obtained from yfinance for the ticker 'AAPL' (Apple Inc.) from '2018-01-01' to '2023-01-01'. Additionally, there's an attempt to download a dataset from KaggleHub: suruchiarora/yahoo-finance-dataset-2018-2023, specifically an Excel file named yahoo_data.xlsx from this dataset.

Models Applied
Two regression models were applied for stock price prediction:

Linear Regression: A fundamental statistical model to establish a linear relationship between features and the target variable.
Random Forest Regressor: An ensemble learning method that constructs a multitude of decision trees during training and outputs the mean prediction of the individual trees.
Key Results and Findings
Linear Regression: Achieved a Mean Squared Error (MSE) of 11.42 and an R-squared (R2) of 0.93 on the test set. This indicates a strong fit, with the model explaining a high percentage of the variance in the target variable.
Random Forest Regressor: Achieved a Mean Squared Error (MSE) of 16.27 and an R-squared (R2) of 0.90 on the test set. While also performing well, it shows slightly higher error and a slightly lower R2 compared to the Linear Regression model in this specific case.



task:3 

ask Objective
The primary objective of this notebook is to predict heart disease using various patient attributes. The problem is framed as a binary classification task, where the goal is to classify whether a patient has heart disease (1) or not (0).

Dataset Used
Name: Heart Disease Data, downloaded from KaggleHub (redwankarimsony/heart-disease-data).
Original Columns: The dataset initially contained 16 columns including id, age, sex, dataset, cp, trestbps, chol, fbs, restecg, thalch, exang, oldpeak, slope, ca, thal, and num.
Preprocessing:
id and dataset columns were dropped as they were not relevant.
The num column, which had values from 0 to 4, was transformed into a binary target variable (0 for no heart disease, 1 for heart disease).
Missing values in numerical columns (trestbps, chol, thalch, oldpeak, ca) were imputed with their respective medians.
Missing values in categorical columns (fbs, restecg, exang, slope, thal) were imputed with their respective modes.
Categorical features were one-hot encoded.
Models Applied
Logistic Regression: A Logistic Regression model was trained for the binary classification task.
The data was split into training (70%) and testing (30%) sets using train_test_split with random_state=42 and stratify=y.
The liblinear solver was used for the Logistic Regression model.
Key Results and Findings
Model Evaluation:

Accuracy: 0.8261
ROC AUC Score: 0.8892
Confusion Matrix:
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

Future Improvement Strategies: The notebook suggests exploring more sophisticated models, hyperparameter tuning, feature engineering, advanced imputation techniques, and addressing class imbalance to further improve model accuracy beyond 82.6%.



task :1 

Task Objective: The primary objective of this notebook is to explore and visualize a simple dataset, specifically to understand its structure, distributions, and relationships between variables.

Dataset Used: The notebook uses the Iris dataset, which is loaded directly from seaborn.load_dataset('iris').

Models Applied: No machine learning models were applied in this notebook. The focus was purely on data exploration and visualization using libraries like pandas, seaborn, and matplotlib.

Key Results and Findings:

Dataset Overview: The Iris dataset contains 150 entries and 5 columns (sepal length, sepal width, petal length, petal width, and species). There are no missing values, and data types are appropriate.
Descriptive Statistics: Basic descriptive statistics (mean, std, min, max, quartiles) for the numerical features were displayed.
Feature Relationships (Scatter Plots): Scatter plots comparing 'Petal Length vs. Petal Width' and 'Sepal Length vs. Sepal Width', colored by species, visually demonstrate clear clusters for different Iris species, suggesting these features are strong discriminators.
Feature Distributions (Histograms): Histograms for each numerical feature ('sepal_length', 'sepal_width', 'petal_length', 'petal_width') show their individual distributions, indicating varying patterns (e.g., some features might have multimodal distributions due to distinct species).
Outlier Identification (Box Plots): Box plots for each numerical feature grouped by species were used to visualize the spread of data and identify potential outliers within each species category, also highlighting differences in feature ranges across species.





