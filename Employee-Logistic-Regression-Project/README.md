# Employee Retention Analysis Using Logistic Regression

## Project Overview
Employee retention is a critical challenge for organizations, as high employee turnover leads to increased recruitment costs, loss of expertise, and reduced productivity. This project applies **Exploratory Data Analysis (EDA)** and **Logistic Regression** to analyze an employee dataset and identify key factors that influence whether employees stay with or leave a company.

The objective is to:
- Explore employee characteristics and work conditions
- Identify variables with direct impact on employee retention
- Visualize relationships between salary, department, and retention
- Build a logistic regression model to predict employee attrition
- Evaluate the performance of the model using standard metrics

---

## Dataset Description
The dataset contains **14,999 employee records** with **10 variables**, each representing employee attributes and work-related factors.

### Dataset Shape
- Rows: 14,999  
- Columns: 10  

### Columns Description
| Column Name | Description | Data Type |
|------------|-------------|-----------|
| satisfaction_level | Employee satisfaction score (0–1) | Float |
| last_evaluation | Last performance evaluation score (0–1) | Float |
| number_project | Number of projects handled | Integer |
| average_montly_hours | Average monthly working hours | Integer |
| time_spend_company | Number of years spent in the company | Integer |
| work_accident | Whether the employee had a work accident (0 = No, 1 = Yes) | Integer |
| left | Whether the employee left the company (0 = Stayed, 1 = Left) | Integer |
| promotion_last_5years | Promotion in the last 5 years (0 = No, 1 = Yes) | Integer |
| department | Employee department | Categorical |
| salary | Salary level (low, medium, high) | Categorical |

---

## Target Variable
- **left**
  - `0` → Employee stayed with the company
  - `1` → Employee left the company

This makes the problem a **binary classification task**, suitable for logistic regression.

---

## Data Quality Checks
The following data validation steps were performed:
- Checked dataset shape and structure
- Verified data types of all variables
- Checked for missing values (none found)
- Identified duplicate rows (duplicates retained as they represent valid repeated employee profiles)
- Verified class distribution of the target variable

---

## Exploratory Data Analysis (EDA)

### 1. Target Variable Distribution
- Employees who stayed: 11,428  
- Employees who left: 3,571  

The dataset is moderately imbalanced, with more employees staying than leaving.

---

### 2. Salary vs Employee Retention
A stacked bar chart was used to visualize the relationship between salary level and employee retention.

**Key Insight:**
- Employees with **low salary** show the highest attrition rate
- Employees with **high salary** have the strongest retention
- Salary level has a clear and direct impact on employee retention

---

### 3. Department vs Employee Retention
Retention rates were analyzed across departments using proportion-based bar charts.

**Key Insight:**
- Departments such as Sales and Technical show relatively higher attrition
- Departments like Management and R&D show stronger retention
- Department influences attrition, but less strongly than salary or satisfaction level

---

### 4. Satisfaction Level Analysis
Satisfaction level was compared between employees who stayed and those who left.

**Key Insight:**
- Employees with low satisfaction levels are significantly more likely to leave
- Satisfaction level is one of the strongest predictors of retention

---

## Feature Selection
Based on EDA findings, the following variables were selected for model building:

### Selected Features
- satisfaction_level
- number_project
- average_montly_hours
- time_spend_company
- promotion_last_5years
- salary (encoded)

### Target
- left

Categorical variables were encoded using one-hot encoding, and numerical variables were scaled for optimal model performance.

---

## Model Building: Logistic Regression

### Why Logistic Regression?
- Suitable for binary classification problems
- Provides interpretable coefficients
- Efficient and widely used in HR analytics

### Steps Followed
1. Feature and target separation
2. Categorical variable encoding
3. Train-test split (80% training, 20% testing)
4. Feature scaling using StandardScaler
5. Model training using Logistic Regression
6. Prediction on test data

---

## Model Evaluation

### Evaluation Metrics
- Accuracy Score
- Confusion Matrix
- Precision, Recall, and F1-score

These metrics were used to assess how well the model predicts employee attrition and retention.

---

## Key Results
- The logistic regression model achieved strong predictive performance
- Satisfaction level, workload, salary, and promotion history were the most influential predictors
- The results align with insights discovered during EDA, validating the feature selection process

---

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

## Conclusion
This project demonstrates how exploratory data analysis and logistic regression can be combined to understand employee retention patterns and build predictive models. The insights derived from this analysis can help organizations design data-driven strategies to improve employee satisfaction and reduce attrition.

---

## Author
**Mary Udo**

Feel free to reach out for collaboration or feedback.
