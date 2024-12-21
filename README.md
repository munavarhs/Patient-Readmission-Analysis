# Hospital Readmission Prediction

## Overview
Hospital readmissions, particularly within 30 days of discharge, are a significant issue in healthcare. This project leverages **machine learning** to predict the likelihood of readmissions using patient data, enabling healthcare providers to target high-risk patients and improve outcomes.

---

## Problem Statement
Hospital readmissions pose challenges in terms of:
- **Financial Costs**: Increased costs and penalties due to programs like the Hospital Readmissions Reduction Program (HRRP).
- **Patient Health**: Unresolved health issues leading to poorer outcomes.
- **Resource Allocation**: Inefficient utilization of hospital resources.

Our solution uses predictive modeling to address these issues by identifying patients likely to be readmitted.

---

## Dataset
We utilized a publicly available dataset from [Kaggle](https://www.kaggle.com/datasets/gbiamgaurav/patient-survival-prediction), containing:
- **Records**: 91,713 patient entries.
- **Features**: 186 attributes, expanded to 239 after preprocessing.
- Key features include:
  - Demographics (age, gender, ethnicity).
  - Clinical measures (glucose levels, heart rate, BMI).
  - Admission details (ICU ID, prior visits, readmission status).

---

## Methods
We implemented the following **machine learning models** for binary classification:
1. **Logistic Regression**: Provided a baseline for comparison.
2. **Random Forest**: Captured complex relationships with hyperparameter tuning.
3. **Gradient Boosting**: Improved accuracy with iterative optimization.
4. **XGBoost Classifier**: Handled class imbalance effectively.
5. **Ensemble Model**: Combined predictions from Random Forest and XGBoost for superior performance.
6. **Decision Tree**: Used as a benchmark.
7. **Naive Bayes**: Provided a simpler probabilistic approach.

### Preprocessing Steps
1. **Data Cleaning**: Removed duplicates and handled missing values.
2. **Feature Engineering**: Added "prior visits" as a new feature.
3. **Encoding**: Converted categorical variables using one-hot encoding.
4. **Scaling**: Normalized numerical columns for balanced feature importance.

---

## Results
| Model                | Accuracy | Precision (Class 1) | Recall (Class 1) | AUC-ROC |
|----------------------|----------|---------------------|------------------|---------|
| Logistic Regression  | 91.9%    | 0.54                | 0.63             | 0.87    |
| Random Forest        | 92.3%    | 0.54                | 0.68             | 0.89    |
| Gradient Boosting    | 92.7%    | 0.62                | 0.66             | 0.87    |
| XGBoost Classifier   | 93.0%    | 0.63                | 0.70             | 0.90    |
| **Ensemble Model**   | **93.3%**| **0.65**            | **0.72**         | **0.91**|
| Decision Tree        | 90.2%    | 0.52                | 0.61             | 0.86    |
| Naive Bayes          | 80.0%    | 0.25                | 0.67             | 0.82    |

### Key Observations
- **Ensemble Model** achieved the best performance with 93.3% accuracy and an AUC-ROC of 0.91.
- **SHAP analysis** highlighted the most impactful features for predictions, enhancing model interpretability.

---

## Impact
- **Healthcare Providers**: Improved patient care through targeted interventions.
- **Hospitals**: Reduced readmission rates, saving costs and resources.
- **Patients**: Better health outcomes and fewer complications.

---

## Contributions
- **Munavar Hussain**: Model selection and evaluation.
- **Sujith Reddy A**: Hyperparameter tuning, data analysis, and report writing.
- **Irfan Mohammed**: Data preprocessing and feature engineering.

---

## Installation and Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/munavarhs/Patient-Readmission-Analysis/
   ```

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
