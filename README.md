# Patient Health Records – Data Cleaning Project

## Overview
This project focuses on cleaning and preprocessing a synthetic healthcare dataset containing patient health information. The dataset includes missing values and outliers to demonstrate different data-cleaning techniques.

## Dataset
The dataset contains 500 patient records with attributes such as:
- Age
- Gender
- Region
- BMI
- Blood Pressure
- Cholesterol
- Glucose
- Disease Risk

## Part A – Missing Value Treatment

Different imputation techniques are applied to different columns:

- **Mean/Median Imputation → BMI**
  - Mean is used because BMI may contain outliers.

- **Most Frequent Imputation → Gender & Region**
  - Missing categorical values are replaced with the most frequently occurring value.

- **Random Sample Imputation → Age**
  - Missing age values are replaced using randomly selected values from the observed data.
  - A missing-value indicator is also created.

- **KNN Imputation → Cholesterol**
  - Missing values are estimated using values from similar patient records.

- **MICE → Glucose**
  - Iterative imputation is used to estimate missing values based on relationships between numerical variables.

## Part B – Outlier Treatment

Different outlier-handling techniques are applied:

- **Z-Score → Cholesterol & Glucose**
  - Values with an absolute Z-score greater than 3 are treated as outliers.

- **IQR Method → BMI**
  - Values outside the lower and upper IQR limits are removed.

- **Percentile Method → Age**
  - Extreme values outside the selected percentile range are removed.

- **Winsorization → Blood Pressure**
  - Extreme values are capped instead of removing the records.

## Libraries Used
- Pandas
- NumPy
- Scikit-learn
- SciPy
- Matplotlib / Seaborn (for visualization)
