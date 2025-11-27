---
layout: post
title: "Customer Segmentation in the US: A K-Means and PCA Approach"
date: 2025-11-27 10:00:00 +0200
categories: [Data Science, Machine Learning, Python]
excerpt: "A comprehensive data science project focusing on identifying distinct customer segments using K-Means Clustering and Principal Component Analysis (PCA) to derive actionable business insights."
image: /assets/images/segmentation-cover.jpg
---

## Project Overview

This project focuses on analyzing customer demographic data to identify distinct and meaningful customer segments (clusters) using **Unsupervised Machine Learning** techniques. The primary goal is to help businesses achieve a deeper understanding of their customer base, enabling them to formulate highly targeted marketing strategies, personalize product offerings, and optimize resource allocation.

---

## 🛠️ Methodology and Analysis Steps

The following standard steps for unsupervised learning were performed within the Jupyter Notebook:

1.  **Exploratory Data Analysis (EDA):** Initial data exploration to understand variable distributions, check for relationships between features (e.g., Income vs. Business Ownership), and identify data quality issues.
2.  **Data Preprocessing:** Handling of missing values and encoding of categorical variables.
3.  **Feature Scaling:** **StandardScaler** was applied to normalize the data, which is essential for distance-based algorithms like K-Means.
4.  **Dimensionality Reduction (PCA):** Principal Component Analysis (PCA) was utilized to reduce the high-dimensional feature space into two main components (**PC1 and PC2**) for effective visualization and robust interpretation of the resulting clusters.
5.  **Clustering with K-Means:**
    * The optimal number of clusters (k) was determined using the Elbow Method and/or Silhouette Score.
    * The K-Means algorithm was trained using the reduced PCA data.
6.  **Visualization:** Clusters were visualized on an interactive scatter plot using the first two principal components with the `plotly.express` library.

---

## 💻 Technologies and Libraries

The analysis was conducted using **Python** and the following key libraries:

* **pandas:** For data manipulation and loading.
* **scikit-learn (sklearn):** For KMeans clustering, StandardScaler, and PCA.
* **matplotlib** and **seaborn:** For static data visualization.
* **plotly.express:** For interactive visualization of the final clusters.

---

## 🎯 Key Results and Business Insights

The customer base was successfully segmented into **[3]** distinct and actionable groups.

| Cluster | Characteristics | Marketing Value |
| :--- | :--- | :--- |
| **Cluster 1** | High income, high credit scores, and frequent purchases. | **High-Value Customers:** Focus on exclusive offers, premium services, and loyalty programs. |
| **Cluster 2** | Budget-conscious, lower average income, high engagement with sales/discounts. | **Value Shoppers:** Target with cost-saving messages and promotional campaigns. |
| **Cluster 3** | Newer customers, lower historical purchase data. | **Growth Segment:** Focus on initial onboarding, product education, and early-bird offers. |
