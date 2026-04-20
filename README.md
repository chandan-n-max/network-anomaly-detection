# Network Anomaly Detection

## 📌 Problem Statement

The goal of this project is to detect anomalous network traffic using machine learning techniques. Network anomalies may indicate potential cyber-attacks such as DDoS, unauthorized access, or malicious activities. Early detection helps improve cybersecurity and maintain system integrity.

---

## 📊 Dataset

The dataset contains network traffic features including:

* Protocol type (TCP, UDP, ICMP)
* Service type (HTTP, FTP, etc.)
* Bytes transferred (srcbytes, dstbytes)
* Connection statistics (count, error rates, etc.)

A total of **123 processed features** were used after encoding.

---

## 🔍 Exploratory Data Analysis (EDA)

* Analyzed distribution of normal vs attack traffic
* Observed that attack traffic often shows **higher byte transfer**
* Identified skewed distributions and presence of outliers
* Found strong correlations among connection-based features
* Visualized protocol and service behavior using Tableau

---

## 🧪 Hypothesis Testing

* Tested whether higher traffic volume is associated with anomalies
* Result: **Statistically significant difference found**
* Conclusion: High data transfer is strongly linked to anomalous behavior

---

## ⚙️ Data Preprocessing

* Converted categorical variables using **One-Hot Encoding**
* Handled missing values using **median imputation**
* Scaled features where required
* Split dataset into training and testing sets

---

## 🤖 Machine Learning Models

### 1. Logistic Regression

* Accuracy: ~99%
* Used as baseline model

### 2. Random Forest Classifier

* Accuracy: ~99.9%
* ROC-AUC: ~0.999
* Provided feature importance insights

---

## 📈 Key Insights

* Features like **srcbytes and dstbytes** are strong indicators of anomalies
* Connection patterns (same/different service rates) play a critical role
* Certain protocols (ICMP) show higher anomaly ratios
* Attack traffic shows higher variance and extreme values

---

## ⚠️ Model Evaluation Note

The model achieved very high accuracy due to:

* Highly structured dataset
* Strong separability between normal and attack classes

In real-world scenarios, performance may vary due to noisy and unseen data.

---

## 🚀 Deployment

* Built a **Flask API** for real-time predictions
* Exposed API using **ngrok** for public access

### Endpoints:

* `/` → Check server status
* `/predict` → Predict anomaly

### Example Request:

```json
{
  "srcbytes": 1000,
  "dstbytes": 500
}
```

### Example Response:

```json
{
  "prediction": 0
}
```

---

## 📊 Tableau Dashboard

Interactive dashboard created to visualize:

* Traffic distribution
* Protocol vs anomaly trends
* Service-level attack patterns
* Data transfer behavior

🔗 https://public.tableau.com/views/Network_Anomaly_Detection_17765861548260/Dashboard1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

---

## 🧾 Project Structure

```
network-anomaly-detection/
│
├── notebook/
│   └── project.ipynb
│
├── deployment/
│   ├── app.py
│   ├── model.pkl
│   ├── features.pkl
│
├── README.md
```

---

## 🔮 Future Work

* Apply cross-validation for better generalization
* Deploy on cloud platforms (AWS / Render)
* Use deep learning models for complex pattern detection
* Improve real-time data handling

---

## 🎯 Conclusion

This project demonstrates how machine learning can effectively detect anomalies in network traffic. With proper preprocessing and feature engineering, even simple models can achieve high performance on structured datasets.

---

## 👤 Author

Chandan N
