# Customer-Segmentation

## Introduction

“Customer segmentation is the compass that guides marketing endeavors, revealing the unique constellations within the vast galaxy of consumer diversity, allowing brands to navigate the cosmos of personalized engagement.”

Sprocket Central is an Australian company that sells bicycles, they have a list of one thousand new customers and want to determine which new customers to target marketing efforts.

Customer segmentation means dividing customers into groups with common attributes like demographics or behavior. These divisions (segments) help marketers and sales reps be more effective.

Companies need to identify target audiences for their product offerings, they target segments rather than a whole market to get better payoffs. Precision improves marketing with personalized messages, better conversions, lower costs, and higher ROI.

To collect transaction data
To calculate RFM scores
To carry out segmentation from RFM scores
To carry out segment analysis
To determine which customers to target from our new customer list
There are three datasets made available for this analysis;

The transactions table contains over 19,000 transactions from three states for 2017

The Customer demographic table contains information such as customer_id, first_name, last_name, gender, date of birth (DOB), job_title, job_industry_category, wealth_segment, owns_car.

The Customer Address table contains information such as customer_id, address, postcode, state, and country.

The New customer list contains all information in the customer demographic and address table but no customer_id since they are not registered customers.

The dataset was imported into the SQL server, a little data cleaning was carried out and additional fields such as the age and age_group needed for the analysis were added.

RFM analysis is a customer segmentation technique that evaluates customer behavior based on three key factors:

Recency (how recently a customer made a purchase)
Frequency (how often a customer makes purchases)
Monetary Value (the total amount a customer has spent).
By assigning scores to each factor, customers are divided into distinct segments. This approach enables businesses to gain insights into customer engagement, loyalty, and spending patterns, allowing for tailored marketing strategies, personalized communication, and effective targeting of promotions to different groups, ultimately enhancing customer relationships and driving business growth.

The tool used; Microsoft SQL Server, Microsoft Excel
