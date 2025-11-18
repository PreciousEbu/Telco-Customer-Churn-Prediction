

# **Telco Customer Churn Prediction (R)**

### *Machine Learning Project | Classification | Customer Analytics*

![Project Banner](https://img.shields.io/badge/Customer%20Churn-Machine%20Learning-blue.svg)
![R](https://img.shields.io/badge/Built%20With-R-276DC3.svg?logo=r\&logoColor=white)
![Random Forest](https://img.shields.io/badge/Model-Random%20Forest-green.svg)
![Logistic Regression](https://img.shields.io/badge/Model-Logistic%20Regression-orange.svg)

---

## **📌 Project Overview**

Customer churn—customers discontinuing service—is a critical business metric for subscription-based industries, especially telecommunications. With increasing market competition, understanding *why* customers leave and *predicting churn early* helps companies implement targeted retention strategies.

This project builds a predictive machine-learning model in **R** to identify customers likely to churn and uncover the major behavioral and service-related factors influencing churn.

---

## **📈 Business Problem**

The liberalization of the European telecom market led to increased competition and a surge in customer switching behavior. The business needed:

* A **predictive model** to identify customers at risk of churning.
* Insight into whether **price sensitivity** is a major driver of churn.
* Actionable intelligence to guide **customer retention strategies**.

---

## **🎯 Project Goals**

* Develop a machine-learning model that predicts churn with strong accuracy.
* Evaluate whether customer churn is significantly driven by **price sensitivity** (monthly charges).
* Identify the key demographic and service-related features influencing churn.
* Provide data-driven recommendations for retention.

---

## **🔍 Exploratory Data Analysis (EDA)**

Key insights discovered through visualizations and statistical summaries:

### **1. Price Sensitivity**

* Customers who churned generally paid **higher monthly charges**.
* Lower monthly charges corresponded with **higher retention**, supporting the price-sensitivity hypothesis.

### **2. Customer Tenure**

* Longer-tenured customers were *less likely* to churn.
* A significant proportion of churned customers left within their **first month**.

### **3. Service & Contract Insights**

* Customers on **month-to-month contracts** churned the most.
* **Fiber optic** subscribers showed higher churn rates compared to DSL users.
* Customers without value-added services (online backup, security, device protection, tech support) were more prone to churn.

### **4. Demographics**

* Most churned customers:

  * Had **no partner**
  * Had **no dependents**
  * Were **non-senior citizens**

### **Class Balance**

* **Active customers:** 73.46%
* **Churned customers:** 26.54%
* The dataset is moderately imbalanced.

---

## **📌 Key Findings**

* The most influential churn predictors were:
  **Tenure**, **Monthly Charges**, **Contract Type**, **Internet Service**, and **Total Charges**.
* **Price sensitivity is a major driver of churn**, confirmed through statistical tests.
* However, **price alone does not fully explain churn**—contract and service-related features also play strong roles.
* Machine learning models effectively predict churn and support proactive retention planning.

---

## **🤖 Machine Learning Models**

### **📌 Models Evaluated**

* **Random Forest**
* **Generalized Linear Models (Logistic Regression)**

  * Compared across models using **AIC**
  * Model 4 had the lowest AIC and was selected for further evaluation

---

## **📊 Model Performance**

### **Random Forest**

* **Accuracy:** 79.44%
* Higher error rate in predicting positive churn (“Yes”) compared to “No”.

---

### **Logistic Regression – Model 4**

Using the model with the lowest AIC:

| Metric          | Score  |
| --------------- | ------ |
| **Accuracy**    | 0.7974 |
| **Sensitivity** | 0.9575 |
| **Specificity** | 0.3547 |

---

### **Cross-Validated Logistic Regression (Final Model)**

After applying cross-validation:

| Metric          | Score  |
| --------------- | ------ |
| **Accuracy**    | 0.807  |
| **Sensitivity** | 0.9104 |
| **Specificity** | 0.5214 |

✔️ **Selected as the final candidate model due to superior balanced performance.**

---

## **📐 Evaluation Metrics**

* **Accuracy**
* **Sensitivity (Recall for churners)**
* **Specificity (Correct identification of non-churners)**

---

## **📦 Tech Stack**

* **Language:** R
* **Libraries:** `tidyverse`, `caret`, `ggplot2`, `randomForest`, `dplyr`, `readr`
* **Techniques:** Classification, EDA, Model Evaluation, Cross-Validation

---

## **📁 Repository Structure** 

```
├── data/
│   └── Telco-Customer-Churn.csv
├── scripts/
│   └── churn_analysis.R
├── models/
│   └── final_model.rds
├── README.md
└── plots/
```

