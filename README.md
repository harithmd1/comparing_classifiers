# Bank Marketing Classification Project

## Overview
This project compares the performance of four classification algorithms — **K-Nearest Neighbors (KNN)**, **Logistic Regression (LR)**, **Decision Trees (DT)**, and **Support Vector Machines (SVM)** — using the **Bank Marketing Dataset** from the UCI Machine Learning Repository.  
The dataset represents marketing campaigns of a Portuguese banking institution conducted via telephone calls, with the goal of predicting whether a client will **subscribe to a term deposit**.

---

## Data
**Dataset Source:**  
UC Irvine Machine Learning Repository — *Bank Marketing Data Set*  

The dataset contains demographic, economic, and campaign-related attributes.  
Two versions are available:
- `bank-full.csv` (classic version)
- `bank-additional-full.csv` (includes macroeconomic features)

> **Note:** The feature `duration` is dropped to prevent data leakage, as it’s only known after the call ends.

---

## Objective
- Preprocess the dataset (numeric & categorical handling)
- Handle class imbalance via `class_weight='balanced'`
- Train, tune, and evaluate multiple classifiers using **Stratified 5-fold CV**
- Compare accuracy, F1-score, ROC-AUC, and PR-AUC
- Identify the best-performing model and provide insights

---

## Model Comparison

| Model | Type | Strengths | Weaknesses |
|--------|------|------------|-------------|
| Logistic Regression | Linear | Fast, interpretable, robust to noise | Limited for nonlinear data |
| Decision Tree | Nonlinear | Handles complex patterns, interpretable | Prone to overfitting |
| KNN | Instance-based | Simple, no training time | Slow for prediction on large data |
| SVM (RBF) | Kernel-based | Excellent for nonlinear separation | Computationally expensive, less interpretable |

---

## Methodology
1. **Data Loading** — Auto-detects dataset (semicolon/comma delimited)
2. **Preprocessing** — Standardization for numeric columns and one-hot encoding for categorical columns
3. **Model Training** — CV-based hyperparameter tuning with `GridSearchCV`
4. **Evaluation** — Metrics include Accuracy, F1, ROC-AUC, PR-AUC, and confusion matrix
5. **Visualization** — Time vs ROC-AUC trade-offs, ROC and PR curves for the best model

---
