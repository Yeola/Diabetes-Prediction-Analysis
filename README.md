# Diabetes Prediction

## Table of Content

- [Project Overview](#project-overview)
- [Data sources](#data-sources)
- [Tools](#tools)
- [Data preparation](#data-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview

This data analysis projects aims to provide insights into the health performance of patient over the years and predict whether they are diabetic or not. By analyzing various aspects of the patients data,we seek to identify trends,make driven recommendations,and gain a deeper understanding of their health performance.

### Data sources

The primary dataset used for this analysis is the "diabetes_prediction_dataset " file,containing detailed information about health performance of each patient.

### Tools 

- Excel - Data Cleaning [Download here](https://microsoft.com)
- Python - Data Analysis
- PowerBI - Creating Reports
- Machine learning models - To predict whether or not a patient has diabetes

### Data preparation

In the initial data preparation phase,we performed the following tasks:
1. Data loading and inspection.
2. Handling incorrect data types.
3. Data cleaning and formatting.

### Exploratory Data Analysis

EDA involved exploring the dataset to answer key questions, such as;

- Which feature has the strongest correlation with diabetes?
- Which gender has the most occurence of diabetic patient?
- How does diabetic prevalence change with age?

  Data Analysis

  ```Python
  df['age_group']=0
  age_group=[]
  for i in df["age"]:
    if i >=60:
       age_group.append("old ")
    elif (i>=35) and (i<60):
        age_group.append("old adult")
    elif (i>=20) and (i<34):
       age_group.append("young adult")
    elif (i>=13) and (i<19):
        age_group.append("teenager")
    else:
        age_group.append("children");
        ```
###  Findings

The analysis results are summarized as follows:
-The strongly correlated features with diabetes are Blood glucose level, HbA1c Level while BMI, Hypertension and Age shows a moderate correlation with diabetes and heart disease showing the weakest correlation.
-Diabetic patients are high in blood_glucose_level, bmi, HbA1c_level, Age and in smoking history(former & never )and low in hypertension and heart disease
-Non-Diabetic patients are high in heart disease, hypertension and in smoking history(No info & never )and low in blood_glucose_level, bmi, HbA1c_level, Age

### Recommendations
Based on the analysis,we recommend the following actions;
1.Implement age-specific diabetes screening programs,especially for high-risk groups(e.g Old Adults & Elderly).
2.Promote healthy lifestyle programs focusing weight management,diet,and execise.
3.Encourage glucose monitoring programs and provide dietary guidance & medical consultations to patients with high fasting glucose levels to help manage blood sugar levels effectively.
4.Establish routine HbA1c screening for early intervention.
5.Educate current and former smokers on the link between smoking & blood sugar imbalance.

### Limitations
I had to remove all the duplicates from the data as they would have affected the accuracy of my analysis and Predictions,Also the target variable is imbalanced with non_diabetic having over 90% samples and diabetic having less than 10% samples but even then,we can still the correlations between the features and diabetes.

###  References

