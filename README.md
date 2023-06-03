# Health-insurance-cross-sell-prediction
Our client is an Insurance company that has provided Health Insurance to its customers now they need your help in building a model to predict whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.

An insurance policy is an arrangement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee. Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called ‘sum assured’) to the customer.
## Objective
Building a model to predict whether a customer would be interested in Vehicle Insurance or not. It will be extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

### Data Description

The Dataset used for the analysis includes the following columns:

id : Unique ID for the customer

Gender : Gender of the customer

Age : Age of the customer

Driving_License : 0 - Customer does not have DL,1 - Customer already has DL

Region_Code : Unique code for the region of the customer

Previously_Insured : 1 - Customer already has Vehicle Insurance, 0-Customer doesn't have Vehicle Insurance

Vehicle_Age : Age of the Vehicle Vehicle_Damage : 1 - Customer got his/her vehicle damaged in the past. 0 -Customer didn't get his/her vehicle damaged in the past.

Annual_Premium : The amount customer needs to pay as premium in the year

PolicySalesChannel : Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.

Vintage : Number of Days, Customer has been associated with the company

Response : 1 - Customer is interested, 0 - Customer is not interested
## Approach 
In this project, these are the steps that we followed:
step 1 - Data loading
step 2 - Data cleaning and data wrangling
step 3 - Exploratory data analysis (univariate, Bivariate and multivariate analysis)
step 4 -  Performed one hot encoding, Response coding for categorical feature and Normalization, Standardization for numerical data.
step 5 - Model training with hyperparameter tuning.
step 6 - Saving the model using joblib
### conclusion
For determining the cross sell Prediction we started with the exploratory data analysis , data transformation, and then model training. The following conclusion were made from this project is:

The features like driving_license, previously_insured, vehicle age of particular category were found common in customers who responded positively. Like (customers having driving license, not previously_insured, vehicle age in 1-2 years are responded positively about vehicle_insurance)
There are few policy_sales_channel (26,124,52) and Region_code (28,8,46) have many positive respondent and most of other have very few.

From model training:
The best performing model is RandomForestClassifier with hyperparameters (max_depth = 10, n_estimators = 200, min_samples_split = 100). Although the train score of all the models are almost similar but test score observe was best for RandomForest classifier.
Random Forest predicts : out of total 195381 total test points, the 153279 predicted value are true making the accuracy of 78.45% with precision of 71.6.
