**Author**: Adeyemi Toba  
**Date**: April 3, 2025  
  **Lab**: Lab 04 – Regression Analysis on the Titanic Dataset

---

## 📌 Overview

This project explores how well we can **predict Titanic passenger fare** using linear and polynomial regression models. The objective is to analyze the relationship between a passenger's characteristics and their fare using the Titanic dataset.  

This lab builds on previous data cleaning and feature engineering efforts from Lab 02 and Lab 03, now applying regression techniques to a continuous target: `fare`.

---

## 📂 Dataset

- **Source**: Titanic dataset
- **Target Variable**: `fare` 
- **Features Used**:
  - `age`
  - `family_size`
  - `pclass`
  - `sex` (encoded)

---

## 🔧 Models Used

| Model Type             | Description                                      |
|------------------------|--------------------------------------------------|
| Linear Regression      | Baseline model for all 4 cases                   |
| Ridge Regression       | Regularized linear model to prevent overfitting  |
| ElasticNet Regression  | Combination of Lasso + Ridge                     |
| Polynomial Regression  | Captures nonlinear patterns (degree 3 and 6)     |

---

## 🔍 Feature Cases

| Case | Features Used                                  |
|------|------------------------------------------------|
| 1    | age                                             |
| 2    | family_size                                     |
| 3    | age + family_size                               |
| 4    | age + family_size + pclass + sex_encoded        |

---

## 📊 Model Performance Summary

| Case | MAE   | MSE     | R²   |
|------|-------|---------|------|
| 1    | 25.45 | 1524.64 | 0.01 |
| 2    | 24.78 | 1451.91 | 0.06 |
| 3    | 23.68 | 1398.10 | 0.10 |
| 4    | 22.55 | 1325.50 | 0.14 |

> ✅ Case 4 had the best performance across all metrics.

---

## 💡 Final Thoughts

- Age and family size alone offer limited predictive power.
- Including encoded categorical features like `sex` and `pclass` improves accuracy.
- Polynomial regression better captures nonlinear relationships, especially when visualized.
- More features and advanced models could further improve fare prediction.

---

## 🧪 Optional Enhancements

- Add advanced models like Random Forest or Gradient Boosting.
- Tune hyperparameters using GridSearchCV.
- Use pipelines to streamline data preprocessing.

---

## 📁 Folder Structure

```bash
Lab04/
├── ml04_Toba.ipynb          # Main notebook
├── README.md                # Summary of the lab
└── /data                    



















