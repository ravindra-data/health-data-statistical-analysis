# Health Data Statistical Analysis

Statistical analysis of a synthetic health-records dataset using Python. The project covers inferential statistics, hypothesis testing, confidence intervals, z-test / t-test, chi-square, ANOVA, covariance and correlation, with labelled charts and a short interpretation for each result.

## Project Overview

The dataset has **1,000 health records** and **15 fields** (age, weight, BMI, blood pressure, smoking status, diabetes, and more). The notebook tests whether factors such as smoking, age and BMI are related to diabetes.

All tests use a significance level of **α = 0.05**.

## Dataset Structure

| Field | Type | Description |
|---|---|---|
| record_id | String | Unique identifier for each health record (e.g. PAT-100001) |
| age_group | String | Age category (18-25, 26-35, 36-45, 46-60, 60+) |
| age | Int | Age of the individual |
| weight | Int | Weight of the individual (kg) |
| gender | String | Male / Female / Other |
| region | String | North / South / East / West |
| smoking_status | String | Smoker / Non-Smoker / Former Smoker |
| exercise_frequency | String | Daily / Weekly / Rarely / Never |
| bmi | Float | Body Mass Index |
| blood_pressure | Float | Systolic blood pressure (mmHg) |
| diabetes | Boolean | Has diabetes (True/False) |
| hypertension | Boolean | Has hypertension (True/False) |
| cholesterol_level | Float | Total cholesterol (mg/dL) |
| glucose_level | Float | Fasting glucose (mg/dL) |
| visit_date | Date | Date of health check-up |

> The data is **synthetic** (generated with Python) and is used only for learning. Conclusions apply to this dataset only.

## Tests Performed

| Test | Variables | Result |
|---|---|---|
| 95% Confidence Intervals | age, weight, BMI | Narrow intervals (n = 1,000) |
| t-test / z-test | BMI vs Diabetes | Reject H₀: diabetic people have higher BMI |
| Chi-square | Smoking vs Diabetes | Fail to reject H₀ (p = 0.18) |
| ANOVA | Diabetes rate across age groups | Reject H₀: rate rises with age |
| Covariance and Correlation | Age vs BMI | Reject H₀: moderate positive correlation (r = 0.37) |

## Repository Files

```
├── Health_Statistics_Easy.ipynb   # Main notebook (theory + analysis + charts)
├── health_dataset.csv             # Dataset used by the notebook
├── requirements.txt               # Python libraries needed
└── README.md
```

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/health-data-statistical-analysis.git
   cd health-data-statistical-analysis
   ```
2. Install the libraries
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook and choose **Run All**
   ```bash
   jupyter notebook Health_Statistics_Easy.ipynb
   ```

Keep `health_dataset.csv` in the same folder as the notebook.

## Tools Used

Python, Pandas, NumPy, SciPy, Matplotlib, Jupyter Notebook
