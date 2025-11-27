---
layout: post
title: "Mexico City Apartment Price Prediction: A Ridge Regression Approach"
date: 2025-11-26 10:00:00 +0200
categories: [Machine Learning, Regression, Python]
excerpt: "An end-to-end machine learning solution designed to predict apartment sale prices in Mexico City using a robust Scikit-learn pipeline and Ridge Regression for high interpretability."
image: /assets/images/mexico-real-estate.jpg
---

## Project Overview

This project delivers a full, end-to-end machine learning solution aimed at **predicting the sale price of apartments in Mexico City**. We utilized a supervised learning approach, specifically **Ridge Regression**, to effectively model the relationship between key apartment features (such as size, location coordinates, and borough) and their market price.

---

## 🛠️ Methodology: Data Wrangling and Modeling Pipeline

### 1. Data Wrangling and EDA

The analysis commenced with a custom **`wrangle`** function to meticulously clean the real estate data. This phase included:

* Filtering the dataset to exclusively include apartment listings within Mexico City.
* Cleaning and standardizing feature names for consistency.
* Initial exploration of key features, notably 'surface\_covered\_in\_m2', 'lat', 'lon', and the categorical feature 'borough'.

### 2. Robust Scikit-learn Modeling Pipeline

A solid Scikit-learn pipeline was constructed to ensure the data preparation steps were consistent and repeatable:

* **Features Used:** 'surface\_covered\_in\_m2', 'lat', 'lon', and 'borough' were selected to predict 'price'.
* **Pipeline Steps:**
    * **OneHotEncoder:** Applied to transform the categorical feature 'borough' into numerical columns.
    * **SimpleImputer:** Used to handle any potential missing values within the feature set.
    * **Ridge Regression:** Chosen as the final linear model due to its effectiveness in handling collinear features and providing an interpretable prediction equation.

---

## 💻 Key Technologies and Libraries

* **Python:** The core language for the analysis.
* **pandas:** Essential for data manipulation and the custom `wrangle` function.
* **scikit-learn (sklearn):** Used for building the prediction pipeline, including `Ridge`, `OneHotEncoder`, and evaluating the model performance.
* **category\_encoders:** Utilized for specialized categorical encoding within the pipeline structure.

---

## 🎯 Evaluation and Prediction

* **Evaluation Metric:** The model was evaluated using the **Mean Absolute Error (MAE)** to accurately quantify prediction accuracy, providing a clear understanding of the average error margin in the predicted price.
* **Interpretability:** The final model's intercept and coefficients were extracted to derive a clear, linear equation, allowing for direct interpretation of how each feature influences the predicted price.
* **Prediction Function:** A user-friendly function, `make_prediction(area, lat, lon, borough)`, was created, making the model instantly ready for practical use with new apartment listings.
