# Exam-Mark-Prediction-using-LINEAR-REGRESSION-Multiple-Variable
ML Python Project

## Prediction

![](https://github.com/developer-venish/Exam-Mark-Prediction-using-LINEAR-REGRESSION-Multiple-Variable/blob/main/prediction.png)

---------------------------------------------------------------------------------------

Note :- All the code in this project has been tested and run successfully in Google Colab. I encourage you to try running it in Colab for the best experience and to ensure smooth execution. Happy coding!

---------------------------------------------------------------------------------------


This code performs linear regression on a dataset to predict the target variable based on the input features. Here's a breakdown of the code:

1. Import the necessary libraries:
   - `pandas`: for data manipulation and analysis.
   - `LinearRegression` from `sklearn.linear_model`: for creating and training a linear regression model.
   - `files` from `google.colab`: for uploading files in Google Colab.

2. Use the `files.upload()` function to upload a file named 'data.csv'.

3. Read the uploaded CSV file into a pandas DataFrame called `dataset`.

4. Print the shape of the dataset using `dataset.shape` to see the number of rows and columns.

5. Print the first 5 rows of the dataset using `dataset.head(5)` to inspect the data.

6. Check for columns with missing values using `dataset.columns[dataset.isna().any()]`. This will return the column(s) that contain NaN values.

7. Fill the missing values in the 'hours' column with the mean value of that column using `dataset.hours.fillna(dataset.hours.mean())`. This replaces the NaN values with the mean value.

8. Assign the input features (all columns except the last one) to the variable `X` using `dataset.iloc[:,:-1].values`. This selects all rows and all columns except the last one and converts them into a NumPy array.

9. Print the shape of `X` using `X.shape` to see the dimensions of the input feature array.

10. Assign the target variable (last column) to the variable `Y` using `dataset.iloc[:,-1].values`. This selects all rows and the last column and converts it into a NumPy array.

11. Create an instance of the `LinearRegression` model called `model`.

12. Fit the model to the training data using `model.fit(X, Y)`. This trains the linear regression model using the input features `X` and the target variable `Y`.

13. Create a new array `a` with a single sample to make a prediction. The values in `a` represent the input features for which we want to predict the target variable.

14. Use the trained model to make a prediction on the input features `a` using `model.predict(a)`. The predicted result is stored in the variable `PredictedmodelResult`.

15. Print the predicted result using `print(PredictedmodelResult)`.

---------------------------------------------------------------------------------------

Linear regression with multiple variables, also known as multiple linear regression, is a statistical technique used to predict a continuous dependent variable based on two or more independent variables. It extends the concept of simple linear regression, where there is only one independent variable.

In multiple linear regression, the relationship between the dependent variable and the independent variables is modeled as a linear equation of the form:

y = b0 + b1*x1 + b2*x2 + ... + bn*xn

where:
- y is the dependent variable (the variable we want to predict)
- b0 is the y-intercept or the constant term
- b1, b2, ..., bn are the coefficients or weights associated with each independent variable x1, x2, ..., xn
- x1, x2, ..., xn are the independent variables

The goal of multiple linear regression is to estimate the values of the coefficients (b0, b1, b2, ..., bn) that best fit the data and minimize the difference between the predicted values and the actual values of the dependent variable.

To perform multiple linear regression, the following steps are typically followed:
1. Collect and prepare the data: Gather the data for the dependent variable and the independent variables. Ensure the data is properly formatted and handle any missing values or outliers.

2. Split the data: Divide the dataset into a training set and a test set. The training set will be used to train the model, while the test set will be used to evaluate its performance.

3. Create and fit the model: Instantiate a linear regression model and fit it to the training data. The model will estimate the coefficients based on the training data.

4. Evaluate the model: Use the test set to assess the performance of the model. Calculate metrics such as mean squared error (MSE), root mean squared error (RMSE), or R-squared to measure how well the model fits the data.

5. Make predictions: Apply the trained model to new data to make predictions of the dependent variable based on the values of the independent variables.

Multiple linear regression allows for the analysis of relationships between multiple variables and the prediction of a dependent variable using multiple predictors. It is widely used in various fields, including economics, finance, social sciences, and data analysis, to uncover patterns and make predictions based on multiple factors.

---------------------------------------------------------------------------------------
