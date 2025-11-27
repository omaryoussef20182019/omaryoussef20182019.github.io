---
layout: post
title: "Buenos Aires Apartment Price Prediction: Machine Learning for Real Estate"
date: 2025-11-25 10:00:00 +0200
categories: [Machine Learning, Regression, Python]
excerpt: "A data science project focused on building a robust Ridge Regression model to accurately predict apartment sale prices in the highly competitive Buenos Aires real estate market."
image: /assets/images/Housing in Buenos Aires.jpeg
---

## Project Overview

This data science project is aimed at building a robust machine learning model to **predict the sale price of apartments in Buenos Aires, Argentina**. The solution employs a supervised learning pipeline, utilizing key features such as covered surface area, geographic coordinates, and neighborhood to accurately estimate the selling price, providing valuable insights for investors and buyers.

---

## 🛠️ Methodology: Preparation and Modeling

### 1. Data Wrangling and Preparation

The modeling process began with meticulous data preparation, essential for real estate analysis:

* **Custom `wrangle` Function:** A specialized function was created to load and clean the raw data, ensuring standardization of feature names and filtering the dataset to include only relevant apartment listings.
* **Feature Selection:** The model uses the key features: `'surface_covered_in_m2'`, `'lat'`, `'lon'`, and the categorical feature `'neighborhood'` to predict the target variable `'price'`.

### 2. Scikit-learn Modeling Pipeline

A Scikit-learn pipeline was implemented to automate and ensure the consistency of all preprocessing and modeling steps:

* **OneHotEncoder:** Applied to the categorical feature `'neighborhood'` to transform neighborhood names into a numerical format suitable for the linear model.
* **Ridge Regression:** Chosen as the core regression algorithm. Ridge Regression is particularly effective for handling potential **multicollinearity** common in real estate datasets, improving model stability and generalization.

### 3. Evaluation and Deployment

* **Model Performance:** The model's performance was measured using the **Mean Absolute Error (MAE)** to quantify the average prediction error, providing a clear dollar value of the model's accuracy.
* **Deployment Ready:** A convenient function, `make_prediction(area, lat, lon, neighborhood)`, was developed for easy price forecasting based on user-specified apartment characteristics.

---

## 💻 Key Technologies and Libraries

* **Python:** The core environment for analysis.
* **pandas & numpy:** For efficient data handling and numerical operations.
* **scikit-learn (sklearn):** Used extensively for the core regression model (`Ridge`), pipeline construction (`make_pipeline`), encoding (`OneHotEncoder`), and model evaluation (`mean_absolute_error`).
* **seaborn & plotly.express:** For clear and effective data visualization during the EDA and results presentation.
* **ipywidgets:** Used to create interactive prediction tools directly within the Jupyter Notebook environment.

---

## 🎯 Example Prediction

The notebook showcases the model's functionality with clear, interpretable output:

```python
# Example prediction for an apartment in Villa Crespo
make_prediction(110, -34.60, -58.46, "Villa Crespo")
