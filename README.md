# Lung Cancer Risk Prediction using Machine Learning

## Overview

This project presents an **end-to-end Machine Learning framework for early lung cancer risk prediction** using structured clinical survey data. The workflow includes data preprocessing, exploratory analysis, feature selection, comparative evaluation of multiple machine learning models, and neural network experimentation for binary classification.

The implementation was developed as the primary experimental pipeline for the research paper:

**Machine Learning Framework for Early Lung Cancer Risk Prediction Using Patient-Reported Clinical Data**  
**Conference:** MPCON 2026  
**Status:** Accepted • Presented • Under Press

The objective of this work is to build a reproducible, interpretable, and efficient ML pipeline for healthcare-oriented risk prediction using non-invasive patient-reported data.

---

# Problem Statement

Early lung cancer diagnosis often depends on expensive or invasive diagnostic methods. This project investigates whether **survey-based demographic, lifestyle, and symptom information** can be used to predict lung cancer risk through Machine Learning models.

The goal is to develop an interpretable predictive framework that may support low-cost preliminary risk assessment.

---

# Dataset Description

The dataset contains structured survey-based clinical information including:

### Demographic Features
- Age
- Gender

### Lifestyle Factors
- Smoking
- Alcohol Consumption
- Peer Pressure

### Symptom Indicators
- Coughing
- Wheezing
- Chest Pain
- Fatigue
- Swallowing Difficulty
- Shortness of Breath
- Allergy
- Anxiety
- Yellow Fingers
- Chronic Disease

### Target Variable

```text
1 → Lung Cancer Present
0 → Lung Cancer Absent
```

The problem is treated as a **binary classification task**.

---

# Project Workflow

## 1. Data Preprocessing

Implemented preprocessing pipeline including:

- Duplicate removal
- Missing value imputation (Median / Mode)
- IQR-based outlier detection
- Label encoding
- Min-Max normalization
- Stratified train-test splitting (80:20)

Purpose:
- Reduce noise
- Improve model stability
- Handle skewed distributions
- Improve generalization

---

## 2. Exploratory Data Analysis (EDA)

Performed:

- Feature distribution analysis
- Correlation analysis
- Heatmap visualization
- Class balance inspection
- Relationship analysis among clinical variables

EDA helped identify meaningful patterns before model training.

---

## 3. Feature Selection

Feature selection was performed using:

- Pearson Correlation
- Correlation threshold filtering
- Heatmap-based multicollinearity inspection

Selected variables retained both:

- Statistical relevance
- Clinical interpretability

---

## 4. Machine Learning Models

Implemented and compared multiple classical ML algorithms:

### Classical Models

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Gaussian Naive Bayes
- AdaBoost
- Support Vector Machine (RBF Kernel)

---

## 5. Deep Learning Model

Implemented a Feedforward Neural Network using **TensorFlow/Keras**

Architecture included:

Input Layer → Hidden Layers (ReLU) → Sigmoid Output Layer

Experimented with:

- Different learning rates
- Hidden layers
- Epochs
- Hyperparameter tuning

---

# Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Stratified Cross Validation

Cross-validation was used to improve robustness and reduce overfitting.

---

# Performance Summary

| Model | Accuracy | AUC |
|------|------|------|
| Decision Tree | ~76% | ~0.80 |
| KNN | ~77% | ~0.81 |
| Random Forest | ~81% | ~0.85 |
| Gaussian Naive Bayes | ~75% | ~0.79 |
| AdaBoost | ~80% | ~0.84 |
| Logistic Regression | ~77% | ~0.82 |
| SVM (RBF) | ~80% | ~0.86 |
| Neural Network | ~82% | ~0.86 |

### Observations

- **Random Forest** achieved strong overall stability and interpretability.
- **SVM** produced competitive ROC-AUC performance.
- **Neural Networks** reached comparable accuracy but required additional tuning.
- Ensemble methods performed effectively on limited structured clinical data.

---

# Technologies Used

## Programming

- Python

## Libraries & Frameworks

- NumPy
- pandas
- Matplotlib
- scikit-learn
- TensorFlow / Keras

## Machine Learning Concepts

- Binary Classification
- Feature Engineering
- Statistical Analysis
- Cross Validation
- Hyperparameter Tuning
- Neural Networks
- Model Evaluation

---

# Reproducibility

To ensure reproducible experiments, the workflow includes:

- Fixed random seeds
- Standardized preprocessing
- Consistent train-test splits
- Cross-validation
- Deterministic evaluation pipeline

This improves transparency and benchmarking reliability.

---

# Repository Structure

```text
├── 1stProposal.ipynb          # Complete implementation notebook
├── survey_lung_cancer.csv     # Dataset
├── README.md
```

---

# Key Outcomes

✔ Developed an end-to-end healthcare ML pipeline  
✔ Compared classical ML and Deep Learning approaches  
✔ Achieved ~80–82% predictive accuracy  
✔ Demonstrated reproducible workflow design  
✔ Contributed to an accepted research publication

---

# Future Improvements

Potential extensions include:

- Explainable AI (SHAP / LIME)
- Hyperparameter optimization
- Larger clinical datasets
- Multimodal healthcare prediction
- Integration with medical imaging data
- Deployment using Flask or FastAPI

---

# Research Contribution

This repository contributed to:

**Machine Learning Framework for Early Lung Cancer Risk Prediction Using Patient-Reported Clinical Data**

**Conference:** MPCON 2026  
**Publication Status:** Accepted • Presented • Under Press

---

# Disclaimer

This project is intended solely for **research and educational purposes** and should not be used as an independent clinical diagnostic system.
