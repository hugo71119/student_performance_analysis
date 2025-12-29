# Student Performance Analysis (EDA)

## Overview
This repository contains an exploratory data analysis (EDA) of a student performance dataset (5,000 records).  
The goal is to evaluate which factors are associated with student outcomes and to validate how the target variables are constructed.

> Note: The main notebook is written mostly in Spanish.

## Dataset
The dataset includes:
- **Demographics:** Age, Gender, Class
- **Context variables:** Study_Hours_Per_Day, Attendance_Percentage, Internet_Access, Parental_Education, Extracurricular_Activities
- **Academic scores:** Math_Score, Science_Score, English_Score, Previous_Year_Score
- **Outcomes:** Final_Percentage, Performance_Level, Pass_Fail

## Key Questions
1. Do study hours, attendance, or previous year score correlate with final performance?
2. Are there meaningful differences in performance by Internet access, parental education, or extracurricular activities?
3. Are the outcome variables consistent with subject scores (data validation)?

## Key Findings
- **Weak association** between `Study_Hours_Per_Day`, `Attendance_Percentage`, `Previous_Year_Score` and `Final_Percentage` (Pearson and Spearman correlations close to 0).
- `Final_Percentage` is **perfectly aligned** with the average of subject scores (Math/Science/English), indicating it is a **derived metric** (target leakage).
  Because of this, subject scores are not used as predictors when evaluating external/context factors.
- Socio-educational variables (Internet access, parental education, extracurricular activities) show **small differences** in average performance and pass rate.

## Why This Project Matters
This project demonstrates:
- A clean EDA workflow (data types, missing values, distributions)
- Group comparisons (means, pass rate)
- Correlation analysis (Pearson/Spearman)
- Data validation and critical interpretation (recognizing derived targets and limitations)

## Files
- `student_performance_analysis.ipynb` — main notebook (mostly Spanish)

## How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/hugo71119/student_performance_analysis.git
   cd student_performance_analysis
