📊 HR Salary Prediction using Linear Regression
Project Overview

This project applies Linear Regression, a supervised machine learning algorithm, to predict employee salaries based on key hiring factors such as:

Years of experience

Test score (out of 10)

Interview score (out of 10)

The dataset contains missing values and categorical data, so data cleaning and preprocessing were performed before training the model.

Tools and Libraries Used

Python

Pandas

NumPy

Matplotlib

Scikit-learn

Google Colab

CSV

Warnings were suppressed to keep the notebook output clean and readable.

Dataset Description

The dataset contains the following columns:

experience – years of experience recorded as words (e.g. "ten", "eleven")

test_score(out of 10) – candidate test score, with missing values

interview_score(out of 10) – interview performance score

salary – target variable to be predicted

Data Cleaning and Preprocessing
Handling Missing Values in Experience

The experience column was originally stored as text, which cannot be used directly by machine learning models.

To resolve this:

A numeric version of the experience column was created using map().

Each word-based experience value was matched to its numeric equivalent.

Missing values were imputed using the mean of the numeric experience column.

The column was rounded and converted to integers.

The original text-based experience column was removed.

What does map() do?

map() is used to replace values in a column based on a dictionary or mapping rule.

In this project, it was used to:

Match text values like "ten" and "eleven"

Convert them into numeric values like 10 and 11

This allowed the experience feature to be treated as a proper numeric variable for modeling.

Handling Missing Values in Test Scores

The test_score(out of 10) column contained missing values.

Steps taken:

The median test score was calculated.

Missing values were filled using the median to reduce the effect of outliers.

Feature Selection
Independent Variables (X)

Experience (numeric)

Test score (out of 10)

Interview score (out of 10)

Dependent Variable (y)

Salary

Model Training

A Linear Regression model was trained using Scikit-learn.

Steps:

Independent and dependent variables were defined.

The model was trained using the .fit() method.

Model coefficients, intercept, and score were evaluated.

The model score was relatively low (around 0.4), which is expected due to:

Very small dataset size

Limited number of features

Salary Predictions
Prediction 1

Inputs:

2 years of experience

Test score: 9

Interview score: 6

Predicted Salary:
₦47,056.9

Prediction 2

Inputs:

12 years of experience

Test score: 10

Interview score: 10

Predicted Salary:
₦88,227.6

Key Learnings

Machine learning models require numeric data

Text-based numeric values should be converted before modeling

Missing values must be handled before training

Linear Regression is sensitive to dataset size and feature quality

Conclusion

This project demonstrates a complete end-to-end machine learning workflow, including:

Data cleaning

Feature engineering

Handling missing values

Model training

Prediction and evaluation

It serves as a foundational example of applying linear regression to real-world HR data.
