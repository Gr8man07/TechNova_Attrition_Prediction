# TechNova Attrition Prediction

## 1. Context

TechNova Solutions, a mid-sized IT services company with 1,200 employees, faces an attrition rate above industry standards. Despite offering competitive salaries and benefits, the company struggles to retain talent—especially in technical and client-facing roles. This turnover increases costs, delays projects, and reduces employee satisfaction.

This project addresses employee attrition, a critical challenge for many organizations. High turnover leads to increased recruitment costs, loss of expertise, and reduced productivity. By analyzing employee data, we aim to uncover patterns and factors that influence whether employees stay or leave. Understanding these drivers enables HR teams to take proactive steps to improve retention.

---

## 2. Problem Statement

Employee attrition affects organizational performance, profitability, and morale. As a Data Scientist at TechNova, my task is to accurately identify employees at risk of leaving based on personal, professional, and behavioral characteristics.

- **Proactive prediction** is essential to replace reactive retention strategies.
- **Targeted interventions** for high performers can enhance retention and optimize resource allocation.

---

## 3. Objective

The primary goal is to develop a machine learning model that predicts whether an employee is likely to leave the company. Additional objectives include:

- Exploring and understanding the dataset thoroughly  
- Identifying key factors influencing employee attrition  
- Preprocessing and transforming data for effective modeling  
- Building and evaluating predictive models  
- Deriving actionable insights and recommendations for HR  

---

## 4. Data Understanding

The dataset (`employee_churn_dataset.csv`) contains various employee-related attributes such as demographics, job information, performance metrics, and churn labels.

### Findings / Observations

- The dataset includes **10,000 rows and 22 columns**, with **no missing values**—a clean foundation for modeling.
- The target variable `Churn` is encoded as **0 (stay)** and **1 (leave)**.
- No duplicate employee records were found, ensuring model integrity.
- Features include both **numerical** (e.g., Tenure, Salary) and **categorical** (e.g., Marital Status, Department) variables.
- Categorical features are properly encoded into binary columns.
- Salary shows high cardinality (9566 unique values), which is expected for a continuous variable.
- Employee ID count matches the total number of rows, confirming uniqueness.

---

## 5. Feature Engineering

### Findings / Observations

- **Workload_Index** may indicate overwork-related churn. It is highly right-skewed (Mean: 24.26, Max: 299.00), suggesting a small group of employees face extreme workloads.
- **Engagement_Score** captures morale and is potentially predictive of churn. It is well-behaved, ranging from 1.0 to 10.99.
- These engineered features enrich the dataset by quantifying employee experience and performance beyond raw metrics.

---

## Repository Contents

- `TechNova_Attrition_Prediction_C0926301.ipynb`: Main notebook with full analysis, modeling, and recommendations
- `README.md`: Project overview and documentation

---

## Notes

- The notebook includes all required sections: context, problem statement, EDA, preprocessing, modeling, evaluation, and recommendations.
- Visualizations and observations are provided throughout to support insights.
- Recommendations are directly tied to model findings to guide HR strategy.

---

## Conclusion

The dataset's imbalance—approximately 20% churn rate—significantly impacted model performance. Across all models, recall for the minority class (churn) ranged from 0.02 to 0.16, indicating a strong bias toward predicting the majority class (non-churn), despite mitigation efforts such as SMOTE and class weighting.

This imbalance limits the model's ability to accurately identify at-risk employees. While feature engineering and hyperparameter tuning provided valuable insights, the results suggest that more advanced resampling techniques or ensemble methods may be necessary to improve future predictions. Alternatively, collecting a more balanced dataset could enhance model generalization.

The current model, particularly logistic regression with a recall of 0.16, serves as a baseline for HR interventions. However, its predictive power for churn remains constrained by this fundamental data challenge.


---


