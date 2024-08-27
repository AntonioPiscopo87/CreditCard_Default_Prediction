![credit-card-default-surges-as-retail-credit-grows](https://github.com/user-attachments/assets/4875dd4d-9c86-4c87-bad4-e0858c2ef8f9)
# Credit Card Default Prediction - Feature Engineering

## Overview

This repository contains a Jupyter Notebook that demonstrates the process of preparing data for Machine Learning algorithms to predict credit card defaults. The focus is on feature engineering, where the raw data is transformed into features that better serve the prediction model.

## Table of Contents

1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Prerequisites](#prerequisites)
4. [Dataset](#dataset)
5. [Analysis Steps](#analysis-steps)
   - [1. Data Loading](#1-data-loading)
   - [2. Data Exploration](#2-data-exploration)
   - [3. Handling Missing Values](#3-handling-missing-values)
   - [4. Feature Engineering](#4-feature-engineering)
   - [5. Feature Transformation](#5-feature-transformation)
   - [6. Categorical Variable Encoding](#6-categorical-variable-encoding)
   - [7. Correlation Analysis](#7-correlation-analysis)
6. [Results](#results)
7. [How to Use](#how-to-use)
8. [License](#license)
9. [Acknowledgments](#acknowledgments)

## Project Structure

The repository is structured as follows:

```
credit-card-default-prediction/
│
├── data/
│   └── credit_demo.csv                  # Raw dataset used in the analysis
│
├── notebooks/
│   └── demo_credit_fe_practice.ipynb    # Jupyter Notebook containing the analysis
│
├── README.md                            # Project documentation
├── LICENSE                              # License for the project
└── .gitignore                           # Git ignore file
```

## Prerequisites

Before running the notebook, ensure you have the following installed:

- **Python 3.x**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Scikit-learn**

You can install the required Python packages using pip:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## Dataset

The dataset used in this analysis, `credit_demo.csv`, contains information related to credit card balances, payment history, and demographic details of credit card holders. The target variable is `default`, which indicates whether the individual defaulted on their credit card payment.

## Analysis Steps

### 1. Data Loading
The dataset is loaded using Pandas, with missing values handled appropriately during import.

### 2. Data Exploration
The initial exploration involves examining the dataset's structure, summary statistics, and the proportion of defaulters vs. non-defaulters.

### 3. Handling Missing Values
Missing values are identified and treated using strategies such as filling with the mean for continuous variables.

### 4. Feature Engineering
Features are engineered to enhance the predictive power of the model:
- **Credit Limit Bucketing**: `LIMIT_BAL` is bucketed into `LOW`, `MEDIUM`, and `HIGH`.
- **Age Bucketing**: `AGE` is bucketed into categories like `lessthan30`, `betw29-35`, etc.
- **Bill Amount Bucketing**: `BILL_AMT` is categorized into `LOW`, `MEDIUM`, and `HIGH`.
- **Payment Amount Bucketing**: `PAY_AMT` is also bucketed similarly.

### 5. Feature Transformation
Outliers in features like `AGE` are treated, and transformations are applied to ensure the data is well-prepared for modeling.

### 6. Categorical Variable Encoding
Categorical features such as `GENDER`, `MARRIAGE`, and `EDUCATION` are encoded using methods like One-Hot Encoding to make them usable in machine learning models.

### 7. Correlation Analysis
Correlation analysis is performed on continuous variables to understand their relationships with the target variable and each other.

## Results

The analysis results in a transformed dataset that is ready for machine learning algorithms. The engineered features like `LIMIT_BAL`, `AGE`, `BILL_AMT`, and `PAY_AMT` have been bucketed and encoded to better represent the data's underlying patterns.

## How to Use

1. **Clone this repository**:
    ```bash
    git clone https://github.com/yourusername/credit-card-default-prediction.git
    cd credit-card-default-prediction
    ```

2. **Run the Jupyter Notebook**:
    ```bash
    jupyter notebook notebooks/demo_credit_fe_practice.ipynb
    ```

3. **Follow the steps in the notebook** to reproduce the feature engineering and data preparation process.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- The dataset used in this analysis was provided as a demo for educational purposes.
- Special thanks to the contributors of open-source libraries like Pandas, NumPy, and Scikit-learn that made this analysis possible.

---

This README should provide a comprehensive guide for anyone looking to understand and run the feature engineering process for credit card default prediction. Feel free to customize it further based on your specific needs.
![image](https://github.com/user-attachments/assets/25da22a3-f487-46e6-9bcd-ca59ddab6957)
