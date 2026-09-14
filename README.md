# smartkart-customer-churn-prediction
End-to-end customer churn prediction pipeline using Python and Logistic Regression, with data cleaning, outlier treatment, feature engineering, model evaluation, and business-focused insights.
# 🛒 SmartKart Customer Churn Prediction

An end-to-end **Machine Learning pipeline for predicting customer churn** in a retail/e-commerce business.

The project demonstrates how customer data can be transformed from messy raw records into actionable churn predictions using **Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, and Logistic Regression**.

## 🎯 Business Problem

Customer churn directly affects revenue, customer lifetime value, and retention costs.

SmartKart wants to identify customers who are likely to **churn (leave)** so that the retention team can take preventive action through targeted offers, improved customer service, or personalised engagement.

### Business Objective

> **Predict customers who are at risk of churn and provide insights that can support customer retention decisions.**

---

## 📊 Dataset

The project uses a deliberately messy dataset:

**Dataset:** `SmartKart_dirty_100_rows.csv`

* **100 customer records**
* **5 columns**
* Customer ID
* Age
* Monthly Spend
* Complaints
* Churn

The dataset intentionally contains real-world data-quality issues such as:

* Missing values
* Duplicate records
* Incorrect data types
* Invalid values
* Extreme outliers
* Inconsistent text formatting

---

## 🔄 ML Pipeline

The project follows a complete **15-step machine learning workflow**:

```text
Data Collection
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Outlier Detection & Treatment
      ↓
Feature Selection
      ↓
Target Variable Definition
      ↓
Target Encoding
      ↓
Train-Test Split
      ↓
Feature Standardisation
      ↓
Model Building
      ↓
Model Training
      ↓
Prediction
      ↓
Model Evaluation
      ↓
Model Interpretation
      ↓
Business Output
```

---

## 🧹 Data Cleaning

Before training the model, the dataset is cleaned to improve data quality.

Key preprocessing activities include:

* Removing duplicate records
* Removing unnecessary whitespace
* Converting `Age` from text to numeric
* Correcting invalid entries such as `"thirty"`
* Handling unrealistic ages
* Handling negative spending values
* Filling missing values using the **median**
* Verifying that no missing values remain

The cleaning process reduced the dataset from **100 to 95 rows** after removing 5 duplicate records.

---

## 📈 Outlier Treatment

Extreme observations are detected using the **Interquartile Range (IQR) method**.

Examples include:

* Extremely high `Monthly_Spend`
* Unrealistically high `Complaints`

Instead of deleting affected customer records, extreme values are **capped** to reduce their influence on the Logistic Regression model.

---

## 🤖 Machine Learning Model

### Logistic Regression

The project uses **Logistic Regression** as the classification model.

The model predicts whether a customer belongs to:

```text
0 → Not Churned
1 → Churned
```

Logistic Regression is appropriate for this business problem because the target variable is binary.

---

## 🛠️ Technologies Used

| Technology          | Purpose                   |
| ------------------- | ------------------------- |
| Python              | Programming language      |
| Pandas              | Data manipulation         |
| NumPy               | Numerical operations      |
| Matplotlib          | Data visualisation        |
| Seaborn             | Statistical visualisation |
| Scikit-learn        | Machine Learning          |
| Google Colab        | Development environment   |
| Logistic Regression | Churn classification      |

---

## 📁 Project Structure

```text
smartkart-customer-churn-prediction/
│
├── data/
│   └── SmartKart_dirty_100_rows.csv
│
├── notebooks/
│   └── SmartKart_Churn_Prediction_ML_Pipeline.ipynb
│
├── README.md
│
└── requirements.txt
```

---

## 📌 Key Features

* End-to-end ML workflow
* Real-world style dirty-data preprocessing
* Missing-value treatment
* Duplicate detection
* Invalid-value handling
* IQR-based outlier treatment
* Feature selection
* Feature standardisation
* Logistic Regression classification
* Model evaluation
* Business interpretation

---

## 💼 Business Value

A churn prediction system can help a retail/e-commerce company:

* Identify high-risk customers
* Prioritise retention campaigns
* Reduce customer attrition
* Improve customer lifetime value
* Allocate retention budgets more effectively
* Support data-driven CRM decisions

Instead of treating every customer equally, the business can focus retention efforts on customers who are more likely to leave.

---

## ⚠️ Project Limitations

This project is primarily a **demonstration ML pipeline**.

The dataset contains only 100 records and uses a limited number of customer features. Therefore, the model should not be considered production-ready without validation on a larger, representative business dataset.

For a production system, additional features could include:

* Purchase frequency
* Recency
* Customer tenure
* Discount usage
* Average order value
* Website/app activity
* Payment behaviour
* Customer service interactions
* Product category preferences

---

## 🚀 Future Improvements

Potential next steps include:

1. Test additional classification algorithms such as Random Forest, XGBoost, and Gradient Boosting.
2. Perform cross-validation and hyperparameter tuning.
3. Handle class imbalance if present.
4. Add ROC-AUC and Precision-Recall analysis.
5. Build a customer churn-risk dashboard.
6. Deploy the model using Streamlit or Flask.
7. Create an automated prediction pipeline.
8. Monitor model performance after deployment.

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/smartkart-customer-churn-prediction.git
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

Open:

```text
notebooks/SmartKart_Churn_Prediction_ML_Pipeline.ipynb
```

The original notebook is designed to run in **Google Colab** and asks the user to upload the SmartKart CSV dataset.

---

## 📊 Project Outcome

The final outcome is a trained classification model capable of predicting customer churn and translating those predictions into **business-focused customer retention insights**.

---

## 👨‍💻 Project

**SmartKart Customer Churn Prediction**

**Domain:** Retail / E-commerce
**Type:** Supervised Machine Learning
**Task:** Binary Classification
**Model:** Logistic Regression
**Focus:** Customer Retention & Churn Analytics

---

## ⭐ If you find this project useful

Consider giving the repository a ⭐ and following the project for future updates.
