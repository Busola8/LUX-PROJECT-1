# LUX-PROJECT-1
PREDICTION STEPS
Churn has to do with  how frequently users of a product or service stop using it after a certain amount of time has passed. The Customer churn, sometimes referred to as customer turnover, is an important sign of a company's ability to keep clients, and it's crucial in sectors like telecoms, subscription services, and retail where customer connections are continuous.


Solution:
This project tries to predict churn in the telecom industry starting with the features that fundamentally contribute to the churn rate such as, demographics (gender,senior citizens),internet usage (streaming TV,streaming movies,internet service), billing information (monthly bill, paperless billing, total charges),tech support
Using previously availble data and model,we obtain meaningful information concerning the churn rate.
In the solution below, i made use of LightGBM and XBOOST, as well as LogisticRegression as models with XBOOST having the highest accuracy
The reason for that many models is simply to compare accuracy results and get the best possible predictions.
The step are as follows:

Step 1:Data collection
We need to obtain historical data on customers such as tech support, home data usage(streaming TV, streaming movies, internet service),billing details(monthly payment, total payment), demoraphics(age,senior citizen),contract duration(one year, month to month).

Step 2:Data preprocessing
next we preprocess the data properly in terms of missing values, dealing with categorical data, dummy variables.
Step 3:Feature Engineering
Here we identify the best features for the prediction using algorithms such as 
Mutual Information-based Selection: Mutual information measures the dependency between variables and can be used for feature selection.
Feature Importance-based Selection: This involves using an ensemble model (like a Random Forest) to determine feature importance and selecting the most important features
Correlation-based Feature Selection: This technique involves selecting features that have a high correlation with the target variable ("Churn" in this case)
Recursive Feature Addition (RFE): RFE works by recursively removing the least important features based on a model (e.g., a classifier) and selecting the most important features
Acculmulated selected features from these algorithms:
StreamingTV,TechSupport,Partner,PaymentMethod,SeniorCitizen,DeviceProtection,StreamingMovies,OnlineBackup,TotalCharges,Dependents.

Step 4:Model training:
I made use of LightGBM and XGBOOST, as well as LogisticRegression as models with XBOOST having the highest accuracy
The reason for that many models is simply to compare accuracy results and get the best possible predictions as they are all powerfull tools that can handle complex data.

Step 5:Model Training:
Here we split the data set to prevent overfitting the model using train test split. This helps the model to have high accuracy in real life predictions.

Step 6:Model Evaluation:
After obtaining information from the model we can now draw assumptions based on accuracy score and prediction scores and others.
The company can use the model to predict real life data and obtain information about customer churn in the future.

RESULTS FROM THE CODE BELOW:
More of the customers did not churn at this company with non churn customers being 5174 and churn customers as 1869 of the values. Sprint will be able to use this information for future predictions and target the proper age demographics(age, senior citizen), and improve customer service with information from tech support as well as better service quality in terms of billing. This offers better general communication and relationship with clients.

Model accuracy from XGBOOST:
ROC-AUC Score: 0.7231138706654171
Precision Score: 0.6652173913043479
Recall Score: 0.5454545454545454
F1 Score: 0.5994123408423115
F2 score of XGBoost Classifier: 0.8064363464268812.
Accuracy Score: 0.8064363464268812.

Model Accuracy from LightGBM:
ROC-AUC Score: 0.7185070841832516
Precision Score: 0.6544276457883369
Recall Score: 0.5401069518716578
F1 Score: 0.591796875
F2 score of LGBM Classifier: 0.8021769995267393.
Accuracy Score: 0.8021769995267393



Also from the results we can gather information about male being more than females and most common modes of payment where it was electronic mode so the company can improve its online user operations for the ease of the customers. 
In the churn and contract contrast, people with month to month contract being the most common also had the highest churn rate and information about the age demographics for targeted marketing towards younger people as they are more in comparism to the senior citizens. 

