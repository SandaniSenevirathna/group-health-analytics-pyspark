# Group Health Analytics Using PySpark

## Overview

This project was developed as part of **Big Data Assignment 01**. The objective is to analyze student biodata and health indicators using **PySpark**. The project demonstrates data loading, cleaning, feature engineering, analytical computations, and result exporting within a distributed data processing environment.

The dataset contains demographic information, physical measurements, and health-related biomarkers of students. Through this analysis, students are categorized based on BMI and health risk factors to identify individuals who may require further health attention.

---

## Objectives

* Load and process large datasets using PySpark.
* Perform data cleaning and preprocessing.
* Engineer new health-related features such as BMI and risk indicators.
* Conduct analytical aggregations and departmental comparisons.
* Export processed results for reporting and decision-making.

---

## Dataset Description

The dataset (`biodata_advanced.csv`) contains the following attributes:

| Column            | Description               |
| ----------------- | ------------------------- |
| student_id        | Unique student identifier |
| name              | Student name              |
| age               | Age in years              |
| gender            | Gender of student         |
| height            | Height in centimeters     |
| weight            | Weight in kilograms       |
| bloodgroup        | Blood group               |
| department        | Academic department       |
| year              | Academic year             |
| systolic          | Systolic blood pressure   |
| diastolic_bp      | Diastolic blood pressure  |
| cholesterol_mg_dl | Cholesterol level (mg/dL) |

---

## Technologies Used

* Python 3
* PySpark
* Google Colab
* Google Drive
* Pandas (for exporting results)

---

## Project Workflow

### Part A – Dataset Setup & Loading

* Upload dataset to Google Drive.
* Connect Google Drive to Google Colab.
* Load dataset using PySpark.
* Display sample records.
* Examine dataset dimensions and schema.

### Part B – Data Cleaning & Preprocessing

* Identify missing and invalid values.
* Replace invalid values (0 values) with null values.
* Handle missing data through row removal or imputation.
* Validate data quality before analysis.

### Part C – Feature Engineering

Created the following new features:

#### BMI

BMI is calculated using:

BMI = Weight (kg) / Height² (m²)

#### BMI Categories

* Underweight
* Normal
* Overweight
* Obese

#### High Blood Pressure Flag

A student is marked as having high blood pressure when:

* Systolic BP ≥ 140

OR

* Diastolic BP ≥ 90

#### At-Risk Flag

A student is considered at risk if any of the following conditions are met:

* BMI category is Overweight or Obese
* High blood pressure flag is True
* Cholesterol level ≥ 200 mg/dL

---

## Analysis Performed

### Department-Level Analysis

* Average BMI per department
* Percentage of at-risk students per department

### Year-Level Analysis

* Mean systolic blood pressure by year
* Mean diastolic blood pressure by year

### Pivot Analysis

Department × Gender → Average BMI

### Risk Assessment

Generated a sorted list of at-risk students including:

* BMI
* BMI Category
* Blood Pressure
* Cholesterol Level

---

## Output Files

### Notebook

```text
StudentID_Bigdata_Assignment1.ipynb
```

### PDF Report

```text
StudentID_Bigdata_Assignment1.pdf
```

### Exported Results

```text
StudentID_at_risk_students.csv
```

---

## Project Structure

```text
group-health-analytics-pyspark/
│
├── data/
│   └── biodata_advanced.csv
│
├── notebook/
│   └── StudentID_Bigdata_Assignment1.ipynb
│
├── output/
│   └── StudentID_at_risk_students.csv
│
├── report/
│   └── StudentID_Bigdata_Assignment1.pdf
│
├── requirements.txt
└── README.md
```

---

## Learning Outcomes

Through this project, the following skills were developed:

* Distributed data processing using PySpark
* Data cleaning and preprocessing techniques
* Feature engineering for health analytics
* Aggregation and pivot operations in Spark
* Data-driven decision making
* Exporting and presenting analytical results

---

## Author

Group Health Analytics Using PySpark
CCS3309-Big Data Analytics

