# TMN CUSTOMER CHURN ANALYSIS
---

## Table of Contents
- [Introduction](#introduction)
- [Purpose of the Analysis](#purpose-of-the-analysis)
- [Dataset Overview](#dataset-overview)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Key Insights and Findings](#key-insights-and-findings)
- [Summary of Key Insights](#summary-of-key-insights)
- [Recommendations](#recommendations)


# INTRODUCTION 
### An end-to-end Customer Churn Analysis project built with Power BI. This repository covers data preparation, exploratory data analysis, churn rate calculation, customer segmentation, and interactive dashboard design. The analysis highlights key factors influencing customer churn and provides business-driven insights to support data-informed retention strategies.

## PURPOSE OF THE ANALYSIS 

- The goal of this analysis is to identify factors driving customer churn and develop 
strategies to reduce attrition. 
- Churn is a major issue for data providers, impacting revenue and customer lifetime 
value. 
- The report provides insights into churn patterns and recommendations for 
improving retention.

## DATASET OVERVIEW 

### Key Features: 
- Customer demographics 
- Subscription details (e.g., contract type, monthly charges) 
- Usage patterns (e.g., international plan, call minutes) 
- Churn indicator (Yes/No)

## DATA CLEANING AND PREPARATION 

### DATA CLEANING STEPS 
- Handling Missing Values: (e.g., "Replaced missing values in 'Total Charges' with 
median values") 
- Removing Duplicates: (e.g., "Dropped duplicate records based on Customer ID") 
- Data Type Corrections: (e.g., "Converted 'Monthly Charges' to a numeric format") 
- Removing irrelevant columns: (e.g., Senior, Under 30, Phone number)
  
### FEATURE ENGINEERING (Creating New Columns) 
- Contract Category: Monthly vs. Yearly contracts (Created using SWITCH()) 
- Demographics Grouping: Categorized customers into Youth, Adult, Senior by 
adding Conditional columns. 
- Replaced Values: (e.g., group contract, churn Label, Intl. Active) 
- Consumption Grouping: Categorized data consumption groups into <5GB, 5-10GB, 
10GB+ 
- Age Bins: Created 10-year age brackets (20–30, 30–40, etc.) 
### CREATING KEY DAX MEASURES 
- Total Customers: DISTINCTCOUNT(CustomerID) 
- Total Churned Customers: CALCULATE(DISTINCTCOUNT(CustomerID), Churn = 
"Yes") 
- Churn Rate: DIVIDE([Total Churned Customers], [Total Customers])

## EXPLORATORY DATA ANALYSIS (EDA)

### Churn Overview 
- Total Customers: 6,687 
- Total Churned Customers: 1,796 
- Overall Churn Rate: 26.9% 
### Customer Segmentation 
- Churn Rate by Age Group (Youth, Adult, Senior) 
- Churn Rate by Contract Type (Monthly vs. Yearly) 
### Financial Insights 
- Average Monthly Charges by Group Size 
- Total Revenue Loss Due to Churn 
### Churn Trends & Patterns 
- Top Reasons for Churn (Bar Chart in Descending Order) 
- Churn Rate by International Plan (Yes vs. No) 
- State-Level Churn Map (Visualizing churn rates by state)

## KEY INSIGHTS AND FINDINGS 

### Overview of Churn 
• Total Customers: 6,687 
• Total Churned Customers: 1,796 
• Overall Churn Rate: 26.9% 
 
- The churn rate is high (26.9%), indicating a significant portion of 
customers are leaving. Understanding why customers churn is critical for improving 
retention. 
### Churn Reasons Analysis: 
- The top 3 churn reasons are competition-related (better offers, better devices, 
more data). 
- Customer service issues (attitude of support person) is also a major factor. 
- A portion of customers left without providing a reason ("Don't know" - 123 cases). 
### Churn by State: 
- California has the highest churn rate (67.4%), which is significantly above average. 
- The East Coast and Midwest states show high churn levels. 
### Churn Rate by Age Group: 
- Seniors have the highest churn rate (39.1%), possibly due to tech adoption issues. 
-  Adults & Youth churn at similar rates (~25%), indicating possible pricing concerns. 
### Churn Rate by Contract type: 
- Month-to-Month contracts have the highest churn (46.3%), indicating customers 
prefer flexibility. 
- Long-term contracts significantly reduce churn

### Churn by Payment Method: 
- Customers paying via paper check (38.0%) and direct debit (34.5%) have higher 
churn rates. 
- Credit card users churn the least (14.5%), suggesting automatic payments improve 
retention. 
### Churn Rate by International Plan: 
- Customers with inactive international plans churn less (7.6%), but 
- Customers actively using Intl. Plans churn the most (71.2%). 
### Churn Rate by Data Usage: 
- Customers with Unlimited plan has a higher churn rate of 32.1% 
### Churn Rate by Account Length: 
-  Most churn happens in the first year (48.5%), indicating early customer 
dissatisfaction. 
- Long-term customers have very low churn (3.7%).
  
## Summary of Key Insights 
- The churn rate is 26.9%, with high churn in CA, PA, and OH (California, 
Pennsylvania, and Ohio). 
- Seniors, monthly contracts, and paper check users churn the most. 
- Competitive offers & poor customer service drive churn.

## RECOMMENDATIONS
### 1. ADDRESS COMPETITOR-RELATED CHURN 
#### Observation: Many customers left due to better offers, or more data from competitors. 
#### Solution: 
- Investigate market competition in high-churn states. 
- Conduct competitive pricing analysis and introduce special offers for high-risk 
customers. 
- Offer limited-time discounts or loyalty plans to prevent switching. 
-  Introduce exclusive device upgrade programs for long-term customers. 
### 2. IMPROVE NETWORK & SERVICE QUALITY 
#### Observation: Network reliability & poor customer service are key churn factors. 
#### Solution: 
- Invest in network expansion & quality improvements in high-churn states (e.g., 
California). 
- Implement proactive customer support (e.g., call center training, chatbot 
assistance).  
- Offer priority support or VIP service tiers for loyal customer. 
Consider state-specific promotions to retain customers. 
- Improve network reliability in states with poor service reviews. 
### 3. REDUCE HIGH CHURN IN MONTHLY PLANS 
#### Observation: Month-to-month contract churn rate = 46.3%, while yearly plans 
have only 6.6% churn. 
#### Solution: 
- Encourage long-term contracts with discounts or extra data incentives. 
- Provide better value-add services (e.g., bundled streaming services or cloud storage). 
### 4. IMPROVE CUSTOMER RETENTION IN THE FIRST YEAR 
#### Observation: 48.5% of customers churn within the first year. 
#### Solution: 
- Implement a customer onboarding program to ensure users understand their data 
plans. 
- Offer exclusive retention discounts after 6 months. 
- Send personalized usage reports to educate users on optimizing their plans. 
### 5. OPTIMIZE INTERNATIONAL DATA PLANS 
#### Observation: Customers actively using international plans have a 71.2% churn 
rate. 
#### Solution: 
- Review international plan pricing to ensure competitive rates. 
- Offer discounted international bundles for frequent travelers. 
- Improve roaming agreements for better international data speeds. 
###6. FOCUS ON HIGH-CHURN PAYMENT METHODS 
#### Observation: Customers who pay by paper check have a 38% churn rate, while 
credit card users churn the least (14.5%). 
#### Solution: 
- Encourage automatic payments (credit card, direct debit) with small discounts. 
- Phase out manual payments or introduce a processing fee for paper checks. 
### 7. ADDRESS AGE-RELATED CHURN
- Offer simpler plans & support for seniors. 
- Provide family bundle discounts to retain younger users.
