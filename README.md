# MSCS 634 – Final Data Mining Project (Deliverable 4)

## Project Overview
This project presents an end-to-end data mining workflow applied to a healthcare dataset. The goal is to demonstrate how different analytical techniques—data preprocessing, exploratory data analysis (EDA), regression, classification, clustering, and association rule mining—can be combined to extract meaningful insights from real-world data.

This repository consolidates all work from Deliverables 1, 2, and 3 into a single final submission, highlighting key findings, practical recommendations, and ethical considerations.

---

## Dataset Description
The dataset contains patient-level healthcare records with a mix of demographic, clinical, operational, and financial attributes, including:

- Age, Gender, Blood Type  
- Medical Condition and Test Results  
- Admission Type and Insurance Provider  
- Admission and Discharge Dates  
- Billing Amount  

The dataset was selected because it supports multiple data mining tasks within a single domain and reflects realistic healthcare scenarios involving cost analysis, risk identification, and operational planning.

---

## Project Workflow

### 1. Data Cleaning and Exploration (Deliverable 1)
- Removed duplicate records to maintain data integrity  
- Handled missing values using median (numeric) and mode (categorical) strategies  
- Parsed admission and discharge dates and engineered time-based features  
- Reviewed outliers in age and billing amount  
- Performed exploratory data analysis to understand distributions and relationships  

Key EDA visualizations include age distribution, billing amount distribution, and billing variation across medical conditions.

---

### 2. Regression Modeling (Deliverable 2)
**Objective:** Predict patient billing amount  

- Models used:  
  - Linear Regression (baseline)  
  - Ridge Regression (regularized)  

- Evaluation metrics:  
  - R²  
  - RMSE  
  - MAE  

Ridge Regression performed better due to its ability to handle high-dimensional feature spaces created by one-hot encoding of categorical variables. Visualizations include predicted vs. actual billing amounts and residual analysis.

---

### 3. Classification, Clustering, and Pattern Mining (Deliverable 3)

#### Classification
**Objective:** Identify diabetes-related patterns  

- Binary target variable created from medical condition  
- Models used:  
  - Decision Tree  
  - Tuned k-Nearest Neighbors (GridSearchCV with F1-score)  

Performance was evaluated using accuracy, F1-score, confusion matrices, and ROC curves. F1-score and AUC were emphasized to account for class imbalance.

---

#### Clustering
**Objective:** Segment patients into meaningful groups  

- K-Means clustering applied after feature preprocessing  
- Elbow method used to select optimal number of clusters (k = 3)  
- PCA used for 2D visualization  

Clusters revealed distinct patient segments with varying clinical and operational characteristics.

---

#### Association Rule Mining
**Objective:** Discover frequent co-occurrence patterns  

- Apriori algorithm applied to categorical healthcare attributes  
- Rules filtered using support, confidence, and lift thresholds  

The resulting rules revealed interpretable relationships between medical conditions, medications, admission types, and insurance providers.

---

## Key Findings
- Regularized regression improved billing prediction stability  
- Tuned k-NN improved diabetes classification performance  
- Patient segmentation revealed distinct operational profiles  
- Association rules provided interpretable patterns for planning and decision support  

---

## Practical Recommendations
- Use billing prediction models to flag anomalous or high-risk charges  
- Apply classification results as a decision-support tool for risk prioritization  
- Use patient clusters for staffing and resource allocation planning  
- Leverage association rules for inventory management and care pathway validation  

---

## Ethical Considerations
Healthcare data analysis requires careful attention to ethics:

- **Privacy:** Healthcare attributes are sensitive and require strict access control  
- **Bias and Fairness:** Models may inherit bias from imbalanced data or proxy features  
- **Responsible Use:** All models should support—not replace—human decision-making  

Evaluation beyond accuracy (e.g., F1-score and AUC) and transparent model interpretation were used to reduce ethical risk.

### Technical Difficulties
I have attached the pictures of Visualization since these are empty on the github repo 
Please refer to `Screenshots` Folder
---