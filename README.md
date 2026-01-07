# 📊 Telco Customer Churn Analysis 

## 📌 Project Overview
Customer churn is one of the most important challenges faced by subscription-based businesses. When customers leave, revenue drops and companies must spend significantly more to acquire new customers.

This project applies **data analytics, machine learning, and explainable AI (SHAP)** to:
- Understand **why customers churn**
- Predict **who is likely to churn**
- Provide **data-driven business strategies** to reduce customer loss

The dataset contains customer demographics, service usage, billing details, and contract information.

---

## 🧩 Business Problem
The company wants to reduce customer churn but lacks visibility into:
- Which customers are at risk  
- What factors drive churn  
- How to intervene before customers leave  

This project builds a **churn prediction system** and converts insights into **actionable business decisions**.

---

## 📂 Dataset
The dataset contains:
- Customer tenure  
- Monthly and total charges  
- Contract type  
- Payment method  
- Service subscriptions  
- Churn status  

Target variable:
- `Churn = 1` → Customer left  
- `Churn = 0` → Customer stayed  

---

## 🛠 Data Cleaning & Preparation
The following steps were applied:
- Handled missing values  
- Converted incorrect data types (e.g., `TotalCharges`)  
- Encoded categorical variables  
- Validated the churn target  

This ensured data quality and model reliability.

---

## 📊 Exploratory Data Analysis (EDA)

Key insights:
- **Short-tenure customers churn the most**
- **Month-to-month contracts have the highest churn**
- **High monthly charges strongly increase churn risk**
- **Customers with fewer services are more likely to leave**

These findings guided feature engineering and modeling.

---

## ⚙️ Feature Engineering
New features were created to capture customer behavior:
- `tenure_group`
- `service_count`
- `avg_monthly_spend`

These features improve both prediction accuracy and business interpretability.

---

## 🤖 Churn Prediction Models
Multiple classification models were trained, including:
- Logistic Regression  
- Random Forest / Gradient Boosting  

Models were evaluated using:
- Confusion Matrix  
- Precision  
- Recall  
- ROC-AUC  

The best-performing model was selected for explainability and deployment.

---

## 🔍 Model Explainability with SHAP

Machine learning models can behave like black boxes. **SHAP (SHapley Additive Explanations)** was used to explain **why** the model predicts churn.

### What SHAP Does
SHAP assigns each feature a contribution value for each prediction:
- **Positive SHAP value** → pushes toward churn  
- **Negative SHAP value** → pushes toward staying  

This allows us to understand both **global trends** and **individual customer behavior**.

---

### 🔑 Global SHAP Insights (Top Churn Drivers)

| Feature | Impact |
|--------|--------|
| Tenure | Short tenure strongly increases churn |
| Contract Type | Month-to-month customers churn more |
| Monthly Charges | High charges push customers to leave |
| Total Charges | Low lifetime spend signals weak loyalty |
| Service Count | Fewer services increases churn risk |

These results align with EDA, increasing confidence in the model.

---

### 👤 Local SHAP (Individual Customers)
For any customer, SHAP can explain:
> *“This customer is likely to churn because they have a short tenure, are on a month-to-month contract, and pay high monthly charges.”*

This makes churn predictions **actionable** for customer success and marketing teams.

---

## 📈 Post-Prediction Analysis
The model performs best for:
- New customers  
- High-spending users  
- Month-to-month subscribers  

It struggles when customers have mixed or contradictory behaviors.

---

## 💡 Business Recommendations

### 1️⃣ Focus on High-Risk Customers
Target customers who:
- Have short tenure  
- Are on month-to-month contracts  
- Pay high monthly charges  

Offer discounts, loyalty rewards, or service upgrades.

---

### 2️⃣ Promote Long-Term Contracts
Encourage customers to move to yearly or two-year plans using incentives.

---

### 3️⃣ Improve Early Customer Experience
Most churn occurs in the first few months. Strengthen onboarding, support, and engagement.

---

### 4️⃣ Deploy the Churn Model
Use churn predictions to:
- Assign churn risk scores  
- Trigger proactive retention campaigns  

---
