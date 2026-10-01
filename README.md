# Task 1: Data Cleaning & Preprocessing

## Overview

This project is part of an internship task focused on **Data Cleaning and Preprocessing for Machine Learning**.

The Titanic dataset was used to demonstrate how raw data can be cleaned, transformed, and prepared for Machine Learning applications.

The project covers missing-value handling, categorical encoding, feature scaling, outlier detection, and outlier removal.

---

## Objective

The objective of this task is to understand and implement the basic steps involved in preparing raw data for Machine Learning.

### Key Tasks Performed

- Explored the dataset and its structure
- Checked data types and missing values
- Handled missing values
- Converted categorical variables into numerical variables
- Standardized numerical features
- Detected outliers using boxplots and the IQR method
- Removed potential outliers
- Created a final cleaned dataset

---

## Dataset

The **Titanic Dataset** was used for this task.

The dataset contains information about passengers, including:

- Passenger class
- Age
- Sex
- Number of siblings/spouses
- Number of parents/children
- Passenger fare
- Port of embarkation
- Survival status

The original dataset is available in the `dataset/` folder.

The processed dataset is available in the `output/` folder.

---

## Technologies and Tools Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Google Colab**
- **GitHub**

---

## Project Workflow

### 1. Dataset Exploration

The dataset was initially explored to understand its structure and contents.

The following operations were performed:

- Displayed the first and last few records
- Checked the number of rows and columns
- Examined column names
- Checked data types
- Generated statistical summaries
- Checked missing values

---

### 2. Handling Missing Values

Missing values were identified using Pandas.

Different techniques were used depending on the type of column:

- Missing values in the `Age` column were replaced using the **median**.
- Missing values in the `Embarked` column were replaced using the **mode**.
- The `Cabin` column was removed because it contained a large number of missing values.

This resulted in a cleaner dataset with fewer missing values.

---

### 3. Removing Unnecessary Columns

The following columns were removed because they were not required for the preprocessing demonstration:

- `PassengerId`
- `Name`
- `Ticket`

---

### 4. Categorical Variable Encoding

Categorical variables cannot be directly used by most Machine Learning algorithms.

Therefore, categorical features such as:

- `Sex`
- `Embarked`

were converted into numerical features using **One-Hot Encoding**.

Pandas `get_dummies()` was used for this purpose.

---

### 5. Feature Scaling

Numerical features can have very different ranges.

For example, the values of `Fare` can be much larger than values of `Pclass`.

Therefore, numerical features were standardized using **StandardScaler** from Scikit-learn.

Standardization transforms numerical features so that they have approximately:

- Mean = 0
- Standard deviation = 1

---

### 6. Outlier Detection

Outliers were detected using:

- Boxplots
- Interquartile Range (IQR) method

The IQR method uses:

```text
IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR
