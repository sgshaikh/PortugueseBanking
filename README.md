
Python Code Link:https://github.com/sgshaikh/PortugueseBanking/blob/main/PortugueseBanking_Classification.ipynb


1) Business Problem
A Portuguese banking institution has data on its existing customers. The objective is to use data collected on customer demographics, previous campaign interactions and existing accounts with the bank to predict if the customer will subscribe to a term deposit

The bank will want to determine if it is worthwhile to spend money and resources on trying to sell a banking product to the client. Having a model with high ROC can be very profitable for the bank.


2) Data Interpretation and Description

The features of the dataset can be devised into several  categories:

Demographics of the banking client: Age, Job, Marital Status, Education Level
Credit Information of the banking client: Has defaulted in the past, has a home loan, Has a personal loan
Features about previous marketing outreach: contact type, contact day/month/date/duration, # of previous contacts, outcome of previous contact
 

There are 45210 rows with no NULL values and the distribution of the target variable is highly skewed

no 0.883015 yes 0.116985

A pair plot yielded some information about the relationship between features. Not all features look to be good predictors of outcome


3) Findings from the comparison of different models

After comparing SVM, KNN, Logistic Regression and Decision Trees by using GridSearchCV to tune their hyper parameters the best model came out to be:

LogisticRegression
C (regularization strength): 1
penalty: 'l2'

Model Performance for the best model is
Test Precision: 0.3325942350332594
Test Recall: 0.6474820143884892
Test ROC AUC Score: 0.7811787899996744



4) Next steps and recommendations 

Since the variable being predicted is highly skewed, logistic regression performed really well. Since it can cost a lot of money for the bank to do an outreach to a customer, as next steps I would tune the features to increase the precision of the model. 

Since this is a regression model, the output probabilities can be looked at and a cut off can be determined based on cost of outreach to find the appropriate number of customers to do outreach.


The model shows that the available data can fairly accurately predict which customers have a higher likelihood to subscribe to a term deposit. 