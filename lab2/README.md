# Titanic Survival Prediction - Lab2

**Author:** Adeyemi Toba  
**Date:** March 12, 2025  
**Objective:** Predict passenger survival on the Titanic using key features.

## 📜 Project Overview
This project analyzes the Titanic dataset to predict passenger survival based on attributes such as age, fare, class, and family size. The dataset is explored, cleaned, and prepared for machine learning models by handling missing values, performing feature engineering, and applying train-test splitting.

## 📁 Folder Structure
```
📦 Titanic-Survival-Prediction
 ┣ 📂 data                # Dataset (raw & processed)
 ┃ ┣ 📜 titanic.csv
 ┃ ┣ 📜 processed_titanic_data.csv
 ┣ 📂 notebooks           # Jupyter Notebooks
 ┃ ┣ 📜 Lab02
         mI02-Toba.ipynb
 ┣ 📂 scripts             # Python scripts for preprocessing & modeling
 ┃ ┣ 📜 preprocess.py
 ┃ ┣ 📜 train_model.py
 ┣ 📜 README.md           # Project documentation
 ┣ 📜 requirements.txt     # Dependencies
 ┗ 📜 .gitignore          # Git exclusions
```

## 📊 Data Exploration & Preprocessing
### ✅ Steps:
1. **Importing & Inspecting Data**
   - Load Titanic dataset using Seaborn
   - Identify missing values and check dataset structure
   - Summary statistics and correlation analysis
   - Data Visualization

2. **Data Visualization**
   - Histograms: Visualize numeric feature distributions
   - Boxenplots: Detect outliers
   - Scatter Plots & Pairplots: Analyze feature relationships
   - Count Plots: Explore categorical distributions

3. **Data Cleaning**
   - Fill missing values (age, embark_town)
   - Convert categorical data to numerical format
   - Handle outliers

4. **Feature Engineering**
   - Create `family_size` (sum of `sibsp` + `parch` + 1)
   - Encode `sex` and `embarked` as numerical features
   - Generate `alone` feature (binary)

5. **Train-Test Splitting**
   - Basic Random Split (`train_test_split`)
   - Stratified Split (`StratifiedShuffleSplit`)
   - Compare class distributions

## 📈 Visualizations
- **Survival Rate by Class:**  
  ```python
  sns.countplot(x='class', hue='survived', data=titanic)
  ```
- **Age vs Fare Scatter Plot:**  
  ```python
  sns.scatterplot(x='age', y='fare', hue='survived', data=titanic)
  ```
- **Distribution of Family Size:**  
  ```python
  sns.histplot(titanic['family_size'], kde=True)
  ```
- **Boxenplots for Outliers:**  
  ```python
  sns.boxenplot(x=titanic['fare'])
  ```

## 📌 Model Training & Evaluation
This project prepares data for machine learning. Next steps include:
- Training models (Logistic Regression, Random Forest, XGBoost)
- Evaluating performance using accuracy, precision, recall, and F1-score
- Hyperparameter tuning to improve predictions

## 🔧 Installation & Usage
### 📥 Install Dependencies
```bash
pip install -r requirements.txt
```

### 🚀 Run Jupyter Notebook
```bash
jupyter notebook


















