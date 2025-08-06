# HR-Analysis
# 🚀 Promotion Prediction System

This project aims to automate and accelerate the employee promotion process by predicting promotion eligibility based on historical HR data.

---

## 🧩 Problem Statement

The company currently evaluates employees for promotion through training and assessments, which delays role transitions. This model helps **identify eligible candidates earlier** using a predictive approach.

---

## 📁 Dataset Overview

| File | Description | Link |
|------|-------------|-------|
| `train.csv` | Employee data with promotion outcome |https://github.com/nsainithin/HR-Analysis/blob/main/Training%20dataset/train.csv |
| `test.csv` | Employee data without outcome (for prediction) | https://github.com/nsainithin/HR-Analysis/blob/main/Testing%20dataset/test.csv |
| `sample_submission.csv` | Required submission format | https://github.com/nsainithin/HR-Analysis/blob/main/Output/sample_submission.csv |

---

## 📊 Features Used
| Variable	| Definition |
|-----------|------------|
|employee_id |	Unique ID for employee|
|department |	Department of employee|
|region |	Region of employment (unordered)|
|education |	Education Level|
|gender |	Gender of Employee|
|recruitment_channel |	Channel of recruitment for employee|
|no_of_trainings |	no of other trainings completed in previous year on soft skills, technical skills etc.|
|age |	Age of Employee|
|previous_year_rating |	Employee Rating for the previous year|
|length_of_service |	Length of service in years|
||KPIs_met >80% |	if Percent of KPIs(Key performance Indicators) >80% then 1 else 0|
|awards_won? |	if awards won during previous year then 1 else 0|
|avg_training_score |	Average score in current training evaluations|
|is_promoted |	(Target) Recommended for promotion|


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
