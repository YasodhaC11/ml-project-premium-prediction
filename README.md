# Health Insurance Premium Prediction

## Project Overview
This project predicts **annual health insurance premiums** based on demographic, medical, and financial data. It uses **Linear, Ridge, and XGBoost regression models** and implements **age-based model segmentation** to improve prediction accuracy for younger users. The project includes a **Streamlit frontend** for interactive, real-time premium prediction.

---

## Dataset
- **Records:** 50,000  
- **Features (13):**  
  `age`, `gender`, `region`, `marital_status`, `number_of_dependants`, `bmi_category`, `smoking_status`, `employment_status`, `income_level`, `income_lakhs`, `medical_history`, `insurance_plan`, `annual_premium_amount`  
- Dataset includes **numerical and categorical features**, and **medical history** is used to calculate a **custom risk score**.

---

## Features / Preprocessing
- **Outlier detection and treatment** for numerical features  
- **Categorical encoding:** One-hot encoding for categorical variables, mapping for insurance plan and income levels  
- **Scaling:** MinMaxScaler applied to numerical features  
- **Feature Engineering:**  
  - Calculated **medical risk score** from medical history  
  - Added **genetical risk** feature for young users (age ≤25)  
- **Multicollinearity check:** Variance Inflation Factor (VIF) analysis  

---

## Modeling
- **Models:** Linear Regression, Ridge Regression, XGBoost  
- **Model Segmentation:**  
  - **Age >25:** XGBoost R²≈0.998, extreme errors 0.5%  
  - **Age ≤25 (with genetical risk):** XGBoost R²≈0.988, extreme errors 2%  
- **Hyperparameter Tuning:** RandomizedSearchCV for XGBoost  
- **Error Analysis:** Residuals & percentage difference analysis  
- **Serialization:** Models and scalers saved using Joblib  

---

## Streamlit App
- Built an **interactive frontend** using Streamlit  
- Users can input **age, income, dependants, medical history, genetical risk, and other demographic details**  
- Provides **real-time premium prediction**  
- **Live Demo:** [Streamlit Cloud](https://project-ml-premium-prediction.streamlit.app/)  

---

## Installation
1. Clone the repository:  
2. pip install -r requirements.txt
3. streamlit run main.py

