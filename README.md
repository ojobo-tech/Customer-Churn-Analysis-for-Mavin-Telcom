Customer Churn Analysis Using SQL
Why are customers leaving Maven Telecom?

The telecom industry is highly competitive, and customers have a wide selection of options to choose from. Companies rely heavily on customer retention to ensure continued growth and success. However, losing customers, also known as churn, is inevitable in any industry. As a data analyst on this project, my job is to provide an in-depth analysis of Maven Telecom's churn dataset and to answer the following questions:

1. What are the key drivers of churn?
2. What is the ideal profile of a churned customer?
3. What steps can Maven Telecom take to reduce churn and retain customers?

Project Strategy
I downloaded the dataset from Maven Analytics and it contained information about customer demographics, subscription plans, and account records for Maven Telecom. I performed all data preparation and analysis using SQL (MySQL), and all the SQL codes will be provided below. The visualizations and dashboard were designed with MS PowerBI and Figma respectively.

Project Steps:
1. Data Cleaning and Processing
2. Exploratory Data Analysis
3. Building the Ideal Churn Profile
4. Data Insights
5. Customer Retention Strategies
6. Data Visualisation

Data Cleaning and Processing
This dataset is bound to have null values because all customers have unique combinations of subscription preferences. Therefore, the presence of null values in my analysis is a deliberate and informed decision that allows me to provide a more complete understanding of Maven's customer base.
I checked for duplicate values in the unique key (Customer_ID), and found none.


Analysis
#1. Exploratory Analysis
1a. Total Number of Customers
The analysis showed that there are 7043 customers in total.

1b. How many customers were lost to churn?
Maven lost 1869 customers which accounted for 26.5% of the total customers within the period this data was recorded. It's a pretty significant figure and we'll investigate why they're leaving later on in this article.

1c. How much revenue was lost to churned customers?
Out of the $21.3m revenue recorded, Maven lost $3.7m to churned customers and they accounted for 17% of Maven's total revenue.

1d. What's the typical tenure for churned customers?
To find out how long customers typically stay at Maven before leaving, I used the CASE statement in SQL. The CASE statement creates a derived column (Tenure) and groups customers who leave the company in 12 months or less as '12 months' etc.
I found that ~42% of churned customers spent 6 months or less at Maven before leaving.
Almost half of the customers who churned had a relatively short tenure with the company, so there are opportunities for Maven to improve customer retention among newer customers.

1e. What Payment method did the churned customers use?
71.1% of the churned customers use Bank Withdrawal as their method of payment for services to Maven Telecom. Could this be a reason for the churn rate? We will investigate further.


2. Demography of Churned Customers.
These are the key insights based on the demography of our churned customers.

2a. What is the Gender of the Churned Customers?
Of the 1869 customers lost to churn, 939 customers which account for 50.2% of churned customers are Female.

2b. What is the Marital Status of the Churned Customers?
1200 customers which account for 64.2% of the 1869 customers lost to churn customers are Single.

2c. What is the Age Category of the Churned Customers?
Compared to the other age categories, 25.6% of the churned customers are between the ages of 40–55 years, while 24.3% are between the ages of 25–40 years. This signifies that the majority of the churn experienced came from customers in their middle age.

2d. Which cities had the highest churn percentage?
San Diego had the highest churn percentage at 9.9%, accounting for 185 churned customers from the cities where Maven has customers.


3. Service Used by Churned Customers

3a. What internet type did churners have?
66% of all churned customers used Fiber Optic. While ~70% of customers who left for competitors also used Fiber Optic. Maven should review the quality and service of their Fiber Optic internet, as this could be the reason customers are leaving for competitors.

3b. What contract was churners on?
Almost all churned customers (89%) were on a month-to-month contract.
This shows that customers on a month-to-month contract are more likely to churn, as they have greater flexibility to cancel or switch providers without incurring any penalty.

3c. What promotional offers did churned customers have?
56% of churners did not get any promotional offer while 23% had Offer E. Offers are a great way to reward and retain your loyal customers.

3d. Did churners get premium tech support?
77% of churned customers did not have premium tech support. It's possible that this service could have improved their after-sales experience and reduced churn.


4. General Reasons for Churn

4a. What Category produced the most churn?
45% of churned customers stated 'Competitor' as their reason for leaving. It's interesting to note that a significant number of customers (17.2%) left due to dissatisfaction and (16.8%) left due to the attitude of the support staff. Maven also lost about $1.7 million to Competitors, making it the most expensive type of churn.

4b. Why did Customers leave Maven Telecom?
Of the total churn experienced, 16.7% of customers left because the 'competitor had better devices', 16.6% left because the 'competitor made a better offer', and 11.8% left because of the 'attitude of support staff'.

4c. Why did Maven lose customers to competitors?
Of the 45% of customers that left to a competitor, 37.2% of customers left because the 'competitor had better devices', 37% left because the 'competitor made better offer', 14% left because the 'competitor offered more data' and 12% left because the 'competitor offered better download speeds'.


5. The key churn indicators are therefore:

Contract: 89% of churned customers were on the month-to-month contract
Premium Tech Support: 77% of churners did not have premium tech support
Internet Type: 66% of churners used Fiber Optic internet
Offer: 56% of churners did not have any promotional offers, while 23% had Offer E.
Competitor: 45% of churners moved to competitors.

6. The ideal churn customer profile

I built a simple churn profile with Figma with the key churn indicators I discussed in previous sections, and the churn demographic results below:

25.6% of churned customers are between 40–55 years old

~50% of churned customers are Female

64% of churned customers are Single

94% of churned customers have no dependents in their household; it's possible they have more flexibility and fewer commitments, making it easier for them to switch providers or cancel their subscriptions.


7. Key Insights from the Analysis

Maven has 1869 churned customers, which accounted for $3.7m of total revenue lost.

42% of churned customers only stayed for 6 months or less.

The top 3 reasons for churn are competitors made better offers, competitors had better devices and attitude of support staff.

Maven lost ~$1.7 million to competitors, making it the most expensive type of churn

The key indicators of churn are Month-to-Month contract type, No Premium Tech Support, Fiber Optic internet, No promotional offer, and Offer E.
70% of customers who churned to competitors used Fiber Optic, 56% received no promotional offer, 89% are on a month-to-month contract

8. Customer Retention Strategies

Loyalty Programs: Since the top reason for churn is 'competitors making better offers', and more than half of churned customers did not have any promotional offers, Maven could implement different loyalty programs to retain their customers. For instance, they could reward customers on long-term contracts with discounted rates, free upgrade, or additional features.

Improve Customer Support: Invest in training and development of support staff to ensure they provide excellent customer service. This could include regular coaching and feedback sessions, as well as incentives for staff who receive positive customer feedback.

Make better devices: Evaluate the features, performance, and pricing of your devices to ensure they are in line with market standards and demand.
Premium Tech Support: Since customers who did not have access to premium tech support were more likely to churn, Maven should consider offering this service to all customers.

Improve Fiber Optic Service: Invest in improving your Fiber Optic offerings like faster speeds, more stable connections, and better customer support for Fiber Optic customers.

Engage High-Value Customers: Prioritize engaging these customers to prevent them from leaving. Provide personalized offers, send targeted communications, and provide premium tech support to ensure these customers remain satisfied with their service.

After-Sales Service: Schedule regular check-ins with customers to ensure they are still satisfied with their service. These check-ins could be in the form of surveys, phone calls, or email communications.
