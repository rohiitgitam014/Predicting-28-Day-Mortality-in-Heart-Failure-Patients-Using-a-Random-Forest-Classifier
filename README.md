# Predicting 28-Day Mortality in Heart Failure Patients Using a Random Forest Classifier: A Machine Learning Approach

## Abstract

Heart failure (HF) is one of the leading causes of hospitalization among older adults and is associated with high mortality, frequent hospital readmissions, and increasing healthcare costs worldwide. Early prediction of short-term mortality can assist clinicians in identifying high-risk patients, optimizing treatment strategies, and improving patient outcomes. This project presents a machine learning approach for predicting **28-day mortality** in hospitalized heart failure patients using Electronic Health Records (EHR). The study utilizes a publicly available dataset containing clinical information from **2,008 patients** admitted to **Zigong Fourth People's Hospital, Sichuan Province, China**, between **December 2016 and June 2019**. The dataset contains **168 clinical variables**, including demographic information, vital signs, laboratory measurements, echocardiographic findings, medication records, and follow-up outcomes.

A complete data science workflow was implemented, beginning with data understanding and preprocessing, followed by exploratory data analysis (EDA) to understand data distributions and relationships among variables. Since the mortality classes were imbalanced, the Synthetic Minority Oversampling Technique (SMOTE) was applied to the training data. A **Random Forest Classifier** was selected as the prediction model because of its robustness, ability to handle high-dimensional healthcare data, and resistance to overfitting. Hyperparameter optimization was performed using **RandomizedSearchCV**, and model performance was evaluated using Accuracy, Precision, Recall, F1-score, ROC-AUC Score, Confusion Matrix, and Classification Report.

The results demonstrate that machine learning techniques can effectively analyze electronic healthcare records and support early mortality prediction in hospitalized heart failure patients. Such predictive models have the potential to enhance clinical decision-making, improve patient management, and contribute to the development of intelligent healthcare systems.

**Keywords:** Heart Failure, Electronic Health Records, Machine Learning, Random Forest, SMOTE, Mortality Prediction, Healthcare Analytics

---

# 1. Introduction

Heart failure is a chronic and progressive cardiovascular disease that affects millions of people worldwide. It occurs when the heart is unable to pump sufficient blood to meet the body's metabolic requirements, leading to reduced organ perfusion and fluid accumulation. Despite significant advances in medical treatment, heart failure remains one of the most common reasons for hospitalization among elderly patients and continues to be associated with substantial mortality and morbidity.

According to previous clinical studies, the one-year mortality rate following hospitalization for acute heart failure ranges from **20% to 60%**, depending on disease severity, age, and associated comorbidities. These statistics highlight the importance of identifying patients at high risk of mortality as early as possible.

Electronic Health Records (EHRs) have become valuable resources for healthcare research because they contain detailed patient information collected during routine clinical practice. Advances in machine learning have enabled researchers to analyze these large datasets and identify hidden patterns that support disease diagnosis, prognosis, and clinical decision-making.

This project focuses on predicting **28-day mortality** in hospitalized heart failure patients using a Random Forest Classifier trained on structured electronic healthcare records.

---

# 2. Background

Several publicly available datasets have contributed significantly to cardiovascular research. The Cleveland Heart Disease Dataset and the Nationwide Inpatient Sample (NIS) are among the most widely used resources for studying heart disease and hospitalization outcomes. However, most existing datasets originate from Western healthcare systems, limiting their applicability to different populations.

To address this gap, researchers developed a comprehensive heart failure dataset using electronic healthcare records collected from Zigong Fourth People's Hospital in Sichuan Province, China. The dataset provides detailed demographic, clinical, laboratory, medication, and follow-up information for hospitalized heart failure patients, making it a valuable resource for machine learning research.

The availability of such datasets enables researchers to develop predictive models capable of identifying high-risk patients and supporting evidence-based clinical decisions.

---

# 3. Dataset Description

The dataset used in this project consists of electronic healthcare records collected retrospectively from hospitalized heart failure patients admitted between **December 2016 and June 2019**.

### Dataset Overview

* **Hospital:** Zigong Fourth People's Hospital
* **Location:** Sichuan Province, China
* **Study Period:** December 2016 – June 2019
* **Number of Patients:** 2,008
* **Number of Variables:** 168
* **Target Variable:** 28-Day Mortality

The dataset includes comprehensive clinical information recorded during hospitalization.

### Patient Information

* Body Temperature
* Pulse Rate
* Respiration Rate
* Systolic Blood Pressure
* Diastolic Blood Pressure
* Mean Arterial Pressure
* Weight
* Height
* Body Mass Index (BMI)
* Type of Heart Failure
* NYHA Functional Classification
* Killip Grade
* Glasgow Coma Scale (GCS)

### Echocardiographic Findings

* Left Ventricular Ejection Fraction (LVEF)
* Left Ventricular End Diastolic Diameter
* Mitral Valve Peak E Velocity
* Mitral Valve Peak A Velocity
* E/A Ratio
* Tricuspid Valve Regurgitation Velocity
* Tricuspid Valve Regurgitation Pressure

### Medication Data

The dataset also contains medication information, including:

* Furosemide
* Torsemide
* Spironolactone
* Dobutamine
* Digoxin
* Milrinone
* Nitroglycerin
* Isosorbide Mononitrate

Follow-up outcomes were recorded at **28 days**, **3 months**, and **6 months** after hospitalization. This project focuses on predicting the **28-day mortality outcome**.

---

# 4. Study Methodology

The original dataset was developed through a retrospective review of electronic healthcare records. Heart failure diagnosis was established according to the **European Society of Cardiology (ESC)** guidelines, which include clinical symptoms, elevated BNP or NT-proBNP levels, and objective evidence of structural or functional cardiac abnormalities.

Ethical approval for the study was obtained from the Ethics Committee of Zigong Fourth People's Hospital (Approval Number: **2020-010**). Patient follow-up information was collected through hospital visits or telephone interviews when necessary.

---

# 5. Data Science Workflow

The following workflow was implemented in this project:

1. Business Understanding
2. Data Collection
3. Data Preprocessing
4. Exploratory Data Analysis (EDA)
5. Train-Test Split
6. Handling Class Imbalance Using SMOTE
7. Random Forest Classifier Development
8. Hyperparameter Tuning Using RandomizedSearchCV
9. Model Evaluation

---

# 6. Data Preprocessing

The dataset was loaded into Python using the Pandas library. Data quality was assessed by examining missing values, duplicate records, and data types. The dataset was then divided into training and testing subsets to enable unbiased model evaluation.

---

# 7. Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the characteristics of the dataset.

The following visualizations were created:

* Histplots for numerical and categorical variables
* Bar plots to compare categorical variables with mortality outcomes
* Correlation heatmap to identify relationships among numerical features
* Class distribution plots to examine target imbalance

EDA provided valuable insights into feature distributions and relationships before model development.

---

# 8. Handling Class Imbalance

Healthcare datasets frequently exhibit class imbalance because mortality events occur less frequently than survival cases. Training a model on such data may lead to biased predictions favoring the majority class.

To address this issue, the **Synthetic Minority Oversampling Technique (SMOTE)** was applied to the training dataset. SMOTE generates synthetic samples for the minority class, enabling the Random Forest model to learn more balanced decision boundaries.

---

# 9. Random Forest Classifier

Random Forest is an ensemble learning algorithm that constructs multiple decision trees using bootstrap sampling and random feature selection. The final prediction is determined through majority voting across all trees.

The algorithm offers several advantages for healthcare datasets:

* High predictive performance
* Robustness against overfitting
* Ability to model nonlinear relationships
* Effective handling of high-dimensional data
* Automatic estimation of feature importance

These characteristics make Random Forest a suitable choice for predicting patient mortality using electronic healthcare records.

---

# 10. Hyperparameter Tuning

To optimize model performance, **RandomizedSearchCV** was employed to search for the best combination of Random Forest hyperparameters.

Hyperparameter tuning improves model generalization while reducing the risk of overfitting and excessive computational cost.

---

# 11. Model Evaluation

The trained model was evaluated using several performance metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC Score
* Confusion Matrix
* Classification Report

Using multiple evaluation metrics provides a comprehensive assessment of model performance, particularly for imbalanced healthcare datasets.

---

# 12. Applications

The developed model has several practical applications:

* Early identification of high-risk heart failure patients
* Clinical decision support
* Hospital resource management
* Personalized treatment planning
* Healthcare analytics and research

---

# 13. Limitations

This project has several limitations:

* The dataset was collected from a single hospital.
* Results may not generalize to other healthcare settings or populations.
* Medication administration timestamps are unavailable.
* Longitudinal measurements during hospitalization are not included.

Future studies using multi-center datasets could improve model generalizability.

---

# 14. Future Work

Potential directions for future research include:

* External validation using datasets from multiple hospitals
* Comparison with Gradient Boosting, XGBoost, and deep learning models
* Integration of Explainable AI techniques such as SHAP and LIME
* Deployment as a real-time clinical decision support system
* Incorporation of longitudinal patient data

---

# 15. Conclusion

This project demonstrates the application of machine learning to predict **28-day mortality** in hospitalized heart failure patients using electronic healthcare records. By combining exploratory data analysis, SMOTE for handling class imbalance, a Random Forest Classifier, and hyperparameter tuning with RandomizedSearchCV, the project presents a structured and effective data science workflow for clinical risk prediction. The findings highlight the potential of machine learning to support clinicians in identifying high-risk patients, improving treatment planning, and enhancing healthcare decision-making. As larger and more diverse healthcare datasets become available, predictive models such as this can play an increasingly important role in advancing precision medicine and patient care.

---

## Reference

Zhang, Z., Cao, L., Chen, R., Zhao, Y., Lv, L., Xu, Z., & Xu, P. (2021). *Electronic healthcare records and external outcome data for hospitalized patients with heart failure*. **Scientific Data, 8(1), 46**. [https://doi.org/10.1038/s41597-021-00835-9](https://doi.org/10.1038/s41597-021-00835-9)

This article is suitable as the foundation for your GitHub repository's `README.md` or a Medium post, while clearly distinguishing the published dataset description from your own machine learning implementation using a Random Forest classifier.
