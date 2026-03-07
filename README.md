# Bank Customer Churn Analysis & Prediction

## Overview
Customer churn is a critical issue in the banking industry. Retaining existing customers is significantly more cost-effective than acquiring new ones.

This project analyzes **165,000+ banking customer records** to identify the key behavioral and financial factors that contribute to customer churn and builds predictive models to detect customers at risk of leaving.

The project integrates **data analysis, statistical testing, machine learning models, and explainable AI techniques** to generate insights that support customer retention strategies.

---

## Dataset

The dataset contains **165K+ customer records** with demographic, financial, and behavioral attributes.

### Features

| Feature | Description |
|------|------|
| CreditScore | Customer credit score |
| Geography | Customer country |
| Gender | Customer gender |
| Age | Customer age |
| Tenure | Years with the bank |
| Balance | Customer account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Whether customer has a credit card |
| IsActiveMember | Whether customer is an active member |
| EstimatedSalary | Estimated annual salary |
| Exited | Target variable (1 = churn, 0 = retained) |

---

## Project Workflow

### 1. Data Cleaning
- Removed identifier variables (`CustomerId`, `Surname`)
- Checked and removed duplicate records
- Verified dataset consistency

---

### 2. Exploratory Data Analysis (EDA)

EDA was conducted to understand data distribution and customer characteristics.

Key analysis included:
- Distribution analysis of continuous variables
- Categorical variable analysis
- Outlier detection
- Customer segmentation patterns

Visualization techniques used:
- Histogram
- KDE plots
- Count plots
- Correlation heatmaps

---

### 3. Statistical Testing

Statistical tests were applied to evaluate relationships between variables and churn.

Methods used:
- **ANOVA** to test differences between groups
- **Correlation analysis** for numerical variables
- **Cramer's V** for categorical relationships

These tests helped determine which features have significant statistical relationships with churn.

---

### 4. Feature Engineering

Data preprocessing included:

- One-hot encoding for categorical variables
- Binary encoding for gender
- Feature scaling using **MinMaxScaler**
- Outlier detection using **IQR and DBSCAN**

These steps improved model performance and data quality.

---

### 5. Handling Class Imbalance

The dataset contains an imbalance between churned and retained customers.

To address this issue:

**SMOTEENN** was applied:
- **SMOTE** generates synthetic minority samples
- **ENN (Edited Nearest Neighbors)** removes noisy samples

This improves model performance on the minority class.

---

### 6. Machine Learning Models

Several classification models were implemented:

- Logistic Regression
- Decision Tree
- Artificial Neural Network (ANN)

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Special focus was placed on **recall for churn detection**, since missing a churned customer has a high business cost.

---

### 7. Model Explainability

To interpret model predictions, **SHAP (SHapley Additive exPlanations)** was used.

SHAP helps identify:
- Global feature importance
- Individual prediction explanations

This improves transparency and helps translate model outputs into business insights.

---

## Key Insights

Key factors influencing customer churn include:

- **Inactive customers are significantly more likely to churn**
- **Customer age has a strong relationship with churn probability**
- **Customers using fewer products tend to churn more often**
- **Account balance patterns may indicate potential churn risk**

These insights can help banks design more effective retention strategies.

---

## Tools & Technologies

Programming language:
- Python

Libraries used:
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- scikit-learn
- statsmodels
- imbalanced-learn
- shap
- yellowbrick

---

## Project Structure

```
Bank-Churn-Analysis
│
├── data
│   └── dataset.csv
│
├── notebooks
│   └── churn_analysis.ipynb
│
├── images
│   └── visualizations
│
└── README.md
```

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/yourusername/bank-churn-analysis.git
```

Install required packages:

```bash
pip install -r requirements.txt
```

Run the notebook:

```
jupyter notebook
```

Open the notebook and execute the cells.

---

## Business Value

This analysis enables banks to:

- Identify customers at high risk of leaving
- Design targeted retention strategies
- Improve customer satisfaction
- Reduce revenue loss caused by churn

Predictive analytics can significantly improve long-term customer retention.

---

## Author

Nguyen Trung  
Aspiring Data Analyst
