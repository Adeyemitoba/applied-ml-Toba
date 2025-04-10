# Lab 5: Ensemble Models for Wine Quality Prediction
**Author:** Adeyemi Toba  
**Date:** April 10, 2025

## 🎯 Objective
This project applies ensemble machine learning models to predict the quality of red wine based on physicochemical characteristics. Ensemble models help improve accuracy and generalization compared to single-model approaches. Two models were chosen and compared: **Random Forest** and **Gradient Boosting**.

## 📊 Dataset
- **Source:** [UCI Machine Learning Repository – Wine Quality](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- **Attributes:** 11 physicochemical features and 1 quality target (score 0–10).
- **Preprocessing:** Quality scores were mapped to three classes:  
  - `0 = low` (3–4)  
  - `1 = medium` (5–6)  
  - `2 = high` (7–8)

## 🛠️ Features
- All features except `quality`, `quality_label`, and `quality_numeric` were used for training.

## 🔍 Models Evaluated
1. **Random Forest (100 estimators)**
2. **Gradient Boosting (100 estimators, learning_rate=0.1)**

Each model was evaluated using:
- Accuracy
- F1 Score
- Confusion Matrix
- Generalization gap (Train vs. Test metrics)

## ✅ Results Summary
| Model                 | Train Accuracy | Test Accuracy | Train F1 | Test F1 | Accuracy Gap | F1 Gap |
|----------------------|----------------|---------------|----------|---------|---------------|--------|
| Random Forest (100)  | 1.000          | 0.8875        | 1.0000   | 0.8661  | 0.1125        | 0.1339 |
| Gradient Boosting    | 0.9601         | 0.8562        | 0.9584   | 0.8411  | 0.1039        | 0.1173 |

- 🏆 **Best Performing Model:** *Random Forest* had the highest test accuracy and F1 score.
- ⚖️ **Best Generalization:** *Gradient Boosting* had slightly smaller train-test performance gaps.

## 💡 Insights & Reflections
Both ensemble methods were effective, but Random Forest achieved the best predictive performance. However, it also showed signs of overfitting with perfect training scores. Gradient Boosting was more balanced, suggesting better generalization to unseen data.

## 🤝 Comparative Analysis
Compared with **[Kate Huntsman's Lab 5](https://github.com/katehuntsman/applied-ml-huntsman/blob/main/lab05/ensemble-huntsman.ipynb)**:
- We both implemented and compared Random Forest and Gradient Boosting.
- Our results were similar in ranking and performance trends.
- Kate's work also highlighted overfitting in Random Forest and better generalization in Gradient Boosting.

## 🚀 Next Steps
- Perform hyperparameter tuning (max_depth, learning_rate, etc.)
- Try advanced libraries like **XGBoost** or **LightGBM**
- Explore cross-validation for more robust performance evaluation




















