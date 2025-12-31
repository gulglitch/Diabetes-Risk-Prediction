# Diabetes Risk Prediction

A machine learning project that predicts diabetes risk using clinical health indicators, achieving **97.75% ROC-AUC** with XGBoost.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-1.5+-green.svg)

## Overview

This project develops predictive models to identify individuals at risk of diabetes using health metrics like BMI, blood glucose levels, HbA1c, and lifestyle factors. Designed as a **screening tool** to enable early intervention and preventive care.

## Key Results

| Model | Accuracy | Recall | ROC-AUC |
|-------|----------|--------|---------|
| Logistic Regression | 89.13% | 87% | 0.9622 |
| Random Forest | 90.83% | 89% | 0.9746 |
| **XGBoost** | **89.51%** | **93%** | **0.9775** |

> **XGBoost** catches **93% of diabetes cases** — critical for medical screening where missing a diagnosis has serious consequences.

## Dataset Features

- **Demographics**: Age, Gender
- **Health Metrics**: BMI, Blood Glucose Level, HbA1c Level
- **Medical History**: Hypertension, Heart Disease
- **Lifestyle**: Smoking History
- **Target**: Diabetes (Binary)

**Dataset Size**: 100,000 records

## Pipeline

```
Data Cleaning → EDA → Feature Engineering → Model Training → Evaluation
```

### Feature Engineering Highlights
- Glucose & HbA1c grouped by medical thresholds
- Smoking history simplified to risk levels
- Composite health risk score (hypertension + heart disease)
- Senior high-risk flag (age ≥ 60 with heart conditions)

## Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/Diabetes-Risk-Prediction.git

# Install dependencies
pip install pandas numpy scikit-learn xgboost matplotlib seaborn

# Run the notebook
jupyter notebook PROJECT_Diabetes_Risk_Prediction.ipynb
```

## Visualizations

The project includes comprehensive EDA:
- Distribution plots for all features
- Correlation heatmaps
- Box plots for outlier detection
- ROC curves comparing all models
- Pair plots by diabetes status

## Clinical Relevance

This model prioritizes **high recall** over precision — ideal for medical screening where:
- False positives → Additional testing (low risk)
- False negatives → Missed diagnosis (high risk)


## License

MIT License - feel free to use and modify for your projects.

---

<p align="center">
  <i>Early detection saves lives.</i>
</p>
