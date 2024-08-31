![image](https://github.com/user-attachments/assets/274b5eec-d43c-4ad8-b65c-493e2f4b6f8e)

# Churn Analysis of Databel

Databel is a fictional data provider, and this project focuses on analyzing the reasons behind customer churn.

## About the Dataset

The dataset contains 29 variables (columns) and 6,687 observations (rows).

### Customer Status

- **Customer ID**: Unique identifier for each customer.
- **Churn Label**: Indicates whether a customer churned ("Yes" or "No").
- **Churn Category**: Groups multiple churn reasons for analysis.
- **Churn Reason**: The specific reason why a customer ended their contract.

### Demographics

- **Gender**: The gender of the customer ("Male", "Female", or "Prefer not to say").
- **Age**: The age of the customer.
- **Under 30**: Indicates if the customer is under 30 ("Yes" or "No").
- **Senior**: Indicates if the customer is above 65 ("Yes" or "No").

### Contact Information

- **Contract Type**: Type of contract ("Month to Month", "One Year", or "Two Year").
- **Payment Method**: Preferred payment method ("Credit Card", "Direct Debit", or "Paper Check").
- **State**: The state code where the customer resides.
- **Phone Number**: The customer's phone number.
- **Group**: Indicates if the customer is part of a group contract ("Yes" or "No").
- **Number of Customers in a Group**: The number of customers in the group.

### Subscription Types and Charges

- **Account Length (in months)**: The number of months the customer has been with Databel.
- **Local Calls**: The amount of local calls (within the US) made by the customer.
- **Local Mins**: The number of minutes spent on local calls.
- **Intl Calls**: The amount of international calls made by the customer.
- **Intl Mins**: The number of minutes spent on international calls.
- **Intl Active**: Indicates if the customer made international calls ("Yes" or "No").
- **Intl Plan**: Indicates if the customer has a premium international calling plan ("Yes" or "No").
- **Extra International Charges**: Additional charges for international calls for customers not on a plan.
- **Customer Service Calls**: The number of calls made to customer service.
- **Avg Monthly GB Download**: Average monthly download volume in gigabytes.
- **Unlimited Data Plan**: Indicates if the customer has an unlimited data plan ("Yes" or "No").
- **Extra Data Charges**: Additional charges for data downloads for customers without an unlimited plan.
- **Device Protection & Online Backup**: Indicates if the customer has paid for device protection and backup ("Yes" or "No").
- **Monthly Charges**: The average monthly charges for the customer.
- **Total Charges**: The total sum of all monthly charges.

## Data Preparation

### Initial Data Check

- All variables were checked for correct data types and duplicates. No duplicates were found.
- The main dataset was copied to a new worksheet named "Aggregate" for further analysis.

### Churn Rate Calculation

- A new column named "Churned" was created based on the "Churn Label" column, where "Yes" was converted to 1 and "No" to 0 using the `IF` function in Excel.
- Churn rate was calculated by dividing the sum of churned customers by the total number of customers, resulting in a churn rate of 26.86%.

![Churn Rate Calculation](https://github.com/user-attachments/assets/ae7885cc-1e73-46e9-99be-94f085279493)

### Analyzing Churn Reasons

- A pivot table was created from the "Customer" worksheet to analyze churn reasons by summing the "Churned" values for each reason.

![Churn Reason Analysis](https://github.com/user-attachments/assets/fb86184f-fe5c-4255-8e6f-9534f96c48e8)

### Churn Competitor Preferences

- A competitor analysis was conducted to identify the top 4 reasons customers preferred other companies: better devices, better offers, higher download data, and more data offered.

![Competitor Preferences](https://github.com/user-attachments/assets/26e7d250-92cb-4f78-9b59-496d849d66ea)

### Examining Churn Patterns

- Data consumption patterns were examined based on the data plan using a pivot table.

![Data Consumption Patterns](https://github.com/user-attachments/assets/a42ba6c6-b18e-405a-a803-6d713d0afcb7)

### Age Analysis

- A new column categorizing customers into "Under 30", "Senior", and "Other" based on their age was created using the `IF` function.
- A pivot table indicated that most churn occurs among "Senior" customers.
- Further analysis grouped customers by age ranges of 10 years, revealing the highest churn rate in the 79-88 years old range.

![Age Analysis](https://github.com/user-attachments/assets/f8b746cb-8941-48bf-b6a8-60a82bede22c)
![Age Range Analysis](https://github.com/user-attachments/assets/0b32a851-2738-4cb6-8291-7d2355525d12)

### State Analysis

- Churn rates by state were analyzed based on the international plan, with California showing the highest churn.

![State Analysis](https://github.com/user-attachments/assets/6abba57f-9caa-42a8-aaf2-432d164b0e4b)

## Dashboard

- A comprehensive dashboard was created in Excel summarizing the findings from the analysis.

---

This project aimed to provide insights into customer churn patterns at Databel. The results can help guide strategies to reduce churn and improve customer retention.














