#  Churn Analysis Project


  Churn Analysis has been a key technique for companies across industries. By examining customer data to identify patterns and using advanced data analytics and/or machine learning, businesses can predict which customers are at risk of leaving and can find ways to reduce customer attrition based on data-based 'evidence'.  
  
## Project Background 
  This project present an end-to-end churn analysis of a Telecommunications company based in India and selling their services in their 28 states. From exploring the dataset, cleaning and processing data using SQL, python, and visualizing the insights through Tableau. Especially, using [ML](https://www.ibm.com/think/topics/machine-learning) for predicting retention by various factors.

The SQL queries used to inspect and clean the data for this analysis can be found here [[link](https://console.cloud.google.com/bigquery?sq=828042076658:c8210e7570bd45b4807ae06c005aa615)]. 

Targed SQL queries regarding various business questions can be found here [[link](https://console.cloud.google.com/bigquery?sq=828042076658:0f35266377364fa98d6310feee693a6c)].

An interactive Tableau dashboard used to report and visualize churners prediction using ML can be found here [[link](https://public.tableau.com/shared/TKJ5M752Q?:display_count=n&:origin=viz_share_link)].



# Data Structure & Initial Checks

The companies main database structure as seen below consists of 32 columns as follows:

```bash
customer_churn
 
 Customer_ID                   ├          (STRING, PK)
 Gender                        ├          (STRING)
 Age                           ├          (INTEGER)
 Married                       ├          (BOOLEAN)
 State                         ├          (STRING)
 Number_of_Referrals           ├          (INTEGER)
 Tenure_in_Months              ├          (INTEGER)
 Value_Deal                    ├          (STRING)
 Phone_Service                 ├          (BOOLEAN)
 Multiple_Lines                ├          (BOOLEAN)
 Internet_Service              ├          (BOOLEAN)
 Internet_Type                 ├          (STRING)
 Online_Security               ├          (BOOLEAN)
 Online_Backup                 ├          (BOOLEAN)
 Device_Proctection_Plan       ├          (BOOLEAN)
 Premium_Support               ├          (BOOLEAN)
 Streaming_TV                  ├          (BOOLEAN)
 Streaming_Movies              ├          (BOOLEAN)
 Streaming_Music               ├          (BOOLEAN)
 Unlimited_Data                ├          (BOOLEAN)
 Contract                      ├          (STRING)
 Paperless_Billing             ├          (BOOLEAN)
 Payment_Method                ├          (STRING)
 Monthly_Charge                ├          (FLOAT)
 Total_Charges                 ├          (FLOAT)
 Total_Refunds                 ├          (FLOAT)
 Total_Extra_Data_Charges      ├          (INTEGER)
 Total_Long_Distance_Charges   ├          (FLOAT)
 Total_Revenue                 ├          (FLOAT)
 Customer_Status               ├          (STRING)
 Churn_Category                ├          (STRING)
 Churn_Reason                  ├          (STRING)

```

# Executive Summary

### Overview of Findings
Customer churn is heavily concentrated among short-tenure, month-to-month contract customers, who represent the majority of predicted churners. Higher churn rates are also observed among customers with higher monthly charges but limited value-added services, indicating a perceived value gap. Retention efforts should prioritize early-stage customers through contract upgrades and service bundling.

<img src="img/Churn%20Analysis.png" > 

 **Key Metrics:**
* **Total Customers**
* **Total Churn & Churn Rate**
* **New Joiners**


# Insights Deep Dive
### Churn Analysis:

* **Demographic** Totally there are more than 6 thousand customers in which the higher the age group, the more they've been using the services, especially for people more than 50 years old. However, churn rate in this group of people also high and total churn in female is higher than male users. 
  
* **Geographic & Distribution.** Highest state with churn rate is Jammu & Kashmir (57.19%) and most of the reason for customer churn is because of competitor offering better options of service, beside other factors such as attitude and disatisfaction are also reasonate for 600 churners. 
  
* **Account info.** Churners are increasing in the groups using mailed check (37.8%) and bank withdrawal(34.4%), raising questions over payment creditability. Meanwhile, monthly churners show the highest posibility to be the driver of churning in customers (46.5%), in combination with the reason for churning in customers, churning is evenly distributed between tenure groups (26.1% - 27.5%). However, there are a downward trend in users around a year of using the services, but receiving the highest amount of customer, in total, being loyal with the company over 2 years and more. 
  
* **Services Use.** The company experienced churn rate in 3 main internet type ( Fiber Optic, Cable, and DSL), in which 41.1% of fiber optic internet-user leaving and mostly our customers leaving when  using internet service (93.7%). Howover, Premium Support and Online Security are being trusted causing only 16-17% churners using these services. 

### Churn Prediction: 

* **Predicted Churners:** 378 churners in the next period, in which 246 are female and 132 are male and mostly they are from Uttar Pradesh, Maharashtra and Tamil Nadu. There're not much in the trend of churning across group of the analysis. However, there is a predicted list of churners that will offer the company in further analysis and planning.

Python code for churn prediction using Machine Learning are provided in this [[Link](https://github.com/Ensya/Customer-Churn-Prediction-sample/blob/main/churnprediction.ipynb)]
# Recommendations: 

## Churn Analysis: 
* **Focus on Early-Stage Customer Retention** Prioritize retention efforts within the first 6–12 months, where churn risk is highest. Implement structured onboarding, proactive check-ins, and early incentives to stabilize new customers before churn behavior emerges.
* **Increase Perceived Value Through Service Bundling** Customers using multiple services (internet, security, streaming, premium support) demonstrate lower churn rates. Target high-risk customers with personalized bundle offers to increase perceived value relative to monthly charges.
* **Align Pricing With Value for High-Charge Customers** Higher monthly charges are associated with increased churn when not supported by value-added services. Introduce tiered pricing or loyalty benefits for high-charge customers to reduce dissatisfaction and revenue leakage.
* **Apply Targeted, State-Level Retention Campaigns**
Certain states exhibit significantly higher churn rates. Deploy region-specific retention strategies, such as localized promotions or tailored support, rather than one-size-fits-all campaigns.
## Further Analysis
* **Segment Customers by Revenue and Risk** Since there's already a list of predicted customer churning, segmenting them based on monthly charges, total revenue, and churn probability to distinguish between high-risk, high-value customers and low-impact churn would allow more cost-effective, targeted retention strategies.
* Future analysis could explore churn through cohort-based trends, service bundle effectiveness, and customer value segmentation, as well as leverage predictive modeling to improve early churn detection and retention targeting.
