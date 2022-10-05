# Telco-Customer-Churn-Prediction-using-machine-learning-in-R
### PROJECT OVERVIEW
Customer churn is one of the most important metrics for a growing business to evaluate. It gives a company the hard truth about its customer retention. Customer churn is the percentage of customers that stopped using the company’s product or service during a certain time frame.

### BUSINESS PROBLEM 
The liberalization of the telecommunications market in Europe has led to significant customer churn. Therefore, it is important to diagnose the source of churning customers.

### GOALS 
To build a predictive model that can identify customers who are likely to churn to enable the company employ adequate interventions that were geared towards reducing customers’ churn.
To confirm or reject one of the hypotheses under consideration that churn is driven by the customers’ price sensitivities and that it is possible to predict customers likely to churn using a predictive model.

### EXPLORATORY DATA ANALYSIS
- Scatter plots showed that a linear relationship exists between tenure and monthly charges causing both to increase simultaneously
 
- Another plot showed that Customers with longer tenure are less likely to churn.
  
- With the help of a histogram, it was revealed that customers who churn pay higher Monthly Charges. The Lowest monthly charge shows high proportion of retained customers. This indicates that price sensitivity is one of the drivers of churn.
  
- Another histogram showed that customers with higher total charges tended not to churn.

### RESULTS/FINDINGS
1.	The most important predictors of customers Churn in Telcos are Tenure, Monthly Charges and Contract. 
2.	Customers with longer contract and tenure, more total charges, partners, dependents, online security, online backup, tech support, who are senior citizens and those who use credit card payment method and are less likely to churn while customers who use fiber optic internet service are most likely to churn
3.	Customers with month-month contract are more likely to churn meanwhile a large proportion of customers who churned did so in their first month 
4.	Statistical tests also proved that a linear relationship exists between Monthly charges and Churn. Thus we can say, price sensitivity is a driver of churn which confirmed the hypothesis speculated in our business problem. 
5.	Price sensitivity is not the only driver of Churn. 
6.	It is possible to predict the likelihood of customers to churn using a Logistic regression model

### EVALUATION METRICS
- Accuracy
- Specificity
- Sensitivity

### MACHINE LEARNING
With the help of machine learning, customer churn across all industries can be predict with high accuracy, Thus, businesses can prevent losses and retain customers.
The accuracy of the model was 81% with high sensitivity and specificity as well indicating a good model.

