# 🛠️ Defect Analysis Dashboard | Power BI + Machine Learning

This project applies machine learning and data visualization to analyze and reduce manufacturing defects. A Random Forest Classifier was trained to predict defect occurrence, and key insights are presented through an interactive Power BI dashboard. This tool is designed to support operations teams in identifying root causes and improving process performance.

---

## 📌 Project Overview

- **Objective**: Identify key contributors to product defects and visualize actionable insights for decision-making.
- **Approach**: Conduct exploratory analysis, clean and preprocess data, train classification models, and deploy findings in a Power BI dashboard.
- **Outcome**: Delivered a dashboard that helps operations and quality teams understand and mitigate defect risks.

---

## 🔍 Exploratory Data Analysis (EDA)

Before modeling, I conducted EDA to understand data behavior and early defect patterns.

### Key Insights:
- **Maintenance hours** showed the strongest correlation with defect rates.
- **Quality scores** were significantly lower for defective products.
- **Production volume** has moderate correlation but does not show a strong visual separation between defective and non-defective products.
- No missing values were found, but some columns unrelated to process performance were dropped.

### Summary Statistics:
Used `pandas.describe()` to evaluate:
- Mean, median, min, max of process variables
- Distribution of numeric features
- Detection of skew and spread across variables

### Visualizations Used:
- Pairplots for maintanence hours, quality score, and produdction plot
- Correlation heatmap

*EDA supported later feature selection and business interpretation of the model.*

---

## 🤖 Machine Learning Summary

- **Model Used**: Random Forest Classifier
- **Baseline**: Logistic Regression
- **Imbalance Handling**: Used **SMOTE** to balance class distribution, since non-defective parts were a minority class.

### Evaluation Metrics for Defects:
| Metric        | Random Forest | Logistic Regression |
|---------------|----------------|----------------------|
| Accuracy      | 86%            | 78%                  |
| Precision     | 74%            | 65%                  |
| Recall        | 92%            | 59%                  |
| F1 Score      | 82%            | 61%                  |

### Evaluation Metrics for Non-Defects:
| Metric        | Random Forest | Logistic Regression |
|---------------|----------------|----------------------|
| Accuracy      | 86%            | 78%                  |
| Precision     | 52%            | 37%                  |
| Recall        | 59%            | 71%                  |
| F1 Score      | 56%            | 49%                  |

* Random Forest is most effective at identifying defective items, which is critical in manufacturing if missing a defect is costly*
* Random forest offers better balance as seen by a higher F1 score for both defects and non-defects*

---

## 📊 Power BI Dashboard Features

Built an interactive dashboard to visualize:
- **Feature importance** from the model
- **Evaluation metrics** (accuracy, precision, recall, F1)
- **Relationships** between variables and defect status
- **Actionable insights** for operations and quality teams

### Key Dashboard Pages:
1. **Overview**
2. **Model Comparision**

Dashboard allows users to explore how different production factors impact defect likelihood.

---

## 🧠 Skills Demonstrated

- **Exploratory Data Analysis (EDA)**: Analyzed distributions, trends, and outliers using `pandas` and visualizations.
- **Data Cleaning & Feature Selection**: Ensured there were no missing values, removed irrelevant columns to streamline modeling.
- **Supervised Machine Learning**: Trained and evaluated Random Forest and Logistic Regression classifiers.
- **Class Imbalance Handling**: Applied SMOTE and class imbalance to improve detection of rare defect events.
- **Power BI Dashboarding**: Created interactive visualizations and KPIs for stakeholder-friendly communication.
- **Root Cause Identification**: Used model insights to identify maintenance hours and quality score as primary defect drivers.
- **Process Interpretation for Quality Improvement**: Linked statistical and ML insights to potential changes in production and quality practices.
- **Version Control & Documentation**: Managed the project using Git/GitHub and documented all steps clearly.

---

## 🛠️ Tools & Technologies

- **Python**: pandas, scikit-learn, imbalanced-learn (SMOTE)
- **Power BI**: for dashboarding and interactive visualization
- **Jupyter Notebook**: for model development
- **Git & GitHub**: version control and project sharing

---

## 📁 Repository Structure

