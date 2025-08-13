# Project Overview
This analysis aims to use clustering to identify loyal customers based on a mix of purchase and engagement behaviors and develop straightforward business rule to allow for real time targeting for promotions.

# Business Background and Problem Definition :
Company A is an eCommerce marketplace. 

**Objective**: As part of its initiative to strengthen customer loyalty, the company aims to provide weekly personalized promotions to its top customers.

** To do so? **  
1. Identify a group of Loyal Customers
   - Through K means Clustering and identify the characteristics of loyal customers
2. Develop a busiess rule to identify Loyal Customers
  - Through decision tree, (to allow for business operation team to allow for real time targeted each week by identifying 'Loyal Customers' based on this rule) --> easy and straightforward for business team to understand 
  - Translate the cluster definition into clear rules that business teams can use directly.
  
## Dataset
Aggregaed over the past 60 days: 
Transactional Features:
- total_spend – Total amount spent ($)
- purchase_count – Number of orders placed
- avg_order_value – Average spend per order

Digital Engagement Features:
- avg_session_length – Average session duration (minutes)
- wishlist_adds – Number of items added to wishlist
- product_reviews – Number of product reviews written

# Methodology 
1. Data Preprocessing:
  - One Hot Encoding categorical features
  - Standard Scaling numerical features
2. K Means Clustering
   - Elbow method to determine optimal K
  1. First K-Means Clustering – Full Customer Base:
    - Identify a "top cluster" with significantly higher spend and engagement
  2. Second K-Means Clustering:
    - Recluster only on top cluster segment to isolate the higher spend and engagement customers, to reduce noise and identify more subtle patterns of the loyal customers
3. Decision Tree – Threshold Extraction
   - Create Target Variable: is_premium_candidate = 1 for customers in the final loyal cluster, else 0
   - Train/Test Split and Train/Fit/Predict the model
   - Extract business rules 

# Conclusion 
- Loyal Customers are defined as those customers with higher spending... etc 
- Specifically, offers should be given to customers who had
  - 



**Final Recommendation** 
