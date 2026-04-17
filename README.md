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

| Model               | Test AUC | Notes                                |
| ------------------- | -------- | ------------------------------------ |
| Logistic Regression | 0.8471   | Best AUC + interpretable baseline    |
| XGBoost             | 0.8446   | Strong performance, close second     |
| Random Forest       | 0.8323   | Good performance, slightly lower AUC |

👉 **Final Model Selected:**

---

## **📊 Detailed Model Results**

### ✔ Logistic Regression (Final Model)
* Best overall Test AUC (0.8471)
* Strong interpretability for churn drivers
* Highlights influence of tenure, charges, contract type, and service features

### ✔ XGBoost
* Second-best Test AUC (0.8446)
* Strong predictive performance
* Competitive alternative where nonlinear interactions matter

### ✔ Random Forest
* Test AUC of 0.8323
* Captures nonlinear effects well
* Slightly weaker AUC compared to Logistic Regression and XGBoost
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
│   └── Telco customer churn prediction.Rmd
├── models/
│   └── final_model.rds
└── README.md
```

---

## 🚀 Usage / How to Run

![Run](https://img.shields.io/badge/Run-R-blue)

**Clone the repository:**

```bash
git clone https://github.com/yourusername/customer-churn-prediction.git
cd customer-churn-prediction
```

**Run the analysis:**

1. Open `scripts/churn_analysis.R` in RStudio.
2. Install required packages if not already installed:

```r
install.packages(c(
  "tidyverse", "caret", "randomForest", "Boruta", 
  "xgboost", "pROC", "vip", "janitor"
))
```

3. Execute the script step by step or source it to reproduce the analysis and generate outputs.

---

## 🤝 Acknowledgments & References

![Thanks](https://img.shields.io/badge/Acknowledgments-Community-yellow)

* **Dataset Source:** [Kaggle Telco Customer Churn dataset](https://www.kaggle.com/blastchar/telco-customer-churn)
* **SHAP Methodology:** Lundberg & Lee (2017)

---

## 📄 License

![License](https://img.shields.io/badge/License-MIT-green)

This project is licensed under the **MIT License** — see the LICENSE file for details.

---

