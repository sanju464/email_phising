# 🔐 Email Phishing Detection using Machine Learning

## 🚀 Overview

This project detects phishing emails using machine learning by analyzing textual content.

It uses TF-IDF vectorization and a Naive Bayes classifier to classify emails as **phishing** or **legitimate**.

---

## 🎯 Problem

Phishing emails are a major cybersecurity threat, often used to steal credentials or sensitive information.

Detecting them automatically is critical for improving email security systems.

---

## 🧠 Approach

### 1. Dataset

* Source: Kaggle phishing email dataset
* Multiple datasets combined (Enron, SpamAssassin, etc.)
* Text column: `text_combined`
* Labels:

  * `0` → Legitimate
  * `1` → Phishing

---

### 2. Preprocessing

* Train-test split (80/20, stratified)
* Text cleaned and vectorized using TF-IDF

---

### 3. Feature Engineering

* TF-IDF with:

  * Stopword removal
  * Max features: 5000

---

### 4. Model

* Multinomial Naive Bayes
* Trained on TF-IDF features

---

## 📊 Results

```text id="res1"
Accuracy: 96%
Precision (Phishing): 0.98
Recall (Phishing): 0.95
F1-score: 0.96
```

👉 Strong performance with balanced precision and recall.

---

## 📊 Example Predictions

```text id="ex2"
Input:
"Urgent! Your bank account has been suspended. Click here to verify your password."

Output:
Prediction: Phishing
Confidence: 0.988
```

```text id="ex3"
Input:
"Hi team, please find attached the meeting agenda for tomorrow."

Output:
Prediction: Legitimate
Confidence: 0.993
```

---

## 🛠️ Tech Stack

* Python
* scikit-learn
* Pandas / NumPy
* TF-IDF Vectorization

---

## ▶️ How to Run

```bash id="run2"
pip install pandas scikit-learn kagglehub
python main.py
```

---

## 📌 Future Improvements

* Try advanced models (Random Forest, XGBoost, Transformers)
* Deploy as API for real-time email scanning
* Build browser/email client integration
* Add explainability (why classified as phishing)

---

## 🤝 Why This Project Matters

* Demonstrates applied machine learning
* Real-world cybersecurity use case
* End-to-end pipeline: data → model → evaluation

---

## 📎 Author

Sanju – ML + Cybersecurity focused developer

