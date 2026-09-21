# Diabetes-patient-Analytics-
Patient segmentations, lengths-of-stay analysis and 30 days readmission prediction using python and machine learning 

## Project Overview

This project analysis patient-level healthcare data to explore patient characteristics, segment patients using unsupervised learning, model length of hospital stay, and classify 30-day readmission.

The project was completed as part of my MSc Data Science & Artificial Intelligence studies.

## Objectives

- Perform exploratory data analysis to understand the dataset.
- Identify missing values, outliers, distributions and relationships between variables.
- Segment patients using K-Means clustering.
- Model length of hospital stay using regression techniques.
- Classify patients based on 30-day readmission.
- Evaluate model performance using appropriate statistical and machine-learning metrics.

## Methodology

### 1. Exploratory Data Analysis

The analysis included:

- Data cleaning and preprocessing
- Missing-value analysis
- Outlier analysis
- Distribution analysis
- Correlation analysis
- Data visualisation

### 2. Patient Segmentation

K-Means clustering was applied to create patient segments based on the available patient and admission features.

### 3. Length of Stay Prediction

The target variable was `time_in_hospital`.

The following regression models were evaluated:

- Ridge Regression
- Random Forest Regression

A manual 5-fold out-of-fold cross-validation approach was used, with preprocessing fitted separately within each fold to reduce data leakage.

### 4. 30-Day Readmission Classification

The target variable was `readmitted_30d`.

The following classification models were evaluated:

- Logistic Regression
- Random Forest Classifier

Class weighting was used to address the imbalance between readmitted and non-readmitted cases.

Evaluation included:

- ROC-AUC
- Precision
- Recall
- F1-score
- Confusion matrix

## Results

### Length of Stay

| Model | R² | MAE | RMSE |
|---|---:|---:|---:|
| Ridge Regression | 0.056 | 2.265 days | 2.904 days |
| Random Forest Regression | 0.051 | 2.276 days | 2.912 days |

The regression results indicated limited predictive signal for length of stay from the admission-time features used in the analysis.

### 30-Day Readmission

| Model | ROC-AUC | Minority-Class Recall | Minority-Class Precision |
|---|---:|---:|---:|
| Logistic Regression | 0.616 | 0.44 | 0.16 |
| Random Forest Classifier | 0.619 | 0.45 | 0.16 |

The classification results were evaluated with particular attention to the minority readmission class because of the class imbalance in the dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository Contents

- `diabetes-patient-analytics.ipynb` — Jupyter Notebook containing the analysis and modelling workflow.

## Dataset

The dataset was provided for university coursework and is not included in this public repository.

