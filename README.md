# 🎓 Smart Outcome Predictor

A machine learning project for predicting **student course completion status** and **final course scores** using ensemble learning techniques.

The project explores multiple ensemble methods including **Bagging, AdaBoost, Gradient Boosting, LightGBM, XGBoost, Voting, and Stacking**.

---

## 📌 Project Overview

The **Smart Outcome Predictor** uses student learning and course-related data to build machine learning models for two prediction tasks:

### 🎯 Classification
Predict whether a student will complete the course.

**Target:** `completion_status`

### 📊 Regression
Predict the student's final course score.

**Target:** `final_score`

The project compares different ensemble learning techniques and evaluates their performance using appropriate classification and regression metrics.

---

## 📂 Dataset

The project uses:

`Smart_Outcome_Predictor_Dataset_5200.csv`

### Dataset Size

- 📌 **Rows:** 5,200
- 📌 **Features:** 19 columns
- 📌 **Duplicate Rows:** 0
- 📌 **Duplicate Student IDs:** 0

### 🎯 Target Variables

| Task | Target |
|---|---|
| Classification | `completion_status` |
| Regression | `final_score` |

---

## 🧹 Data Preparation

The following preprocessing steps were performed:

- 🔍 Checked the first few rows
- 📋 Checked dataset information
- 📐 Checked dataset shape
- ❌ Checked missing values
- 🔢 Identified numerical columns
- 🔤 Identified categorical columns
- 🔄 Converted categorical features into numerical values using **Label Encoding**
- 🧩 Used **KNN Imputer** for missing numerical values
- ✂️ Split the data into training and testing sets

### Train-Test Split

The dataset was divided into:

- 🏋️ **80% Training Data**
- 🧪 **20% Testing Data**

For classification, stratified splitting was used to maintain the class distribution.

---

# 🧠 Ensemble Learning Techniques

## 1️⃣ Bagging

**Bagging (Bootstrap Aggregating)** trains multiple models and combines their predictions.

### Models Used

- 🌳 Decision Tree Classifier
- 🌳 Decision Tree Regressor

The project uses **100 estimators** for Bagging.

Bagging is useful for reducing model variance and improving stability.

---

## 2️⃣ AdaBoost

**AdaBoost** trains weak learners sequentially.

Each new learner focuses more on the observations that were incorrectly predicted by previous learners.

### Parameters

- `n_estimators = 100`
- `learning_rate = 0.1`

Both classification and regression versions were implemented.

---

## 3️⃣ Gradient Boosting

Gradient Boosting builds models sequentially to reduce prediction errors made by previous models.

### Parameters

- `n_estimators = 100`
- `learning_rate = 0.1`

Both:

- 📌 Gradient Boosting Classifier
- 📌 Gradient Boosting Regressor

were implemented.

---

## 4️⃣ LightGBM ⚡

**LightGBM** is a gradient boosting framework designed for efficient and fast model training.

The project implements:

- 🟢 `LGBMClassifier`
- 🔵 `LGBMRegressor`

### Parameters

- `n_estimators = 100`
- `learning_rate = 0.1`

---

## 5️⃣ XGBoost 🚀

**XGBoost** is an optimized gradient boosting algorithm that provides strong performance on structured/tabular datasets.

The project implements:

- 🟢 `XGBClassifier`
- 🔵 `XGBRegressor`

### Parameters

- `n_estimators = 100`
- `learning_rate = 0.1`
- `max_depth = 4`

---

# 🤝 Voting Ensemble

The project uses three different classification models:

- 📈 Logistic Regression
- 📍 K-Nearest Neighbors
- 🎯 Support Vector Classifier

### Hard Voting

The final prediction is selected based on the majority vote of the individual models.

### Soft Voting

The predicted probabilities of the models are combined to make the final prediction.

Both **Hard Voting** and **Soft Voting** are compared in the project.

---

# 🧩 Stacking Ensemble

Stacking combines multiple base models and uses another model to make the final prediction.

## Classification Stacking

### Base Models

- Logistic Regression
- KNN
- SVC

### Final Estimator

- Logistic Regression

---

## Regression Stacking

### Base Models

- Random Forest Regressor
- Gradient Boosting Regressor

### Final Estimator

- Linear Regression

---

# 📊 Model Evaluation

Different metrics are used for classification and regression.

## 🟢 Classification Metrics

The classification models are evaluated using:

- ✅ Accuracy
- 🎯 Precision
- 🔄 Recall
- ⭐ F1 Score
- 📈 ROC-AUC

---

## 🔵 Regression Metrics

The regression models are evaluated using:

- 📉 MAE — Mean Absolute Error
- 📉 RMSE — Root Mean Squared Error
- 📈 R² Score

### Metric Interpretation

| Metric | Better Result |
|---|---|
| Accuracy | Higher |
| Precision | Higher |
| Recall | Higher |
| F1 Score | Higher |
| ROC-AUC | Higher |
| MAE | Lower |
| RMSE | Lower |
| R² Score | Higher |

---

# 📋 Model Comparison

The project compares the following classification models:

| Model |
|---|
| 🌳 Bagging |
| 🚀 AdaBoost |
| 📈 Gradient Boosting |
| ⚡ LightGBM |
| 🚀 XGBoost |
| 🤝 Voting |
| 🧩 Stacking |

### Regression Models

| Model |
|---|
| 🌳 Bagging |
| 🚀 AdaBoost |
| 📈 Gradient Boosting |
| ⚡ LightGBM |
| 🚀 XGBoost |
| 🧩 Stacking |

The final comparison tables are generated using Pandas.

---

# 🛠️ Technologies Used

### Programming Language

🐍 Python

### Libraries

- 🐼 Pandas
- 🔢 NumPy
- 📊 Matplotlib
- 🤖 Scikit-learn
- ⚡ LightGBM
- 🚀 XGBoost

---

# 📦 Main Scikit-learn Components

The project uses:

- `model_selection`
- `preprocessing`
- `impute`
- `tree`
- `linear_model`
- `ensemble`
- `metrics`
- `neighbors`
- `svm`

---

# 📁 Project Structure

```text
Smart-Outcome-Predictor/
│
├── 📓 Smart_Outcome_Predictor.ipynb
├── 📄 Smart_Outcome_Predictor_Dataset_5200.csv
└── 📖 README.md
