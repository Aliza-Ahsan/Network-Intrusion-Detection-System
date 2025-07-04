# Network-Intrusion-Detection-System
# Anomaly-Based Network Intrusion Detection System using Machine Learning

## Overview
This project presents a comparative analysis of three machine learning algorithms — **Random Forest**, **CatBoost**, and **XGBoost** — for building an **Anomaly-Based Network Intrusion Detection System (NIDS)**.
The goal is to detect potential intrusions in network traffic and evaluate the impact of different feature selection techniques on model performance.

## Research Objective
To build a robust NIDS using ML algorithms and compare their performance across three settings:

- **No Feature Selection**

- **With Recursive Feature Elimination (RFE)**

- **With Principal Component Analysis (PCA)**

The models were tested on two datasets of different sizes to examine how they perform in varying data volumes and complexities.

## Algorithms Used
1. Random Forest
2. XGBoost
3. CatBoost

Each model was evaluated in terms of accuracy, and other metrics like precision, recall, and AUC-PR (for XGBoost) were also considered to assess performance on imbalanced data.

## Feature Selection Methods
- **Recursive Feature Elimination (RFE): Identifies and retains the most relevant features using model-based ranking.**

- **Principal Component Analysis (PCA): Reduces dimensionality by projecting data onto principal components.**

- **Baseline: No feature selection, models trained on the full feature set.**

## Results

![image](https://github.com/user-attachments/assets/8bbcdb9a-65ff-456c-aed5-ea3f10663a88)

![image](https://github.com/user-attachments/assets/e0bb5e50-d2e8-49f7-86b1-67c306779172)

## Conclusion

For our first dataset, which had 25,193 entries, we observed that Random Forest after applying the feature selection method RFE (Recursive Feature Elimination) achieved an accuracy of 99.84% for detecting anomalous networks in the system. 

And for our second dataset, which had 148, 517 entries, we observed that XGBoost after applying the feature selection method RFE achieved an accuracy of 80.91%. 

Based on the results:
●	XGBoost emerged as the best-performing algorithm overall, particularly with the larger dataset and RFE method.
●	RFE was the most effective feature selection technique, improving model accuracy by focusing on the most relevant features.
●	PCA, while valuable for dimensionality reduction, was less suitable for this specific application, leading to a decline in accuracy.
The findings indicate that XGBoost, combined with proper feature selection like RFE, can effectively detect anomalies in network traffic and offers a promising solution for real-time intrusion detection systems.

## Future Work

1.	Real-Time Implementation of the NIDS
Future efforts should focus on deploying the best-performing model, such as XGBoost with RFE, into a real-time Network Intrusion Detection System (NIDS). This includes creating a system that can monitor live network traffic and classify anomalies instantly. Challenges like minimizing latency, ensuring low false-positive rates, and optimizing the system for real-world data variability will need to be addressed. Additionally, integrating the NIDS with alert mechanisms or automated response systems could significantly enhance its practical utility in mitigating attacks promptly.
2.	Exploration of Deep Learning Architectures
While this study emphasized traditional machine learning algorithms, deep learning techniques such as Long Short-Term Memory networks (LSTMs) and Convolutional Neural Networks (CNNs) can be explored to improve performance. These models are particularly well-suited for handling time-series network traffic data or extracting hierarchical patterns in complex datasets. For example, LSTMs could analyze sequential patterns of network packets, potentially identifying subtle temporal anomalies that static machine learning algorithms might miss. However, the increased computational complexity and the need for large-scale datasets would need careful consideration.

*Note: some notebooks aren't uploaded*
