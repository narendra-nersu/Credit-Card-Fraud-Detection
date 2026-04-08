# 💳 Credit Card Fraud Detection (Production-Ready ML Project)

##  Overview

This project builds a **fraud detection system** using Machine Learning on highly imbalanced financial transaction data. It demonstrates real-world challenges such as class imbalance, proper evaluation metrics, and an end-to-end ML pipeline.

---

##  Key Highlights

* ✔ Handled **extreme class imbalance (0.17% fraud cases)**
* ✔ Applied **Random Undersampling**
* ✔ Implemented **Feature Scaling (StandardScaler)**
* ✔ Built **Logistic Regression model**
* ✔ Evaluated using **Precision, Recall, F1-score, Confusion Matrix**
* ✔ Achieved **~94% accuracy with strong classification performance**

---

## 📂 Dataset

* Transactions: **284,807**
* Fraud cases: **492**
* Features: **V1–V28 (PCA transformed), Time, Amount**

🔗 Dataset: [https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data)

 Dataset not included due to size constraints

---

##  End-to-End Approach

### 🔹 1. Data Understanding

* Loaded dataset using Pandas
* Explored structure using `.head()`, `.info()`
* Verified all features are numerical
* Confirmed **no missing values**

---

### 🔹 2. Problem Insight

* Dataset is **highly imbalanced**:

  * Legit: 284,315
  * Fraud: 492

 Direct training would bias toward normal transactions

---

### 🔹 3. Data Balancing

* Applied **Random Undersampling**:

  * Sampled 492 legitimate transactions
  * Combined with 492 fraud cases

✔ Final dataset: **Balanced (984 samples)**

---

### 🔹 4. Exploratory Analysis

* Compared fraud vs legitimate transactions
* Analyzed statistical differences
* Observed distinct behavioral patterns

---

### 🔹 5. Feature Engineering

* Features (X): All columns except `Class`
* Target (Y): `Class`

---

### 🔹 6. Feature Scaling (Improvement)

* Applied **StandardScaler**
* Improved model convergence and stability

---

### 🔹 7. Train-Test Split

* 80% training / 20% testing
* Used **stratified sampling** to maintain balance

---

### 🔹 8. Model Training

* Algorithm: **Logistic Regression (max_iter=1000)**
* Advantages:

  * Fast and interpretable
  * Works well for binary classification

---

### 🔹 9. Model Evaluation

| Metric            | Score  |
| ----------------- | ------ |
| Training Accuracy | 95.42% |
| Testing Accuracy  | 94.41% |

---

### 🔹 10. Advanced Evaluation Metrics (Key Upgrade)

* **Precision** → Measures correctness of fraud predictions
* **Recall** → Measures how many fraud cases were detected
* **F1-score** → Balance between precision and recall

✔ These metrics are critical for fraud detection systems

---

### 🔹 11. Confusion Matrix Analysis

* Visualized model performance using heatmap
* Helps understand:

  * True Positives (correct fraud detection)
  * False Positives (false alarms)
  * False Negatives (missed frauds)

---

##  Results

* Achieved ~94% accuracy on test data
* Improved evaluation using Precision, Recall, F1-score
* Model demonstrates strong generalization

---

##  Limitations

* Accuracy alone is **not sufficient** for fraud detection
* Undersampling reduces dataset size
* Logistic Regression is a baseline model

---

##  Future Improvements

*  Apply **SMOTE (Oversampling)**
*  Try advanced models:
  * Random Forest
  * XGBoost
*  Add ROC-AUC curve
*  Hyperparameter tuning
*  Deploy using Flask / FastAPI

---

##  Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn


---

## ⚙️ How to Run

```bash
git clone https://github.com/narendra-nersu/Credit-Card-Fraud-Detection.git
cd Credit-Card-Fraud-Detection
pip install numpy pandas scikit-learn matplotlib seaborn
jupyter notebook
```

---




