# AI-Customer-Churn-Intelligence-System

### Customer Churn Prediction, Explainable AI & Business Intelligence Dashboard

An end-to-end customer churn analytics project that uses **Python, Machine Learning, SHAP Explainable AI, and Power BI** to identify customers at risk of churn, understand the key factors influencing churn, and present actionable business insights through interactive dashboards.

---

## 📌 Project Overview

Customer churn is a major challenge for subscription-based businesses such as telecommunications, SaaS, banking, insurance, and streaming services.

Acquiring a new customer is often more expensive than retaining an existing one. Therefore, identifying customers who are likely to leave allows businesses to prioritize retention efforts and understand the factors contributing to customer churn.

This project develops a complete **Customer Churn Intelligence System** that combines:

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Machine Learning
* Churn Risk Prediction
* Model Evaluation
* SHAP Explainable AI
* Power BI Business Intelligence Dashboard

The project focuses not only on **predicting who may churn**, but also on understanding **why the model considers a customer at risk**.

---

# 🎯 Business Problem

Telecommunication companies have thousands of customers with different:

* Contract types
* Tenure periods
* Monthly charges
* Internet services
* Payment methods
* Support services
* Demographic characteristics

However, not every customer has the same likelihood of leaving.

The business needs a data-driven approach to answer questions such as:

* How many customers are currently churning?
* What is the overall churn rate?
* Which customer groups have higher churn?
* Which contract types are associated with higher churn?
* Which payment methods show higher churn?
* Does customer tenure influence churn?
* Do higher monthly charges relate to churn?
* Which factors contribute most to a customer's predicted churn risk?
* Which customers should be prioritized for further retention analysis?

This project addresses these questions using data analytics, machine learning, explainable AI, and business intelligence.

---

# 🎯 Project Objectives

The main objectives of this project are:

1. Clean and prepare customer churn data for analysis.
2. Explore customer characteristics and churn patterns.
3. Identify important factors associated with customer churn.
4. Engineer useful features for machine learning.
5. Build machine learning classification models to predict churn.
6. Compare model performance using multiple evaluation metrics.
7. Use SHAP to explain model predictions.
8. Identify important churn drivers.
9. Build an interactive Power BI dashboard.
10. Present customer-level and business-level churn insights.

---

# 📊 Dataset

The project uses the **IBM Telco Customer Churn Dataset**.

The dataset contains approximately **7,000+ customer records** with information about customer demographics, services, contracts, billing, tenure, and churn status.

### Main Variables

| Category             | Variables                                                                              |
| -------------------- | -------------------------------------------------------------------------------------- |
| Customer Information | `customerID`, `gender`, `SeniorCitizen`, `Partner`, `Dependents`                       |
| Tenure               | `tenure`                                                                               |
| Phone Services       | `PhoneService`, `MultipleLines`                                                        |
| Internet Services    | `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport` |
| Streaming Services   | `StreamingTV`, `StreamingMovies`                                                       |
| Contract             | `Contract`                                                                             |
| Billing              | `PaperlessBilling`, `PaymentMethod`                                                    |
| Charges              | `MonthlyCharges`, `TotalCharges`                                                       |
| Target Variable      | `Churn`                                                                                |

### Target Variable

The target variable is:

```text
Churn
```

It contains two possible outcomes:

```text
Yes → Customer churned
No  → Customer stayed
```

For machine learning, churn is treated as a **binary classification problem**.

---

# 🛠️ Technology Stack

### Programming & Analysis

* Python
* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn
* Power BI

### Machine Learning

* Scikit-learn
* Logistic Regression
* Decision Tree
* Random Forest

### Explainable AI

* SHAP

### Business Intelligence

* Microsoft Power BI

---

# 🔄 Project Workflow

The complete project workflow is:

```text
Customer Churn Dataset
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Feature Engineering
        ↓
Train/Test Split
        ↓
Machine Learning Models
        ↓
Model Evaluation
        ↓
Churn Prediction
        ↓
SHAP Explainability
        ↓
Power BI Dashboard
        ↓
Business Insights
```
---

# 🧹 1. Data Cleaning

Before performing analysis and machine learning, the dataset was cleaned and prepared.

### Data Preparation Steps

* Inspected the dataset structure.
* Checked for missing values.
* Identified incorrect or inconsistent data types.
* Converted numerical fields into appropriate numerical formats.
* Handled missing values.
* Examined categorical variables.
* Prepared the target variable for machine learning.
* Removed `customerID` from the machine learning features because it is an identifier and does not provide predictive information.

### Target Encoding

The `Churn` variable was converted into a binary format:

```text
Yes → 1
No  → 0
```

This allowed the problem to be treated as a binary classification task.

---

# 📈 2. Exploratory Data Analysis

Exploratory Data Analysis was performed to understand customer behavior and identify patterns associated with churn.

The analysis focused on:

### Customer Demographics

* Gender
* Senior Citizen status
* Partner
* Dependents

### Customer Services

* Phone Service
* Multiple Lines
* Internet Service
* Online Security
* Online Backup
* Device Protection
* Tech Support
* Streaming TV
* Streaming Movies

### Customer Relationship

* Tenure
* Contract type

### Billing Information

* Monthly Charges
* Total Charges
* Payment Method
* Paperless Billing

---

# 📊 Key EDA Questions

The analysis investigates questions such as:

* Does churn vary by contract type?
* Which internet service category has higher churn?
* Is churn different across payment methods?
* Does shorter customer tenure relate to higher churn?
* Are customers with higher monthly charges more likely to churn?
* How does total customer spending differ between churned and retained customers?
* Which customer segments demonstrate higher churn levels?

These analyses help establish relationships between customer characteristics and churn behavior before applying machine learning.

---

# ⚙️ 3. Feature Engineering

Feature engineering was performed to prepare meaningful variables for machine learning.

The objective was to transform the available customer information into a format that could be effectively used by classification models.

The feature engineering process focused on areas such as:

* Customer tenure
* Monthly charges
* Customer service usage
* Contract characteristics
* Billing characteristics
* Customer engagement indicators
* Risk-related customer attributes

Categorical variables were encoded into numerical representations suitable for machine learning.

---

# 🤖 4. Machine Learning

The project treats customer churn prediction as a **binary classification problem**.

The models used in the project are:

### 1. Logistic Regression

Logistic Regression was used as a baseline classification model.

It estimates the probability of a customer belonging to the churn or non-churn class.

---

### 2. Decision Tree

The Decision Tree model was used to identify patterns in customer attributes that can separate churned and retained customers.

Decision Trees are also relatively easy to interpret because predictions are based on a sequence of decision rules.

---

### 3. Random Forest

Random Forest combines multiple decision trees to improve predictive performance and reduce dependence on a single tree.

It was used to capture more complex relationships between customer characteristics and churn.

---

# 📏 5. Model Evaluation

The models were evaluated using multiple classification metrics.

### Accuracy

Measures the percentage of total predictions that were correct.

```text
Accuracy =
Correct Predictions / Total Predictions
```

### Precision

Measures how many customers predicted as churners actually churned.

```text
Precision =
True Positives / (True Positives + False Positives)
```

### Recall

Measures how many actual churners were correctly identified.

```text
Recall =
True Positives / (True Positives + False Negatives)
```

### F1-Score

Provides a balance between Precision and Recall.

```text
F1 Score =
2 × (Precision × Recall) /
(Precision + Recall)
```

### ROC-AUC

Measures the model's ability to distinguish between churned and non-churned customers across different classification thresholds.

### Confusion Matrix

The confusion matrix was used to understand:

* True Positives
* True Negatives
* False Positives
* False Negatives

---

# 📊 Model Performance

Model performance should be reported using the **actual results generated by the final notebook/model**.

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------: | --------: | -----: | -------: | ------: |
| Logistic Regression |        — |         — |      — |        — |       — |
| Decision Tree       |        — |         — |      — |        — |       — |
| Random Forest       |        — |         — |      — |        — |       — |

> **Important:** Replace the `—` values with the actual model results from your final notebook. Do not use an estimated accuracy or performance value.

---

# 🔍 6. Explainable AI with SHAP

A major component of this project is **Explainable AI using SHAP**.

Machine learning models can predict whether a customer is likely to churn, but a business also needs to understand:

> **Why does the model consider this customer at risk?**

SHAP helps answer this question.

---

# 🧠 What is SHAP?

**SHAP** stands for:

> **SHapley Additive exPlanations**

SHAP explains the contribution of individual features toward a model's prediction.

For example, a customer's prediction may be influenced by factors such as:

* Monthly Charges
* Tenure
* Contract Type
* Internet Service
* Payment Method
* Customer Services

SHAP allows these factors to be analyzed at both:

### Global Level

Understanding which features are generally important across the dataset.

### Individual Customer Level

Understanding why a particular customer's predicted churn risk is high or low.

---

# 📊 SHAP Analysis

The project uses SHAP visualizations to analyze model behavior.

### SHAP Summary Plot

Shows the overall importance and impact of features across customers.

### SHAP Bar Plot

Provides a simplified view of the most important features.

### SHAP Waterfall Plot

Explains how individual features contribute to one customer's prediction.

### SHAP Force Plot

Provides a detailed visualization of the features pushing a prediction toward or away from churn.

---

# 🎯 Customer Risk Analysis

The churn prediction system can be used to identify customers with higher predicted churn probability.

A customer-level risk analysis can include:

| Customer   | Churn Probability | Contract | Monthly Charges |     Tenure |
| ---------- | ----------------: | -------- | --------------: | ---------: |
| Customer A |      Model Output | Monthly  |      Model Data | Model Data |
| Customer B |      Model Output | Annual   |      Model Data | Model Data |

The purpose is to help businesses prioritize customers for further investigation and retention analysis.

> The model provides **risk predictions**, not guaranteed outcomes.

---

# 📊 7. Power BI Dashboard

The machine learning and analytical results are presented through an interactive Power BI dashboard.

# 💡 Business Insights

The project is designed to help identify patterns such as:

* Customer churn varies across contract types.
* Customers with shorter tenure can represent an important churn-risk segment.
* Monthly charges can be an important factor in churn analysis.
* Payment methods can show different churn patterns.
* Internet service type can be associated with different churn levels.
* Machine learning can help prioritize customers based on predicted churn probability.
* SHAP helps explain which features contribute to individual predictions.

The exact business conclusions should be interpreted from the final dataset, model results, and Power BI dashboard.

---

# 💼 Business Value

The system can support businesses in several ways:

### 1. Early Risk Identification

Identify customers with higher predicted churn probability.

### 2. Customer Segmentation

Understand which customer groups demonstrate higher churn patterns.

### 3. Churn Driver Analysis

Identify the factors that contribute most strongly to model predictions.

### 4. Explainable Predictions

Use SHAP to make machine learning predictions easier to interpret.

### 5. Business Reporting

Use Power BI to communicate churn trends and KPIs to business stakeholders.

### 6. Retention Prioritization

Help analysts and business teams prioritize customers for further retention analysis.

---

# 🏗️ End-to-End Architecture

```text
                 ┌──────────────────────┐
                 │   Telco Customer     │
                 │       Dataset        │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │    Data Cleaning     │
                 │  Missing Values      │
                 │  Data Types          │
                 │  Data Preparation    │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │        EDA           │
                 │ Customer Behavior    │
                 │ Churn Patterns       │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Feature Engineering  │
                 │ Encoding & Features  │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Machine Learning     │
                 │ Logistic Regression  │
                 │ Decision Tree        │
                 │ Random Forest        │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │  Model Evaluation    │
                 │ Accuracy             │
                 │ Precision            │
                 │ Recall               │
                 │ F1-Score             │
                 │ ROC-AUC              │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │   SHAP Explainability│
                 │ Feature Importance   │
                 │ Customer Explanation │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │     Power BI         │
                 │ Interactive Dashboard│
                 │ KPIs & Insights      │
                 └──────────────────────┘
```

---

# 📦 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/AI-Customer-Churn-Intelligence-System.git
```

Navigate to the project directory:

```bash
cd AI-Customer-Churn-Intelligence-System
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment.

### Windows

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
source venv/bin/activate
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

# 📚 Python Libraries

The project uses libraries such as:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
shap
jupyter
```

If additional libraries are used in the final notebooks, add them to `requirements.txt`.

---

# 🚀 How to Run the Project

### Step 1 — Load the Dataset

Place the dataset inside:

```text
data/
```

### Step 2 — Run Data Cleaning

Open:

```text
notebooks/01_Data_Cleaning.ipynb
```

Run the notebook to prepare the dataset.

### Step 3 — Perform EDA

Open:

```text
notebooks/02_EDA.ipynb
```

Explore customer behavior and churn patterns.

### Step 4 — Feature Engineering

Open:

```text
notebooks/03_Feature_Engineering.ipynb
```

Prepare the dataset for machine learning.

### Step 5 — Train Models

Open:

```text
notebooks/04_Model_Training.ipynb
```

Train and evaluate the classification models.

### Step 6 — SHAP Analysis

Open:

```text
notebooks/05_SHAP_Explainability.ipynb
```

Analyze feature importance and individual predictions.

### Step 7 — Power BI

Open:

```text
dashboard/Customer_Churn_Dashboard.pbix
```

Explore the interactive dashboard.

---

# 📸 Dashboard Preview

Add screenshots of your Power BI dashboard to the repository.

Example:

```markdown
## Executive Dashboard

![Executive Dashboard](reports/executive_dashboard.png)
```

```markdown
## Customer Insights

![Customer Insights](reports/customer_insights.png)
```

```markdown
## Churn Intelligence

![Churn Intelligence](reports/churn_intelligence.png)
```

```markdown
## SHAP Analysis

![SHAP Analysis](reports/shap_analysis.png)
```

---

# 📈 Project Outcomes

This project demonstrates an end-to-end approach to customer churn analytics:

* Cleaned and prepared a real-world telecom customer dataset.
* Performed exploratory data analysis to identify churn patterns.
* Created features suitable for machine learning.
* Built multiple classification models.
* Evaluated models using multiple performance metrics.
* Generated customer churn predictions.
* Used SHAP to explain machine learning predictions.
* Identified important churn-related features.
* Developed an interactive Power BI dashboard.
* Converted analytical results into business-oriented insights.

---

# 🔮 Future Enhancements

The current project focuses on **churn prediction, explainability, and business intelligence**.

Potential future improvements include:

### 1. Automated Retention Recommendations

A future version could use a local Large Language Model to convert SHAP explanations into personalized retention recommendations.

Possible architecture:

```text
Churn Prediction
       ↓
SHAP Explanation
       ↓
Customer Risk Factors
       ↓
Local LLM
       ↓
Personalized Retention Recommendation
```

### 2. Model Deployment

Deploy the churn prediction model using:

* Streamlit
* Flask
* FastAPI

### 3. Automated Customer Risk Scoring

Create automated risk categories such as:

```text
Low Risk
Medium Risk
High Risk
```

### 4. Production-Ready Feature Pipeline

A more production-oriented preprocessing pipeline could use:

* `Pipeline`
* `ColumnTransformer`
* `OneHotEncoder`

### 5. Model Monitoring

Monitor:

* Prediction performance
* Data drift
* Feature drift
* Churn distribution
* Model performance over time

---

# ⚠️ Limitations

* The dataset represents a specific telecom customer population and may not generalize to every business.
* Machine learning predictions represent estimated churn risk and are not guaranteed outcomes.
* SHAP explains model behavior; it does not establish that a feature causes churn.
* Business recommendations should be validated using actual customer and business data.
* Model performance depends on the quality and characteristics of the available dataset.

---

# 🎓 Skills Demonstrated

This project demonstrates practical experience in:

### Data Analytics

* Data Cleaning
* Exploratory Data Analysis
* Data Validation
* Feature Engineering
* Customer Analytics
* Churn Analysis

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn

### Machine Learning

* Classification
* Logistic Regression
* Decision Trees
* Random Forest
* Model Evaluation
* Confusion Matrix
* ROC-AUC

### Explainable AI

* SHAP
* Feature Importance
* Individual Prediction Explanation

### Power BI

* Dashboard Development
* KPI Tracking
* Data Visualization
* Interactive Filters
* Business Intelligence
* Customer Risk Analysis

---

# ⭐ Project Highlights

```text
✔ End-to-End Customer Churn Analytics
✔ 7,000+ Telecom Customer Records
✔ Data Cleaning & EDA
✔ Feature Engineering
✔ Multiple Machine Learning Models
✔ Churn Probability Prediction
✔ SHAP Explainable AI
✔ Customer-Level Risk Analysis
✔ Interactive Power BI Dashboard
✔ Business-Oriented Churn Insights
```

---

# 📌 Important Scope Note

The completed project focuses on:

```text
Data Cleaning
      ↓
EDA
      ↓
Feature Engineering
      ↓
Machine Learning
      ↓
Churn Prediction
      ↓
SHAP Explainability
      ↓
Power BI Dashboard
```

An automated **LLM-based retention recommendation system** is considered a future enhancement and is **not part of the completed implementation**.

---

# 👨‍💻 Author

**Sowrabh Bidarkar**

Data Analyst | Business Analytics

### Skills

Python • Machine Learning • Power BI • Data Analytics 

---

# 📄 Disclaimer

This project is created for educational, analytical, and portfolio purposes.

The predictions generated by the machine learning models represent estimated churn risk based on the available dataset and should not be interpreted as guaranteed customer behavior.

Business decisions should be made using appropriate business context, additional customer information, and validated analysis.
