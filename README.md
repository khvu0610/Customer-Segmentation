# Customer-Segmentation

## Introduction

“Customer segmentation is the compass that guides marketing endeavors, revealing the unique constellations within the vast galaxy of consumer diversity, allowing brands to navigate the cosmos of personalized engagement.”

Sprocket Central is an Australian company that sells bicycles, they have a list of one thousand new customers and want to determine which new customers to target marketing efforts.

Customer segmentation means dividing customers into groups with common attributes like demographics or behavior. These divisions (segments) help marketers and sales reps be more effective.

Companies need to identify target audiences for their product offerings, they target segments rather than a whole market to get better payoffs. Precision improves marketing with personalized messages, better conversions, lower costs, and higher ROI.

**To collect transaction data**

**To calculate RFM scores**

**To carry out segmentation from RFM scores**

**To carry out segment analysis**

**To determine which customers to target from our new customer list**

There are three datasets made available for this analysis;

The **transactions** table contains over 19,000 transactions from three states for 2017

The **Customer demographic** table contains information such as **customer_id, first_name, last_name, gender, date of birth (DOB), job_title, job_industry_category, wealth_segment, owns_car**.

The **Customer Address** table contains information such as **customer_id, address, postcode, state, and country**.

The **New customer list** contains all information in the customer demographic and address table but no customer_id since they are not registered customers.

The dataset was imported into the SQL server, a little data cleaning was carried out and additional fields such as the age and age_group needed for the analysis were added.

RFM analysis is a customer segmentation technique that evaluates customer behavior based on three key factors:

**Recency** (how recently a customer made a purchase)

**Frequency** (how often a customer makes purchases)

**Monetary** Value (the total amount a customer has spent).

By assigning scores to each factor, customers are divided into distinct segments. This approach enables businesses to gain insights into customer engagement, loyalty, and spending patterns, allowing for tailored marketing strategies, personalized communication, and effective targeting of promotions to different groups, ultimately enhancing customer relationships and driving business growth.

The tool used: **Microsoft SQL Server, Microsoft Excel**

## Analysis and Results
I began by creating the foundations of this work, our customer segments. A total of ten customer segments were created for two reasons;

Increasing the precision of the results can lead to more precise targeting and personalization of marketing efforts.

A higher number of segments captures a wider range of customer behaviors, preferences, and needs.

The ten segments are;

**customer** — these are average customers.

**one time customers** — these are customers that made one purchase a long time ago.

**active loyal customers** — they are our customers that make good purchases frequently and have a good recency score.

**slipping best customer** — they are the best customers that have not made any purchase recently.

**Potential customers** — they are customers who made a big purchase recently.

**best customers** — they are the perfect customers with a high frequency of purchases, they have purchased recently and purchased a lot.

**churned best customer** — they are the best customers who have not made any purchases for a long time and churned.

**new customers** — they have made a very recent purchase and have a low-frequency score.

**lost customers** — they are normal and loyal customers who have not made any purchases in a very long time.

**declining customers** — they are customers who have not made a purchase recently.

These segments can be defined in any manner based on what a company is looking to identify.

![Customer Count by Segments.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Customer%20Count%20by%20Segments.png)

n this section, I dived deeper to understand the characteristics and traits, as well as purchase patterns of the segments created, this gives us insights into our marketing strategy.

For the purpose of this analysis, I will only be working with three segments; the best customers, active loyal customers, and customers.

To understand our segments better, I will look at their characteristics in terms of age group, job_industry_category, wealth_segment, and car ownership, to understand which of these characteristics are dominant among segments.

I will also look at the purchase patterns to understand the types of products they buy, the average order value (which gives an idea of price sensitivity), and the time of year they tend to make purchases

Let’s dive deeper

_**what is the age distribution of our target segments?**_

![Customer Count by Age Group and Segments.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Customer%20Count%20by%20Age%20Group%20and%20Segments.png)

From the visual representation of our query result, we can see that our chosen segments are made up of people mostly above the age of 55.

_**what is the location distribution of our target segments?**_

![Customer Count by State and Segments.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Customer%20Count%20by%20State%20and%20Segments.png)

Our target segments are people mostly from the state of New south wales with 830 persons coming up second is Victoria with 397 persons.

_**what is the job industry distribution of our target segments?**_

![Customer Count by Job Industry Category.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Customer%20Count%20by%20Job%20Industry%20Category.png)

For the trait of the job industry, we have three categories to consider, these are Manufacturing, Health, and Financial Services, they make up a good portion of our target segment.

_**what is the wealth segment distribution of the target segment?**_

![Customer count by Wealth Segment.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Customer%20count%20by%20Wealth%20Segment.png)

The majority of our target segment belongs to the mass customer wealth segment, with high net worth and affluent customers at even.

_**What is the preferred brand of our target segment?**_

![Order Volume By Brand.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Order%20Volume%20By%20Brand.png)

The Solex brand has the highest order volume among all brands in stock, but if we ignore this brand we can see that the other brands are at evens when comes to order volume.

_**Are there any seasonal trends for our segments?**_

![Order Volume By Month.png](https://github.com/khvu0610/Customer-Segmentation/blob/47cf0fd542e3bbe9ae0349728ee157b65ec5bc8e/Images/Order%20Volume%20By%20Month.png)

The answer is _**Yes**_, there is a seasonal trend. Customers in this segment tend to purchase more products towards the end of the year, specifically in the months of October, November, and December.

**Age Distribution:** The majority of our chosen segments are composed of individuals aged 55 and above. This demographic insight can have implications for product preferences, communication strategies, and overall marketing approaches.

**Geographic Segmentation:** Our target segments are primarily located in the state of New South Wales, with a significant portion residing in Victoria as well.

**Job Industry:** The job industries of Manufacturing, Health, and Financial Services are prominent within your target segment.

**Customer Wealth Segments:** Your target segment comprises mainly Mass Customers, giving us an understanding of the economic diversity of your audience and tailoring your offerings accordingly.

**Brand Preferences:** The Solex brand has the highest order volume among all brands, but excluding Solex, the other brands have relatively similar order volumes. This information guides decisions regarding brand promotions and inventory management.

**Seasonal Trends:** A clear seasonal trend is identified in the data, where customers tend to purchase more products toward the end of the year, specifically in October, November, and December. This means our campaigns should be more active in these months to take advantage of the high purchase volume during the period.

With these insights in mind, we look through our new customers list to identify the most probable customer to target.
