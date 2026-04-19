# network-anomaly-detection
# Network Anomaly Detection

## Problem Statement

The objective of this project is to detect anomalous network traffic using machine learning techniques. Network anomalies may indicate potential cyber-attacks or unusual behavior that can compromise system security.

## Dataset

The dataset contains network traffic features such as protocol type, service, bytes transferred, and connection statistics.

## Approach

### 1. Exploratory Data Analysis (EDA)

* Analyzed distribution of normal vs attack traffic
* Identified key features influencing anomalies
* Visualized protocol and service-based attack patterns

### 2. Data Preprocessing

* Converted categorical variables using one-hot encoding
* Scaled numerical features
* Split data into training and testing sets

### 3. Model Building

* Logistic Regression
* Random Forest Classifier

### 4. Evaluation

* Accuracy, Precision, Recall, F1-score
* ROC-AUC score (~0.999)

### 5. Key Insights

* Features like srcbytes and dstbytes strongly influence anomalies
* TCP protocol dominates traffic but shows varying attack patterns
* Certain services are more prone to attacks

### 6. Deployment

* Built a Flask API for real-time prediction
* Model and scaler saved using pickle

## Results

* Logistic Regression Accuracy: ~99%
* Random Forest Accuracy: ~99.9%
* ROC-AUC Score: ~0.999

## Conclusion

The model effectively detects anomalies in structured network data. However, real-world performance may vary due to noise and unseen patterns.

## Tableau Dashboard

[Add your Tableau link here]

## Future Work

* Improve generalization using cross-validation
* Deploy on cloud platform
* Use deep learning models for complex patterns
