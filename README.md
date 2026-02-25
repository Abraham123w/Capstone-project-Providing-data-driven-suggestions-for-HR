# Employee Attrition Prediction: Salifort Motors 📊🤖

## Project Overview
This repository contains the Capstone Project for the **Google Advanced Data Analytics Professional Certificate**. It applies exploratory data analysis (EDA) and Machine Learning to identify the primary drivers of employee turnover within a consulting firm (Salifort Motors). 

Moving beyond standard descriptive dashboards, this analysis utilizes Python to uncover systemic organizational patterns and builds a predictive model to proactively flag at-risk employees before they leave.

## 💡 Key Business Insights
The algorithm revealed that turnover is not primarily driven by salary, but by structural resource allocation issues:
* **The "Hustle Culture" Risk:** Employees assigned to 6-7 projects work between 250 and 300 hours a month, resulting in a turnover rate near 100%. They do not leave due to a lack of capability; they flee from severe burnout.
* **The Talent Paradox:** The company's highest-rated performers (evaluations between 0.8 and 1.0) are leaving at an accelerated rate. The data mathematically demonstrates that the system punishes efficiency by rewarding it with heavier workloads.
* **The Attrition Window:** Employees with 3 to 5 years of tenure are at the highest risk of leaving, indicating a critical period where retention strategies must be focused.

## ⚙️ Technical Approach & Methodology
1. **Data Preprocessing & EDA:** Cleaned a dataset of 15,000 records. Validated assumptions using Variance Inflation Factor (VIF) for multicollinearity and Cook's Distance for influence diagnostics.
2. **Baseline Model (Logistic Regression):** Built for interpretability, but failed to capture non-linear relationships. It yielded a very low Recall (0.21), meaning it missed almost 80% of the employees who actually quit.
3. **Optimized Model (Random Forest):** Developed an ensemble tree-based model and tuned hyperparameters using `GridSearchCV`. This model successfully captured the complex interactions between working hours, project load, and satisfaction levels.

## 🚀 Model Performance (Tuned Random Forest)
The final model achieved industrial-grade performance on the test set:
* **Accuracy:** 98.36%
* **Precision:** 98.24% *(Extremely low rate of false alarms)*
* **Recall:** 91.75% *(Successfully flags almost all true flight risks)*
* **F1-Score:** 0.9488 *(Perfect balance between precision and sensitivity)*

## 📁 Repository Structure
* `Activity_ Course 7 Salifort Motors project lab.ipynb`: The complete Python notebook containing all the code, statistical diagnostics, and machine learning pipelines.
* `HR_capstone_dataset.csv`: The raw dataset containing employee records.
* `burnout_analysis_high_res.png`: Visualization showing the critical burnout thresholds.
* `random_forest_confusion_matrix_high_res.png`: The confusion matrix proving the predictive power of the final model.

---
*Created by Abraham Castro as part of the Google Advanced Data Analytics program.*
