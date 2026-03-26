# Customer Lifetime Value Prediction using Deep Learning and Survival Analysis

## Overview

This repository contains the implementation and analysis conducted for a postgraduate dissertation focused on predicting Customer Lifetime Value (CLV) in digital commerce environments. The study integrates traditional statistical methods with machine learning and deep learning approaches to evaluate their effectiveness in modelling customer behaviour.

---

## Research Objectives

The primary objectives of this study are:

* To analyse customer purchasing behaviour using transactional data
* To develop predictive models for estimating Customer Lifetime Value
* To evaluate the effectiveness of deep learning and survival analysis techniques
* To compare model performance across different methodological approaches

---

## Dataset

The study utilises the Online Retail dataset, which contains transactional records including customer purchases, dates, quantities, and pricing information.

Due to size constraints, the full dataset is not included in this repository. A sample dataset is provided for demonstration purposes.

Full dataset source:
https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset

---

## Methodology

### Data Preprocessing and Feature Engineering

Customer-level features were derived from transactional data, including:

* Recency (time since last purchase)
* Frequency (number of purchases)
* Tenure (customer lifespan)
* Average Order Value

To ensure methodological validity, variables directly contributing to the target variable were excluded to prevent data leakage.

---

### Modelling Approaches

#### Linear Regression

A baseline regression model was implemented to establish a reference for predictive performance.

#### Long Short-Term Memory (LSTM)

A deep learning model was applied with the intention of capturing temporal patterns in customer transactions. However, due to aggregation of data, the sequential nature required for optimal LSTM performance was limited.

#### Survival Analysis

Survival models, including the Cox Proportional Hazards model and DeepSurv, were implemented to estimate customer lifetime and churn probability.

---

## Results and Findings

* Frequency was identified as a strong predictor of customer value
* Recency demonstrated a significant relationship with churn behaviour
* Survival analysis models achieved strong predictive performance (C-index ≈ 0.96)
* Deep learning models showed limited improvement due to the absence of sequential data

---

## Limitations

* Aggregation of transactional data resulted in loss of temporal sequence information
* Initial modelling approaches were affected by data leakage, which was subsequently corrected
* Limited feature set may have constrained model performance

---

## Future Work

* Utilisation of transaction-level sequential data for deep learning models
* Enhancement of feature engineering techniques
* Exploration of hybrid modelling approaches combining statistical and deep learning methods

---

## Repository Structure

CLV-Prediction-Project/
│
├── notebook/
│   └── clv_prediction_model.ipynb
│
├── data/
│   └── sample_data.csv
│
├── report/
│   └── CLV_Prediction_Report.pdf
│
├── requirements.txt
└── README.md

---

## Reproducibility

To reproduce the analysis:

1. Install required dependencies:
   pip install -r requirements.txt

2. Run the Jupyter Notebook:
   jupyter notebook

---

## Author

Jnanadeep Aravapalli

---

## Note

This repository is intended for academic and research purposes. The implementation reflects the methodological considerations and limitations discussed in the accompanying dissertation.
