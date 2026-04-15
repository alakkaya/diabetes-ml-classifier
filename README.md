# Diabetes Prediction using Machine Learning

## Overview

This project predicts diabetes diagnosis using health indicators from the BRFSS dataset using Logistic Regression, Random Forest, and Gradient Boosting models.

## Dataset

- **Source**: UCI Machine Learning Repository - Diabetes Binary Health Indicators
- **Instances**: 253,680 samples
- **Features**: 21 health indicators
- **Target**: Diabetes_binary (0: Healthy, 1: Diabetic)
- **Class Distribution**: 86.1% healthy, 13.9% diabetic

## Best Model Performance

| Metric   | Score  |
| -------- | ------ |
| ROC-AUC  | 0.8269 |
| Recall   | 0.8567 |
| F1-Score | 0.4174 |
| PR-AUC   | 0.4230 |

**Model**: Gradient Boosting (optimized with GridSearchCV)

## Quick Start

### Installation

```bash
# Clone repository
git clone https://github.com/alakkaya/diabetes-ml-classifier.git
cd diabetes-ml-classifier

# Install dependencies
pip install -r requirements.txt
```

### Running the Analysis

**Option 1: Using Jupyter Notebook**

```bash
jupyter notebook notebook.ipynb
```

**Option 2: Using Anaconda Navigator (GUI)**

- Open Anaconda Navigator
- Launch Jupyter Notebook
- Navigate to the project folder
- Open `notebook.ipynb`

The notebook contains:

- Data exploration and preprocessing
- Class imbalance analysis (outlier handling, missing values)
- Model development: Logistic Regression, Random Forest, Gradient Boosting
- Hyperparameter tuning with GridSearchCV
- Model evaluation with ROC/PR curves and confusion matrices

## Project Structure

```
├── notebook.ipynb          # Complete analysis & modeling
├── requirements.txt        # Python dependencies
├── README.md              # This file
├── data/
│   └── diabetes_binary_health_indicators_BRFSS2015.csv
```

## Key Findings

- Class imbalance required F1-Score and ROC-AUC metrics (not Accuracy)
- Top predictive features: GenHlth, HighBP, BMI
- Optimal threshold: 0.1 (maximizes disease detection)

## Contributors

- Ali Akkaya
- Sümeyye Cücü
