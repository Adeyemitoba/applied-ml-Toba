# 🩺 Breast Cancer Classification - Lab2

**Author:** Adeyemi Toba  
**Date:** March 17, 2025  
**Objective:** Predict tumor malignancy (benign vs. malignant) using key tumor features.

---

## 📜 Project Overview
This project applies **machine learning techniques** to classify tumors as **malignant (cancerous) or benign (non-cancerous)** based on the **Breast Cancer Wisconsin dataset**.  
The dataset is **explored, cleaned, and prepared** for model training by handling missing values, feature engineering, and train-test splitting.

---

## 📁 Folder Structure
📦 Breast-Cancer-Classification ┣ 📂 data # Dataset (raw & processed) ┃ ┣ 📜 breast_cancer.csv ┃ ┣ 📜 processed_breast_cancer_data.csv ┣ 📂 notebooks # Jupyter Notebooks ┃ ┣ 📜 Lab02 ┃ ┣ 📂 scripts # Python scripts for preprocessing & modeling ┃ ┣ 📜 preprocess.py ┃ ┣ 📜 train_model.py ┣ 📜 README.md # Project documentation ┣ 📜 requirements.txt # Dependencies ┗ 📜 .gitignore # Git exclusions


---

## 📊 Data Exploration & Preprocessing
### ✅ Steps:
1. **Importing & Inspecting Data**
   - Load the **Breast Cancer dataset** from `sklearn.datasets`
   - Identify **missing values** and check dataset structure
   - Perform **summary statistics and correlation analysis**
   - **Visualize** key variables

2. **Data Visualization**
   - **Histograms** → Visualize numeric feature distributions  
   - **Boxenplots** → Detect outliers  
   - **Scatter Plots & Pairplots** → Analyze feature relationships  
   - **Count Plots** → Explore categorical distributions  

3. **Data Cleaning**
   - Handle missing values (if applicable)  
   - Convert categorical data (`diagnosis`) into **numerical format**  
   - Normalize numerical features (optional)  

4. **Feature Engineering**
   - Create **`tumor_volume`** (approximate using **sphere volume formula**)  
   - Create **`compactness_ratio`** (`mean compactness` / `mean perimeter`)  

5. **Train-Test Splitting**
   - **Basic Random Split** (`train_test_split`)  
   - **Stratified Split** (`StratifiedShuffleSplit`)  
   - **Compare class distributions**  

---

## 📈 Visualizations
### **Tumor Diagnosis Distribution**
```python
sns.countplot(x='diagnosis', data=df)

## Mean Radius vs. Mean Perimeter Scatter Plot
sns.scatterplot(x='mean radius', y='mean perimeter', hue='diagnosis', data=df)

## Tumor Volume Distribution
sns.histplot(df['tumor_volume'], kde=True)

## Boxenplots for Outliers in Mean Area
sns.boxenplot(x=df['mean area'])
