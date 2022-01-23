# Telco Customer Churn
## Business Understanding
How many customers left in the last month? What is the percentage?

What are the 3 services that are most signed up by customers?

Is there a relationship between the length of time a customer has stayed with the company and the total charges?

## Data Understanding
The Telco customer churn data contains information about a fictional telco company that provided home phone and Internet services to 7043 customers in California in Q3 (IBM Sample Data Sets).

Source Data: Online retail dataset by Kaggle. https://www.kaggle.com/blastchar/telco-customer-churn

The data set includes information about:
*  Customers who left within the last month – the column is called Churn.
*  Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.
*  Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges.
*  Demographic info about customers – gender, age range, and if they have partners and dependents.

Data Dictionary:
*  customerID : A unique ID that identifies each customer
*  gender : Whether the customer is a male or a female
*  SeniorCitizen : Whether the customer is a senior citizen or not (1,0)
*  Partner : Whether the customer has a partner or not (Yes, No)
*  Dependents : Whether the customer has dependents or not (Yes, No)
*  tenure : Number of months the customer has stayed with the company
*  PhoneService : Whether the customer has a phone service or not (Yes, No)
*  MultipleLines : Whether the customer has multiple lines or not (Yes, No, No phone service)
*  InternetService : Customer's internet service provider (DSL, Fiber optic, No)
*  OnlineSecurity : Whether the customer has online security or not (Yes, No, No internet service)
*  OnlineBackup : Indicates if the customer subscribes to an additional online backup service provided by the company (Yes, No, No internet service)
*  DeviceProtection : Indicates if the customer subscribes to an additional device protection plan for their Internet equipment provided by the company (Yes, No, No internet service)
*  TechSupport : Indicates if the customer subscribes to an additional technical support plan from the company with reduced wait times (Yes, No, No internet service)
*  StreamingTV : Indicates if the customer uses their Internet service to stream television programing from a third party provider (Yes, No, No internet service)
*  StreamingMovies : Indicates if the customer uses their Internet service to stream movies from a third party provider (Yes, No, No internet service)
*  Contract : Indicates the customer’s current contract type (Month-to-Month, One Year, Two Year)
*  PaperlessBilling : Indicates if the customer has chosen paperless billing (Yes, No)
*  PaymentMethod : Indicates how the customer pays their bill (Bank transfer (automatic), Credit card (automatic), Electronic check, Mailed check)
*  MonthlyCharges : Indicates the customer’s current total monthly charge for all their services from the company
*  TotalCharges : Indicates the customer’s total charges, calculated to the end of the quarter specified above
*  Churn : Indicates the customer left the company this quarter or not (Yes, No)

## Data Preparation
Packages: 
*  Pandas version 1.1.5
*  Numpy version 1.19.5
*  Matplotlib version 3.2.2
*  Seaborn version 0.11.2

## Data Cleansing
*  The TotalCharges column is categorical data. We will change the column to numerical data type because the column is a number in string, and for easy evaluation it must be changed to numerical data type.
*  There are 11 missing values, all of them for the TotalCharges column. We need remove records with missing values.

## Exploratory Data Analysis
### What are the 3 services that are most signed up by customers?
![image](https://user-images.githubusercontent.com/98216116/150687867-5898f5fc-c3eb-42c4-993b-a85c81b53425.png)

The most services that become customers are PhoneService with 6361, Multiple Lines with 2971, and StreamingMovies with 2732.

### How many customers who left in the last month? What is the percentage?
![image](https://user-images.githubusercontent.com/98216116/150687912-59884080-c068-4076-80a4-2b5b22589de8.png)

There were as many as 1869 customers who left or around 26.54%.

### Is there a relationship between the length of time a customer has stayed with the company and the total charges?
![image](https://user-images.githubusercontent.com/98216116/150688341-39bf756d-c264-4e93-a964-a2d9b796f31a.png)
![image](https://user-images.githubusercontent.com/98216116/150688378-61a60259-3100-46fe-a110-d0a8b546da0e.png)

Yes, because the tenure and TotalCharges columns have a correlation coefficient of 0.83, meaning that the longer the customer has stayed with the company, the greater the total charges paid by the customers.
