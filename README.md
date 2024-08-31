![image](https://github.com/user-attachments/assets/12d4362d-b9ef-4f82-a3ac-3569e2dccc05)


# Churn_Analysis_of_Databel
Databel is fictional data provider.
My task is to analyze why customers are churning.

## About the Dataset

Dataset contains 29 variables(columns) and 6687 Observations(rows).

### In terms of Customer Status:

Customer ID: The unique ID that identifies a customer.

Churn Label: Contains “Yes” or “No” to indicate if a customer churned.

Churn Category: Groups multiple churn reasons together for analysis purposes.

Churn Reason:  The particular reason why the customer ended the contract. 

### In terms of Demographics:

Gender: The gender of the customer, indicated by “Male”, “Female”  
or “Prefer not to say”.

Age: The age of the customer.

Under 30: Indicates if the customer is under 30 with “Yes” or “No”.

Senior: Indicates if the customer is above 65 with “Yes” or “No”.

### In terms of Contact Informations:

Contract Type: Contains “Month to Month”, “One Year” or “Two Year”.

Payment Method: Preferred payment method of the customer indicated
with “Credit Card”, “Direct Debit” or “Paper Check”.

State: The code of the state where the customer lives.

Phone Number: Phone number of the customer.

Group: Indicates if the customer is part of a group contract. A group
contract offers advantages and is generally cheaper.
Contains “Yes” or “No”.

Number of customers in a group: Number of customers part of the group.

### Subscription Types and Charges:

Account Length (in months): The number of months the customer has been with
Databel.

Local Calls: Amount of local (within the US) calls from the customer.

Local Mins:The number of minutes spent calling locally.

Intl Calls:Amount of international (outside the US) calls from
the customer.

Intl Mins:The number of minutes spent calling internationally.

Intl Active: Indicates if the customer called internationally with a “Yes” or “No”.

Intl Active: Indicates if the customer called internationally with
a “Yes” or “No”.

Intl Plan: Indicates if the customer has a premium plan to call internationally for free with “Yes” or “No. This
premium is reflected in the amount of the monthly charge.

Extra International Charges: Contains the extra charges for international calls
for customers who are not on an international plan.

Customer Service Calls: The number of calls made to customer service. 

Avg Monthly GB Download: Contains the average monthly download volume in
gigabytes.

Unlimited Data Plan: Indicates if the customer has free unlimited download capacity with “Yes” or “No”. This premium
is reflected in the amount of the monthly charge.

Extra Data Charges: Contains the extra charges for data downloads for customers who are not on an unlimited plan.

Device Protection  & Online Backup: Indicates if the customer has paid for device
protection and backup with Yes or No .

Monthly Charges: Average of all Monthly Charges to the customer.

Total Charges: Sum of all monthly charges.

## Data Preperation

In first phase, i controlled all variables in term of variable types and chech for duplicates. In the end of this process it has no Duplicates.
Therefore, i copy main table to new worksheed that is called "Aggregate".

To ease my process and calculate all churned customers, i create new variable(columns) called "Churned" based on Churn Label by IF function in Excel from "Yes" to 1 and "No" to 0 values.
![image](https://github.com/user-attachments/assets/19281bc8-049e-4934-8a49-5b1b684ac95f)
IF function is "EĞER" in Turkish.


### Churn Rate
To find churn rate first i count all customers in first column, in second column i sum all churned value from "Churned" column.Lastly, i divide second column to first column.The result is 26.86%

![image](https://github.com/user-attachments/assets/ae7885cc-1e73-46e9-99be-94f085279493)



### Churn Reason
In terms of investigating churn reasons, pivot table from Customer Worksheet is created.As a row Churn reason and as a value sum of "Churned" are choosed.

![image](https://github.com/user-attachments/assets/fb86184f-fe5c-4255-8e6f-9534f96c48e8)

### Churn Competitor Preferences

In order to find why customers choose other companies, Competitor analysis is made and only top 4 reasons is choosed which are better devices,beter offer,higher download data and offered more data.
![image](https://github.com/user-attachments/assets/26e7d250-92cb-4f78-9b59-496d849d66ea)

### Examining Churn Pattern

Next, to make investigation one step further, i examine consumption of data based on Data plan by using pivot table.

![image](https://github.com/user-attachments/assets/a42ba6c6-b18e-405a-a803-6d713d0afcb7)

### Age 

In age,first of all i create new column by 3 categories base on their age. If someone's age below 30, ıt is labelled as "Under 30",above 65 is labelled as "Senior" and between 30 and 65 Labelled as "Other" in Demographics column in Aggregate worksheet. I use If function to create labels.In the end, pivot table indicates that most of churn occures in "Senior".

![image](https://github.com/user-attachments/assets/f8b746cb-8941-48bf-b6a8-60a82bede22c)
![image](https://github.com/user-attachments/assets/6cc48751-2cfd-49b0-84e0-1e5d4dcaa051)

Based on first information, i grooped ages by 10 years range by using pivot table.In the end, pivot table showed the most churned age range is 79-88 years old.
![image](https://github.com/user-attachments/assets/0b32a851-2738-4cb6-8291-7d2355525d12)


### State

To investigate churn rate in State based on Intl plan, i created pivot table and sorted by decreasing.The graph displays the most churn occured in California.

![image](https://github.com/user-attachments/assets/6abba57f-9caa-42a8-aaf2-432d164b0e4b)


## Dashboard

In the end of investigation, i created dashboard using Excel.













