 #  Credit Card Fraud Detection

##  Overview

This project focuses on detecting fraudulent credit card transactions using Machine Learning. The model is trained on a highly imbalanced dataset and uses data balancing techniques to improve performance.

---

##  Problem Statement

Credit card fraud detection is challenging because fraudulent transactions are extremely rare compared to legitimate ones. The objective is to build a model that can accurately identify fraud while minimizing false predictions.

---

## 📂 Dataset

* Total Transactions: **284,807**
* Features: **30 numerical features (V1–V28, Time, Amount)**
* Target:

  * `0` → Legitimate
  * `1` → Fraudulent

🔗 Dataset Link: [https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data]
 Note: Dataset is not included in this repository due to size constraints.

---

##  Approach

### 1️⃣ Data Loading & Understanding

* Loaded dataset using Pandas
* Explored structure using `.head()`, `.tail()`, `.info()`
* Observed all features are numerical

---

### 2️⃣ Data Cleaning

* Checked for missing values
* Found **no null values**, so no cleaning required

---

### 3️⃣ Handling Imbalanced Data

* Original distribution:

  * Legit: **284,315**
  * Fraud: **492**

* Applied **Undersampling**:

  * Selected 492 legit transactions
  * Combined with 492 fraud transactions

✔ Final dataset: **984 samples (balanced)**

---

### 4️⃣ Exploratory Data Analysis (EDA)

* Compared statistical properties of fraud vs legit transactions
* Analyzed transaction amount distributions
* Used `groupby()` to observe feature differences

---

### 5️⃣ Feature Selection

* Features (X): All columns except `Class`
* Target (Y): `Class`

---

### 6️⃣ Train-Test Split

* Split ratio: **80% training / 20% testing**
* Used `stratify` to maintain class balance

---

### 7️⃣ Model Training

* Model used: **Logistic Regression**
* Trained on balanced dataset

---

### 8️⃣ Model Evaluation

* Training Accuracy: **95.42%**
* Testing Accuracy: **94.41%**

✔ Model performs well with good generalization

---

##  Results

* Successfully classified fraudulent transactions
* Balanced dataset improved model performance
* Achieved ~94% accuracy on unseen data

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn

---

## 📁 Project Structure

```
Credit-Card-Fraud-Detection/
│
├── Credit Card Fraud Detection.ipynb
├── .gitignore
├── README.md
```

---

## ⚙️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/narendra-nersu/Credit-Card-Fraud-Detection.git
   ```

2. Install dependencies:

   ```bash
   pip install numpy pandas scikit-learn
   ```

3. Run Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

---

## Limitations

* Used only Logistic Regression
* Accuracy metric alone may not be sufficient for fraud detection
* Undersampling reduces available data

---

##  Future Improvements

* Use Precision, Recall, F1-score
* Apply SMOTE instead of undersampling
* Try advanced models (Random Forest, XGBoost)
* Deploy model using Flask or FastAPI

---

