# Customer Segmentation Analysis

This repository contains a comprehensive analysis of customer segmentation using credit card data. The analysis includes data cleaning, feature engineering, application of various clustering algorithms, and visualization of the results.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Analysis](#data-analysis)
- [Model Development and Evaluation](#model-development-and-evaluation)
- [Cluster Analysis and Insights](#cluster-analysis-and-insights)
- [Conclusions and Recommendations](#conclusions-and-recommendations)
- [How to Run](#how-to-run)
- [License](#license)

## Introduction
Customer segmentation is crucial for personalized marketing strategies. This analysis aims to segment customers based on their credit card usage patterns to help in tailoring marketing efforts effectively.

## Dataset
The dataset summarizes the usage behavior of approximately 9000 active credit card holders over the last 6 months. It includes 18 behavioral variables at the customer level.

### Data Dictionary
- **CUST_ID**: Identification of credit card holder (Categorical)
- **BALANCE**: Balance amount left in their account to make purchases
- **BALANCE_FREQUENCY**: How frequently the balance is updated (0-1)
- **PURCHASES**: Amount of purchases made from account
- **ONEOFF_PURCHASES**: Maximum purchase amount made in one go
- **INSTALLMENTS_PURCHASES**: Amount of purchase done in installments
- **CASH_ADVANCE**: Cash in advance given by the user
- **PURCHASES_FREQUENCY**: How frequently the purchases are being made (0-1)
- **ONEOFF_PURCHASES_FREQUENCY**: How frequently purchases are happening in one go (0-1)
- **PURCHASES_INSTALLMENTS_FREQUENCY**: How frequently purchases in installments are being done (0-1)
- **CASH_ADVANCE_FREQUENCY**: How frequently the cash in advance is being paid
- **CASH_ADVANCE_TRX**: Number of transactions made with "Cash in Advanced"
- **PURCHASES_TRX**: Number of purchase transactions made
- **CREDIT_LIMIT**: Limit of credit card for user
- **PAYMENTS**: Amount of payment done by user
- **MINIMUM_PAYMENTS**: Minimum amount of payments made by user
- **PRC_FULL_PAYMENT**: Percent of full payment paid by user
- **TENURE**: Tenure of credit card service for user

## Data Analysis
1. **Descriptive Statistics**: Analyzed the summary statistics of the dataset.
2. **Handling Missing Values**: Dealt with missing values through appropriate imputation techniques.
3. **Outlier Detection and Removal**: Identified and handled outliers to improve model performance.
4. **Visualization**: Created various plots to understand data distributions and relationships.

## Model Development and Evaluation
1. **Dimensionality Reduction**: Applied PCA to reduce the dimensions while retaining 95% of the variance.
2. **Clustering Algorithms**:
    - **K-Means**: Applied K-Means clustering and evaluated using Silhouette Score.
    - **DBSCAN**: Applied DBSCAN clustering for density-based clustering.
    - **Agglomerative Clustering**: Applied hierarchical clustering for identifying nested clusters.
3. **Evaluation**: Compared clustering results using Silhouette Scores and visual inspection.

## Cluster Analysis and Insights
### Cluster -1 (Outliers)
- **BALANCE**: 1.743770
- **BALANCE_FREQUENCY**: 0.956084
- **PURCHASES**: 2.680871
- **ONEOFF_PURCHASES**: 2.164217
- **INSTALLMENTS_PURCHASES**: 2.359565
- **CASH_ADVANCE**: 1.602530
- **PURCHASES_FREQUENCY**: 0.739153
- **CREDIT_LIMIT**: 1.711607
- **PAYMENTS**: 3.005056
- **MINIMUM_PAYMENTS**: 1.760574
- **TENURE**: 11.421818

**Insights**:
- High card usage pattern (BALANCE, PURCHASES, CASH_ADVANCE).
- High credit limits and large payments (CREDIT_LIMIT, PAYMENTS).
- Potential risk due to high cash advances.

### Cluster 0 (Low Activity)
- **BALANCE**: -0.057452
- **BALANCE_FREQUENCY**: 0.892938
- **PURCHASES**: -0.092286
- **ONEOFF_PURCHASES**: -0.076301
- **INSTALLMENTS_PURCHASES**: -0.077918
- **CASH_ADVANCE**: -0.052409
- **PURCHASES_FREQUENCY**: 0.487574
- **CREDIT_LIMIT**: -0.056845
- **PAYMENTS**: -0.101474
- **MINIMUM_PAYMENTS**: -0.057832
- **TENURE**: 11.537706

**Insights**:
- Low card usage pattern (BALANCE, PURCHASES, CASH_ADVANCE).
- Low credit limits and small payments (CREDIT_LIMIT, PAYMENTS).
- Customers who use the card infrequently.

### Cluster 1 (High Value)
- **BALANCE**: 0.059425
- **BALANCE_FREQUENCY**: 1.000000
- **PURCHASES**: 4.816382
- **ONEOFF_PURCHASES**: 6.037560
- **INSTALLMENTS_PURCHASES**: 0.292395
- **CASH_ADVANCE**: -0.409691
- **PURCHASES_FREQUENCY**: 1.000000
- **CREDIT_LIMIT**: 0.599119
- **PAYMENTS**: 3.046504
- **MINIMUM_PAYMENTS**: -0.146749
- **TENURE**: 12.000000

**Insights**:
- Very high card usage, especially in single purchases (PURCHASES, ONEOFF_PURCHASES).
- High credit limits and large payments (CREDIT_LIMIT, PAYMENTS).
- High-value customers with frequent card usage.

## Conclusions and Recommendations
### Conclusions
- **Cluster -1**: High activity customers with significant card usage and cash advances. Potential risk due to high cash advances.
- **Cluster 0**: Customers with low card usage and low credit limits. Use the card infrequently.
- **Cluster 1**: High-value customers with frequent and high card usage.

### Final Recommendations
- **Cluster -1**: Introduce loyalty programs and incentives to encourage more purchases and reduce cash advances. Monitor and manage risks.
- **Cluster 0**: Implement campaigns to encourage card usage. Educate customers about benefits.
- **Cluster 1**: Develop exclusive offers and premium loyalty programs. Provide personalized financial advice.

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/your-repository-name.git
