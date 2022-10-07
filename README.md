# Telco-Customer-Churn-Prediction-using-machine-learning-in-R
### PROJECT OVERVIEW
Customer churn is one of the most important metrics for a growing business to evaluate. It gives a company the hard truth about its customer retention. Customer churn is the percentage of customers that stopped using the company’s product or service during a certain time frame.

### BUSINESS PROBLEM 
The liberalization of the telecommunications market in Europe has led to significant customer churn. Therefore, it is important to diagnose the source of churning customers.

### PROJECT GOALS 
To build a predictive model that can identify customers who are likely to churn to enable the company employ adequate interventions that were geared towards reducing customers’ churn.
To confirm or reject one of the hypotheses under consideration that churn is driven by the customers’ price sensitivities and that it is possible to predict customers likely to churn by building a predictive model with the help of machine learning.

### EXPLORATORY DATA ANALYSIS
The data was explored using visualization and plots and the following insights were revealed:
- A linear relationship exists between tenure and monthly charges causing both to increase simultaneously.
- Customers with longer tenure are less likely to churn.
- Customers who churned paid higher Monthly Charges. The Lowest monthly charge shows high proportion of retained customers. This indicates that price sensitivity is one of the drivers of churn. However, customers with higher total charges tended not to churn.
- 73.46% of customers are active while 26.54% are churned customers which means only about a quarter of the population are churned customers.
- A higher percentage of the population are active customers and have partners, do not have dependents, are non-senior citizens, use a form of internet service, do not have online backup, do not have online security, do not have device protection, do not need tech support, do not stream movies, do not subscribe to streaming TV, have month to month contracts, prefer paperless billing methods and make use of any payment method.
- On the other hand, most churned customers do not have partners, do not have dependents, are non-senior citizens, use fiber optic internet service, do not have online backup, do not have online security, do not have device protection, do not need tech support, do not stream movies, do not subscribe to streaming TV, have month to month contracts, prefer paperless billing methods and electronic check payment method.

### RESULTS/FINDINGS
1.	The most important predictors of customers Churn in Telcos are Tenure, Monthly Charges and Contract. 
2.	Customers with longer tenure, more total charges, have partners, do not have dependents, online security, online backup and tech support, are non-senior citizens, use DSL internet service, montly contract, prefer paperless billing and any payment method are less likely to churn. 
3.	Customers with month-month contract, use fiber optic internet service, are more likely to churn meanwhile a large proportion of customers who churned did so in their first month.
4.	The Lowest monthly charge shows high proportion of retained customers. This indicates that price sensitivity may be a driver of churn.
5.	Statistical tests also proved that a linear relationship exists between Monthly charges and Churn. Thus we can say, price sensitivity is a driver of churn which confirmed the hypothesis speculated in our business problem. 
6.	Price sensitivity is not the only driver of Churn. 
7.	It is possible to predict the likelihood of customers to churn using a Logistic regression model

### EVALUATION METRICS
- Accuracy
- Specificity
- Sensitivity

### MACHINE LEARNING
With the help of machine learning, customer churn across all industries can be predicted with high accuracy, Thus, businesses can prevent losses and retain customers.
Different logistic regression models were built and their accuracies were as follows:
- Random Forest - 79.44%. The confusion matrix shows that the error rate was higher when predicting “Yes” than “No”.
- Generalized linear models: Model                 AIC value 
                             Model 1               4378.647
                             Model 2               4377.016
                             Model 3               4378.121
                             Model 4               4376.54
- Thus, Model 4 with the lowest AIC was selected. However, when used for prediction, the results of this model was 

            Accuracy : 0.7974 
            
            Sensitivity : 0.9575  
            
            Specificity : 0.3547  
- A Cross validation was then built using model 4 which yielded the following results

            Accuracy : 0.807
            Sensitivity : 0.9104          
            Specificity : 0.5214   
 - Therefore, the cross validation model was selected as the candidate model based on its performance when used for prediction.
