Phishing Email Detection using TF-IDF & Naive Bayes








A Machine Learning project that detects phishing emails using Natural Language Processing (NLP) techniques and Multinomial Naive Bayes, achieving 96% accuracy on a real-world phishing dataset.

🚀 Project Overview

Phishing emails are a major cybersecurity threat. This project builds a text classification model that automatically predicts whether an email is:

✅ Legitimate (0)

⚠️ Phishing (1)

The model uses:

TF-IDF Vectorization

Multinomial Naive Bayes

Stratified Train-Test Split

Performance Evaluation using Precision, Recall, and F1-score

📊 Dataset

Dataset: Phishing Email Dataset

Features:

text_combined → Full email content

label

0 = Legitimate

1 = Phishing

Dataset downloaded using:

kagglehub.dataset_download("naserabdullahalam/phishing-email-dataset")

🛠 Tech Stack

Python

Pandas

Scikit-learn

TF-IDF (TfidfVectorizer)

Multinomial Naive Bayes

Matplotlib (optional for visualization)

🧠 Machine Learning Pipeline
1️⃣ Data Loading
df = pd.read_csv("phishing_email.csv")

2️⃣ Train-Test Split

80% Training

20% Testing

Stratified sampling used

train_test_split(test_size=0.2, stratify=y)

3️⃣ TF-IDF Vectorization

Converts text into numerical features.

TfidfVectorizer(stop_words='english', max_features=5000)

4️⃣ Model Training
MultinomialNB()

5️⃣ Model Evaluation
classification_report(y_test, y_pred)

📈 Model Performance
              precision    recall  f1-score   support

           0       0.94      0.98      0.96      7919
           1       0.98      0.95      0.96      8579

    accuracy                           0.96     16498

🔎 Key Insights

High precision for phishing detection (0.98)

Strong recall for legitimate emails (0.98)

Balanced F1-score (0.96)

Overall Accuracy: 96%

🧪 Example Predictions
Example 1

Input:

Urgent! Your bank account has been suspended. Click here to verify your password immediately.


Output:

Prediction: Phishing
Confidence: 98.8%

Example 2

Input:

Hi team, please find attached the meeting agenda for tomorrow's discussion.


Output:

Prediction: Legitimate
Confidence: 99.3%

📂 Project Structure
📁 phishing-email-detection
 ├── email_phising_using_naive_bayes.ipynb
 ├── phishing_email.csv
 ├── README.md
 └── requirements.txt (optional)

▶️ How to Run
1️⃣ Clone Repository
git clone https://github.com/your-username/phishing-email-detection.git
cd phishing-email-detection

2️⃣ Install Dependencies
pip install pandas scikit-learn kagglehub

3️⃣ Run the Notebook

Open:

email_phising_using_naive_bayes.ipynb


Run all cells sequentially.

🔮 Future Improvements

Add Confusion Matrix Visualization

Compare with:

Logistic Regression

Support Vector Machine (SVM)

Add N-grams (bigrams & trigrams)

Deploy using Streamlit or Flask

Upgrade to Deep Learning (LSTM / BERT)

🎯 Learning Outcomes

NLP preprocessing techniques

TF-IDF feature engineering

Naive Bayes classification

Model evaluation & performance analysis

Real-world phishing detection implementation

👨‍💻 Author

Sanju
Machine Learning Enthusiast

⭐ If You Found This Helpful

Give this repository a ⭐ on GitHub!
