# **Task:2**

**Task Objective**
The primary objective of this notebook is to predict stock closing prices using historical stock data.

**Dataset Used**
The notebook uses stock price data obtained from yfinance for the ticker 'AAPL' (Apple Inc.) from '2018-01-01' to '2023-01-01'. Additionally, there's an attempt to download a dataset from KaggleHub: suruchiarora/yahoo-finance-dataset-2018-2023, specifically an Excel file named yahoo_data.xlsx from this dataset.

**Models Applied**
Two regression models were applied for stock price prediction:

1) Linear Regression: A fundamental statistical model to establish a linear relationship between features and the target variable.
2) Random Forest Regressor: An ensemble learning method that constructs a multitude of decision trees during training and outputs the mean prediction of the individual trees.

**Key Results and Findings**

_Linear Regression:_ Achieved a Mean Squared Error (MSE) of 11.42 and an R-squared (R2) of 0.93 on the test set. This indicates a strong fit, with the model explaining a high percentage of the variance in the target variable.
_Random Forest Regressor:_ Achieved a Mean Squared Error (MSE) of 16.27 and an R-squared (R2) of 0.90 on the test set. While also performing well, it shows slightly higher error and a slightly lower R2 compared to the Linear Regression model in this specific case.

