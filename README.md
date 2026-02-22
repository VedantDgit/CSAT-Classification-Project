# 📊 Customer Support CSAT Prediction using Machine Learning

## 🧠 Project Overview

This project focuses on analyzing and predicting Customer Satisfaction (CSAT) scores using customer support interaction data.

The objective is to build a multi-class classification model that predicts CSAT scores (1–5 scale) and identifies key operational factors affecting customer satisfaction.

---

## 🎯 Problem Statement

Customer satisfaction plays a crucial role in customer retention and brand perception.  
The goal of this project is to:

- Predict CSAT score based on historical support data
- Identify factors that influence customer satisfaction
- Provide actionable business insights to improve service quality

---

## 📁 Dataset Description

The dataset contains approximately **85,000 customer support interaction records**, including:

- Channel Name (Inbound / Outcall)
- Issue Category & Sub-category
- Agent Tenure
- Agent Shift
- Issue timestamps
- CSAT Score (Target Variable)

---

## 🧹 Data Preprocessing Steps

✔ Removed columns with high missing values (>60%)  
✔ Dropped identifier columns (unique_id, order_id, etc.)  
✔ Converted date columns to datetime format  
✔ Engineered new feature: `response_time_min`  
✔ Handled missing values using median (numerical) and mode (categorical)  
✔ Treated outliers using IQR method  
✔ Applied One-Hot Encoding  
✔ Applied Standard Scaling (for Logistic Regression)

---

## 📊 Exploratory Data Analysis (EDA)

The project followed the UBM rule:

- **Univariate Analysis**
- **Bivariate Analysis**
- **Multivariate Analysis**

### Key Insights:

- Dataset is highly imbalanced (majority CSAT = 5)
- Response time significantly affects customer satisfaction
- Communication channel influences CSAT
- Agent experience impacts resolution efficiency

---

## 📈 Hypothesis Testing

Statistical tests were performed to validate observations:

- One-Way ANOVA → Response time vs CSAT
- Chi-Square Test → Channel vs CSAT
- ANOVA → Tenure vs Response Time

Results confirmed that operational factors significantly influence satisfaction.

---

## 🤖 Machine Learning Models Used

1. Logistic Regression  
2. Random Forest  
3. XGBoost  

### Evaluation Metrics:

- Accuracy  
- Weighted F1-Score (Primary metric due to class imbalance)  
- Cross-Validation Score  

### Final Model Selected:

✅ **XGBoost** (Best Weighted F1 Score)

---

## 🔍 Feature Importance

Feature importance analysis revealed:

- `response_time_min` is the most influential predictor.
- Operational efficiency is strongly linked to customer satisfaction.

---

## 💼 Business Impact

The findings suggest that:

- Reducing issue resolution time can significantly improve CSAT.
- Optimizing underperforming communication channels can enhance service quality.
- Investing in agent training improves response efficiency.

This model can help organizations proactively identify dissatisfaction risks and improve customer retention.

---

## 🚀 Deployment Ready

The best-performing model was:

- Saved using `joblib`
- Reloaded successfully for inference
- Verified with unseen data

The project notebook runs end-to-end without errors and is deployment-ready.

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Seaborn & Matplotlib
- Scikit-Learn
- XGBoost
- Joblib

---

## 📂 Repository Structure

   
