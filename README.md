# Project Overview
This analysis leverages clustering to identify loyal customers based on purchase and engagement behaviors, and develops straightforward business rule to enable real time targeting for promotions.

# Business Background and Problem Definition :
Company A is an eCommerce marketplace. As part of its initiative to strengthen customer loyalty, the company aims to provide weekly personalized promotions to its top customers.

**Objective**: 
1. Identify loyal customers using K means clustering.
2. Develop simple, interpretable business rules using decision tree model, enabling the operations team to target loyal customers efficiently each week.

## Dataset
Averaged over the past 6 weeks: 
Transactional Features:
- total_spend – Avg weekly $ spent 
- purchase_count – Avg weekly number of orders placed
- avg_order_value – Average spend per order

Digital Engagement Features:
- avg_session_length – Average session duration (minutes)
- wishlist_adds – Average number of items added to wishlist
- product_reviews – Average product reviews written

# Methodology 
1. Data Preprocessing:
  - Standard Scaling numerical features
2. K Means Clustering:
   - Elbow method to determine optimal number of clusters (k) 
  1. First K-Means Clustering:
   - On the entire customer base to identify a high spending and highly engaged cluster
   - Visualize and confirm using principal component analysis (PCA) 
  2. Second K-Means Clustering:
    - Recluster only within the top cluster to reduce noise and isolate true loyal customers
3. Decision Tree Modeling:
   - Create Target Variable: is_loyal_customer = 1 for customers in the final loyal cluster, else 0
   - Train/Test Split and Train/Fit/Predict the model and evaluate the model (Accuracy, Precision, F1 Scores) 
   - Extract business rules for identifying loyal customers

# Conclusion 
- Loyal Customers are defined as those customers with higher spending and engagement. 
- Specifically, offers should be given to customers who had
   - **avg weekly spend > 61.26**
   - **avg session length > 5.90**
   - **avg wishlist added item > 6.39**
By applying these business rules, the team can efficiently select customers each week to send out the offers for loyal customers.
