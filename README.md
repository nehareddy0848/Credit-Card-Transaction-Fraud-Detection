# Credit-Card-Transaction-Fraud-Detection

Data Source: https://data.ok.gov/dataset/purchase-card-pcard-fiscal-year-2014

## Overview

This project focuses on detecting unusual credit card transactions using unsupervised machine learning techniques. Since the dataset does not contain labeled fraud cases, different anomaly detection models are used to identify suspicious transactions based on patterns in the data.

The goal is to study transaction behavior and flag abnormal activity using multiple models and compare their results.

---

## Dataset

The dataset contains 442,458 transactions with details such as:

- Transaction amount  
- Agency information  
- Cardholder details  
- Vendor information  
- Transaction and posting dates  
- Merchant category codes  

---

## Exploratory Data Analysis

The dataset was explored to understand transaction patterns:

- Distribution of transaction amounts  
- Monthly transaction trends  
- Top vendors and agencies  
- Spending behavior of cardholders  
- Correlation analysis  
- Outlier detection using plots  

---

## Feature Engineering

New features were created to capture abnormal behavior:

- Posting Delay  
- Average Spend per Cardholder  
- Amount Ratio  
- Vendor Frequency  
- Daily Transaction Count  
- Amount Deviation  

---

## Data Preprocessing

- Converted date columns to datetime format  
- Handled missing and infinite values  
- Scaled numerical features using StandardScaler  

---

## Models Used

### K-Nearest Neighbors (KNN)
Detects anomalies based on distance from nearby points.

### Local Outlier Factor (LOF)
Detects anomalies based on local density differences.

### Isolation Forest
Detects anomalies by isolating unusual points using random splits.

---

## Results

### Strict Consensus (All 3 Models Agree)

- Total transactions: 442,458  
- Outliers detected: 2,085  
- Percentage: 0.47%  

### At Least 2 Models Agree

- Outliers detected: 14,308  
- Percentage: 3.23%  

---

## Key Observations

- Most transactions follow normal patterns  
- Some transactions have extremely high amounts  
- Certain vendors appear repeatedly in flagged cases  
- Some cardholders show repeated unusual activity  
- High amount ratio is a strong anomaly indicator  

---

## Tools Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- PyOD  
