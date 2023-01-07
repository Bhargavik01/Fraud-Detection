# Fraud-Detection
Transaction Fraud Detection
There is a shortage of publicly available datasets on financial services, particularly in the emerging mobile money transactions domain. This is a problem for researchers, including those studying fraud detection, as financial datasets are important resources. One reason for the lack of public datasets is the private nature of financial transactions.

The goal of this analysis is to create a generalized model for predicting imbalanced big data that can be applied in real-world situations. PySpark was used to handle the large data aspect of the problem.

The data was downloaded from [here](https://www.kaggle.com/datasets/chitwanmanchanda/fraudulent-transactions-data)

Column names:
* step - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).
* type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
* amount - amount of the transaction in local currency.
* nameOrig - customer who started the transaction
* oldbalanceOrg - initial balance before the transaction
* newbalanceOrig - new balance after the transaction
* nameDest - customer who is the recipient of the transaction
* oldbalanceDest - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).
* newbalanceDest - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).
* isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.
* isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200,000 in a single transaction.
The structure of the notebook is borrowed from here, which used pandas and sklearn to conduct the fraud detection.



process:

+ Data understanding using PySpark
+ Data conversion and feature enginnering
+ Data stratified splitting and Model building
+ Model evaluation
+ sampling techniques to handle unbalanced data
+ Performance over data scale

