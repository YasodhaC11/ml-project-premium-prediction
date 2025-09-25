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
- **Multicollinearity check:** Variance Inflation Factor (V
