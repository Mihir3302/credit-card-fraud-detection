# 💳 Credit Card Fraud Detection using Machine Learning

An **end-to-end Machine Learning project** that detects fraudulent credit card transactions using classification algorithms and techniques for handling highly **imbalanced datasets** such as **SMOTE**.

This project demonstrates the full ML workflow from **Exploratory Data Analysis (EDA)** to **model training, evaluation, and comparison**.

---

# 📌 Project Overview

Credit card fraud causes billions of dollars in financial losses every year. Detecting fraudulent transactions automatically is essential for banks and payment systems.

This project builds a **binary classification model** that predicts whether a transaction is:

* **0 → Normal Transaction**
* **1 → Fraudulent Transaction**

The project focuses on building reliable models while handling **extreme class imbalance** in real-world financial datasets.

---

# 📂 Project Structure

```
credit-card-fraud-detection/
│
├── creditcard.ipynb      # Complete ML pipeline
├── README.md             # Project documentation
└── .gitignore
```

⚠️ The dataset is not included because GitHub limits files larger than 100MB.

---

# 📊 Dataset

**Source:** Kaggle – ULB Machine Learning Group

🔗 Dataset link
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

| Property         | Value   |
| ---------------- | ------- |
| Transactions     | 284,807 |
| Fraud Cases      | 492     |
| Fraud Percentage | ~0.17%  |
| Features         | 30      |

### Feature Description

| Feature | Description                       |
| ------- | --------------------------------- |
| Time    | Time elapsed between transactions |
| Amount  | Transaction amount                |
| V1–V28  | PCA transformed features          |
| Class   | Target variable (Fraud or Normal) |

---

# 🔧 Tech Stack

### Programming

* Python

### Data Processing

* pandas
* numpy

### Visualization

* matplotlib
* seaborn

### Machine Learning

* scikit-learn

### Imbalanced Data Handling

* imbalanced-learn (SMOTE)

---

# 🚀 Machine Learning Pipeline

The notebook follows a structured ML workflow:

### 1️⃣ Import Libraries

Load required libraries for data analysis, modeling, and visualization.

### 2️⃣ Load Dataset

Dataset loaded using **pandas**.

### 3️⃣ Exploratory Data Analysis (EDA)

Key analyses performed:

* Dataset structure & statistics
* Missing value detection
* Duplicate transaction analysis
* Class distribution visualization
* Fraud vs normal transaction comparison
* Transaction time pattern analysis
* Correlation heatmap of all features
* Top fraud-correlated features

---

### 4️⃣ Data Preprocessing

Steps performed:

* Removed **duplicate transactions**
* Standardized **Amount** and **Time**
* Feature scaling using **StandardScaler**
* Train/Test split (**80/20 stratified split**)

---

### 5️⃣ Handling Class Imbalance

The dataset is extremely imbalanced:

Fraud transactions represent only **0.17%** of the data.

To solve this:

* **SMOTE (Synthetic Minority Oversampling Technique)** used
* **Random Under Sampling** used for majority class
* Implemented using **Imbalanced Pipeline**

Test data remains **completely untouched** to prevent data leakage.

---

### 6️⃣ Machine Learning Models

Four classification models were trained and compared:

| Model               | Parameters                |
| ------------------- | ------------------------- |
| Logistic Regression | `class_weight='balanced'` |
| Decision Tree       | `max_depth=10`            |
| Random Forest       | `n_estimators=100`        |
| Gradient Boosting   | `n_estimators=100`        |

---

# 📈 Model Evaluation

Multiple evaluation metrics were used.

| Metric    | Purpose                         |
| --------- | ------------------------------- |
| Accuracy  | Overall prediction performance  |
| Precision | Correct fraud predictions       |
| Recall    | Fraud detection rate            |
| F1 Score  | Balance of precision and recall |
| ROC-AUC   | Overall classification ability  |

⚠️ For fraud detection, **Recall and ROC-AUC are most important** because missing fraud transactions is very costly.

---

# 📊 Visualization & Analysis

The project includes multiple visual insights:

* Class distribution charts
* Fraud transactions by hour
* Correlation heatmap
* Model comparison bar charts
* ROC curves
* Precision-Recall curves
* Confusion matrices
* Feature importance plots

---

# 🏆 Key Results

* Trained and compared **4 ML models**
* Handled **severe class imbalance** using SMOTE
* Identified **best performing fraud detection model**
* Visualized **feature importance and prediction patterns**

Key predictive features include:

* **V14**
* **V17**
* **V12**

---

# ⚙️ How to Run the Project

### 1️⃣ Clone the Repository

```
git clone https://github.com/Mihir3302/credit-card-fraud-detection.git
```

### 2️⃣ Install Required Libraries

```
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

### 3️⃣ Download Dataset

Download dataset from:

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Place `creditcard.csv` in the project folder.

---

### 4️⃣ Run Notebook

```
jupyter notebook creditcard.ipynb
```

Run all cells sequentially.

---

# 🔑 Key Learnings

This project demonstrates:

* Handling **real-world imbalanced datasets**
* Importance of **SMOTE and resampling techniques**
* Comparing multiple ML models effectively
* Using **ROC-AUC and Recall** for fraud detection
* Understanding financial transaction patterns

---

# 👨‍💻 Author

**Mihir**

GitHub
https://github.com/Mihir3302

---

# 📜 License

This project is for **educational and research purposes only**.

The dataset is publicly available on Kaggle under the
**Open Database License (ODbL)**.
