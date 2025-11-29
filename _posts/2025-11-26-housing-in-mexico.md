---
layout: post
title: "Housing in Mexico: Price Prediction"
date: 2025-11-26 10:00:00 +0200
categories: [Machine Learning, Regression, Python]
excerpt: "Predicting apartment prices in Mexico City using Ridge Regression and a Scikit-learn pipeline for interpretability."
image: /assets/images/housing_mexico.jpg
---

## Project Overview

End-to-end ML solution to **predict apartment prices in Mexico City**, considering size, coordinates, and borough.

---

## 🛠️ Methodology

* **Data Wrangling:** Custom `wrangle` function to clean data.
* **Pipeline:** OneHotEncoder for categorical features, SimpleImputer for missing values, Ridge Regression.
* **Evaluation:** MAE and interpretable coefficients.
* **Prediction:** `make_prediction(area, lat, lon, borough)` for new listings.

---

## 💻 Technologies

* **Python, pandas, scikit-learn, category_encoders**
