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

### Tenure and Demographics of Churned Customers

I decided to conduct an in-depth analysis at Databel, starting with identifying the commercial age (Tenure) of our customers. Initially, I calculated customer tenure by subtracting the monthly fee from the annual fee to estimate how long they had been using the service. This calculation was performed on both monthly and yearly bases. If a customer had not completed one year, their Tenure was set to 0; otherwise, the total duration was divided by 12 to compute their Tenure in years.

<img width="870" height="284" alt="image" src="https://github.com/user-attachments/assets/82a02e56-71d0-499c-9aa6-c3ee96cdee49" />


According to the annual Tenure calculations, nearly half of the customers who had not completed one year ended up churning. However, after the second year, churn rates gradually decreased and continued to decline until the seventh year.




When analyzing the distribution, we observed that 34% of customers left before completing their first year. This group is followed by those who completed their 3rd year, 6th year, 2.5 years, and 4th year. The primary reasons for customer churn were competitor offers, negative customer experiences (attitudes), and dissatisfaction.

Most of the churned customers were non-citizens over the age of 30. This suggests that communication strategies and customer experience touchpoints may need to be re-evaluated. Among those who didn’t complete a full year, the majority were again non-citizens and over 30 years old. The data also shows that 73% of those who didn’t complete one year and 62% of those who completed their 6th year churned.

<img width="728" height="639" alt="image" src="https://github.com/user-attachments/assets/9f370cec-94d4-40fa-86b0-57c57ae5e281" />

<img width="785" height="308" alt="image" src="https://github.com/user-attachments/assets/4d8beace-2c2d-4a16-8930-67f5d789260f" />

The main reasons non-citizens over 30 left the service were better offers from competitors, dissatisfaction, and negative experiences with staff. Within this group, the leading complaint was that competitors provided better devices. Most of these customers used debit cards for payments and contacted customer service more frequently than the average. This might indicate that they experienced more problems and didn’t receive adequate support, particularly related to billing or technical issues.

<img width="788" height="450" alt="image" src="https://github.com/user-attachments/assets/362a1518-b5cc-47ef-9898-7bb86e83794a" />


This group also had the highest churn rate among those on monthly contracts. Their usage data shows that they often lacked a dedicated support team to solve their issues, and their primary needs were related to internet data packages.

**Two-Year Tenure and Churn Reasons**

For customers with two years of tenure, the top reason for churn was competitors, followed by negative attitudes and dissatisfaction. Based on these insights, if Databel addresses internal personnel issues, offers competitive internet packages, and provides new devices, it could significantly improve satisfaction among non-citizens and customers over 30.

### Senior Segment (Citizens) Analysis

<img width="801" height="43" alt="image" src="https://github.com/user-attachments/assets/43ac583c-093e-44ff-a33e-d24212012840" />
<img width="894" height="758" alt="image" src="https://github.com/user-attachments/assets/0efbe47e-fd78-426c-91fb-c53927fef580" />

Among senior customers (citizens), the churn rate was 38%. Interestingly, churned customers in this segment spent approximately 20% more than those who remained. The top churn reason was again competitors, followed by the company's attitude. Most complaints in this group were related to better offers from other providers.

<img width="795" height="467" alt="image" src="https://github.com/user-attachments/assets/fcdb4567-bc8c-409c-a7e1-12560f28304b" />
<img width="796" height="309" alt="image" src="https://github.com/user-attachments/assets/7bb9eecd-bd6a-4af2-bc64-a611f5531ff3" />


A deeper analysis revealed that the core problems stemmed from the behavior of customer service and sales representatives, as well as the company's pricing policies. The most churned customers were those with monthly contracts. Moreover, customers who were involved in more than one group or plan were less likely to churn.

<img width="1481" height="42" alt="image" src="https://github.com/user-attachments/assets/570c521f-bb74-4fd2-8bf8-73361ea69b4e" />


In this segment, churned customers had higher average local and international call minutes than other demographics. This group also had the highest churn rate overall.

### Customers Under 30

<img width="1240" height="47" alt="image" src="https://github.com/user-attachments/assets/885415e6-cf3a-4d6d-ad96-a5dbebedf9f5" />
<img width="969" height="140" alt="image" src="https://github.com/user-attachments/assets/c91f5da5-2c87-4b20-a2d8-9abbee2b2982" />

The segment with the lowest churn rate consisted of customers under 30 years old. Within this group, the average age of churned users was around 25. Those who left the service in their second year had the highest average extra data usage, while those who left in their sixth year had the highest spending costs.

<img width="1715" height="40" alt="image" src="https://github.com/user-attachments/assets/a8e317e4-756f-49e0-afd2-467dde9d4006" />

Compared to other segments, this group downloaded approximately three times more data. It also ranked second, after the senior segment, in terms of average local call duration.



## Dashboard

- A comprehensive dashboard was created in Excel summarizing the findings from the analysis.

<img width="1792" height="590" alt="image" src="https://github.com/user-attachments/assets/9c6a1db6-5308-4585-a107-c3e37f79ff3e" />

<img width="1483" height="507" alt="image" src="https://github.com/user-attachments/assets/2086d4cb-c294-4f20-8341-c29addc40c8a" />

<img width="1704" height="603" alt="image" src="https://github.com/user-attachments/assets/4e25d7db-b24c-4edb-b253-761cbfa956b8" />

<img width="1528" height="510" alt="image" src="https://github.com/user-attachments/assets/a3e856f0-df7c-44eb-bfa5-1da5526574d3" />

---

This project aimed to provide insights into customer churn patterns at Databel. The results can help guide strategies to reduce churn and improve customer retention.














