
# Titanic Survival Prediction - Machine Learning Classification - lab03

**Author:** Adeyemi Toba  
**Date:** March 25, 2025  

## 📜 Project Overview

This project explores the Titanic dataset to predict passenger survival using various machine learning classification techniques. It walks through data exploration, preprocessing, feature engineering, model training, evaluation, and comparison using **Decision Tree**, **Support Vector Machine (SVC)**, and **Neural Network (MLPClassifier)** classifiers. The goal is to understand which features most influence survival and evaluate the predictive power of different algorithms under various conditions.


lab03/ │ ├── README.md # Project overview and results summary ├── ml03_Toba.ipynb # Jupyter notebook with code, plots, and analysis ├── decision_tree_titanic.png # Full tree visualization ├──Case 1 (age only) ├── Case 2 (fare only) ├── # Confusion matrix plot - Case 3 (age + family_size) ├── model_comparison_table.md # Markdown-formatted summary table of model performance.

---

## 📂 Dataset

- **Source**: Seaborn's Titanic dataset.
- **Features**:
  - Categorical: `sex`, `embarked`, `class`, `who`, `deck`, `alive`
  - Numerical: `age`, `fare`, `pclass`, `sibsp`, `parch`, `family_size`, `bmi`
- **Target**: `survived` (0 = No, 1 = Yes)

---

## 🔍 Exploratory Data Analysis

- Checked for missing values and filled them using median/mode.
- Engineered new features: 
  - `family_size = sibsp + parch + 1`
  - `bmi = (simulated BMI for demonstration)
- Visualizations:
  - Histograms, boxen plots, scatter plots, correlation matrix
  - Count plots and survival breakdowns by gender, class, and embarkation port
  - Confusion matrix heatmaps

---

## 🧪 Model Evaluation

### ✅ Model Performance Summary

| Model Type             | Case                         | Features Used                  | Accuracy | Precision | Recall | F1-Score |
|------------------------|------------------------------|--------------------------------|----------|-----------|--------|----------|
| **Decision Tree**      | Case 1                       | `age`                          | 0.58     | 0.41      | 0.20   | 0.27     |
| **Decision Tree**      | Case 2                       | `fare`                         | 0.63     | 0.53      | 0.35   | 0.42     |
| **Decision Tree**      | Case 3                       | `age + family_size`            | 0.58     | 0.42      | 0.28   | 0.33     |
| **Decision Tree**      | All Features + `bmi`         | `age, fare, pclass, sex, family_size, bmi` | ~TBD    | ~TBD     | ~TBD   | ~TBD     |
| **SVC (RBF Kernel)**   | Full Model                   | All features (scaled)          | ~0.78    | ~0.72     | ~0.68  | ~0.70    |
| **Neural Network (MLP)** | Full Model                 | All features (scaled)          | ~0.79    | ~0.75     | ~0.71  | ~0.73    |

---
## 🧾 Final Result Summary (Decision Tree Model)

| Case   | Features Used         | Accuracy | Precision | Recall | F1-Score | Notes                      |
|--------|------------------------|----------|-----------|--------|----------|----------------------------|
| Case 1 | age only              | 0.58     | 0.54      | 0.58   | 0.54     | Weak predictor, overfit    |
| Case 2 | fare only             | 0.63     | 0.61      | 0.63   | 0.61     | Slightly better than age   |
| Case 3 | age + family_size     | 0.58     | 0.55      | 0.58   | 0.55     | No big improvement         |

✅ **Best Accuracy**: Case 2 (using `fare` only)
🔍 **Observation**: Fare has better predictive power than age alone. Adding family_size didn't improve performance significantly.

## How to Use this Project
Clone this repository git clone https://github.com/Adeyemitoba/applied-ml-Toba.git

Install dependencies pip install -r requirements.txt

Run the Jupyter Notebook to explore results.


















