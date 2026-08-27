# Medical Insurance Cost Prediction Using Linear Regression

Project Overview

This project uses Linear Regression to predict medical insurance charges based on demographic and personal characteristics.

The goal is to demonstrate a complete machine learning workflow, from loading and preparing data to training a regression model and evaluating its predictions.

Objective

The objective of this project is to predict an individual's medical insurance charges using the following characteristics:

* Age
* Sex
* BMI
* Number of children
* Smoking status
* Region

The target variable is `charges`, which represents the individual's medical insurance cost.

Dataset

The project uses the Medical Insurance Dataset, which contains information about individuals and their associated medical insurance charges.

 Features

| Feature    | Description                        |
| ---------- | ---------------------------------- |
| `age`      | Age of the individual              |
| `sex`      | Sex of the individual              |
| `bmi`      | Body Mass Index                    |
| `children` | Number of children/dependants      |
| `smoker`   | Whether the individual is a smoker |
| `region`   | Residential region                 |

Target Variable

`charges` — medical insurance charges.

Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

Machine Learning Workflow

The project follows these steps:

1. Load the medical insurance dataset.
2. Separate the features from the target variable.
3. Identify categorical and numerical features.
4. Apply One-Hot Encoding to categorical variables.
5. Split the data into training and testing sets.
6. Build a preprocessing and Linear Regression pipeline.
7. Train the model using the training data.
8. Generate predictions on the test data.
9. Evaluate model performance using MSE and R².

Data Preprocessing

The categorical variables:

* `sex`
* `smoker`
* `region`

were transformed using One-Hot Encoding.

The numerical variables:

* `age`
* `bmi`
* `children`

were passed through without transformation.

A Scikit-learn `ColumnTransformer` and `Pipeline` were used to combine preprocessing and model training into a single workflow.

Model

Linear Regression

Linear Regression was selected as the predictive model because the target variable, medical insurance charges, is continuous.

The model learns the relationship between the input variables and insurance charges and then uses those relationships to estimate charges for unseen observations.

Model Evaluation

The model was evaluated on the test dataset using two metrics.

| Metric                   |        Result |
| ------------------------ | ------------: |
| Mean Squared Error (MSE) | 33,596,915.85 |
| R² Score                 |          0.78 |

Interpretation

The R² score of 0.78** indicates that the model explains approximately 78% of the variation in medical insurance charges in the test data.

The MSE measures the average squared difference between the actual and predicted charges. Because the target variable is measured in monetary values, the MSE is relatively large due to the squaring of prediction errors.

Key Takeaways

This project demonstrates that demographic and lifestyle-related characteristics can be used to build a predictive model for medical insurance charges.

The project also demonstrates practical machine learning concepts including:

* Feature and target selection
* Categorical data encoding
* Train-test splitting
* Machine learning pipelines
* Linear Regression
* Model prediction
* Regression evaluation metrics

How to Run the Project

1. Clone the repository

git clone https://github.com/lethabomeidawg/medical-insurance-cost-prediction.git

2. Navigate to the project
   
cd medical-insurance-cost-prediction

3. Install the required libraries

pip install -r requirements.txt

4. Open the notebook

jupyter notebook

Open:
notebooks/medical_insurance_linear_regression.ipynb

Future Improvements

The Linear Regression model provides a useful baseline. Future versions of the project could compare its performance against other regression algorithms, such as:

* Random Forest Regression
* Gradient Boosting
* XGBoost

Additional improvements could include:

* Cross-validation
* Hyperparameter tuning
* Feature engineering
* More detailed exploratory data analysis
* Comparison of multiple machine learning models

Author

**Lethabo Thosago**

This project was developed as part of my data science and machine learning portfolio.

