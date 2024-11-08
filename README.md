# LITA_CAPSTONE_PROJECT_CUSTOMER_DATA
This is my capstone project on Customer Data while I was learning Data Analysis with the Incubator Hub 

### Project Title: Customer Segmentation for a Subscription Service

[Project Overview](#project-overview)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

[Results](#results)

[Recommendation](#recommendation)

### Project Overview
---
The primary aim of this project is to analyze customer data collected over a period of a year and 8 months for a subscription service in order to identify trends and gain insight into customer behaviour and subscription patterns(cancellations and renewals).

### Tools Used
---
- Microsoft excel for data cleaning, analysis and data visualization
- SQL- Structured Query Language for Data Query
- PowerBI for Data cleaning and data visualization
- Github for Portfolio Building

### Data Cleaning and Preparation
---
In the initial phase of data cleaning and preparations, we performed the following actions;
- Data Loading and Inspection
- Handling Missing Variables
- Handling duplicates
- Data cleaning and formating

### Exploratory Data Analysis
---
This step involved the exploration of our dataset to answer some questions such as;
- Most Popular Subscription Type
- Overall Subscription Pattern
- Subscription and Cancellations

### Data Analysis
---
These are some queries/lines of codes and functions used during the analysisof the data;
```SQL
select top 1 subscriptionType,count(customerid) as total_customers
from [dbo].[Customer Data] group by subscriptiontype
order by total_customers desc 

select sum(case when canceled = 0 then 1 else 0 end) 
as active_subscriptions,
sum(case when canceled = 1 then 1 else 0 end) 
as canceled_subscriptions from [dbo].[Customer Data]

=INDEX(Table3[SubscriptionType],MODE(MATCH(Table3[SubscriptionType],Table3[SubscriptionType],0)))
```
### Data Visualization
---
![Customer Data Pivot](https://github.com/user-attachments/assets/ee9e7f53-94b1-415b-baa9-b40a012e3e15)

![customer data sql](https://github.com/user-attachments/assets/f8b3b538-022a-40ed-bb1c-4042b13af551)

![top3 region by sub cancellations](https://github.com/user-attachments/assets/15f4345d-736d-48f5-8a1d-2e06b760256f)

![active and canceled sub](https://github.com/user-attachments/assets/ded65e83-6672-42e8-90d9-322f77f91a18)

![Customer Data Visual](https://github.com/user-attachments/assets/3a2fe616-c714-4ac9-830e-8fe69b5affd6)

### Results
---
Based on the analysis, the following insights were drawn:
1. Active subscriptions were 18,612 with a total of 3,437 subscriptions more than that of the canceled subscriptions(15.175)
2. The eastern region had the highest amount of active subscriptions of 8,488 and no canceled subscrriptions
3. The North had the  highest amount of canceled subscriptions (5,067) a value which when compared to that of the other regions was statistically non-significant 
4. Basic subscription is the only type of subscription used by those in the East and North, Premium subscription type in the South and standard subscription type in the west.
5. The East generated the highest revenue ($16,958,763)
6. Basic subscription type generated the highest revenue with a value of $33,776,735 occupying almost half of the total revenue.

### Recommendation
---
- Other subscription types should be introduced to other regions to reach more customers and generate more revenue
- Emphasis should be placed on the eastern region 












