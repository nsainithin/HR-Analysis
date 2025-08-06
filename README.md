# HR-Analysis
# 🚀 Promotion Prediction System

This project aims to automate and accelerate the employee promotion process by predicting promotion eligibility based on historical HR data.

---

## 🧩 Problem Statement

The company currently evaluates employees for promotion through training and assessments, which delays role transitions. This model helps **identify eligible candidates earlier** using a predictive approach.

---

## 📁 Dataset Overview

| File | Description |
|------|-------------|
| `train.csv` | Employee data with promotion outcome |
| `test.csv` | Employee data without outcome (for prediction) |
| `sample_submission.csv` | Required submission format |

---

## 📊 Features Used

- `department`, `region`, `education`, `gender`, `recruitment_channel`
- `no_of_trainings`, `age`, `previous_year_rating`
- `length_of_service`, `KPIs_met >80%`, `awards_won?`, `avg_training_score`

---

## 🛠️ Preprocessing Steps

- Label encoding of categorical features
- Imputation of missing values (`previous_year_rating`)
- Train/test split for internal validation

---

## 🤖 Model

- **Model Used**: `RandomForestClassifier`
- **Handling Imbalance**: `class_weight='balanced'`
- **Validation Accuracy**: 94%
- **F1-score (Promoted Class)**: 43%

---

## 📤 Output

- Final predictions are saved to: `promotion_submission.csv`
- Format: Matches `sample_submission.csv`

---

## 📈 Future Improvements

- Handle class imbalance better using SMOTE or under-sampling
- Try advanced models (XGBoost, LightGBM)
- Feature engineering (department-specific scoring, training effectiveness, etc.)

---

## 📎 How to Run

1. Load `train.csv`, `test.csv`, `sample_submission.csv`
2. Preprocess data
3. Train the model
4. Predict on test set
5. Export `promotion_submission.csv`

---
