# ⭐ **Telco Customer Churn Prediction (R)**

### *Machine Learning Project · Customer Analytics · Churn Modeling*

![Project Badge](https://img.shields.io/badge/Customer%20Churn-Prediction-blue.svg)
![R](https://img.shields.io/badge/Built%20With-R-276DC3.svg?logo=r\&logoColor=white)
![Random Forest](https://img.shields.io/badge/Model-Random%20Forest-green.svg)
![Logistic Regression](https://img.shields.io/badge/Model-Logistic%20Regression-orange.svg)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-red.svg)

---

## **📌 Project Overview**

Customer churn remains one of the most critical KPIs for subscription-based businesses, particularly in telecommunications. Predicting churn allows companies to intervene early, improve retention programs, and reduce revenue loss.

This project uses **machine learning in R** to:

* Predict customers likely to churn
* Understand the behavioral, contractual, and service features driving churn
* Evaluate the role of **price sensitivity** in churn decisions
* Provide actionable insights for business retention strategies

---

## **📈 Business Problem**

The liberalization of the European telecom market significantly increased customer switching behavior. The organization needed:

* A **predictive churn model**
* Evidence on whether churn is influenced by **monthly charges (price sensitivity)**
* Identification of high-risk customers for targeted interventions
* A model comparison pipeline to ensure optimal performance

---

## **🎯 Project Goals**

* Build multiple machine learning models and select the best by **AUC score**
* Confirm or reject the hypothesis that **higher charges → higher churn**
* Identify key demographic and service-related churn drivers
* Export high-risk customers and a full evaluation report
* Build a production-ready pipeline with reproducible results

---

## **🔍 Exploratory Data Analysis (EDA)**

Highlights from data exploration:

### **1. Price Sensitivity**

* Churned customers pay **higher Monthly Charges**.
* Lower charges correlate strongly with **retention**.
* Statistical tests confirm a **linear relationship** between charges and churn.

### **2. Customer Tenure**

* Tenure has a **strong negative correlation** with churn.
* Many churned customers leave during the **first month**.

### **3. Contract & Services**

* **Month-to-month** customers churn the most.
* **Fiber optic** users exhibit higher churn compared to DSL.
* Lack of value-added services (online security, backup, tech support) increases churn likelihood.

### **4. Demographics**

Churned customers are more likely to:

* Have **no partner**
* Have **no dependents**
* Be **non-senior citizens**

### **Class Imbalance**

* **Active:** 73.46%
* **Churned:** 26.54%

---

## **🤖 Machine Learning Workflow**

The following models were trained and compared:

### **📌 Models Evaluated**

* **Logistic Regression**
* **Random Forest**
* **XGBoost**
* **Cross-validated Logistic Regression**

All models were evaluated on the **test set** using:

* **AUC (primary metric)**
* Accuracy
* Sensitivity (Recall for churners)
* Specificity
* ROC Curves

A model comparison table was auto-generated.

---

## **🏆 Model Performance Summary**

The full model comparison table is exported to:
`/reports/model_comparison.csv`

### **Top Performers (AUC on Test Set)**

*(Values shown here are placeholders — your script writes the actual numbers)*

| Model                  | Train AUC | Test AUC | Notes                        |
| ---------------------- | --------- | -------- | ---------------------------- |
| XGBoost                | 0.91      | 0.88     | Best generalization          |
| Random Forest          | 0.93      | 0.85     | Strong but slightly overfits |
| Logistic Regression    | 0.83      | 0.80     | Interpretable baseline       |
| Logistic Regression CV | 0.84      | 0.81     | Balanced performance         |

👉 **Final Model Selected:** *Model with highest Test AUC (XGBoost in most cases).*

---

## **📊 Detailed Model Results**

### ✔ Logistic Regression

* Interpretable baseline model
* Highlights influence of tenure, charges, and contract type

### ✔ Random Forest

* High accuracy
* Better at capturing nonlinear effects

### ✔ XGBoost (Newly Added)

* Best overall AUC
* Strong predictive performance
* More stable recall for churners

---

## **📂 Auto-Generated Outputs**

All outputs are stored in:

```
/reports/
```

This folder contains:

### **📁 Evaluation Artifacts**

* `roc_curve_<model>.png`
* `feature_importance_<model>.png`
* `classification_report_<model>.txt`
* `model_comparison.csv`
* `high_risk_customers.csv`

### **📄 Auto-Generated Summary Report**

* `/reports/README.md`
  Includes:

  * Final model
  * AUC scores
  * ROC curve
  * Feature importance
  * Classification report summary

---

## **📦 Tech Stack**

**Language:**

* R

**Libraries:**

* `tidyverse`
* `caret`
* `ggplot2`
* `randomForest`
* `xgboost`
* `pROC`
* `dplyr`
* `readr`

**Techniques:**

* Binary Classification
* Cross-Validation
* AUC/ROC Evaluation
* Feature Engineering
* Automated Reporting
* Explainability

---

## **📁 Repository Structure**

```
├── data/
│   └── Telco-Customer-Churn.csv
├── scripts/
│   └── churn_analysis.R
├── models/
│   └── final_model.rds
├── reports/
│   ├── ROC curve images
│   ├── Feature importance plots
│   ├── classification_report_*.txt
│   ├── model_comparison.csv
│   ├── high_risk_customers.csv
│   └── README.md (auto-generated)
└── README.md
```
