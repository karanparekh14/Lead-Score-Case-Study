# Lead Scoring Case Study

**Building a logistic regression model to identify high-potential sales leads and improve conversion rates.**

**Author:** Karan Parekh

---

## Problem Statement

X Education, an online course provider, acquires thousands of leads daily but converts only ~30%. The sales team wastes effort calling low-potential prospects. The goal: **build a lead scoring model** that assigns scores (0–100) to each lead, enabling the sales team to focus on "Hot Leads" most likely to convert.

---

## Approach

| Step | Description |
|------|------------|
| **Data Cleaning** | Handled missing values, removed columns with >40% nulls, imputed categorical features |
| **EDA** | Analyzed conversion rates across lead sources, occupations, and engagement metrics |
| **Feature Engineering** | Created dummy variables for categorical features, dropped redundant/multicollinear columns |
| **Model Building** | Logistic Regression with Recursive Feature Elimination (RFE) for feature selection |
| **Evaluation** | ROC-AUC, Precision-Recall curves, optimal threshold selection via F1 score |
| **Scoring** | Mapped predicted probabilities to 0–100 lead scores |

---

## Key Results

- **ROC-AUC:** ~0.86 on test set
- **Optimal Threshold:** Selected via precision-recall tradeoff to maximize F1
- **Top Predictors:** Lead source, total time spent on website, last activity type, current occupation
- **Business Impact:** Model enables sales team to prioritize top-scoring leads, significantly improving conversion efficiency

---

## Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn` · `Statsmodels` · `Logistic Regression` · `RFE`

---

## Repository Structure

```
├── Lead Score Case Study_Karan Parekh.ipynb   # Full analysis notebook
├── Leads.csv                                   # Dataset (9,000+ leads)
├── Assignment Subjective Questions.pdf          # Business questions answered
├── Summary.pdf                                  # Executive summary of findings
└── README.md
```

---

## How to Run

```bash
git clone https://github.com/karanparekh14/Lead-Score-Case-Study.git
cd Lead-Score-Case-Study
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
jupyter notebook "Lead Score Case Study_Karan Parekh.ipynb"
```

---

## Pipeline Overview

```
Raw Data (9,000+ leads)
    ↓
Data Cleaning & Imputation
    ↓
Exploratory Data Analysis
    ↓
Feature Engineering (Dummy Variables)
    ↓
Train/Test Split (70/30)
    ↓
Logistic Regression + RFE
    ↓
Model Evaluation (ROC, Precision-Recall)
    ↓
Lead Score Assignment (0–100)
```
