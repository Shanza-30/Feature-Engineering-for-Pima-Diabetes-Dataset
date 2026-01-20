#  Feature Engineering for Model Gains

## Overview
This project focuses on **feature engineering** to boost the performance of machine learning models on the **Pima Indians Diabetes dataset**. The goal is to create new synthetic features, retrain the model, and compare performance metrics before and after feature engineering.


## Dataset
**Source:** [Kaggle – Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

**Features:**
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Target: Outcome (0 = No Diabetes, 1 = Diabetes)

---

## Synthetic Features Created
1. **Glucose_BMI_Ratio** – Ratio of glucose to BMI to normalize risk.  
2. **High_Glucose** – Flag for glucose > 140 mg/dL.  
3. **Low_BP** – Flag for low blood pressure (<60 mmHg).  
4. **High_Insulin** – Flag for insulin > 100.  
5. **BMI_Age_Interaction** – Interaction between BMI and Age.  
6. **Preg_Age_Interaction** – Interaction between Pregnancies and Age.  
7. **Age_Group** – Binned age categories.  
8. **BMI_Group** – Binned BMI categories (underweight/normal/overweight/obese).  
9. **Log_Insulin** – Log transformation to reduce skew.  
10. **Glucose_Sq** – Squared glucose to capture nonlinear effects.

---

## Methodology
1. **Baseline Model:** Logistic Regression with original 8 features.  
2. **Feature Engineering:** Added 10 new synthetic features.  
3. **Enhanced Model:** Logistic Regression retrained with original + engineered features.  
4. **Evaluation:** 5-fold cross-validation, accuracy comparison, and performance visualization.

---

## Results
- **Baseline Accuracy:** *[0.76]*  
- **Feature Engineered Accuracy:** *[0.77]*  


## Tools & Libraries
- Python 3.x  
- Pandas  
- Numpy  
- scikit-learn  
- Matplotlib / Seaborn  

