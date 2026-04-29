## Overview

This project analyzes the CDC's Behavioral Risk Factor Surveillance System (BRFSS) 2015 dataset to predict whether an individual has diabetes using common health indicators. Unlike traditional approaches that prioritize accuracy, this model focuses on **recall (sensitivity)** to ensure high-risk individuals are not missed.

### The Problem
- 37 million Americans have diabetes, and 1 in 5 are unaware
- Healthcare is often reactive rather than preventive
- Late detection leads to severe complications and high costs ($10,000+ per patient annually)

### Our Solution
A predictive model that uses simple lifestyle and health indicators (BMI, age, general health) to flag at-risk individuals before complications develop.

## Key Results

| Metric | Value |
|--------|-------|
| **Best Model** | Decision Tree |
| **Recall (Sensitivity)** | 78.5% |
| **AUC-ROC** | 0.799 |
| **Accuracy** | 68.4% |
| **Dataset Size** | 88,163 patient records |
| **Diabetes Prevalence** | 14% |

### Top 5 Predictors of Diabetes
1. BMI (0.138)
2. Age (0.132)
3. Income (0.090)
4. General Health (0.086)
5. Physical Health Days (0.074)

## Technologies Used

- **Python 3.8+**
- **pandas** - Data cleaning and manipulation
- **NumPy** - Numerical computations
- **scikit-learn** - Machine learning models (Logistic Regression, Random Forest, Decision Tree)
- **Matplotlib** - Data visualization

## Models Compared

| Model | Accuracy | Recall | AUC-ROC | Verdict |
|-------|----------|--------|---------|---------|
| Logistic Regression | 71.4% | 76.4% | 0.812 | Good, more false positives |
| Random Forest | 84.4% | 15.2% | 0.776 | Misses too many diabetics |
| **Decision Tree** | **68.4%** | **78.5%** | **0.799** | **Best at finding at-risk patients** |

## How to Run

### Prerequisites
```bash
pip install pandas numpy scikit-learn matplotlib
